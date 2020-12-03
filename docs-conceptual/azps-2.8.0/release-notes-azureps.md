---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 656e61e7f208367fc7fae28f73d1b6f289831d77
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427735"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="ff51b-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff51b-103">Azure PowerShell release notes</span></span>
## <a name="280---october-2019"></a><span data-ttu-id="ff51b-104">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-104">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="ff51b-105">Generale</span><span class="sxs-lookup"><span data-stu-id="ff51b-105">General</span></span>
* <span data-ttu-id="ff51b-106">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-106">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff51b-107">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-107">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-108">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="ff51b-108">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff51b-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-109">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-110">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-110">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="ff51b-111">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="ff51b-111">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-112">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-112">Az.Automation</span></span>
* <span data-ttu-id="ff51b-113">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="ff51b-113">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff51b-114">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-114">Az.Batch</span></span>
* <span data-ttu-id="ff51b-115">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="ff51b-115">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-116">Az.Compute</span></span>
* <span data-ttu-id="ff51b-117">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff51b-117">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="ff51b-118">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-118">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="ff51b-119">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="ff51b-119">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="ff51b-120">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-120">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-121">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-121">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-122">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="ff51b-122">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="ff51b-123">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="ff51b-123">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="ff51b-124">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-124">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-126">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="ff51b-126">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="ff51b-127">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="ff51b-127">Az.HealthcareApis</span></span>
* <span data-ttu-id="ff51b-128">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-128">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="ff51b-129">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="ff51b-129">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="ff51b-130">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="ff51b-130">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="ff51b-131">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="ff51b-131">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-132">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-133">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="ff51b-133">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="ff51b-134">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff51b-134">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-135">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-135">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-136">Aggiunta di nuovi ricevitori di gruppi di azioni per New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="ff51b-136">New action group receivers added for New-AzActionGroupReceiver:   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="ff51b-137">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="ff51b-137">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="ff51b-138">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="ff51b-138">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="ff51b-139">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ff51b-139">Webhooks now supports Azure active directory authentication.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-140">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-140">Az.Network</span></span>
* <span data-ttu-id="ff51b-141">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="ff51b-141">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="ff51b-142">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-142">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="ff51b-143">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ff51b-143">New cmdlets added:</span></span>
        - <span data-ttu-id="ff51b-144">New-AzIpsecTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-144">New-AzIpsecTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="ff51b-145">Cmdlet aggiornati con il parametro facoltativo -TrafficSelectorPolicies</span><span class="sxs-lookup"><span data-stu-id="ff51b-145">Cmdlets updated with optional parameter -TrafficSelectorPolicies</span></span>
        - <span data-ttu-id="ff51b-146">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-146">New-AzVirtualNetworkGatewayConnection</span></span>
        - <span data-ttu-id="ff51b-147">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-147">Set-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff51b-148">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="ff51b-148">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="ff51b-149">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-149">Updated cmdlets:</span></span>
        - <span data-ttu-id="ff51b-150">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-150">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff51b-151">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-151">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff51b-152">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-152">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ff51b-153">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="ff51b-153">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="ff51b-154">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="ff51b-154">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="ff51b-155">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ff51b-155">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="ff51b-156">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="ff51b-156">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff51b-157">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff51b-157">Az.RedisCache</span></span>
* <span data-ttu-id="ff51b-158">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="ff51b-158">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-159">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-159">Az.Sql</span></span>
* <span data-ttu-id="ff51b-160">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ff51b-160">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-161">Az.Storage</span></span>
* <span data-ttu-id="ff51b-162">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-162">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="ff51b-163">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ff51b-163">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ff51b-164">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ff51b-164">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="ff51b-165">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="ff51b-165">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="ff51b-166">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-166">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff51b-167">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff51b-167">Az.StorageSync</span></span>
* <span data-ttu-id="ff51b-168">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="ff51b-168">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-169">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-169">Az.Websites</span></span>
* <span data-ttu-id="ff51b-170">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="ff51b-170">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="ff51b-171">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-171">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ff51b-172">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-172">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-173">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="ff51b-173">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="ff51b-174">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="ff51b-174">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="ff51b-175">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-175">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-176">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-176">Az.Automation</span></span>
* <span data-ttu-id="ff51b-177">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="ff51b-177">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="ff51b-178">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="ff51b-178">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="ff51b-179">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="ff51b-179">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-180">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-180">Az.Compute</span></span>
* <span data-ttu-id="ff51b-181">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-181">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="ff51b-182">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-182">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ff51b-183">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="ff51b-183">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="ff51b-184">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ff51b-184">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="ff51b-185">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ff51b-185">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="ff51b-186">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-186">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="ff51b-187">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="ff51b-187">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="ff51b-188">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="ff51b-188">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="ff51b-189">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="ff51b-189">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-190">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-190">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-191">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ff51b-191">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="ff51b-192">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="ff51b-192">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ff51b-193">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff51b-193">Az.HDInsight</span></span>
* <span data-ttu-id="ff51b-194">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ff51b-194">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-195">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-195">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-196">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="ff51b-196">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="ff51b-197">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ff51b-197">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="ff51b-198">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="ff51b-198">New cmdlets are:</span></span>
    - <span data-ttu-id="ff51b-199">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff51b-199">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff51b-200">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff51b-200">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff51b-201">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff51b-201">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="ff51b-202">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="ff51b-202">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-203">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-204">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="ff51b-204">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="ff51b-205">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="ff51b-205">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="ff51b-206">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="ff51b-206">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="ff51b-207">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="ff51b-207">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="ff51b-208">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="ff51b-208">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="ff51b-209">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="ff51b-209">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="ff51b-210">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-210">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="ff51b-211">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-211">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="ff51b-212">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-212">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ff51b-213">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ff51b-213">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="ff51b-214">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-214">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="ff51b-215">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="ff51b-215">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="ff51b-216">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="ff51b-216">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="ff51b-217">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ff51b-217">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="ff51b-218">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="ff51b-218">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="ff51b-219">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="ff51b-219">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="ff51b-220">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="ff51b-220">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="ff51b-221">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-221">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="ff51b-222">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="ff51b-222">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="ff51b-223">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-223">Overall improved help files</span></span>
* <span data-ttu-id="ff51b-224">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="ff51b-224">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-225">Az.Network</span></span>
* <span data-ttu-id="ff51b-226">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="ff51b-226">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="ff51b-227">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="ff51b-227">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="ff51b-228">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="ff51b-228">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="ff51b-229">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="ff51b-229">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="ff51b-230">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="ff51b-230">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="ff51b-231">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ff51b-231">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="ff51b-232">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="ff51b-232">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="ff51b-233">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ff51b-233">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="ff51b-234">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-234">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="ff51b-235">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="ff51b-235">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="ff51b-236">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-236">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="ff51b-237">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-237">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="ff51b-238">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-238">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-239">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="ff51b-239">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="ff51b-240">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-240">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="ff51b-241">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ff51b-241">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff51b-242">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ff51b-242">New-VpnSite</span></span>
        - <span data-ttu-id="ff51b-243">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="ff51b-243">Update-VpnSite</span></span>
        - <span data-ttu-id="ff51b-244">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-244">New-VpnConnection</span></span>
        - <span data-ttu-id="ff51b-245">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-245">Update-VpnConnection</span></span>
* <span data-ttu-id="ff51b-246">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="ff51b-246">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-247">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-247">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-248">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="ff51b-248">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="ff51b-249">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="ff51b-249">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-250">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-250">Az.Resources</span></span>
* <span data-ttu-id="ff51b-251">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="ff51b-251">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-252">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-252">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-253">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ff51b-253">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="ff51b-254">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="ff51b-254">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="ff51b-255">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff51b-255">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff51b-256">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff51b-256">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff51b-257">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff51b-257">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff51b-258">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ff51b-258">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="ff51b-259">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff51b-259">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff51b-260">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff51b-260">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff51b-261">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff51b-261">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff51b-262">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff51b-262">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff51b-263">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="ff51b-263">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="ff51b-264">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="ff51b-264">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="ff51b-265">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ff51b-265">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="ff51b-266">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="ff51b-266">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="ff51b-267">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="ff51b-267">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="ff51b-268">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ff51b-268">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff51b-269">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff51b-269">Az.SignalR</span></span>
* <span data-ttu-id="ff51b-270">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="ff51b-270">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-271">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-271">Az.Sql</span></span>
* <span data-ttu-id="ff51b-272">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="ff51b-272">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="ff51b-273">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="ff51b-273">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="ff51b-274">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-274">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="ff51b-275">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="ff51b-275">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="ff51b-276">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="ff51b-276">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-277">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-277">Az.Storage</span></span>
* <span data-ttu-id="ff51b-278">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="ff51b-278">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="ff51b-279">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-279">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="ff51b-280">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-280">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="ff51b-281">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-281">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="ff51b-282">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="ff51b-282">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="ff51b-283">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-283">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="ff51b-284">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ff51b-284">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="ff51b-285">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff51b-285">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff51b-286">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff51b-286">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff51b-287">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff51b-287">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="ff51b-288">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ff51b-288">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-289">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-289">Az.Websites</span></span>
* <span data-ttu-id="ff51b-290">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione delle app al nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="ff51b-290">Fixing issue where webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="ff51b-291">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="ff51b-291">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="ff51b-292">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="ff51b-292">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="ff51b-293">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-293">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="ff51b-294">Generale</span><span class="sxs-lookup"><span data-stu-id="ff51b-294">General</span></span>
* <span data-ttu-id="ff51b-295">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="ff51b-295">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff51b-296">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-296">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-297">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="ff51b-297">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="ff51b-298">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ff51b-298">Az.Aks</span></span>
* <span data-ttu-id="ff51b-299">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="ff51b-299">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="ff51b-300">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="ff51b-300">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff51b-301">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-301">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-302">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="ff51b-302">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="ff51b-303">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="ff51b-303">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="ff51b-304">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="ff51b-304">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="ff51b-305">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="ff51b-305">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="ff51b-306">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ff51b-306">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff51b-307">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-307">Az.Batch</span></span>
* <span data-ttu-id="ff51b-308">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ff51b-308">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff51b-309">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff51b-309">Az.Cdn</span></span>
* <span data-ttu-id="ff51b-310">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="ff51b-310">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-311">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-311">Az.Compute</span></span>
* <span data-ttu-id="ff51b-312">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-312">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="ff51b-313">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff51b-313">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="ff51b-314">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-314">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="ff51b-315">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-315">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="ff51b-316">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="ff51b-316">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="ff51b-317">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff51b-317">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="ff51b-318">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ff51b-318">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="ff51b-319">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="ff51b-319">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-320">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-320">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-321">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="ff51b-321">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="ff51b-322">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="ff51b-322">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="ff51b-323">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="ff51b-323">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="ff51b-324">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="ff51b-324">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-326">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="ff51b-326">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff51b-327">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-327">Az.EventHub</span></span>
* <span data-ttu-id="ff51b-328">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-328">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="ff51b-329">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ff51b-329">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="ff51b-330">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="ff51b-330">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="ff51b-331">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ff51b-331">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="ff51b-332">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ff51b-332">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ff51b-333">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="ff51b-333">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-334">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-334">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-335">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-335">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-336">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-336">Az.Network</span></span>
* <span data-ttu-id="ff51b-337">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-337">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="ff51b-338">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="ff51b-338">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="ff51b-339">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="ff51b-339">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="ff51b-340">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="ff51b-340">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="ff51b-341">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="ff51b-341">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="ff51b-342">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-342">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="ff51b-343">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ff51b-343">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-344">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-344">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-345">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="ff51b-345">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="ff51b-346">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="ff51b-346">Added example</span></span>
    - <span data-ttu-id="ff51b-347">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="ff51b-347">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="ff51b-348">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff51b-348">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="ff51b-349">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="ff51b-349">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-350">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-350">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-351">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-351">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-352">Az.Resources</span></span>
* <span data-ttu-id="ff51b-353">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="ff51b-353">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="ff51b-354">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="ff51b-354">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="ff51b-355">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="ff51b-355">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="ff51b-356">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-356">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-357">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-357">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-358">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-358">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="ff51b-359">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="ff51b-359">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="ff51b-360">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="ff51b-360">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-361">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-361">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-362">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="ff51b-362">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="ff51b-363">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="ff51b-363">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="ff51b-364">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="ff51b-364">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="ff51b-365">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="ff51b-365">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="ff51b-366">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="ff51b-366">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="ff51b-367">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="ff51b-367">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-368">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-368">Az.Sql</span></span>
* <span data-ttu-id="ff51b-369">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-369">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-370">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-370">Az.Storage</span></span>
* <span data-ttu-id="ff51b-371">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ff51b-371">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="ff51b-372">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ff51b-372">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="ff51b-373">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-373">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="ff51b-374">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff51b-374">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="ff51b-375">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="ff51b-375">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="ff51b-376">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff51b-376">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-377">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-377">Az.Websites</span></span>
* <span data-ttu-id="ff51b-378">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ff51b-378">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="ff51b-379">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-379">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-380">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-380">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-381">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff51b-381">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="ff51b-382">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-382">Az.ApplicationInsights</span></span>
* <span data-ttu-id="ff51b-383">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="ff51b-383">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-384">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-384">Az.Automation</span></span>
* <span data-ttu-id="ff51b-385">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="ff51b-385">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-386">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-386">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-387">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-387">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-388">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-388">Az.Compute</span></span>
* <span data-ttu-id="ff51b-389">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff51b-389">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ff51b-390">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff51b-390">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ff51b-391">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="ff51b-391">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="ff51b-392">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="ff51b-392">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-393">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-393">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-394">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-394">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="ff51b-395">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="ff51b-395">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff51b-396">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-396">Az.EventHub</span></span>
* <span data-ttu-id="ff51b-397">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ff51b-397">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ff51b-398">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ff51b-398">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff51b-399">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-399">Az.KeyVault</span></span>
* <span data-ttu-id="ff51b-400">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="ff51b-400">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff51b-401">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-401">Az.LogicApp</span></span>
* <span data-ttu-id="ff51b-402">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="ff51b-402">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="ff51b-403">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="ff51b-403">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="ff51b-404">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-404">Az.ManagedServices</span></span>
* <span data-ttu-id="ff51b-405">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="ff51b-405">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-406">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-406">Az.Network</span></span>
* <span data-ttu-id="ff51b-407">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="ff51b-407">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="ff51b-408">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-408">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-409">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff51b-409">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff51b-410">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-410">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff51b-411">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-411">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff51b-412">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-412">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff51b-413">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-413">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff51b-414">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-414">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="ff51b-415">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="ff51b-415">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="ff51b-416">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-416">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="ff51b-417">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="ff51b-417">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="ff51b-418">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-418">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="ff51b-419">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-419">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="ff51b-420">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-420">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="ff51b-421">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="ff51b-421">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="ff51b-422">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="ff51b-422">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="ff51b-423">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-423">Updated cmdlets</span></span>
        - <span data-ttu-id="ff51b-424">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-424">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff51b-425">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-425">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="ff51b-426">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-426">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="ff51b-427">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-427">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="ff51b-428">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-428">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="ff51b-429">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ff51b-429">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff51b-430">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-430">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ff51b-431">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-431">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="ff51b-432">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-432">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="ff51b-433">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="ff51b-433">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="ff51b-434">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="ff51b-434">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="ff51b-435">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="ff51b-435">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-436">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-436">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-437">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="ff51b-437">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="ff51b-438">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="ff51b-438">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-439">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-439">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-440">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-440">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ff51b-441">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-441">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="ff51b-442">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-442">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="ff51b-443">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-443">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="ff51b-444">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-444">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="ff51b-445">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-445">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ff51b-446">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-446">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="ff51b-447">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-447">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="ff51b-448">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-448">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="ff51b-449">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="ff51b-449">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-450">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-450">Az.Resources</span></span>
- <span data-ttu-id="ff51b-451">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ff51b-451">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="ff51b-452">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ff51b-452">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-453">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-453">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-454">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="ff51b-454">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="ff51b-455">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="ff51b-455">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-456">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-456">Az.Sql</span></span>
* <span data-ttu-id="ff51b-457">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ff51b-457">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="ff51b-458">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="ff51b-458">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="ff51b-459">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="ff51b-459">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-460">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-460">Az.Storage</span></span>
* <span data-ttu-id="ff51b-461">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="ff51b-461">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff51b-462">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff51b-462">Az.StorageSync</span></span>
* <span data-ttu-id="ff51b-463">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="ff51b-463">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="ff51b-464">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="ff51b-464">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-465">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-465">Az.Websites</span></span>
* <span data-ttu-id="ff51b-466">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-466">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="ff51b-467">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-467">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="ff51b-468">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="ff51b-468">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="ff51b-469">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-469">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-470">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-470">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-471">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="ff51b-471">Add support for profile cmdlets</span></span>
* <span data-ttu-id="ff51b-472">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="ff51b-472">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="ff51b-473">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff51b-473">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="ff51b-474">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ff51b-474">Az.Advisor</span></span>
* <span data-ttu-id="ff51b-475">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="ff51b-475">GA release of Az.Advisor</span></span>
* <span data-ttu-id="ff51b-476">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ff51b-476">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="ff51b-477">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-477">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-478">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="ff51b-478">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="ff51b-479">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff51b-479">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="ff51b-480">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="ff51b-480">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="ff51b-481">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="ff51b-481">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="ff51b-482">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="ff51b-482">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="ff51b-483">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff51b-483">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="ff51b-484">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="ff51b-484">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-485">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-485">Az.Automation</span></span>
* <span data-ttu-id="ff51b-486">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="ff51b-486">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-487">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-487">Az.Compute</span></span>
* <span data-ttu-id="ff51b-488">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-488">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-489">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-489">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-490">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="ff51b-490">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff51b-491">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff51b-491">Az.EventGrid</span></span>
* <span data-ttu-id="ff51b-492">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="ff51b-492">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-493">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-493">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-494">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-494">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-495">Az.Network</span></span>
* <span data-ttu-id="ff51b-496">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="ff51b-496">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="ff51b-497">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="ff51b-497">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff51b-498">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-498">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff51b-499">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="ff51b-499">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="ff51b-500">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="ff51b-500">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-501">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-501">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-502">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="ff51b-502">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-503">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-503">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-504">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="ff51b-504">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-505">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-505">Az.Resources</span></span>
    - <span data-ttu-id="ff51b-506">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="ff51b-506">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="ff51b-507">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="ff51b-507">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="ff51b-508">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="ff51b-508">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="ff51b-509">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="ff51b-509">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-510">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-510">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-511">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ff51b-511">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-512">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-512">Az.Sql</span></span>
* <span data-ttu-id="ff51b-513">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="ff51b-513">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="ff51b-514">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-514">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="ff51b-515">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-515">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff51b-516">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-516">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff51b-517">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-517">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="ff51b-518">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-518">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ff51b-519">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-519">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="ff51b-520">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="ff51b-520">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="ff51b-521">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="ff51b-521">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-522">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-522">Az.Storage</span></span>
* <span data-ttu-id="ff51b-523">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-523">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="ff51b-524">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff51b-524">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="ff51b-525">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="ff51b-525">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="ff51b-526">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="ff51b-526">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="ff51b-527">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-527">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="ff51b-528">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-528">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="ff51b-529">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-529">Set-AzStorageAccount</span></span>
* <span data-ttu-id="ff51b-530">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="ff51b-530">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="ff51b-531">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ff51b-531">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="ff51b-532">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="ff51b-532">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="ff51b-533">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="ff51b-533">Az.StorageSync</span></span>
* <span data-ttu-id="ff51b-534">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="ff51b-534">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="ff51b-535">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-535">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-536">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-537">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="ff51b-537">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="ff51b-538">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="ff51b-538">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="ff51b-539">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="ff51b-539">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="ff51b-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ff51b-540">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="ff51b-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="ff51b-541">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-542">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-542">Az.Compute</span></span>
* <span data-ttu-id="ff51b-543">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-543">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="ff51b-544">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="ff51b-544">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="ff51b-545">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ff51b-545">Az.Dns</span></span>
* <span data-ttu-id="ff51b-546">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-546">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff51b-547">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff51b-547">Az.EventGrid</span></span>
* <span data-ttu-id="ff51b-548">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="ff51b-548">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="ff51b-549">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-549">New cmdlets:</span></span>
    - <span data-ttu-id="ff51b-550">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff51b-550">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff51b-551">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-551">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff51b-552">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff51b-552">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff51b-553">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-553">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="ff51b-554">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ff51b-554">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="ff51b-555">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-555">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff51b-556">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-556">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ff51b-557">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-557">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="ff51b-558">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-558">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="ff51b-559">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-559">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="ff51b-560">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="ff51b-560">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ff51b-561">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-561">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="ff51b-562">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ff51b-562">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="ff51b-563">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-563">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="ff51b-564">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="ff51b-564">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="ff51b-565">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-565">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="ff51b-566">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-566">Updated cmdlets:</span></span>
    - <span data-ttu-id="ff51b-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ff51b-567">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="ff51b-568">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ff51b-568">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ff51b-569">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ff51b-569">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="ff51b-570">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="ff51b-570">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="ff51b-571">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ff51b-571">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="ff51b-572">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="ff51b-572">Event subscription expiration date,</span></span>
            - <span data-ttu-id="ff51b-573">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-573">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="ff51b-574">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-574">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="ff51b-575">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-575">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="ff51b-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ff51b-576">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="ff51b-577">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-577">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="ff51b-578">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="ff51b-578">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="ff51b-579">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ff51b-579">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="ff51b-580">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="ff51b-580">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ff51b-581">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff51b-581">Az.FrontDoor</span></span>
* <span data-ttu-id="ff51b-582">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="ff51b-582">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="ff51b-583">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="ff51b-583">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="ff51b-584">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="ff51b-584">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="ff51b-585">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="ff51b-585">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-586">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-586">Az.Network</span></span>
* <span data-ttu-id="ff51b-587">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-587">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="ff51b-588">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-588">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="ff51b-589">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="ff51b-590">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ff51b-590">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="ff51b-591">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-591">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-592">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="ff51b-592">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="ff51b-593">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-593">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="ff51b-594">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-594">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-595">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-595">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff51b-596">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-596">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff51b-597">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="ff51b-597">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="ff51b-598">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-598">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="ff51b-599">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-599">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="ff51b-600">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff51b-600">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="ff51b-601">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-601">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-602">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff51b-602">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff51b-603">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff51b-603">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff51b-604">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ff51b-604">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="ff51b-605">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-605">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="ff51b-606">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="ff51b-606">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="ff51b-607">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ff51b-607">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="ff51b-608">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="ff51b-608">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="ff51b-609">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ff51b-609">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="ff51b-610">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="ff51b-610">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="ff51b-611">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="ff51b-611">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="ff51b-612">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-612">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="ff51b-613">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="ff51b-613">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="ff51b-614">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-614">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="ff51b-615">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="ff51b-615">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="ff51b-616">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-616">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="ff51b-617">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-617">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="ff51b-618">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="ff51b-618">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="ff51b-619">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-619">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="ff51b-620">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="ff51b-620">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="ff51b-621">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ff51b-621">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="ff51b-622">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-622">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="ff51b-623">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="ff51b-623">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="ff51b-624">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="ff51b-624">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="ff51b-625">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff51b-625">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="ff51b-626">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-626">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ff51b-627">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-627">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="ff51b-628">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-628">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-629">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-629">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-630">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="ff51b-630">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-631">Az.Resources</span></span>
* <span data-ttu-id="ff51b-632">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="ff51b-632">Support for additional Template Export options</span></span>
    - <span data-ttu-id="ff51b-633">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-633">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ff51b-634">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-634">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="ff51b-635">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="ff51b-635">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-636">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-636">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-637">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="ff51b-637">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-638">Az.Sql</span></span>
* <span data-ttu-id="ff51b-639">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ff51b-639">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="ff51b-640">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ff51b-640">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="ff51b-641">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="ff51b-641">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="ff51b-642">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-642">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff51b-643">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-643">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff51b-644">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ff51b-644">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="ff51b-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ff51b-645">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="ff51b-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="ff51b-646">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-647">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-647">Az.Storage</span></span>
* <span data-ttu-id="ff51b-648">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-648">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="ff51b-649">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-649">New-AzStorageAccount</span></span>
* <span data-ttu-id="ff51b-650">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="ff51b-650">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="ff51b-651">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-651">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-652">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-652">Az.Websites</span></span>
* <span data-ttu-id="ff51b-653">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="ff51b-653">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="ff51b-654">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="ff51b-654">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="ff51b-655">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-655">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="ff51b-656">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff51b-656">Az.Cdn</span></span>
* <span data-ttu-id="ff51b-657">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="ff51b-657">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-658">Az.Compute</span></span>
* <span data-ttu-id="ff51b-659">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-659">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="ff51b-660">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff51b-660">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff51b-661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-661">Az.EventHub</span></span>
* <span data-ttu-id="ff51b-662">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="ff51b-662">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="ff51b-663">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff51b-663">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-664">Az.Network</span></span>
* <span data-ttu-id="ff51b-665">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ff51b-665">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="ff51b-666">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="ff51b-666">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff51b-667">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-667">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff51b-668">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="ff51b-668">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-669">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-669">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-670">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="ff51b-670">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-671">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-671">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-672">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff51b-672">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-673">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-674">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="ff51b-674">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="ff51b-675">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-675">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-676">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-676">Az.Sql</span></span>
* <span data-ttu-id="ff51b-677">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="ff51b-677">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="ff51b-678">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-678">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="ff51b-679">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="ff51b-679">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="ff51b-680">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-680">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-681">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-681">Az.Websites</span></span>
* <span data-ttu-id="ff51b-682">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="ff51b-682">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="ff51b-683">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-683">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="ff51b-684">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-684">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-685">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="ff51b-685">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="ff51b-686">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-686">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="ff51b-687">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-687">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="ff51b-688">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="ff51b-688">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="ff51b-689">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-689">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="ff51b-690">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="ff51b-690">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="ff51b-691">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-691">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="ff51b-692">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-692">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="ff51b-693">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-693">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="ff51b-694">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="ff51b-694">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="ff51b-695">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-695">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="ff51b-696">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="ff51b-696">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="ff51b-697">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="ff51b-697">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="ff51b-698">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-698">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="ff51b-699">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-699">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="ff51b-700">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-700">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="ff51b-701">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-701">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="ff51b-702">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="ff51b-702">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="ff51b-703">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-703">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="ff51b-704">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-704">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="ff51b-705">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="ff51b-705">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="ff51b-706">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ff51b-706">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="ff51b-707">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="ff51b-707">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="ff51b-708">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-708">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="ff51b-709">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ff51b-709">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="ff51b-710">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="ff51b-710">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="ff51b-711">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-711">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="ff51b-712">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ff51b-712">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="ff51b-713">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ff51b-713">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="ff51b-714">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="ff51b-714">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="ff51b-715">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="ff51b-715">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="ff51b-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="ff51b-716">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="ff51b-717">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ff51b-717">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="ff51b-718">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff51b-718">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff51b-719">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="ff51b-719">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="ff51b-720">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="ff51b-720">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="ff51b-721">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="ff51b-721">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="ff51b-722">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="ff51b-722">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="ff51b-723">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="ff51b-723">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="ff51b-724">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff51b-724">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff51b-725">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-725">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ff51b-726">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ff51b-726">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ff51b-727">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-727">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="ff51b-728">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ff51b-728">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ff51b-729">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="ff51b-729">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="ff51b-730">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-730">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="ff51b-731">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ff51b-731">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="ff51b-732">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="ff51b-732">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="ff51b-733">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="ff51b-733">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="ff51b-734">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-734">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="ff51b-735">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="ff51b-735">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="ff51b-736">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="ff51b-736">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="ff51b-737">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="ff51b-737">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="ff51b-738">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="ff51b-738">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="ff51b-739">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="ff51b-739">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="ff51b-740">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="ff51b-740">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="ff51b-741">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff51b-741">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ff51b-742">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ff51b-742">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ff51b-743">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ff51b-743">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ff51b-744">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-744">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ff51b-745">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="ff51b-745">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="ff51b-746">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ff51b-746">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="ff51b-747">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="ff51b-747">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="ff51b-748">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-748">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="ff51b-749">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="ff51b-749">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="ff51b-750">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="ff51b-750">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="ff51b-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="ff51b-751">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="ff51b-752">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="ff51b-752">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="ff51b-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="ff51b-753">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="ff51b-754">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ff51b-754">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="ff51b-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="ff51b-755">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="ff51b-756">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="ff51b-756">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="ff51b-757">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="ff51b-757">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="ff51b-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-758">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="ff51b-759">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="ff51b-759">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="ff51b-760">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="ff51b-760">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="ff51b-761">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="ff51b-761">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-762">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-762">Az.Automation</span></span>
* <span data-ttu-id="ff51b-763">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="ff51b-763">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="ff51b-764">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="ff51b-764">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="ff51b-765">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="ff51b-765">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="ff51b-766">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="ff51b-766">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="ff51b-767">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="ff51b-767">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="ff51b-768">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="ff51b-768">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="ff51b-769">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-769">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-770">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-770">Az.Compute</span></span>
* <span data-ttu-id="ff51b-771">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="ff51b-771">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="ff51b-772">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="ff51b-772">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-773">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-773">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-774">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-774">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-775">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-776">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-776">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-777">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-777">Az.Network</span></span>
* <span data-ttu-id="ff51b-778">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="ff51b-778">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="ff51b-779">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="ff51b-779">Updated cmdlet:</span></span>
        - <span data-ttu-id="ff51b-780">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff51b-780">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="ff51b-781">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ff51b-781">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-782">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-782">Az.Resources</span></span>
* <span data-ttu-id="ff51b-783">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="ff51b-783">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-784">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-784">Az.Sql</span></span>
* <span data-ttu-id="ff51b-785">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="ff51b-785">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="ff51b-786">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-786">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-787">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-788">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="ff51b-788">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-789">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-789">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-790">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-790">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="ff51b-791">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="ff51b-791">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-792">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-792">Az.Compute</span></span>
* <span data-ttu-id="ff51b-793">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="ff51b-793">Proximity placement group feature.</span></span>
    - <span data-ttu-id="ff51b-794">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-794">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="ff51b-795">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-795">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="ff51b-796">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="ff51b-796">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="ff51b-797">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="ff51b-797">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="ff51b-798">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff51b-798">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="ff51b-799">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ff51b-799">Breaking changes</span></span>
    - <span data-ttu-id="ff51b-800">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="ff51b-800">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="ff51b-801">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="ff51b-801">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="ff51b-802">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="ff51b-802">Az.DeploymentManager</span></span>
* <span data-ttu-id="ff51b-803">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="ff51b-803">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="ff51b-804">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="ff51b-804">Az.Dns</span></span>
* <span data-ttu-id="ff51b-805">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="ff51b-805">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="ff51b-806">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="ff51b-806">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="ff51b-807">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="ff51b-807">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="ff51b-808">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff51b-808">Az.FrontDoor</span></span>
* <span data-ttu-id="ff51b-809">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-809">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="ff51b-810">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="ff51b-810">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="ff51b-811">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff51b-811">Az.HDInsight</span></span>
* <span data-ttu-id="ff51b-812">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-812">Removed two cmdlets:</span></span>
    - <span data-ttu-id="ff51b-813">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff51b-813">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="ff51b-814">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff51b-814">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ff51b-815">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="ff51b-815">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="ff51b-816">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="ff51b-816">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="ff51b-817">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="ff51b-817">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="ff51b-818">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-818">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-819">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-819">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-820">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="ff51b-820">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="ff51b-821">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="ff51b-821">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="ff51b-822">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-822">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="ff51b-823">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="ff51b-823">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="ff51b-824">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="ff51b-824">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="ff51b-825">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="ff51b-825">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="ff51b-826">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="ff51b-826">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="ff51b-827">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-827">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff51b-828">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-828">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff51b-829">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-829">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff51b-830">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-830">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff51b-831">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-831">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="ff51b-832">[Altre](/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="ff51b-832">[More](/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="ff51b-833">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ff51b-833">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-834">Az.Network</span></span>
* <span data-ttu-id="ff51b-835">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="ff51b-835">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="ff51b-836">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-836">New cmdlets</span></span>
        - <span data-ttu-id="ff51b-837">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-837">New-AzNatGateway</span></span>
        - <span data-ttu-id="ff51b-838">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-838">Get-AzNatGateway</span></span>
        - <span data-ttu-id="ff51b-839">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-839">Set-AzNatGateway</span></span>
        - <span data-ttu-id="ff51b-840">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-840">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="ff51b-841">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="ff51b-841">Updated cmdlets</span></span>
        - <span data-ttu-id="ff51b-842">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ff51b-842">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="ff51b-843">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="ff51b-843">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="ff51b-844">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-844">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="ff51b-845">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-845">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="ff51b-846">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="ff51b-846">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff51b-847">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-847">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff51b-848">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="ff51b-848">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="ff51b-849">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="ff51b-849">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="ff51b-850">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-850">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-851">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-851">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-852">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="ff51b-852">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="ff51b-853">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff51b-853">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="ff51b-854">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ff51b-854">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="ff51b-855">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-855">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="ff51b-856">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="ff51b-856">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="ff51b-857">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="ff51b-857">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="ff51b-858">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ff51b-858">Az.Relay</span></span>
* <span data-ttu-id="ff51b-859">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="ff51b-859">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-860">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-860">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-861">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff51b-861">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-862">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-862">Az.Storage</span></span>
* <span data-ttu-id="ff51b-863">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="ff51b-863">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="ff51b-864">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="ff51b-864">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="ff51b-865">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="ff51b-865">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="ff51b-866">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-866">New-AzStorageAccount</span></span>
* <span data-ttu-id="ff51b-867">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="ff51b-867">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="ff51b-868">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-868">New-AzStorageAccount</span></span>
    - <span data-ttu-id="ff51b-869">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-869">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="ff51b-870">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-870">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-871">Az.Websites</span></span>
* <span data-ttu-id="ff51b-872">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-872">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="ff51b-873">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="ff51b-873">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="ff51b-874">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-874">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff51b-875">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ff51b-875">Highlights since the last major release</span></span>
* <span data-ttu-id="ff51b-876">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ff51b-876">General availability of `Az` module</span></span>
* <span data-ttu-id="ff51b-877">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff51b-877">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff51b-878">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff51b-878">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff51b-879">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-879">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff51b-880">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ff51b-880">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff51b-881">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-881">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff51b-882">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-882">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff51b-883">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-883">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-884">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="ff51b-884">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="ff51b-885">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-885">Az.Batch</span></span>
* <span data-ttu-id="ff51b-886">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-886">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff51b-887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff51b-887">Az.Cdn</span></span>
* <span data-ttu-id="ff51b-888">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-888">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-889">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-889">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-890">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-890">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-891">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-891">Az.Compute</span></span>
* <span data-ttu-id="ff51b-892">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="ff51b-892">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="ff51b-893">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-893">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-894">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ff51b-894">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-895">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-896">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="ff51b-896">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-897">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-898">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-898">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff51b-899">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff51b-899">Az.EventGrid</span></span>
* <span data-ttu-id="ff51b-900">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="ff51b-900">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff51b-901">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-901">Az.EventHub</span></span>
* <span data-ttu-id="ff51b-902">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="ff51b-902">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="ff51b-903">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="ff51b-903">Az.HDInsight</span></span>
* <span data-ttu-id="ff51b-904">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-904">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-905">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-905">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-906">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-906">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff51b-907">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-907">Az.KeyVault</span></span>
* <span data-ttu-id="ff51b-908">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-908">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-909">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ff51b-909">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="ff51b-910">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ff51b-910">Az.MachineLearning</span></span>
* <span data-ttu-id="ff51b-911">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-911">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="ff51b-912">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ff51b-912">Az.Media</span></span>
* <span data-ttu-id="ff51b-913">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-913">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-914">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-914">Az.Monitor</span></span>
  * <span data-ttu-id="ff51b-915">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="ff51b-915">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="ff51b-916">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="ff51b-916">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="ff51b-917">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="ff51b-917">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="ff51b-918">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff51b-918">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ff51b-919">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff51b-919">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="ff51b-920">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="ff51b-920">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="ff51b-921">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="ff51b-921">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-922">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-922">Az.Network</span></span>
* <span data-ttu-id="ff51b-923">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-923">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-924">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ff51b-924">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="ff51b-925">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="ff51b-925">Az.NotificationHubs</span></span>
* <span data-ttu-id="ff51b-926">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-926">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-927">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-927">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-928">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-928">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="ff51b-929">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="ff51b-929">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="ff51b-930">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-930">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-931">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-931">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-932">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-932">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-933">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-933">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="ff51b-934">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="ff51b-934">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="ff51b-935">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="ff51b-935">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff51b-936">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff51b-936">Az.RedisCache</span></span>
* <span data-ttu-id="ff51b-937">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-937">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-938">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-938">Az.Resources</span></span>
* <span data-ttu-id="ff51b-939">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ff51b-939">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-940">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-940">Az.Sql</span></span>
* <span data-ttu-id="ff51b-941">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="ff51b-941">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="ff51b-942">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-942">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-943">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="ff51b-943">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="ff51b-944">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ff51b-944">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="ff51b-945">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="ff51b-945">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="ff51b-946">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="ff51b-946">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="ff51b-947">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="ff51b-947">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-948">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-948">Az.Websites</span></span>
* <span data-ttu-id="ff51b-949">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="ff51b-949">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="ff51b-950">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="ff51b-950">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="ff51b-951">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="ff51b-951">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="ff51b-952">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="ff51b-952">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="ff51b-953">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-953">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff51b-954">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ff51b-954">Highlights since the last major release</span></span>
* <span data-ttu-id="ff51b-955">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ff51b-955">General availability of `Az` module</span></span>
* <span data-ttu-id="ff51b-956">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff51b-956">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff51b-957">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff51b-957">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff51b-958">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-958">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff51b-959">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ff51b-959">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff51b-960">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-960">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff51b-961">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-961">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="ff51b-962">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-962">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-963">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="ff51b-963">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff51b-964">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-964">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff51b-965">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="ff51b-965">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="ff51b-966">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ff51b-966">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-967">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-967">Az.Automation</span></span>
* <span data-ttu-id="ff51b-968">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="ff51b-968">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="ff51b-969">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="ff51b-969">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="ff51b-970">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-970">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-971">Az.Compute</span></span>
* <span data-ttu-id="ff51b-972">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-972">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="ff51b-973">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="ff51b-973">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="ff51b-974">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-974">Az.ContainerInstance</span></span>
* <span data-ttu-id="ff51b-975">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="ff51b-975">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-976">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-976">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-977">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="ff51b-977">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="ff51b-978">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ff51b-978">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-979">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-979">Az.Resources</span></span>
* <span data-ttu-id="ff51b-980">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="ff51b-980">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="ff51b-981">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="ff51b-981">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="ff51b-982">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="ff51b-982">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="ff51b-983">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ff51b-983">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="ff51b-984">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="ff51b-984">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="ff51b-985">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="ff51b-985">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-986">Az.Sql</span></span>
* <span data-ttu-id="ff51b-987">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="ff51b-987">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-988">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-988">Az.Storage</span></span>
* <span data-ttu-id="ff51b-989">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="ff51b-989">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="ff51b-990">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff51b-990">New-AzStorageContext</span></span>
* <span data-ttu-id="ff51b-991">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="ff51b-991">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="ff51b-992">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ff51b-992">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ff51b-993">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="ff51b-993">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="ff51b-994">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-994">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="ff51b-995">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-995">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="ff51b-996">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="ff51b-996">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="ff51b-997">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-997">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ff51b-998">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-998">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="ff51b-999">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-999">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="ff51b-1000">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff51b-1000">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="ff51b-1001">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1001">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="ff51b-1002">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1002">Highlights since the last major release</span></span>
* <span data-ttu-id="ff51b-1003">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="ff51b-1003">General availability of `Az` module</span></span>
* <span data-ttu-id="ff51b-1004">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="ff51b-1004">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="ff51b-1005">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="ff51b-1005">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="ff51b-1006">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1006">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="ff51b-1007">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ff51b-1007">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff51b-1008">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1008">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="ff51b-1009">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-1009">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-1010">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1010">Az.Automation</span></span>
* <span data-ttu-id="ff51b-1011">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff51b-1011">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="ff51b-1012">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="ff51b-1012">Dynamic grouping</span></span>
    * <span data-ttu-id="ff51b-1013">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="ff51b-1013">Pre-Post script</span></span>
    * <span data-ttu-id="ff51b-1014">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="ff51b-1014">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1015">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1015">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1016">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="ff51b-1016">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="ff51b-1017">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1017">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff51b-1018">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-1018">Az.KeyVault</span></span>
* <span data-ttu-id="ff51b-1019">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-1019">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1020">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1020">Az.Network</span></span>
* <span data-ttu-id="ff51b-1021">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-1021">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="ff51b-1022">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="ff51b-1022">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1023">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1023">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-1024">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="ff51b-1024">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="ff51b-1025">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="ff51b-1025">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1026">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1026">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1027">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-1027">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="ff51b-1028">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="ff51b-1028">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1029">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1029">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1030">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1030">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-1031">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1031">Az.Storage</span></span>
* <span data-ttu-id="ff51b-1032">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1032">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="ff51b-1033">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1033">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff51b-1034">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1034">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff51b-1035">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1035">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="ff51b-1036">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="ff51b-1036">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="ff51b-1037">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="ff51b-1037">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="ff51b-1038">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-1038">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-1039">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1039">Az.Websites</span></span>
* <span data-ttu-id="ff51b-1040">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="ff51b-1040">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="ff51b-1041">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1041">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-1042">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1042">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-1043">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="ff51b-1043">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="ff51b-1044">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-1044">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-1045">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1045">Az.Automation</span></span>
* <span data-ttu-id="ff51b-1046">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-1046">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="ff51b-1047">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1047">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="ff51b-1048">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1048">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff51b-1049">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff51b-1049">Az.Cdn</span></span>
* <span data-ttu-id="ff51b-1050">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="ff51b-1050">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1051">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1051">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1052">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="ff51b-1052">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-1053">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-1053">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-1054">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="ff51b-1054">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff51b-1055">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-1055">Az.LogicApp</span></span>
* <span data-ttu-id="ff51b-1056">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="ff51b-1056">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1057">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1057">Az.Network</span></span>
* <span data-ttu-id="ff51b-1058">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1058">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1059">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1059">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-1060">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-1060">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="ff51b-1061">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="ff51b-1061">SDK Update</span></span>
* <span data-ttu-id="ff51b-1062">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff51b-1062">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="ff51b-1063">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff51b-1063">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1064">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1064">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1065">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1065">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="ff51b-1066">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="ff51b-1066">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="ff51b-1067">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ff51b-1067">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="ff51b-1068">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="ff51b-1068">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="ff51b-1069">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="ff51b-1069">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="ff51b-1070">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="ff51b-1070">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1071">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1071">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1072">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1072">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="ff51b-1073">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1073">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-1074">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1074">Az.Storage</span></span>
* <span data-ttu-id="ff51b-1075">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-1075">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="ff51b-1076">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1076">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="ff51b-1077">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1077">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff51b-1078">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="ff51b-1078">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-1079">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1079">Az.Automation</span></span>
* <span data-ttu-id="ff51b-1080">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1080">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="ff51b-1081">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1081">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="ff51b-1082">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1082">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-1083">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1083">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-1084">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1084">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1085">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1086">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="ff51b-1086">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="ff51b-1087">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="ff51b-1087">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="ff51b-1088">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1088">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="ff51b-1089">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1089">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1090">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1090">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-1091">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="ff51b-1091">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="ff51b-1092">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-1092">Az.EventHub</span></span>
* <span data-ttu-id="ff51b-1093">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="ff51b-1093">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff51b-1094">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-1094">Az.KeyVault</span></span>
* <span data-ttu-id="ff51b-1095">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ff51b-1095">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff51b-1096">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-1096">Az.LogicApp</span></span>
* <span data-ttu-id="ff51b-1097">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1097">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="ff51b-1098">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="ff51b-1098">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="ff51b-1099">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1099">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="ff51b-1100">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff51b-1100">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff51b-1101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff51b-1101">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff51b-1102">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff51b-1102">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="ff51b-1103">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="ff51b-1103">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="ff51b-1104">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1104">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="ff51b-1105">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1105">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff51b-1106">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1106">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff51b-1107">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1107">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="ff51b-1108">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1108">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="ff51b-1109">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-1109">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="ff51b-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-1110">Az.Monitor</span></span>
* <span data-ttu-id="ff51b-1111">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="ff51b-1111">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1112">Az.Network</span></span>
* <span data-ttu-id="ff51b-1113">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="ff51b-1113">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-1114">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-1114">Az.OperationalInsights</span></span>
* <span data-ttu-id="ff51b-1115">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1115">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="ff51b-1116">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1116">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="ff51b-1117">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1117">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1118">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1118">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1119">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ff51b-1119">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ff51b-1120">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ff51b-1120">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="ff51b-1121">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="ff51b-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="ff51b-1122">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="ff51b-1122">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1123">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1123">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1124">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="ff51b-1124">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="ff51b-1125">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="ff51b-1125">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-1126">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1126">Az.Websites</span></span>
* <span data-ttu-id="ff51b-1127">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="ff51b-1127">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="ff51b-1128">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1128">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-1129">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1129">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-1130">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff51b-1130">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff51b-1131">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1131">Az.AnalysisServices</span></span>
<span data-ttu-id="ff51b-1132">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1132">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1133">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1133">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1134">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="ff51b-1134">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="ff51b-1135">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="ff51b-1135">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="ff51b-1136">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1136">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1137">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1137">Az.RecoveryServices</span></span>
<span data-ttu-id="ff51b-1138">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1138">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1139">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1139">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1140">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="ff51b-1140">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="ff51b-1141">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="ff51b-1141">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="ff51b-1142">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="ff51b-1142">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="ff51b-1143">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="ff51b-1143">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1144">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1144">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1145">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1145">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="ff51b-1146">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="ff51b-1146">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="ff51b-1147">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="ff51b-1147">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="ff51b-1148">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1148">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1149">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-1150">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1150">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="ff51b-1151">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1151">Az.AnalysisServices</span></span>
* <span data-ttu-id="ff51b-1152">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1152">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1153">Az.RecoveryServices</span></span>
* <span data-ttu-id="ff51b-1154">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1154">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="ff51b-1155">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1155">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-1156">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1156">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-1157">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="ff51b-1157">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="ff51b-1158">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1158">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff51b-1159">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="ff51b-1159">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="ff51b-1160">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="ff51b-1160">Az.Aks</span></span>
* <span data-ttu-id="ff51b-1161">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1161">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="ff51b-1162">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1162">Az.Automation</span></span>
* <span data-ttu-id="ff51b-1163">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="ff51b-1163">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="ff51b-1164">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1164">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="ff51b-1165">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="ff51b-1165">Az.Cdn</span></span>
* <span data-ttu-id="ff51b-1166">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1166">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1167">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1167">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1168">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1168">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="ff51b-1169">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="ff51b-1169">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="ff51b-1170">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ff51b-1170">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="ff51b-1171">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ff51b-1171">Az.ContainerRegistry</span></span>
* <span data-ttu-id="ff51b-1172">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1172">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="ff51b-1173">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="ff51b-1173">Az.DataFactory</span></span>
* <span data-ttu-id="ff51b-1174">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-1174">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1175">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1175">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-1176">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ff51b-1176">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="ff51b-1177">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="ff51b-1177">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="ff51b-1178">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1178">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-1179">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-1179">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-1180">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1180">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="ff51b-1181">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-1181">Az.KeyVault</span></span>
* <span data-ttu-id="ff51b-1182">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1182">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1183">Az.Network</span></span>
* <span data-ttu-id="ff51b-1184">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1184">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1185">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1185">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1186">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="ff51b-1186">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="ff51b-1187">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ff51b-1187">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="ff51b-1188">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="ff51b-1188">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="ff51b-1189">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="ff51b-1189">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="ff51b-1190">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="ff51b-1190">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="ff51b-1191">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="ff51b-1191">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="ff51b-1192">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="ff51b-1192">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-1193">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-1193">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-1194">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="ff51b-1194">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="ff51b-1195">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1195">Fix some error messages.</span></span>
* <span data-ttu-id="ff51b-1196">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1196">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="ff51b-1197">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1197">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff51b-1198">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff51b-1198">Az.SignalR</span></span>
* <span data-ttu-id="ff51b-1199">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1199">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1200">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1200">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1201">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1201">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff51b-1202">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="ff51b-1202">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="ff51b-1203">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="ff51b-1203">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="ff51b-1204">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="ff51b-1204">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-1205">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1205">Az.Storage</span></span>
* <span data-ttu-id="ff51b-1206">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1206">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff51b-1207">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1207">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="ff51b-1208">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="ff51b-1208">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="ff51b-1209">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="ff51b-1209">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="ff51b-1210">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="ff51b-1210">Az.TrafficManager</span></span>
* <span data-ttu-id="ff51b-1211">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1211">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-1212">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1212">Az.Websites</span></span>
* <span data-ttu-id="ff51b-1213">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="ff51b-1213">Update incorrect online help URLs</span></span>
* <span data-ttu-id="ff51b-1214">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1214">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="ff51b-1215">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="ff51b-1215">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="ff51b-1216">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="ff51b-1216">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="ff51b-1217">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1217">Az.Accounts</span></span>
* <span data-ttu-id="ff51b-1218">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="ff51b-1218">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1219">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1219">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1220">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1220">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="ff51b-1221">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="ff51b-1221">Updated the description of ID in help files</span></span>
* <span data-ttu-id="ff51b-1222">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1222">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1223">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1223">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-1224">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1224">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="ff51b-1225">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="ff51b-1225">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="ff51b-1226">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="ff51b-1226">Az.EventGrid</span></span>
* <span data-ttu-id="ff51b-1227">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1227">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="ff51b-1228">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="ff51b-1228">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="ff51b-1229">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ff51b-1229">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ff51b-1230">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ff51b-1230">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ff51b-1231">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1231">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ff51b-1232">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ff51b-1232">Dead letter endpoint.</span></span>
    - <span data-ttu-id="ff51b-1233">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="ff51b-1233">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="ff51b-1234">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="ff51b-1234">Event Time-To-Live,</span></span>
        - <span data-ttu-id="ff51b-1235">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1235">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="ff51b-1236">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="ff51b-1236">Dead letter endpoint.</span></span>
* <span data-ttu-id="ff51b-1237">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1237">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="ff51b-1238">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1238">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="ff51b-1239">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-1239">Az.IotHub</span></span>
* <span data-ttu-id="ff51b-1240">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="ff51b-1240">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="ff51b-1241">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="ff51b-1241">Az.LogicApp</span></span>
* <span data-ttu-id="ff51b-1242">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="ff51b-1242">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1243">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1243">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1244">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1244">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="ff51b-1245">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="ff51b-1245">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="ff51b-1246">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff51b-1246">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ff51b-1247">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="ff51b-1247">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="ff51b-1248">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1248">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="ff51b-1249">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="ff51b-1249">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="ff51b-1250">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="ff51b-1250">Az.SignalR</span></span>
* <span data-ttu-id="ff51b-1251">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1251">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1252">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1253">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1253">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="ff51b-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1254">Az.Storage</span></span>
* <span data-ttu-id="ff51b-1255">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="ff51b-1255">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="ff51b-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff51b-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="ff51b-1257">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="ff51b-1257">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="ff51b-1258">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="ff51b-1258">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-1259">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1259">Az.Websites</span></span>
* <span data-ttu-id="ff51b-1260">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1260">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="ff51b-1261">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1261">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="ff51b-1262">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1262">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="ff51b-1263">Generale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1263">General</span></span>

- <span data-ttu-id="ff51b-1264">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="ff51b-1264">General Availability of Az Module</span></span>
- <span data-ttu-id="ff51b-1265">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="ff51b-1265">Online help for each module</span></span>
- <span data-ttu-id="ff51b-1266">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1266">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="ff51b-1267">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="ff51b-1267">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="ff51b-1268">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1268">Az.Accounts</span></span>
- <span data-ttu-id="ff51b-1269">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1269">Changed from Az.Profile</span></span>
- <span data-ttu-id="ff51b-1270">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="ff51b-1270">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ff51b-1271">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-1271">Az.ApiManagement</span></span>
- <span data-ttu-id="ff51b-1272">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="ff51b-1272">Fixes for #7002</span></span>
- <span data-ttu-id="ff51b-1273">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1273">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="ff51b-1274">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ff51b-1274">Az.Batch</span></span>
- <span data-ttu-id="ff51b-1275">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1275">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="ff51b-1276">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1276">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="ff51b-1277">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1277">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="ff51b-1278">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="ff51b-1278">Az.Billing</span></span>
- <span data-ttu-id="ff51b-1279">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1279">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="ff51b-1280">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1280">Az.CognitivServices</span></span>
- <span data-ttu-id="ff51b-1281">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-1281">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="ff51b-1282">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="ff51b-1282">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ff51b-1283">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1283">Az.ContainerInstance</span></span>
- <span data-ttu-id="ff51b-1284">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="ff51b-1284">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="ff51b-1285">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="ff51b-1285">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="ff51b-1286">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1286">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1287">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1287">Az.DataLakeStore</span></span>
- <span data-ttu-id="ff51b-1288">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1288">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="ff51b-1289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ff51b-1289">Az.Monitor</span></span>
- <span data-ttu-id="ff51b-1290">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1290">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="ff51b-1291">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ff51b-1291">Az.KeyVault</span></span>
- <span data-ttu-id="ff51b-1292">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="ff51b-1292">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="ff51b-1293">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="ff51b-1293">Az.MachineLearning</span></span>
- <span data-ttu-id="ff51b-1294">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1294">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="ff51b-1295">Az.Media</span><span class="sxs-lookup"><span data-stu-id="ff51b-1295">Az.Media</span></span>
- <span data-ttu-id="ff51b-1296">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="ff51b-1296">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ff51b-1297">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1297">Az.Network</span></span>
<span data-ttu-id="ff51b-1298">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1298">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="ff51b-1299">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="ff51b-1299">New cmdlets added:</span></span>
        - <span data-ttu-id="ff51b-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1300">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1301">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1302">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1303">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1304">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1305">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-1305">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="ff51b-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1306">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="ff51b-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff51b-1307">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="ff51b-1308">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1308">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="ff51b-1309">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ff51b-1309">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="ff51b-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-1310">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ff51b-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="ff51b-1311">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="ff51b-1312">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-1312">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="ff51b-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-1313">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="ff51b-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1314">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="ff51b-1315">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ff51b-1315">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="ff51b-1316">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff51b-1316">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ff51b-1317">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff51b-1317">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="ff51b-1318">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="ff51b-1318">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="ff51b-1319">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ff51b-1319">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="ff51b-1320">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1320">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="ff51b-1321">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-1321">Az.OperationalInsights</span></span>
- <span data-ttu-id="ff51b-1322">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1322">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="ff51b-1323">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1323">Az.Profile</span></span>
- <span data-ttu-id="ff51b-1324">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="ff51b-1324">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1325">Az.RecoveryServices</span></span>
- <span data-ttu-id="ff51b-1326">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1326">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="ff51b-1327">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1327">Az.Resources</span></span>
- <span data-ttu-id="ff51b-1328">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1328">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ff51b-1329">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-1329">Az.ServiceFabric</span></span>
- <span data-ttu-id="ff51b-1330">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1330">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="ff51b-1331">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1331">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="ff51b-1332">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ff51b-1332">Az.SIgnalR</span></span>
- <span data-ttu-id="ff51b-1333">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="ff51b-1333">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="ff51b-1334">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1334">Az.Sql</span></span>
- <span data-ttu-id="ff51b-1335">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="ff51b-1335">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="ff51b-1336">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1336">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="ff51b-1337">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1337">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="ff51b-1338">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1338">Az.Storage</span></span>
- <span data-ttu-id="ff51b-1339">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1339">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ff51b-1340">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1340">Az.Websites</span></span>
- <span data-ttu-id="ff51b-1341">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1341">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="ff51b-1342">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1342">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="ff51b-1343">Generale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1343">General</span></span>

* <span data-ttu-id="ff51b-1344">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ff51b-1344">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="ff51b-1345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1345">Az.Compute</span></span>

* <span data-ttu-id="ff51b-1346">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1346">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1347">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1347">Az.DataLakeStore</span></span>

* <span data-ttu-id="ff51b-1348">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="ff51b-1348">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="ff51b-1349">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="ff51b-1349">Az.FrontDoor</span></span>

* <span data-ttu-id="ff51b-1350">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ff51b-1350">Fixed some broken links</span></span>
    - <span data-ttu-id="ff51b-1351">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1351">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="ff51b-1352">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1352">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="ff51b-1353">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1353">Az.RecoveryServices</span></span>

* <span data-ttu-id="ff51b-1354">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1354">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="ff51b-1355">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1355">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="ff51b-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1356">Az.Resources</span></span>

* <span data-ttu-id="ff51b-1357">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="ff51b-1357">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="ff51b-1358">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1358">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="ff51b-1359">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1359">Az.Sql</span></span>

* <span data-ttu-id="ff51b-1360">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="ff51b-1360">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="ff51b-1361">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="ff51b-1361">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="ff51b-1362">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1362">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="ff51b-1363">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1363">Az.Storage</span></span>

* <span data-ttu-id="ff51b-1364">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-1364">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="ff51b-1365">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="ff51b-1365">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="ff51b-1366">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1366">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ff51b-1367">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="ff51b-1367">Support Static Website configuration</span></span>
    - <span data-ttu-id="ff51b-1368">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff51b-1368">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="ff51b-1369">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="ff51b-1369">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="ff51b-1370">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1370">Az.Websites</span></span>

* <span data-ttu-id="ff51b-1371">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ff51b-1371">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="ff51b-1372">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1372">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="ff51b-1373">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1373">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="ff51b-1374">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1374">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="ff51b-1375">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ff51b-1375">Az.ApiManagement</span></span>
* <span data-ttu-id="ff51b-1376">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1376">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="ff51b-1377">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="ff51b-1377">Az.Automation</span></span>
* <span data-ttu-id="ff51b-1378">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="ff51b-1378">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="ff51b-1379">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="ff51b-1379">Added Update Management cmdlets</span></span>
* <span data-ttu-id="ff51b-1380">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="ff51b-1380">Added Source Control cmdlets</span></span>
* <span data-ttu-id="ff51b-1381">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="ff51b-1381">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="ff51b-1382">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="ff51b-1382">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="ff51b-1383">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1383">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1384">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ff51b-1384">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="ff51b-1385">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1385">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="ff51b-1386">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1386">Az.ContainerInstance</span></span>
* <span data-ttu-id="ff51b-1387">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1387">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="ff51b-1388">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ff51b-1388">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="ff51b-1389">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="ff51b-1389">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="ff51b-1390">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1390">Az.Network</span></span>
* <span data-ttu-id="ff51b-1391">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="ff51b-1391">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="ff51b-1392">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="ff51b-1392">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="ff51b-1393">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1393">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="ff51b-1394">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="ff51b-1394">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="ff51b-1395">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="ff51b-1395">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="ff51b-1396">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1396">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="ff51b-1397">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1397">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="ff51b-1398">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="ff51b-1398">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="ff51b-1399">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ff51b-1399">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="ff51b-1400">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="ff51b-1400">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="ff51b-1401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="ff51b-1401">Az.Relay</span></span>
* <span data-ttu-id="ff51b-1402">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1402">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="ff51b-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1403">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1404">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="ff51b-1404">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="ff51b-1405">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="ff51b-1405">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="ff51b-1406">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="ff51b-1406">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="ff51b-1407">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-1407">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-1408">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1408">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="ff51b-1409">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1409">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1410">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="ff51b-1410">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="ff51b-1411">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1411">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff51b-1412">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1412">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff51b-1413">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1413">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff51b-1414">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="ff51b-1414">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="ff51b-1415">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff51b-1415">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff51b-1416">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff51b-1416">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff51b-1417">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff51b-1417">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="ff51b-1418">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="ff51b-1418">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="ff51b-1419">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1419">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="ff51b-1420">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1420">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="ff51b-1421">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1421">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="ff51b-1422">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1422">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ff51b-1423">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1423">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="ff51b-1424">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1424">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="ff51b-1425">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1425">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="ff51b-1426">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1426">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="ff51b-1427">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1427">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="ff51b-1428">Generale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1428">General</span></span>
* <span data-ttu-id="ff51b-1429">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="ff51b-1429">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="ff51b-1430">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1430">Az.Profile</span></span>
* <span data-ttu-id="ff51b-1431">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff51b-1431">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="ff51b-1432">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="ff51b-1432">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="ff51b-1433">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="ff51b-1433">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="ff51b-1434">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="ff51b-1434">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="ff51b-1435">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="ff51b-1435">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="ff51b-1436">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="ff51b-1436">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="ff51b-1437">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="ff51b-1437">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-1438">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1438">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-1439">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1439">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1440">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1440">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1441">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ff51b-1441">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="ff51b-1442">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="ff51b-1442">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="ff51b-1443">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1443">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1444">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1444">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-1445">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1445">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="ff51b-1446">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1446">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="ff51b-1447">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="ff51b-1447">Az.Insights</span></span>
* <span data-ttu-id="ff51b-1448">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="ff51b-1448">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="ff51b-1449">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="ff51b-1449">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="ff51b-1450">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1450">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="ff51b-1451">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="ff51b-1451">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1452">Az.Network</span></span>
* <span data-ttu-id="ff51b-1453">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff51b-1453">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="ff51b-1454">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff51b-1454">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="ff51b-1455">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="ff51b-1455">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="ff51b-1456">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ff51b-1456">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="ff51b-1457">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="ff51b-1457">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="ff51b-1458">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="ff51b-1458">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="ff51b-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="ff51b-1459">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="ff51b-1460">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="ff51b-1460">Az.PolicyInsights</span></span>
* <span data-ttu-id="ff51b-1461">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="ff51b-1461">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1462">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1462">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1463">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="ff51b-1463">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="ff51b-1464">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1464">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="ff51b-1465">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="ff51b-1465">Az.ServiceBus</span></span>
* <span data-ttu-id="ff51b-1466">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1466">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="ff51b-1467">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ff51b-1467">Az.ServiceFabric</span></span>
* <span data-ttu-id="ff51b-1468">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1468">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="ff51b-1469">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1469">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="ff51b-1470">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="ff51b-1470">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="ff51b-1471">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="ff51b-1471">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="ff51b-1472">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1472">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="ff51b-1473">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1473">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="ff51b-1474">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1474">Az.Profile</span></span>
* <span data-ttu-id="ff51b-1475">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="ff51b-1475">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="ff51b-1476">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="ff51b-1476">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1477">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1478">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="ff51b-1478">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="ff51b-1479">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1479">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="ff51b-1480">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="ff51b-1480">Az.DataLakeStore</span></span>
* <span data-ttu-id="ff51b-1481">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1481">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="ff51b-1482">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1482">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="ff51b-1483">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1483">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ff51b-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1484">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="ff51b-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1485">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1486">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1486">Az.Network</span></span>
* <span data-ttu-id="ff51b-1487">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1487">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="ff51b-1488">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1488">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1489">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1489">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1490">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1490">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="ff51b-1491">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1491">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="ff51b-1492">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1492">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="ff51b-1493">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1493">Azure.Storage</span></span>
* <span data-ttu-id="ff51b-1494">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="ff51b-1494">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="ff51b-1495">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1495">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="ff51b-1496">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="ff51b-1496">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="ff51b-1497">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="ff51b-1497">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="ff51b-1498">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="ff51b-1498">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="ff51b-1499">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="ff51b-1499">Az.CognitiveServices</span></span>
* <span data-ttu-id="ff51b-1500">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1500">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="ff51b-1501">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ff51b-1501">Az.Compute</span></span>
* <span data-ttu-id="ff51b-1502">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="ff51b-1502">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="ff51b-1503">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1503">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="ff51b-1504">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="ff51b-1504">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="ff51b-1505">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="ff51b-1505">Az.DataFactoryV2</span></span>
* <span data-ttu-id="ff51b-1506">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="ff51b-1506">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="ff51b-1507">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ff51b-1507">Az.Network</span></span>
* <span data-ttu-id="ff51b-1508">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1508">Added NetworkProfile functionality.</span></span> <span data-ttu-id="ff51b-1509">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1509">new cmdlets added</span></span>
    - <span data-ttu-id="ff51b-1510">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1510">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff51b-1511">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1511">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff51b-1512">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1512">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff51b-1513">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ff51b-1513">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="ff51b-1514">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-1514">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="ff51b-1515">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-1515">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="ff51b-1516">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="ff51b-1516">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="ff51b-1517">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ff51b-1517">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="ff51b-1518">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ff51b-1518">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="ff51b-1519">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="ff51b-1519">Az.RedisCache</span></span>
* <span data-ttu-id="ff51b-1520">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="ff51b-1520">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="ff51b-1521">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="ff51b-1521">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="ff51b-1522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ff51b-1522">Az.Resources</span></span>
* <span data-ttu-id="ff51b-1523">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff51b-1523">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="ff51b-1524">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="ff51b-1524">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="ff51b-1525">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="ff51b-1525">Az.Sql</span></span>
* <span data-ttu-id="ff51b-1526">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="ff51b-1526">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="ff51b-1527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="ff51b-1527">Az.Websites</span></span>
* <span data-ttu-id="ff51b-1528">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="ff51b-1528">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="ff51b-1529">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="ff51b-1529">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="ff51b-1530">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="ff51b-1530">0.2.0 - September 2018</span></span>
 <span data-ttu-id="ff51b-1531">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="ff51b-1531">Initial Release</span></span>