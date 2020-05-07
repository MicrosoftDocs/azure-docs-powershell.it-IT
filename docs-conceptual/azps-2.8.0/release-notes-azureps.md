---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 98a24c805fbf43dd899119d43301b4261c1f60dc
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "75035762"
---
## <a name="280---october-2019"></a><span data-ttu-id="ab09e-103">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-103">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ab09e-104">Generale</span><span class="sxs-lookup"><span data-stu-id="ab09e-104">General</span></span>
* <span data-ttu-id="ab09e-105">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-105">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ab09e-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-106">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-107">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="ab09e-107">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ab09e-108">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-108">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-109">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-109">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ab09e-110">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ab09e-110">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-111">Az.Automation</span></span>
* <span data-ttu-id="ab09e-112">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="ab09e-112">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="ab09e-113">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-113">Az.Batch</span></span>
* <span data-ttu-id="ab09e-114">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ab09e-114">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-115">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-115">Az.Compute</span></span>
* <span data-ttu-id="ab09e-116">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ab09e-116">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ab09e-117">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-117">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ab09e-118">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ab09e-118">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="ab09e-119">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-119">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-120">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-120">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-121">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ab09e-121">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ab09e-122">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ab09e-122">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ab09e-123">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-123">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-124">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-124">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-125">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="ab09e-125">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ab09e-126">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ab09e-126">Az.HealthcareApis</span></span>
* <span data-ttu-id="ab09e-127">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-127">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ab09e-128">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ab09e-128">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ab09e-129">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="ab09e-129">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ab09e-130">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="ab09e-130">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-131">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-131">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-132">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ab09e-132">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ab09e-133">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab09e-133">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-134">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-134">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-135">Aggiunta di nuovi ricevitori di gruppi di azioni per New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ab09e-135">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ab09e-136">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="ab09e-136">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ab09e-137">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="ab09e-137">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ab09e-138">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ab09e-138">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-139">Az.Network</span></span>
* <span data-ttu-id="ab09e-140">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="ab09e-140">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ab09e-141">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-141">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ab09e-142">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ab09e-142">New cmdlets added:</span></span>
        - <span data-ttu-id="ab09e-143">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-143">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ab09e-144">Cmdlet aggiornati con il parametro facoltativo -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="ab09e-144">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="ab09e-145">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-145">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="ab09e-146">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-146">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ab09e-147">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="ab09e-147">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ab09e-148">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-148">Updated cmdlets:</span></span>
        - <span data-ttu-id="ab09e-149">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-149">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ab09e-150">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-150">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ab09e-151">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-151">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ab09e-152">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="ab09e-152">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ab09e-153">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ab09e-153">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ab09e-154">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ab09e-154">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ab09e-155">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ab09e-155">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ab09e-156">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab09e-156">Az.RedisCache</span></span>
* <span data-ttu-id="ab09e-157">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="ab09e-157">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-158">Az.Sql</span></span>
* <span data-ttu-id="ab09e-159">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ab09e-159">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-160">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-160">Az.Storage</span></span>
* <span data-ttu-id="ab09e-161">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-161">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ab09e-162">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ab09e-162">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ab09e-163">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ab09e-163">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ab09e-164">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ab09e-164">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ab09e-165">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-165">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ab09e-166">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ab09e-166">Az.StorageSync</span></span>
* <span data-ttu-id="ab09e-167">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ab09e-167">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-168">Az.Websites</span></span>
* <span data-ttu-id="ab09e-169">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="ab09e-169">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ab09e-170">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-170">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ab09e-171">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-171">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-172">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="ab09e-172">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ab09e-173">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="ab09e-173">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ab09e-174">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-174">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-175">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-175">Az.Automation</span></span>
* <span data-ttu-id="ab09e-176">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="ab09e-176">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ab09e-177">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ab09e-177">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ab09e-178">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="ab09e-178">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-179">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-179">Az.Compute</span></span>
* <span data-ttu-id="ab09e-180">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-180">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ab09e-181">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-181">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ab09e-182">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="ab09e-182">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ab09e-183">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ab09e-183">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ab09e-184">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ab09e-184">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ab09e-185">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-185">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ab09e-186">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ab09e-186">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ab09e-187">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="ab09e-187">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ab09e-188">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ab09e-188">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-189">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-189">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-190">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ab09e-190">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ab09e-191">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ab09e-191">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ab09e-192">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ab09e-192">Az.HDInsight</span></span>
* <span data-ttu-id="ab09e-193">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ab09e-193">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-194">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-194">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-195">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="ab09e-195">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ab09e-196">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ab09e-196">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ab09e-197">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="ab09e-197">New cmdlets are:</span></span>
    - <span data-ttu-id="ab09e-198">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ab09e-198">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ab09e-199">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ab09e-199">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ab09e-200">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ab09e-200">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ab09e-201">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ab09e-201">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-202">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-202">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-203">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="ab09e-203">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ab09e-204">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="ab09e-204">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ab09e-205">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="ab09e-205">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ab09e-206">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ab09e-206">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ab09e-207">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="ab09e-207">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ab09e-208">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ab09e-208">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ab09e-209">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-209">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ab09e-210">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-210">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ab09e-211">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-211">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ab09e-212">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ab09e-212">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ab09e-213">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-213">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ab09e-214">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ab09e-214">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ab09e-215">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="ab09e-215">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ab09e-216">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ab09e-216">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ab09e-217">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ab09e-217">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ab09e-218">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="ab09e-218">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ab09e-219">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="ab09e-219">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ab09e-220">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-220">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ab09e-221">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="ab09e-221">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ab09e-222">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-222">Overall improved help files</span></span>
* <span data-ttu-id="ab09e-223">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="ab09e-223">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-224">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-224">Az.Network</span></span>
* <span data-ttu-id="ab09e-225">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="ab09e-225">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="ab09e-226">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="ab09e-226">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ab09e-227">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="ab09e-227">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ab09e-228">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="ab09e-228">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ab09e-229">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="ab09e-229">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ab09e-230">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ab09e-230">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ab09e-231">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="ab09e-231">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ab09e-232">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ab09e-232">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ab09e-233">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-233">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ab09e-234">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ab09e-234">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ab09e-235">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-235">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ab09e-236">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-236">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ab09e-237">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-237">New cmdlets</span></span>
        - <span data-ttu-id="ab09e-238">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ab09e-238">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ab09e-239">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-239">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ab09e-240">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ab09e-240">Updated cmdlet:</span></span>
        - <span data-ttu-id="ab09e-241">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ab09e-241">New-VpnSite</span></span>
        - <span data-ttu-id="ab09e-242">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ab09e-242">Update-VpnSite</span></span>
        - <span data-ttu-id="ab09e-243">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-243">New-VpnConnection</span></span>
        - <span data-ttu-id="ab09e-244">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-244">Update-VpnConnection</span></span>
* <span data-ttu-id="ab09e-245">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="ab09e-245">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-246">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-246">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-247">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="ab09e-247">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ab09e-248">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="ab09e-248">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-249">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-249">Az.Resources</span></span>
* <span data-ttu-id="ab09e-250">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="ab09e-250">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-251">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-251">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-252">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ab09e-252">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ab09e-253">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="ab09e-253">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ab09e-254">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab09e-254">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ab09e-255">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab09e-255">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ab09e-256">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab09e-256">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ab09e-257">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab09e-257">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ab09e-258">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab09e-258">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ab09e-259">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab09e-259">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ab09e-260">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab09e-260">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ab09e-261">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab09e-261">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ab09e-262">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ab09e-262">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ab09e-263">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ab09e-263">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ab09e-264">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ab09e-264">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ab09e-265">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ab09e-265">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ab09e-266">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ab09e-266">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ab09e-267">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ab09e-267">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ab09e-268">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ab09e-268">Az.SignalR</span></span>
* <span data-ttu-id="ab09e-269">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="ab09e-269">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-270">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-270">Az.Sql</span></span>
* <span data-ttu-id="ab09e-271">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="ab09e-271">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ab09e-272">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="ab09e-272">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ab09e-273">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-273">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ab09e-274">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab09e-274">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ab09e-275">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ab09e-275">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-276">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-276">Az.Storage</span></span>
* <span data-ttu-id="ab09e-277">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ab09e-277">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ab09e-278">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-278">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ab09e-279">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-279">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ab09e-280">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-280">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ab09e-281">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="ab09e-281">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ab09e-282">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-282">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ab09e-283">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ab09e-283">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ab09e-284">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ab09e-284">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ab09e-285">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ab09e-285">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ab09e-286">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ab09e-286">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ab09e-287">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ab09e-287">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-288">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-288">Az.Websites</span></span>
* <span data-ttu-id="ab09e-289">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione delle app al nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="ab09e-289">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ab09e-290">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="ab09e-290">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ab09e-291">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="ab09e-291">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ab09e-292">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-292">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ab09e-293">Generale</span><span class="sxs-lookup"><span data-stu-id="ab09e-293">General</span></span>
* <span data-ttu-id="ab09e-294">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="ab09e-294">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ab09e-295">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-295">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-296">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="ab09e-296">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ab09e-297">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ab09e-297">Az.Aks</span></span>
* <span data-ttu-id="ab09e-298">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="ab09e-298">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ab09e-299">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ab09e-299">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ab09e-300">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-300">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-301">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ab09e-301">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ab09e-302">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="ab09e-302">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ab09e-303">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="ab09e-303">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ab09e-304">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ab09e-304">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ab09e-305">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ab09e-305">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ab09e-306">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-306">Az.Batch</span></span>
* <span data-ttu-id="ab09e-307">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ab09e-307">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ab09e-308">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab09e-308">Az.Cdn</span></span>
* <span data-ttu-id="ab09e-309">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="ab09e-309">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-310">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-310">Az.Compute</span></span>
* <span data-ttu-id="ab09e-311">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-311">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ab09e-312">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ab09e-312">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ab09e-313">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-313">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ab09e-314">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-314">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ab09e-315">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ab09e-315">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ab09e-316">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab09e-316">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ab09e-317">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ab09e-317">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ab09e-318">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="ab09e-318">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-319">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-320">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ab09e-320">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ab09e-321">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ab09e-321">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ab09e-322">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ab09e-322">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ab09e-323">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="ab09e-323">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-324">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-324">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-325">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="ab09e-325">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ab09e-326">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-326">Az.EventHub</span></span>
* <span data-ttu-id="ab09e-327">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-327">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ab09e-328">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ab09e-328">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ab09e-329">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ab09e-329">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ab09e-330">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ab09e-330">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ab09e-331">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ab09e-331">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ab09e-332">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="ab09e-332">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-333">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-333">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-334">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-334">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-335">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-335">Az.Network</span></span>
* <span data-ttu-id="ab09e-336">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-336">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ab09e-337">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="ab09e-337">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ab09e-338">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="ab09e-338">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ab09e-339">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="ab09e-339">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ab09e-340">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="ab09e-340">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="ab09e-341">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-341">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ab09e-342">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ab09e-342">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-343">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-343">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-344">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="ab09e-344">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ab09e-345">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ab09e-345">Added example</span></span>
    - <span data-ttu-id="ab09e-346">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="ab09e-346">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ab09e-347">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ab09e-347">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ab09e-348">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ab09e-348">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-349">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-349">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-350">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-350">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-351">Az.Resources</span></span>
* <span data-ttu-id="ab09e-352">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ab09e-352">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ab09e-353">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="ab09e-353">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ab09e-354">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="ab09e-354">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ab09e-355">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-355">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-356">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-356">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-357">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-357">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ab09e-358">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ab09e-358">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ab09e-359">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="ab09e-359">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-360">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-360">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-361">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="ab09e-361">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ab09e-362">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ab09e-362">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ab09e-363">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ab09e-363">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ab09e-364">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="ab09e-364">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ab09e-365">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ab09e-365">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ab09e-366">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ab09e-366">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-367">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-367">Az.Sql</span></span>
* <span data-ttu-id="ab09e-368">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-368">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-369">Az.Storage</span></span>
* <span data-ttu-id="ab09e-370">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ab09e-370">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ab09e-371">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ab09e-371">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ab09e-372">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-372">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ab09e-373">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ab09e-373">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ab09e-374">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ab09e-374">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ab09e-375">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ab09e-375">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-376">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-376">Az.Websites</span></span>
* <span data-ttu-id="ab09e-377">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab09e-377">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ab09e-378">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-378">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-379">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-379">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-380">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ab09e-380">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ab09e-381">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-381">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ab09e-382">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="ab09e-382">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="ab09e-383">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-383">Az.Automation</span></span>
* <span data-ttu-id="ab09e-384">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="ab09e-384">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-385">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-385">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-386">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-386">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-387">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-387">Az.Compute</span></span>
* <span data-ttu-id="ab09e-388">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ab09e-388">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ab09e-389">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ab09e-389">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ab09e-390">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="ab09e-390">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ab09e-391">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ab09e-391">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-392">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-392">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-393">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-393">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ab09e-394">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="ab09e-394">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ab09e-395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-395">Az.EventHub</span></span>
* <span data-ttu-id="ab09e-396">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ab09e-396">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ab09e-397">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ab09e-397">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ab09e-398">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-398">Az.KeyVault</span></span>
* <span data-ttu-id="ab09e-399">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="ab09e-399">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ab09e-400">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-400">Az.LogicApp</span></span>
* <span data-ttu-id="ab09e-401">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="ab09e-401">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ab09e-402">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="ab09e-402">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ab09e-403">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-403">Az.ManagedServices</span></span>
* <span data-ttu-id="ab09e-404">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="ab09e-404">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-405">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-405">Az.Network</span></span>
* <span data-ttu-id="ab09e-406">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="ab09e-406">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ab09e-407">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-407">New cmdlets</span></span>
        - <span data-ttu-id="ab09e-408">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab09e-408">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ab09e-409">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-409">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ab09e-410">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-410">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ab09e-411">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-411">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ab09e-412">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-412">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ab09e-413">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-413">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ab09e-414">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ab09e-414">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ab09e-415">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-415">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ab09e-416">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="ab09e-416">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ab09e-417">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-417">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ab09e-418">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-418">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ab09e-419">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-419">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ab09e-420">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="ab09e-420">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ab09e-421">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="ab09e-421">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ab09e-422">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-422">Updated cmdlets</span></span>
        - <span data-ttu-id="ab09e-423">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-423">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ab09e-424">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-424">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ab09e-425">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-425">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ab09e-426">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-426">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ab09e-427">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-427">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ab09e-428">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ab09e-428">Updated cmdlet:</span></span>
        - <span data-ttu-id="ab09e-429">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-429">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ab09e-430">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-430">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ab09e-431">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-431">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ab09e-432">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="ab09e-432">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ab09e-433">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="ab09e-433">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ab09e-434">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="ab09e-434">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-435">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-435">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-436">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="ab09e-436">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="ab09e-437">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="ab09e-437">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-438">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-438">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-439">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-439">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ab09e-440">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-440">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ab09e-441">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-441">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ab09e-442">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-442">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ab09e-443">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-443">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ab09e-444">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-444">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ab09e-445">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-445">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ab09e-446">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-446">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ab09e-447">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-447">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ab09e-448">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ab09e-448">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-449">Az.Resources</span></span>
- <span data-ttu-id="ab09e-450">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ab09e-450">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ab09e-451">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ab09e-451">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-452">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-452">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-453">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ab09e-453">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ab09e-454">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ab09e-454">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-455">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-455">Az.Sql</span></span>
* <span data-ttu-id="ab09e-456">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ab09e-456">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ab09e-457">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="ab09e-457">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ab09e-458">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="ab09e-458">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-459">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-459">Az.Storage</span></span>
* <span data-ttu-id="ab09e-460">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ab09e-460">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ab09e-461">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ab09e-461">Az.StorageSync</span></span>
* <span data-ttu-id="ab09e-462">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ab09e-462">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ab09e-463">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ab09e-463">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-464">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-464">Az.Websites</span></span>
* <span data-ttu-id="ab09e-465">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-465">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ab09e-466">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-466">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ab09e-467">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ab09e-467">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ab09e-468">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-468">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-469">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-469">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-470">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="ab09e-470">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ab09e-471">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="ab09e-471">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ab09e-472">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ab09e-472">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ab09e-473">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ab09e-473">Az.Advisor</span></span>
* <span data-ttu-id="ab09e-474">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ab09e-474">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ab09e-475">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ab09e-475">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ab09e-476">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-476">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-477">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ab09e-477">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ab09e-478">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ab09e-478">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ab09e-479">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="ab09e-479">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ab09e-480">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="ab09e-480">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ab09e-481">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ab09e-481">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ab09e-482">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ab09e-482">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ab09e-483">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="ab09e-483">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-484">Az.Automation</span></span>
* <span data-ttu-id="ab09e-485">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="ab09e-485">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-486">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-486">Az.Compute</span></span>
* <span data-ttu-id="ab09e-487">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-487">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-488">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-488">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-489">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="ab09e-489">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ab09e-490">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab09e-490">Az.EventGrid</span></span>
* <span data-ttu-id="ab09e-491">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="ab09e-491">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-492">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-493">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-493">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-494">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-494">Az.Network</span></span>
* <span data-ttu-id="ab09e-495">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="ab09e-495">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ab09e-496">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="ab09e-496">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ab09e-497">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-497">Az.PolicyInsights</span></span>
* <span data-ttu-id="ab09e-498">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ab09e-498">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ab09e-499">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ab09e-499">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-500">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-500">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-501">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ab09e-501">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-502">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-502">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-503">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="ab09e-503">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-504">Az.Resources</span></span>
    - <span data-ttu-id="ab09e-505">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="ab09e-505">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ab09e-506">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ab09e-506">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ab09e-507">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ab09e-507">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ab09e-508">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="ab09e-508">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-509">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-509">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-510">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ab09e-510">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-511">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-511">Az.Sql</span></span>
* <span data-ttu-id="ab09e-512">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="ab09e-512">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ab09e-513">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-513">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ab09e-514">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-514">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ab09e-515">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-515">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ab09e-516">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-516">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ab09e-517">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-517">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ab09e-518">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-518">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ab09e-519">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ab09e-519">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ab09e-520">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="ab09e-520">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-521">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-521">Az.Storage</span></span>
* <span data-ttu-id="ab09e-522">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-522">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ab09e-523">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ab09e-523">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ab09e-524">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="ab09e-524">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ab09e-525">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="ab09e-525">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ab09e-526">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-526">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ab09e-527">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-527">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ab09e-528">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-528">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ab09e-529">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="ab09e-529">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ab09e-530">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ab09e-530">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ab09e-531">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ab09e-531">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ab09e-532">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ab09e-532">Az.StorageSync</span></span>
* <span data-ttu-id="ab09e-533">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ab09e-533">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ab09e-534">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-534">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-535">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-535">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-536">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="ab09e-536">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ab09e-537">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ab09e-537">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ab09e-538">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="ab09e-538">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ab09e-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ab09e-539">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ab09e-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ab09e-540">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-541">Az.Compute</span></span>
* <span data-ttu-id="ab09e-542">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-542">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ab09e-543">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="ab09e-543">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ab09e-544">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ab09e-544">Az.Dns</span></span>
* <span data-ttu-id="ab09e-545">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-545">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ab09e-546">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab09e-546">Az.EventGrid</span></span>
* <span data-ttu-id="ab09e-547">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ab09e-547">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ab09e-548">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-548">New cmdlets:</span></span>
    - <span data-ttu-id="ab09e-549">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ab09e-549">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ab09e-550">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-550">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ab09e-551">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ab09e-551">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ab09e-552">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-552">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ab09e-553">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ab09e-553">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ab09e-554">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-554">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ab09e-555">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-555">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ab09e-556">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-556">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ab09e-557">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-557">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ab09e-558">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-558">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ab09e-559">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ab09e-559">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ab09e-560">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-560">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ab09e-561">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ab09e-561">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ab09e-562">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-562">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="ab09e-563">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ab09e-563">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ab09e-564">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-564">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ab09e-565">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-565">Updated cmdlets:</span></span>
    - <span data-ttu-id="ab09e-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ab09e-566">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ab09e-567">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-567">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ab09e-568">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-568">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ab09e-569">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="ab09e-569">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ab09e-570">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ab09e-570">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ab09e-571">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="ab09e-571">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ab09e-572">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-572">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ab09e-573">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-573">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ab09e-574">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-574">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="ab09e-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ab09e-575">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ab09e-576">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-576">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ab09e-577">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ab09e-577">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ab09e-578">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-578">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ab09e-579">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ab09e-579">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ab09e-580">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ab09e-580">Az.FrontDoor</span></span>
* <span data-ttu-id="ab09e-581">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ab09e-581">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ab09e-582">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ab09e-582">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ab09e-583">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ab09e-583">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ab09e-584">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="ab09e-584">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-585">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-585">Az.Network</span></span>
* <span data-ttu-id="ab09e-586">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-586">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ab09e-587">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-587">New cmdlets</span></span>
        - <span data-ttu-id="ab09e-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ab09e-588">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ab09e-589">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ab09e-589">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ab09e-590">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-590">New cmdlets</span></span> 
        - <span data-ttu-id="ab09e-591">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ab09e-591">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ab09e-592">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-592">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ab09e-593">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-593">New cmdlets</span></span> 
        - <span data-ttu-id="ab09e-594">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-594">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="ab09e-595">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-595">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ab09e-596">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ab09e-596">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ab09e-597">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-597">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ab09e-598">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-598">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ab09e-599">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab09e-599">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ab09e-600">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-600">New cmdlets</span></span>
        - <span data-ttu-id="ab09e-601">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab09e-601">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ab09e-602">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab09e-602">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ab09e-603">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ab09e-603">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ab09e-604">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-604">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ab09e-605">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ab09e-605">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ab09e-606">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ab09e-606">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ab09e-607">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ab09e-607">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ab09e-608">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab09e-608">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ab09e-609">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ab09e-609">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ab09e-610">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ab09e-610">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ab09e-611">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-611">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ab09e-612">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="ab09e-612">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ab09e-613">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-613">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ab09e-614">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="ab09e-614">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ab09e-615">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-615">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ab09e-616">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-616">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ab09e-617">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ab09e-617">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ab09e-618">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-618">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ab09e-619">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="ab09e-619">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ab09e-620">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ab09e-620">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ab09e-621">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-621">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ab09e-622">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ab09e-622">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ab09e-623">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ab09e-623">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="ab09e-624">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ab09e-624">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="ab09e-625">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-625">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ab09e-626">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-626">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ab09e-627">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-627">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-628">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-628">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-629">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ab09e-629">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-630">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-630">Az.Resources</span></span>
* <span data-ttu-id="ab09e-631">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="ab09e-631">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ab09e-632">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-632">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ab09e-633">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-633">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ab09e-634">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="ab09e-634">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-635">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-635">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-636">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="ab09e-636">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-637">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-637">Az.Sql</span></span>
* <span data-ttu-id="ab09e-638">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ab09e-638">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ab09e-639">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ab09e-639">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ab09e-640">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="ab09e-640">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ab09e-641">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-641">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ab09e-642">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-642">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ab09e-643">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ab09e-643">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ab09e-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ab09e-644">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ab09e-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ab09e-645">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-646">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-646">Az.Storage</span></span>
* <span data-ttu-id="ab09e-647">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-647">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ab09e-648">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-648">New-AzStorageAccount</span></span>
* <span data-ttu-id="ab09e-649">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="ab09e-649">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ab09e-650">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-650">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-651">Az.Websites</span></span>
* <span data-ttu-id="ab09e-652">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="ab09e-652">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ab09e-653">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ab09e-653">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ab09e-654">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-654">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ab09e-655">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab09e-655">Az.Cdn</span></span>
* <span data-ttu-id="ab09e-656">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="ab09e-656">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-657">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-657">Az.Compute</span></span>
* <span data-ttu-id="ab09e-658">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-658">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ab09e-659">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab09e-659">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ab09e-660">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-660">Az.EventHub</span></span>
* <span data-ttu-id="ab09e-661">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="ab09e-661">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ab09e-662">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab09e-662">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-663">Az.Network</span></span>
* <span data-ttu-id="ab09e-664">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ab09e-664">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ab09e-665">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="ab09e-665">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ab09e-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="ab09e-667">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ab09e-667">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-668">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-668">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-669">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="ab09e-669">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-670">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-670">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-671">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab09e-671">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-672">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-672">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-673">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ab09e-673">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ab09e-674">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-674">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-675">Az.Sql</span></span>
* <span data-ttu-id="ab09e-676">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="ab09e-676">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ab09e-677">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-677">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ab09e-678">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ab09e-678">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ab09e-679">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-679">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-680">Az.Websites</span></span>
* <span data-ttu-id="ab09e-681">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="ab09e-681">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ab09e-682">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-682">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ab09e-683">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-683">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-684">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="ab09e-684">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ab09e-685">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-685">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ab09e-686">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-686">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ab09e-687">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="ab09e-687">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ab09e-688">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-688">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ab09e-689">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="ab09e-689">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ab09e-690">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-690">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ab09e-691">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-691">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ab09e-692">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-692">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ab09e-693">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="ab09e-693">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ab09e-694">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-694">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ab09e-695">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="ab09e-695">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ab09e-696">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="ab09e-696">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ab09e-697">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-697">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ab09e-698">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-698">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ab09e-699">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-699">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ab09e-700">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-700">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ab09e-701">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ab09e-701">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ab09e-702">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-702">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="ab09e-703">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-703">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ab09e-704">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="ab09e-704">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ab09e-705">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ab09e-705">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ab09e-706">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="ab09e-706">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ab09e-707">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-707">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="ab09e-708">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ab09e-708">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ab09e-709">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ab09e-709">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ab09e-710">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-710">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ab09e-711">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ab09e-711">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ab09e-712">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ab09e-712">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ab09e-713">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="ab09e-713">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ab09e-714">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="ab09e-714">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="ab09e-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ab09e-715">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ab09e-716">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ab09e-716">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ab09e-717">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ab09e-717">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ab09e-718">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ab09e-718">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ab09e-719">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="ab09e-719">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ab09e-720">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="ab09e-720">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ab09e-721">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="ab09e-721">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ab09e-722">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="ab09e-722">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ab09e-723">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ab09e-723">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="ab09e-724">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-724">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ab09e-725">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ab09e-725">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ab09e-726">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-726">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ab09e-727">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ab09e-727">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ab09e-728">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ab09e-728">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ab09e-729">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-729">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ab09e-730">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ab09e-730">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="ab09e-731">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ab09e-731">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="ab09e-732">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ab09e-732">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ab09e-733">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-733">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ab09e-734">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ab09e-734">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ab09e-735">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ab09e-735">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ab09e-736">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="ab09e-736">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ab09e-737">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ab09e-737">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ab09e-738">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="ab09e-738">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ab09e-739">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ab09e-739">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ab09e-740">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ab09e-740">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ab09e-741">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ab09e-741">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ab09e-742">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ab09e-742">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ab09e-743">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-743">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ab09e-744">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ab09e-744">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ab09e-745">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ab09e-745">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ab09e-746">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ab09e-746">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ab09e-747">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-747">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ab09e-748">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="ab09e-748">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ab09e-749">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ab09e-749">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ab09e-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ab09e-750">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ab09e-751">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ab09e-751">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ab09e-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ab09e-752">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ab09e-753">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ab09e-753">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ab09e-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ab09e-754">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ab09e-755">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ab09e-755">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ab09e-756">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ab09e-756">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ab09e-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-757">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ab09e-758">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ab09e-758">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="ab09e-759">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ab09e-759">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ab09e-760">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ab09e-760">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-761">Az.Automation</span></span>
* <span data-ttu-id="ab09e-762">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="ab09e-762">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ab09e-763">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ab09e-763">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ab09e-764">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ab09e-764">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ab09e-765">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="ab09e-765">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ab09e-766">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ab09e-766">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ab09e-767">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="ab09e-767">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ab09e-768">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-768">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-769">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-769">Az.Compute</span></span>
* <span data-ttu-id="ab09e-770">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ab09e-770">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ab09e-771">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="ab09e-771">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-772">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-772">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-773">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-773">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-774">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-774">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-775">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-775">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-776">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-776">Az.Network</span></span>
* <span data-ttu-id="ab09e-777">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="ab09e-777">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ab09e-778">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ab09e-778">Updated cmdlet:</span></span>
        - <span data-ttu-id="ab09e-779">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ab09e-779">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ab09e-780">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ab09e-780">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-781">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-781">Az.Resources</span></span>
* <span data-ttu-id="ab09e-782">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="ab09e-782">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-783">Az.Sql</span></span>
* <span data-ttu-id="ab09e-784">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ab09e-784">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ab09e-785">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-785">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-786">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-787">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="ab09e-787">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-788">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-788">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-789">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-789">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ab09e-790">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="ab09e-790">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-791">Az.Compute</span></span>
* <span data-ttu-id="ab09e-792">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="ab09e-792">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ab09e-793">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-793">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ab09e-794">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-794">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ab09e-795">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ab09e-795">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ab09e-796">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ab09e-796">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ab09e-797">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ab09e-797">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="ab09e-798">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ab09e-798">Breaking changes</span></span>
    - <span data-ttu-id="ab09e-799">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ab09e-799">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ab09e-800">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ab09e-800">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ab09e-801">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ab09e-801">Az.DeploymentManager</span></span>
* <span data-ttu-id="ab09e-802">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="ab09e-802">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ab09e-803">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ab09e-803">Az.Dns</span></span>
* <span data-ttu-id="ab09e-804">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="ab09e-804">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ab09e-805">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="ab09e-805">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ab09e-806">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="ab09e-806">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ab09e-807">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ab09e-807">Az.FrontDoor</span></span>
* <span data-ttu-id="ab09e-808">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-808">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ab09e-809">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ab09e-809">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ab09e-810">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ab09e-810">Az.HDInsight</span></span>
* <span data-ttu-id="ab09e-811">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-811">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ab09e-812">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ab09e-812">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ab09e-813">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ab09e-813">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ab09e-814">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ab09e-814">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ab09e-815">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="ab09e-815">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ab09e-816">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ab09e-816">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ab09e-817">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-817">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-818">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-818">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-819">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="ab09e-819">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="ab09e-820">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ab09e-820">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ab09e-821">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-821">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ab09e-822">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ab09e-822">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ab09e-823">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ab09e-823">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ab09e-824">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ab09e-824">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ab09e-825">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ab09e-825">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ab09e-826">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-826">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ab09e-827">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-827">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ab09e-828">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-828">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ab09e-829">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-829">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ab09e-830">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-830">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ab09e-831">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="ab09e-831">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ab09e-832">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ab09e-832">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-833">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-833">Az.Network</span></span>
* <span data-ttu-id="ab09e-834">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ab09e-834">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ab09e-835">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-835">New cmdlets</span></span>
        - <span data-ttu-id="ab09e-836">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-836">New-AzNatGateway</span></span>
        - <span data-ttu-id="ab09e-837">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-837">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ab09e-838">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-838">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ab09e-839">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-839">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ab09e-840">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ab09e-840">Updated cmdlets</span></span>
        - <span data-ttu-id="ab09e-841">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ab09e-841">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ab09e-842">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ab09e-842">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ab09e-843">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-843">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ab09e-844">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-844">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ab09e-845">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ab09e-845">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ab09e-846">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-846">Az.PolicyInsights</span></span>
* <span data-ttu-id="ab09e-847">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ab09e-847">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ab09e-848">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ab09e-848">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ab09e-849">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-849">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-850">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-850">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-851">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="ab09e-851">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ab09e-852">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ab09e-852">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ab09e-853">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ab09e-853">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ab09e-854">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-854">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ab09e-855">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="ab09e-855">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ab09e-856">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="ab09e-856">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ab09e-857">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ab09e-857">Az.Relay</span></span>
* <span data-ttu-id="ab09e-858">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="ab09e-858">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-859">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-859">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-860">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab09e-860">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-861">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-861">Az.Storage</span></span>
* <span data-ttu-id="ab09e-862">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ab09e-862">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ab09e-863">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ab09e-863">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ab09e-864">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ab09e-864">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ab09e-865">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-865">New-AzStorageAccount</span></span>
* <span data-ttu-id="ab09e-866">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ab09e-866">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ab09e-867">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-867">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ab09e-868">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-868">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ab09e-869">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-869">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-870">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-870">Az.Websites</span></span>
* <span data-ttu-id="ab09e-871">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-871">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ab09e-872">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="ab09e-872">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ab09e-873">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-873">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ab09e-874">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ab09e-874">Highlights since the last major release</span></span>
* <span data-ttu-id="ab09e-875">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ab09e-875">General availability of `Az` module</span></span>
* <span data-ttu-id="ab09e-876">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ab09e-876">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ab09e-877">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ab09e-877">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ab09e-878">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-878">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ab09e-879">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ab09e-879">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ab09e-880">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-880">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ab09e-881">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-881">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ab09e-882">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-882">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-883">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="ab09e-883">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ab09e-884">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-884">Az.Batch</span></span>
* <span data-ttu-id="ab09e-885">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-885">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ab09e-886">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab09e-886">Az.Cdn</span></span>
* <span data-ttu-id="ab09e-887">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-887">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-888">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-888">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-889">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-889">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-890">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-890">Az.Compute</span></span>
* <span data-ttu-id="ab09e-891">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="ab09e-891">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ab09e-892">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-892">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-893">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ab09e-893">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-894">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-894">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-895">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="ab09e-895">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-896">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-896">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-897">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-897">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ab09e-898">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab09e-898">Az.EventGrid</span></span>
* <span data-ttu-id="ab09e-899">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ab09e-899">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ab09e-900">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-900">Az.EventHub</span></span>
* <span data-ttu-id="ab09e-901">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ab09e-901">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="ab09e-902">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ab09e-902">Az.HDInsight</span></span>
* <span data-ttu-id="ab09e-903">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-903">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-904">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-904">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-905">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-905">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ab09e-906">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-906">Az.KeyVault</span></span>
* <span data-ttu-id="ab09e-907">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-907">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-908">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ab09e-908">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ab09e-909">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ab09e-909">Az.MachineLearning</span></span>
* <span data-ttu-id="ab09e-910">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-910">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ab09e-911">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ab09e-911">Az.Media</span></span>
* <span data-ttu-id="ab09e-912">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-912">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-913">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-913">Az.Monitor</span></span>
  * <span data-ttu-id="ab09e-914">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ab09e-914">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ab09e-915">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ab09e-915">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ab09e-916">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ab09e-916">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ab09e-917">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ab09e-917">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ab09e-918">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ab09e-918">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ab09e-919">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ab09e-919">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ab09e-920">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ab09e-920">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-921">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-921">Az.Network</span></span>
* <span data-ttu-id="ab09e-922">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-922">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-923">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ab09e-923">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ab09e-924">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ab09e-924">Az.NotificationHubs</span></span>
* <span data-ttu-id="ab09e-925">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-925">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-926">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-926">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-927">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-927">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ab09e-928">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ab09e-928">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ab09e-929">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-929">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-930">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-930">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-931">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-931">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-932">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-932">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ab09e-933">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ab09e-933">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ab09e-934">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="ab09e-934">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ab09e-935">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab09e-935">Az.RedisCache</span></span>
* <span data-ttu-id="ab09e-936">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-936">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-937">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-937">Az.Resources</span></span>
* <span data-ttu-id="ab09e-938">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ab09e-938">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-939">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-939">Az.Sql</span></span>
* <span data-ttu-id="ab09e-940">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="ab09e-940">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ab09e-941">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-941">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-942">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="ab09e-942">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ab09e-943">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ab09e-943">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ab09e-944">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="ab09e-944">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ab09e-945">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="ab09e-945">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ab09e-946">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ab09e-946">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-947">Az.Websites</span></span>
* <span data-ttu-id="ab09e-948">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-948">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ab09e-949">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ab09e-949">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ab09e-950">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="ab09e-950">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ab09e-951">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ab09e-951">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ab09e-952">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-952">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ab09e-953">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ab09e-953">Highlights since the last major release</span></span>
* <span data-ttu-id="ab09e-954">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ab09e-954">General availability of `Az` module</span></span>
* <span data-ttu-id="ab09e-955">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ab09e-955">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ab09e-956">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ab09e-956">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ab09e-957">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-957">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ab09e-958">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ab09e-958">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ab09e-959">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-959">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ab09e-960">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-960">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ab09e-961">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-961">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-962">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ab09e-962">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ab09e-963">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-963">Az.AnalysisServices</span></span>
* <span data-ttu-id="ab09e-964">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="ab09e-964">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ab09e-965">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-965">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-966">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-966">Az.Automation</span></span>
* <span data-ttu-id="ab09e-967">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="ab09e-967">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ab09e-968">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="ab09e-968">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ab09e-969">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-969">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-970">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-970">Az.Compute</span></span>
* <span data-ttu-id="ab09e-971">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-971">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ab09e-972">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="ab09e-972">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="ab09e-973">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-973">Az.ContainerInstance</span></span>
* <span data-ttu-id="ab09e-974">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="ab09e-974">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-975">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-975">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-976">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ab09e-976">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ab09e-977">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ab09e-977">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-978">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-978">Az.Resources</span></span>
* <span data-ttu-id="ab09e-979">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="ab09e-979">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ab09e-980">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ab09e-980">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ab09e-981">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="ab09e-981">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ab09e-982">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ab09e-982">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ab09e-983">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="ab09e-983">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ab09e-984">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ab09e-984">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-985">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-985">Az.Sql</span></span>
* <span data-ttu-id="ab09e-986">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="ab09e-986">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-987">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-987">Az.Storage</span></span>
* <span data-ttu-id="ab09e-988">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="ab09e-988">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ab09e-989">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab09e-989">New-AzStorageContext</span></span>
* <span data-ttu-id="ab09e-990">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ab09e-990">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ab09e-991">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ab09e-991">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ab09e-992">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ab09e-992">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ab09e-993">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-993">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ab09e-994">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-994">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ab09e-995">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="ab09e-995">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ab09e-996">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-996">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ab09e-997">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-997">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ab09e-998">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-998">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ab09e-999">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ab09e-999">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ab09e-1000">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1000">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ab09e-1001">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1001">Highlights since the last major release</span></span>
* <span data-ttu-id="ab09e-1002">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ab09e-1002">General availability of `Az` module</span></span>
* <span data-ttu-id="ab09e-1003">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ab09e-1003">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ab09e-1004">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ab09e-1004">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ab09e-1005">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1005">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ab09e-1006">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ab09e-1006">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ab09e-1007">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1007">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ab09e-1008">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-1008">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-1009">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1009">Az.Automation</span></span>
* <span data-ttu-id="ab09e-1010">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab09e-1010">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ab09e-1011">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="ab09e-1011">Dynamic grouping</span></span>
    * <span data-ttu-id="ab09e-1012">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="ab09e-1012">Pre-Post script</span></span>
    * <span data-ttu-id="ab09e-1013">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="ab09e-1013">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1014">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1014">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1015">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ab09e-1015">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ab09e-1016">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1016">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ab09e-1017">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-1017">Az.KeyVault</span></span>
* <span data-ttu-id="ab09e-1018">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-1018">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1019">Az.Network</span></span>
* <span data-ttu-id="ab09e-1020">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-1020">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ab09e-1021">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="ab09e-1021">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1022">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1022">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-1023">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="ab09e-1023">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ab09e-1024">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="ab09e-1024">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1025">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1025">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1026">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-1026">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ab09e-1027">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="ab09e-1027">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1028">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1028">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1029">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1029">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1030">Az.Storage</span></span>
* <span data-ttu-id="ab09e-1031">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1031">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ab09e-1032">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1032">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ab09e-1033">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1033">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ab09e-1034">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1034">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ab09e-1035">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ab09e-1035">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ab09e-1036">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ab09e-1036">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ab09e-1037">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-1037">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-1038">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1038">Az.Websites</span></span>
* <span data-ttu-id="ab09e-1039">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="ab09e-1039">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="ab09e-1040">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1040">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-1041">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1041">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-1042">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="ab09e-1042">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ab09e-1043">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-1043">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-1044">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1044">Az.Automation</span></span>
* <span data-ttu-id="ab09e-1045">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-1045">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ab09e-1046">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1046">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ab09e-1047">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1047">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ab09e-1048">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab09e-1048">Az.Cdn</span></span>
* <span data-ttu-id="ab09e-1049">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="ab09e-1049">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1050">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1050">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1051">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="ab09e-1051">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-1052">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-1052">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-1053">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ab09e-1053">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ab09e-1054">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-1054">Az.LogicApp</span></span>
* <span data-ttu-id="ab09e-1055">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="ab09e-1055">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1056">Az.Network</span></span>
* <span data-ttu-id="ab09e-1057">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1057">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1058">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1058">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-1059">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-1059">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ab09e-1060">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="ab09e-1060">SDK Update</span></span>
* <span data-ttu-id="ab09e-1061">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ab09e-1061">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ab09e-1062">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ab09e-1062">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1063">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1063">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1064">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1064">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ab09e-1065">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ab09e-1065">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ab09e-1066">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ab09e-1066">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ab09e-1067">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ab09e-1067">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ab09e-1068">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ab09e-1068">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ab09e-1069">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ab09e-1069">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1070">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1070">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1071">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1071">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ab09e-1072">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1072">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-1073">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1073">Az.Storage</span></span>
* <span data-ttu-id="ab09e-1074">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-1074">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ab09e-1075">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1075">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ab09e-1076">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1076">Az.AnalysisServices</span></span>
* <span data-ttu-id="ab09e-1077">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="ab09e-1077">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-1078">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1078">Az.Automation</span></span>
* <span data-ttu-id="ab09e-1079">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1079">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ab09e-1080">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1080">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ab09e-1081">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1081">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-1082">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1082">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-1083">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1083">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1084">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1084">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1085">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="ab09e-1085">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ab09e-1086">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="ab09e-1086">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ab09e-1087">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1087">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ab09e-1088">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1088">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1089">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1089">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-1090">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="ab09e-1090">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ab09e-1091">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-1091">Az.EventHub</span></span>
* <span data-ttu-id="ab09e-1092">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="ab09e-1092">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="ab09e-1093">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-1093">Az.KeyVault</span></span>
* <span data-ttu-id="ab09e-1094">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ab09e-1094">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ab09e-1095">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-1095">Az.LogicApp</span></span>
* <span data-ttu-id="ab09e-1096">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1096">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ab09e-1097">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="ab09e-1097">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ab09e-1098">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1098">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ab09e-1099">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ab09e-1099">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ab09e-1100">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ab09e-1100">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ab09e-1101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ab09e-1101">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ab09e-1102">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ab09e-1102">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ab09e-1103">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1103">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ab09e-1104">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1104">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ab09e-1105">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1105">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ab09e-1106">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1106">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ab09e-1107">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1107">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ab09e-1108">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-1108">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ab09e-1109">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-1109">Az.Monitor</span></span>
* <span data-ttu-id="ab09e-1110">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ab09e-1110">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1111">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1111">Az.Network</span></span>
* <span data-ttu-id="ab09e-1112">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ab09e-1112">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-1113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-1113">Az.OperationalInsights</span></span>
* <span data-ttu-id="ab09e-1114">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1114">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ab09e-1115">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1115">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="ab09e-1116">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1116">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="ab09e-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1117">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1118">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ab09e-1118">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ab09e-1119">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ab09e-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ab09e-1120">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ab09e-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ab09e-1121">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ab09e-1121">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1122">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1123">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="ab09e-1123">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ab09e-1124">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="ab09e-1124">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-1125">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1125">Az.Websites</span></span>
* <span data-ttu-id="ab09e-1126">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ab09e-1126">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ab09e-1127">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1127">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-1128">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1128">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-1129">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ab09e-1129">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ab09e-1130">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1130">Az.AnalysisServices</span></span>
<span data-ttu-id="ab09e-1131">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1131">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1132">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1132">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1133">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="ab09e-1133">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ab09e-1134">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ab09e-1134">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ab09e-1135">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1135">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1136">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1136">Az.RecoveryServices</span></span>
<span data-ttu-id="ab09e-1137">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1137">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1138">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1138">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1139">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ab09e-1139">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="ab09e-1140">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ab09e-1140">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ab09e-1141">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ab09e-1141">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="ab09e-1142">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ab09e-1142">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1143">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1143">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1144">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1144">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ab09e-1145">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="ab09e-1145">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ab09e-1146">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ab09e-1146">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ab09e-1147">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1147">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-1148">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1148">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-1149">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1149">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ab09e-1150">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1150">Az.AnalysisServices</span></span>
* <span data-ttu-id="ab09e-1151">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1151">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1152">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1152">Az.RecoveryServices</span></span>
* <span data-ttu-id="ab09e-1153">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1153">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ab09e-1154">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1154">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-1155">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1155">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-1156">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ab09e-1156">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ab09e-1157">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1157">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ab09e-1158">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ab09e-1158">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ab09e-1159">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ab09e-1159">Az.Aks</span></span>
* <span data-ttu-id="ab09e-1160">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1160">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ab09e-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1161">Az.Automation</span></span>
* <span data-ttu-id="ab09e-1162">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="ab09e-1162">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ab09e-1163">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1163">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ab09e-1164">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ab09e-1164">Az.Cdn</span></span>
* <span data-ttu-id="ab09e-1165">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1165">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1166">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1167">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1167">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ab09e-1168">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ab09e-1168">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ab09e-1169">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ab09e-1169">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ab09e-1170">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ab09e-1170">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ab09e-1171">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1171">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ab09e-1172">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ab09e-1172">Az.DataFactory</span></span>
* <span data-ttu-id="ab09e-1173">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-1173">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1174">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1174">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-1175">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ab09e-1175">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ab09e-1176">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ab09e-1176">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ab09e-1177">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1177">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-1178">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-1178">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-1179">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1179">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ab09e-1180">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-1180">Az.KeyVault</span></span>
* <span data-ttu-id="ab09e-1181">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1181">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1182">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1182">Az.Network</span></span>
* <span data-ttu-id="ab09e-1183">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1183">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1184">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1185">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="ab09e-1185">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ab09e-1186">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ab09e-1186">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ab09e-1187">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ab09e-1187">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ab09e-1188">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ab09e-1188">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ab09e-1189">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ab09e-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ab09e-1190">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="ab09e-1190">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ab09e-1191">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ab09e-1191">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-1192">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-1192">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-1193">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ab09e-1193">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ab09e-1194">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1194">Fix some error messages.</span></span>
* <span data-ttu-id="ab09e-1195">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1195">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ab09e-1196">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1196">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ab09e-1197">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ab09e-1197">Az.SignalR</span></span>
* <span data-ttu-id="ab09e-1198">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1198">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1199">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1199">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1200">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1200">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ab09e-1201">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="ab09e-1201">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ab09e-1202">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="ab09e-1202">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ab09e-1203">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ab09e-1203">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-1204">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1204">Az.Storage</span></span>
* <span data-ttu-id="ab09e-1205">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1205">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ab09e-1206">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1206">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ab09e-1207">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ab09e-1207">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ab09e-1208">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ab09e-1208">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ab09e-1209">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ab09e-1209">Az.TrafficManager</span></span>
* <span data-ttu-id="ab09e-1210">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1210">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-1211">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1211">Az.Websites</span></span>
* <span data-ttu-id="ab09e-1212">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ab09e-1212">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ab09e-1213">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1213">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ab09e-1214">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="ab09e-1214">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ab09e-1215">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ab09e-1215">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ab09e-1216">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1216">Az.Accounts</span></span>
* <span data-ttu-id="ab09e-1217">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ab09e-1217">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1218">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1219">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1219">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ab09e-1220">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ab09e-1220">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ab09e-1221">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1221">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1222">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1222">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-1223">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1223">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ab09e-1224">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="ab09e-1224">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ab09e-1225">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ab09e-1225">Az.EventGrid</span></span>
* <span data-ttu-id="ab09e-1226">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1226">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ab09e-1227">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ab09e-1227">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ab09e-1228">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ab09e-1228">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ab09e-1229">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ab09e-1229">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ab09e-1230">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1230">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ab09e-1231">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ab09e-1231">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ab09e-1232">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ab09e-1232">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ab09e-1233">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ab09e-1233">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ab09e-1234">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1234">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ab09e-1235">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ab09e-1235">Dead letter endpoint.</span></span>
* <span data-ttu-id="ab09e-1236">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1236">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ab09e-1237">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1237">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ab09e-1238">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-1238">Az.IotHub</span></span>
* <span data-ttu-id="ab09e-1239">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="ab09e-1239">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ab09e-1240">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ab09e-1240">Az.LogicApp</span></span>
* <span data-ttu-id="ab09e-1241">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="ab09e-1241">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1242">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1243">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1243">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ab09e-1244">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ab09e-1244">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ab09e-1245">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ab09e-1245">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ab09e-1246">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ab09e-1246">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ab09e-1247">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1247">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ab09e-1248">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ab09e-1248">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ab09e-1249">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ab09e-1249">Az.SignalR</span></span>
* <span data-ttu-id="ab09e-1250">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1250">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1251">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1251">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1252">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1252">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ab09e-1253">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1253">Az.Storage</span></span>
* <span data-ttu-id="ab09e-1254">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="ab09e-1254">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ab09e-1255">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab09e-1255">New-AzStorageContext</span></span>
* <span data-ttu-id="ab09e-1256">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="ab09e-1256">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ab09e-1257">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ab09e-1257">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1258">Az.Websites</span></span>
* <span data-ttu-id="ab09e-1259">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1259">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ab09e-1260">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1260">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ab09e-1261">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1261">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ab09e-1262">Generale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1262">General</span></span>

- <span data-ttu-id="ab09e-1263">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="ab09e-1263">General Availability of Az Module</span></span>
- <span data-ttu-id="ab09e-1264">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="ab09e-1264">Online help for each module</span></span>
- <span data-ttu-id="ab09e-1265">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1265">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ab09e-1266">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="ab09e-1266">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ab09e-1267">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1267">Az.Accounts</span></span>
- <span data-ttu-id="ab09e-1268">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1268">Changed from Az.Profile</span></span>
- <span data-ttu-id="ab09e-1269">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="ab09e-1269">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ab09e-1270">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-1270">Az.ApiManagement</span></span>
- <span data-ttu-id="ab09e-1271">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="ab09e-1271">Fixes for #7002</span></span>
- <span data-ttu-id="ab09e-1272">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1272">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ab09e-1273">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ab09e-1273">Az.Batch</span></span>
- <span data-ttu-id="ab09e-1274">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1274">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ab09e-1275">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1275">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ab09e-1276">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1276">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ab09e-1277">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ab09e-1277">Az.Billing</span></span>
- <span data-ttu-id="ab09e-1278">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1278">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ab09e-1279">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1279">Az.CognitivServices</span></span>
- <span data-ttu-id="ab09e-1280">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-1280">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ab09e-1281">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ab09e-1281">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ab09e-1282">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1282">Az.ContainerInstance</span></span>
- <span data-ttu-id="ab09e-1283">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ab09e-1283">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ab09e-1284">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ab09e-1284">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ab09e-1285">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1285">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1286">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1286">Az.DataLakeStore</span></span>
- <span data-ttu-id="ab09e-1287">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1287">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ab09e-1288">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ab09e-1288">Az.Monitor</span></span>
- <span data-ttu-id="ab09e-1289">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1289">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ab09e-1290">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ab09e-1290">Az.KeyVault</span></span>
- <span data-ttu-id="ab09e-1291">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="ab09e-1291">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ab09e-1292">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ab09e-1292">Az.MachineLearning</span></span>
- <span data-ttu-id="ab09e-1293">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1293">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ab09e-1294">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ab09e-1294">Az.Media</span></span>
- <span data-ttu-id="ab09e-1295">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ab09e-1295">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ab09e-1296">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1296">Az.Network</span></span>
<span data-ttu-id="ab09e-1297">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1297">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ab09e-1298">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ab09e-1298">New cmdlets added:</span></span>
        - <span data-ttu-id="ab09e-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1299">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1300">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1301">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1302">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1303">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1304">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-1304">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ab09e-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1305">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ab09e-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ab09e-1306">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ab09e-1307">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1307">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ab09e-1308">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab09e-1308">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ab09e-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-1309">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ab09e-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ab09e-1310">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ab09e-1311">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-1311">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ab09e-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-1312">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ab09e-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1313">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ab09e-1314">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ab09e-1314">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ab09e-1315">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ab09e-1315">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ab09e-1316">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ab09e-1316">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ab09e-1317">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ab09e-1317">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ab09e-1318">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ab09e-1318">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ab09e-1319">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1319">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ab09e-1320">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-1320">Az.OperationalInsights</span></span>
- <span data-ttu-id="ab09e-1321">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1321">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ab09e-1322">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1322">Az.Profile</span></span>
- <span data-ttu-id="ab09e-1323">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ab09e-1323">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1324">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1324">Az.RecoveryServices</span></span>
- <span data-ttu-id="ab09e-1325">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1325">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ab09e-1326">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1326">Az.Resources</span></span>
- <span data-ttu-id="ab09e-1327">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1327">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ab09e-1328">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-1328">Az.ServiceFabric</span></span>
- <span data-ttu-id="ab09e-1329">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1329">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ab09e-1330">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1330">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ab09e-1331">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ab09e-1331">Az.SIgnalR</span></span>
- <span data-ttu-id="ab09e-1332">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ab09e-1332">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ab09e-1333">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1333">Az.Sql</span></span>
- <span data-ttu-id="ab09e-1334">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="ab09e-1334">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ab09e-1335">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1335">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ab09e-1336">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1336">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ab09e-1337">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1337">Az.Storage</span></span>
- <span data-ttu-id="ab09e-1338">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1338">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ab09e-1339">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1339">Az.Websites</span></span>
- <span data-ttu-id="ab09e-1340">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1340">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ab09e-1341">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1341">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ab09e-1342">Generale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1342">General</span></span>

* <span data-ttu-id="ab09e-1343">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ab09e-1343">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ab09e-1344">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1344">Az.Compute</span></span>

* <span data-ttu-id="ab09e-1345">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1345">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1346">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1346">Az.DataLakeStore</span></span>

* <span data-ttu-id="ab09e-1347">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="ab09e-1347">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ab09e-1348">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ab09e-1348">Az.FrontDoor</span></span>

* <span data-ttu-id="ab09e-1349">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ab09e-1349">Fixed some broken links</span></span>
    - <span data-ttu-id="ab09e-1350">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1350">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ab09e-1351">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1351">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ab09e-1352">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1352">Az.RecoveryServices</span></span>

* <span data-ttu-id="ab09e-1353">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1353">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ab09e-1354">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1354">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ab09e-1355">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1355">Az.Resources</span></span>

* <span data-ttu-id="ab09e-1356">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ab09e-1356">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ab09e-1357">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1357">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ab09e-1358">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1358">Az.Sql</span></span>

* <span data-ttu-id="ab09e-1359">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ab09e-1359">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ab09e-1360">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="ab09e-1360">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ab09e-1361">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1361">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ab09e-1362">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1362">Az.Storage</span></span>

* <span data-ttu-id="ab09e-1363">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-1363">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ab09e-1364">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="ab09e-1364">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ab09e-1365">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1365">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ab09e-1366">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="ab09e-1366">Support Static Website configuration</span></span>
    - <span data-ttu-id="ab09e-1367">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ab09e-1367">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ab09e-1368">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ab09e-1368">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ab09e-1369">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1369">Az.Websites</span></span>

* <span data-ttu-id="ab09e-1370">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ab09e-1370">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="ab09e-1371">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1371">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ab09e-1372">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1372">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ab09e-1373">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1373">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ab09e-1374">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ab09e-1374">Az.ApiManagement</span></span>
* <span data-ttu-id="ab09e-1375">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1375">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ab09e-1376">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ab09e-1376">Az.Automation</span></span>
* <span data-ttu-id="ab09e-1377">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="ab09e-1377">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ab09e-1378">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ab09e-1378">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ab09e-1379">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="ab09e-1379">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ab09e-1380">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ab09e-1380">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ab09e-1381">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="ab09e-1381">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ab09e-1382">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1382">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1383">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ab09e-1383">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ab09e-1384">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1384">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ab09e-1385">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1385">Az.ContainerInstance</span></span>
* <span data-ttu-id="ab09e-1386">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1386">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ab09e-1387">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ab09e-1387">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ab09e-1388">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="ab09e-1388">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ab09e-1389">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1389">Az.Network</span></span>
* <span data-ttu-id="ab09e-1390">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ab09e-1390">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ab09e-1391">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="ab09e-1391">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ab09e-1392">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1392">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="ab09e-1393">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ab09e-1393">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ab09e-1394">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ab09e-1394">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ab09e-1395">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1395">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ab09e-1396">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1396">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ab09e-1397">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ab09e-1397">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ab09e-1398">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ab09e-1398">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ab09e-1399">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab09e-1399">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ab09e-1400">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ab09e-1400">Az.Relay</span></span>
* <span data-ttu-id="ab09e-1401">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1401">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ab09e-1402">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1402">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1403">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ab09e-1403">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ab09e-1404">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="ab09e-1404">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ab09e-1405">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ab09e-1405">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ab09e-1406">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-1406">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-1407">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1407">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ab09e-1408">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1408">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1409">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="ab09e-1409">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ab09e-1410">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1410">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ab09e-1411">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1411">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ab09e-1412">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1412">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ab09e-1413">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ab09e-1413">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ab09e-1414">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ab09e-1414">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ab09e-1415">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ab09e-1415">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ab09e-1416">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ab09e-1416">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ab09e-1417">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ab09e-1417">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ab09e-1418">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1418">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ab09e-1419">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1419">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ab09e-1420">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1420">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ab09e-1421">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1421">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ab09e-1422">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1422">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ab09e-1423">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1423">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ab09e-1424">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1424">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ab09e-1425">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1425">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ab09e-1426">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1426">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ab09e-1427">Generale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1427">General</span></span>
* <span data-ttu-id="ab09e-1428">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="ab09e-1428">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ab09e-1429">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1429">Az.Profile</span></span>
* <span data-ttu-id="ab09e-1430">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ab09e-1430">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ab09e-1431">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="ab09e-1431">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ab09e-1432">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ab09e-1432">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ab09e-1433">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="ab09e-1433">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ab09e-1434">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="ab09e-1434">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ab09e-1435">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ab09e-1435">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ab09e-1436">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="ab09e-1436">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-1437">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1437">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-1438">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1438">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1439">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1439">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1440">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ab09e-1440">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ab09e-1441">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ab09e-1441">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ab09e-1442">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1442">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1443">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1443">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-1444">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1444">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ab09e-1445">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1445">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ab09e-1446">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ab09e-1446">Az.Insights</span></span>
* <span data-ttu-id="ab09e-1447">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="ab09e-1447">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ab09e-1448">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="ab09e-1448">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ab09e-1449">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1449">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ab09e-1450">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="ab09e-1450">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1451">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1451">Az.Network</span></span>
* <span data-ttu-id="ab09e-1452">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="ab09e-1452">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ab09e-1453">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ab09e-1453">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ab09e-1454">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ab09e-1454">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ab09e-1455">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ab09e-1455">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ab09e-1456">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ab09e-1456">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ab09e-1457">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ab09e-1457">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ab09e-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ab09e-1458">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ab09e-1459">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ab09e-1459">Az.PolicyInsights</span></span>
* <span data-ttu-id="ab09e-1460">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="ab09e-1460">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1461">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1462">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ab09e-1462">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ab09e-1463">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1463">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ab09e-1464">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ab09e-1464">Az.ServiceBus</span></span>
* <span data-ttu-id="ab09e-1465">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1465">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ab09e-1466">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab09e-1466">Az.ServiceFabric</span></span>
* <span data-ttu-id="ab09e-1467">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1467">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ab09e-1468">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1468">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ab09e-1469">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ab09e-1469">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ab09e-1470">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ab09e-1470">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ab09e-1471">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1471">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ab09e-1472">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1472">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ab09e-1473">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1473">Az.Profile</span></span>
* <span data-ttu-id="ab09e-1474">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="ab09e-1474">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ab09e-1475">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ab09e-1475">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1476">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1476">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1477">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="ab09e-1477">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ab09e-1478">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1478">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ab09e-1479">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ab09e-1479">Az.DataLakeStore</span></span>
* <span data-ttu-id="ab09e-1480">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1480">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ab09e-1481">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1481">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ab09e-1482">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1482">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ab09e-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1483">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ab09e-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1484">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1485">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1485">Az.Network</span></span>
* <span data-ttu-id="ab09e-1486">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1486">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ab09e-1487">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1487">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1488">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1488">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1489">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1489">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ab09e-1490">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1490">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ab09e-1491">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1491">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ab09e-1492">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1492">Azure.Storage</span></span>
* <span data-ttu-id="ab09e-1493">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="ab09e-1493">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ab09e-1494">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1494">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ab09e-1495">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ab09e-1495">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ab09e-1496">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="ab09e-1496">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ab09e-1497">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ab09e-1497">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="ab09e-1498">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ab09e-1498">Az.CognitiveServices</span></span>
* <span data-ttu-id="ab09e-1499">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1499">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ab09e-1500">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ab09e-1500">Az.Compute</span></span>
* <span data-ttu-id="ab09e-1501">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="ab09e-1501">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ab09e-1502">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1502">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ab09e-1503">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="ab09e-1503">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ab09e-1504">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ab09e-1504">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ab09e-1505">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ab09e-1505">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ab09e-1506">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ab09e-1506">Az.Network</span></span>
* <span data-ttu-id="ab09e-1507">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1507">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ab09e-1508">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1508">new cmdlets added</span></span>
    - <span data-ttu-id="ab09e-1509">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1509">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ab09e-1510">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1510">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ab09e-1511">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1511">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ab09e-1512">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ab09e-1512">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ab09e-1513">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-1513">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ab09e-1514">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-1514">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ab09e-1515">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="ab09e-1515">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ab09e-1516">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ab09e-1516">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ab09e-1517">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ab09e-1517">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ab09e-1518">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ab09e-1518">Az.RedisCache</span></span>
* <span data-ttu-id="ab09e-1519">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="ab09e-1519">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ab09e-1520">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ab09e-1520">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ab09e-1521">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ab09e-1521">Az.Resources</span></span>
* <span data-ttu-id="ab09e-1522">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ab09e-1522">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ab09e-1523">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="ab09e-1523">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ab09e-1524">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ab09e-1524">Az.Sql</span></span>
* <span data-ttu-id="ab09e-1525">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="ab09e-1525">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ab09e-1526">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ab09e-1526">Az.Websites</span></span>
* <span data-ttu-id="ab09e-1527">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="ab09e-1527">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ab09e-1528">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="ab09e-1528">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ab09e-1529">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="ab09e-1529">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ab09e-1530">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="ab09e-1530">Initial Release</span></span>
