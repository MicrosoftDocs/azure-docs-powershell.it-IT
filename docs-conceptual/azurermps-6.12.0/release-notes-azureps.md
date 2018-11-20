---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: 8a7b184ed06eb078956229fa67d02840014e3aaf
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574533"
---
# <a name="release-notes"></a><span data-ttu-id="c20a0-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="c20a0-103">Release notes</span></span>

<span data-ttu-id="c20a0-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6120---november-2018"></a><span data-ttu-id="c20a0-105">6.12.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-105">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-107">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c20a0-107">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c20a0-108">Parametro TenantId nel cmdlet Connect-AzureRmAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="c20a0-108">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c20a0-109">Aggiornamento della descrizione di TenantId per Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c20a0-109">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="c20a0-110">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="c20a0-110">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c20a0-111">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="c20a0-111">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c20a0-112">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="c20a0-112">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c20a0-113">Risoluzione del problema per il quale 'Disconnect-AzureRmAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="c20a0-113">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="c20a0-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c20a0-114">AzureRM.Automation</span></span>
* <span data-ttu-id="c20a0-115">Cmdlet DLL filename rinominato in Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="c20a0-115">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c20a0-116">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-116">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c20a0-117">Aggiunta dell'operazione Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c20a0-117">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-118">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-118">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-119">Aggiunta dei cmdlet Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c20a0-119">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c20a0-120">Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c20a0-120">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c20a0-121">Correzione dei valori di opzione di SetAzureRmVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="c20a0-121">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-122">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-122">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-123">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c20a0-123">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c20a0-124">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="c20a0-124">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c20a0-125">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-125">AzureRM.Insights</span></span>
* <span data-ttu-id="c20a0-126">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="c20a0-126">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c20a0-127">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="c20a0-127">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c20a0-128">Correzione del problema numero 7513 [Insights] per il quale Set-AzureRMDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="c20a0-128">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c20a0-129">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="c20a0-129">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-130">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-130">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-131">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20a0-131">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c20a0-132">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-132">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c20a0-133">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-133">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c20a0-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c20a0-134">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c20a0-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-135">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c20a0-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-136">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c20a0-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c20a0-137">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c20a0-138">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-138">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c20a0-139">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="c20a0-139">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c20a0-140">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-140">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c20a0-141">Aggiunta del supporto per le condivisioni di File di Azure nei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c20a0-141">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-142">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-142">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-143">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c20a0-143">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c20a0-144">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c20a0-144">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-145">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-145">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-146">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-146">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c20a0-147">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c20a0-147">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c20a0-148">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="c20a0-148">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c20a0-149">Correzione di 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="c20a0-149">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c20a0-150">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c20a0-150">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c20a0-151">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c20a0-151">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c20a0-152">Correzione di 'Update-AzureRmServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c20a0-152">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="c20a0-153">6.11.0 - ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-153">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-154">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-154">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-155">Risoluzione del problema con Get-AzureRmSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="c20a0-155">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="c20a0-156">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c20a0-156">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c20a0-157">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-157">AzureRM.Backup</span></span>
* <span data-ttu-id="c20a0-158">Cmdlet di Backup di Azure deprecati.</span><span class="sxs-lookup"><span data-stu-id="c20a0-158">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-159">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-159">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-160">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzureRmVm'.</span><span class="sxs-lookup"><span data-stu-id="c20a0-160">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="c20a0-161">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c20a0-161">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-162">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-162">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-163">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c20a0-163">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c20a0-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: ottiene o elenca le regole di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c20a0-164">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c20a0-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c20a0-165">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c20a0-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica la regola di rete virtuale specificata nell'account Data Lake Store indicato.</span><span class="sxs-lookup"><span data-stu-id="c20a0-166">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c20a0-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c20a0-167">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-168">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-168">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-169">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="c20a0-169">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c20a0-170">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c20a0-170">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-171">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-171">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-172">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzureRMRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="c20a0-172">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c20a0-173">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="c20a0-173">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="c20a0-174">6.10.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-174">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c20a0-175">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-175">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-176">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="c20a0-176">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c20a0-177">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c20a0-177">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c20a0-178">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c20a0-178">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c20a0-179">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-179">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c20a0-180">Supporto di Get-AzureRmCognitiveServicesAccountSkus senza un account esistente</span><span class="sxs-lookup"><span data-stu-id="c20a0-180">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-181">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-181">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-182">Correzione di Get-AzureRmVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="c20a0-182">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c20a0-183">Aggiunta di un esempio di SimpleParameterSet alla Guida del cmdlet New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-183">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="c20a0-184">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="c20a0-184">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c20a0-185">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c20a0-185">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c20a0-186">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="c20a0-186">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-187">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-187">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-188">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-188">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c20a0-189">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="c20a0-189">new cmdlets added</span></span>
    - <span data-ttu-id="c20a0-190">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-190">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c20a0-191">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-191">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c20a0-192">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-192">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c20a0-193">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-193">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c20a0-194">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-194">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="c20a0-195">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-195">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c20a0-196">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-196">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c20a0-197">Aggiunta dei cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap e Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c20a0-197">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="c20a0-198">Aggiunta dei cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig e Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-198">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c20a0-199">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c20a0-199">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c20a0-200">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="c20a0-200">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c20a0-201">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c20a0-201">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-202">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-202">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-203">Aggiunta del parametro -Mode mancante a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c20a0-203">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="c20a0-204">Correzione del bug del cmdlet Get-AzureRmProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="c20a0-204">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-205">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-205">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-206">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="c20a0-206">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c20a0-207">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-207">AzureRM.Storage</span></span>
* <span data-ttu-id="c20a0-208">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="c20a0-208">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c20a0-209">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c20a0-209">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-210">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-210">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-211">Nuovo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="c20a0-211">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c20a0-212">Nuovi cmdlet New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c20a0-212">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="c20a0-213">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-213">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c20a0-214">Generale</span><span class="sxs-lookup"><span data-stu-id="c20a0-214">General</span></span>
* <span data-ttu-id="c20a0-215">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="c20a0-215">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-216">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-216">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-217">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c20a0-217">Minor changes to the storage common code</span></span>
* <span data-ttu-id="c20a0-218">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="c20a0-218">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="c20a0-219">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c20a0-219">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="c20a0-220">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-220">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-221">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="c20a0-221">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="c20a0-222">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c20a0-222">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c20a0-223">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c20a0-223">AzureRM.Cdn</span></span>
* <span data-ttu-id="c20a0-224">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="c20a0-224">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-225">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-226">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="c20a0-226">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="c20a0-227">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="c20a0-227">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="c20a0-228">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-228">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c20a0-229">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="c20a0-229">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="c20a0-230">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c20a0-230">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c20a0-231">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c20a0-231">AzureRM.Dns</span></span>
* <span data-ttu-id="c20a0-232">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="c20a0-232">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c20a0-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-233">AzureRM.Insights</span></span>
* <span data-ttu-id="c20a0-234">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="c20a0-234">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="c20a0-235">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="c20a0-235">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="c20a0-236">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="c20a0-236">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="c20a0-237">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="c20a0-237">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="c20a0-238">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="c20a0-238">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-239">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-239">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-240">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c20a0-240">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="c20a0-241">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c20a0-241">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="c20a0-242">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c20a0-242">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c20a0-243">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c20a0-243">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c20a0-244">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="c20a0-244">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="c20a0-245">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c20a0-245">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="c20a0-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-246">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c20a0-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-247">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c20a0-248">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-248">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c20a0-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-249">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c20a0-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-250">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="c20a0-251">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c20a0-251">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="c20a0-252">Aggiunta di nuovi cmdlet per la funzionalità Firewall di Azure tramite ARM</span><span class="sxs-lookup"><span data-stu-id="c20a0-252">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="c20a0-253">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c20a0-253">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="c20a0-254">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c20a0-254">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="c20a0-255">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c20a0-255">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="c20a0-256">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c20a0-256">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="c20a0-257">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c20a0-257">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="c20a0-258">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c20a0-258">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="c20a0-259">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c20a0-259">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="c20a0-260">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c20a0-260">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="c20a0-261">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c20a0-261">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="c20a0-262">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c20a0-262">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="c20a0-263">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c20a0-263">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="c20a0-264">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c20a0-264">New Cmdlets added:</span></span>
      - <span data-ttu-id="c20a0-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-265">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-266">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-267">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-268">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-269">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-270">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c20a0-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-271">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c20a0-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-272">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c20a0-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-273">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="c20a0-274">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-274">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="c20a0-275">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-275">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c20a0-276">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-276">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c20a0-277">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c20a0-277">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="c20a0-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c20a0-278">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="c20a0-279">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-279">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="c20a0-280">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-280">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c20a0-281">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-281">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="c20a0-282">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-282">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="c20a0-283">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="c20a0-283">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="c20a0-284">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c20a0-284">Updated cmdlets:</span></span>
  - <span data-ttu-id="c20a0-285">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-285">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c20a0-286">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-286">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c20a0-287">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-287">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c20a0-288">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-288">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c20a0-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-289">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="c20a0-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-290">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c20a0-291">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-291">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c20a0-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-292">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c20a0-293">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-293">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c20a0-294">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-294">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c20a0-295">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-295">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c20a0-296">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-296">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c20a0-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-297">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c20a0-298">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-298">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c20a0-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-299">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c20a0-300">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-300">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c20a0-301">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-301">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c20a0-302">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-302">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c20a0-303">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c20a0-303">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="c20a0-304">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="c20a0-304">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="c20a0-305">New-AzureRmDelegation: crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-305">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="c20a0-306">Remove-AzureRmDelegation: acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-306">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="c20a0-307">Add-AzureRmDelegation: acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-307">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="c20a0-308">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="c20a0-308">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="c20a0-309">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="c20a0-309">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c20a0-310">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c20a0-310">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c20a0-311">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="c20a0-311">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c20a0-312">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c20a0-312">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c20a0-313">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="c20a0-313">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-314">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-314">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-315">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="c20a0-315">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="c20a0-316">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="c20a0-316">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="c20a0-317">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c20a0-317">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="c20a0-318">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="c20a0-318">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="c20a0-319">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="c20a0-319">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-320">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-320">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-321">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="c20a0-321">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="c20a0-322">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="c20a0-322">AzureRM.SignalR</span></span>
* <span data-ttu-id="c20a0-323">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="c20a0-323">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="c20a0-324">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="c20a0-324">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c20a0-325">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-325">AzureRM.Storage</span></span>
* <span data-ttu-id="c20a0-326">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-326">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="c20a0-327">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c20a0-327">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="c20a0-328">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c20a0-328">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c20a0-329">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c20a0-329">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c20a0-330">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c20a0-330">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c20a0-331">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c20a0-331">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c20a0-332">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c20a0-332">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c20a0-333">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c20a0-333">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c20a0-334">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-334">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c20a0-335">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-335">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c20a0-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-336">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c20a0-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-337">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-338">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-338">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-339">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c20a0-339">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="c20a0-340">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c20a0-340">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="c20a0-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c20a0-341">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="c20a0-342">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-342">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c20a0-343">Generale</span><span class="sxs-lookup"><span data-stu-id="c20a0-343">General</span></span>
* <span data-ttu-id="c20a0-344">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-344">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c20a0-345">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="c20a0-345">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c20a0-346">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c20a0-346">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c20a0-347">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-347">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c20a0-348">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c20a0-348">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c20a0-349">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="c20a0-349">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c20a0-350">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c20a0-350">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c20a0-351">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c20a0-351">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c20a0-352">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="c20a0-352">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c20a0-353">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c20a0-353">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c20a0-354">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="c20a0-354">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c20a0-355">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c20a0-355">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c20a0-356">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="c20a0-356">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c20a0-357">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="c20a0-357">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-358">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-358">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-359">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c20a0-359">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c20a0-360">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="c20a0-360">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c20a0-361">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-361">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c20a0-362">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="c20a0-362">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-363">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-363">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-364">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="c20a0-364">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c20a0-365">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c20a0-365">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c20a0-366">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="c20a0-366">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c20a0-367">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-367">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-368">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c20a0-368">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-369">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-369">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-370">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="c20a0-370">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c20a0-371">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c20a0-371">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c20a0-372">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c20a0-372">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c20a0-373">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c20a0-373">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c20a0-374">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-374">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c20a0-375">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-375">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c20a0-376">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="c20a0-376">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c20a0-377">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="c20a0-377">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c20a0-378">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-378">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c20a0-379">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-379">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c20a0-380">Generale</span><span class="sxs-lookup"><span data-stu-id="c20a0-380">General</span></span>
* <span data-ttu-id="c20a0-381">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-381">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-382">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-383">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c20a0-383">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-384">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-384">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-385">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c20a0-385">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c20a0-386">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="c20a0-386">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c20a0-387">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="c20a0-387">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c20a0-388">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-388">AzureRM.IotHub</span></span>
* <span data-ttu-id="c20a0-389">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="c20a0-389">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-390">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-390">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-391">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="c20a0-391">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c20a0-392">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c20a0-392">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c20a0-393">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="c20a0-393">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-394">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-394">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-395">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c20a0-395">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-396">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-396">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-397">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="c20a0-397">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c20a0-398">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c20a0-398">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c20a0-399">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c20a0-399">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c20a0-400">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c20a0-400">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c20a0-401">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="c20a0-401">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c20a0-402">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-402">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c20a0-403">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="c20a0-403">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c20a0-404">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="c20a0-404">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c20a0-405">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-405">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-406">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-406">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-407">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="c20a0-407">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c20a0-408">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-408">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-409">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-409">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-410">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c20a0-411">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="c20a0-411">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c20a0-412">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="c20a0-412">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c20a0-413">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="c20a0-413">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c20a0-414">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-414">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-415">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="c20a0-415">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="c20a0-416">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c20a0-416">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c20a0-417">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-417">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c20a0-418">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-418">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c20a0-419">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-419">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c20a0-420">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-420">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c20a0-421">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c20a0-421">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c20a0-422">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-422">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c20a0-423">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-423">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c20a0-424">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-424">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c20a0-425">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c20a0-425">AzureRM.Automation</span></span>
* <span data-ttu-id="c20a0-426">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-426">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c20a0-427">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-427">AzureRM.Backup</span></span>
* <span data-ttu-id="c20a0-428">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-428">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c20a0-429">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c20a0-429">AzureRM.Batch</span></span>
* <span data-ttu-id="c20a0-430">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-430">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c20a0-431">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c20a0-431">AzureRM.Billing</span></span>
* <span data-ttu-id="c20a0-432">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-432">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c20a0-433">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c20a0-433">AzureRM.Cdn</span></span>
* <span data-ttu-id="c20a0-434">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-434">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c20a0-435">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-435">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c20a0-436">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-436">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-437">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-437">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-438">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-438">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c20a0-439">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-439">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c20a0-440">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-440">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c20a0-441">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c20a0-441">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c20a0-442">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="c20a0-442">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c20a0-443">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c20a0-443">AzureRM.Consumption</span></span>
* <span data-ttu-id="c20a0-444">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-444">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c20a0-445">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c20a0-445">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c20a0-446">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-446">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c20a0-447">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c20a0-447">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c20a0-448">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c20a0-449">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c20a0-449">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c20a0-450">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c20a0-451">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c20a0-451">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c20a0-452">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c20a0-453">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c20a0-453">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c20a0-454">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-455">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-455">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-456">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="c20a0-456">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c20a0-457">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c20a0-457">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c20a0-458">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-458">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c20a0-459">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-459">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c20a0-460">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c20a0-460">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c20a0-461">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-461">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c20a0-462">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c20a0-462">AzureRM.Dns</span></span>
* <span data-ttu-id="c20a0-463">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-463">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c20a0-464">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c20a0-464">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c20a0-465">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-465">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c20a0-466">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-466">AzureRM.EventHub</span></span>
* <span data-ttu-id="c20a0-467">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-467">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c20a0-468">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c20a0-468">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c20a0-469">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-469">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c20a0-470">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-470">AzureRM.Insights</span></span>
* <span data-ttu-id="c20a0-471">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-471">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c20a0-472">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-472">AzureRM.IotHub</span></span>
* <span data-ttu-id="c20a0-473">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-474">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-474">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-475">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c20a0-476">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c20a0-476">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c20a0-477">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c20a0-478">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c20a0-478">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c20a0-479">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c20a0-480">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c20a0-480">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c20a0-481">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c20a0-482">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c20a0-482">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c20a0-483">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c20a0-484">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c20a0-484">AzureRM.Media</span></span>
* <span data-ttu-id="c20a0-485">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-486">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-486">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-487">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-487">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c20a0-488">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c20a0-488">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c20a0-489">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c20a0-489">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c20a0-490">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c20a0-490">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c20a0-491">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c20a0-491">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c20a0-492">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c20a0-492">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c20a0-493">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="c20a0-493">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c20a0-494">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="c20a0-494">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c20a0-495">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c20a0-495">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c20a0-496">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-496">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c20a0-497">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-497">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c20a0-498">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-498">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c20a0-499">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-499">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c20a0-500">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-500">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c20a0-501">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c20a0-501">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c20a0-502">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-502">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c20a0-503">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-503">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c20a0-504">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-504">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c20a0-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c20a0-506">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="c20a0-506">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c20a0-507">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="c20a0-507">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c20a0-508">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="c20a0-508">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c20a0-509">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-509">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c20a0-510">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c20a0-510">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c20a0-511">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-511">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c20a0-512">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="c20a0-512">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c20a0-513">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c20a0-513">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c20a0-514">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-514">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c20a0-515">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c20a0-515">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c20a0-516">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c20a0-517">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c20a0-517">AzureRM.Relay</span></span>
* <span data-ttu-id="c20a0-518">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-519">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-519">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-520">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-520">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c20a0-521">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c20a0-521">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c20a0-522">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-522">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c20a0-523">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-523">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c20a0-524">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-524">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c20a0-525">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-525">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c20a0-526">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-526">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c20a0-527">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c20a0-527">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c20a0-528">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c20a0-528">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c20a0-529">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="c20a0-529">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c20a0-530">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-530">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c20a0-531">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-531">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c20a0-532">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c20a0-532">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c20a0-533">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-533">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-534">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-534">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-535">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-535">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c20a0-536">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c20a0-536">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c20a0-537">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-537">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-538">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-538">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-539">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-539">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c20a0-540">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-540">AzureRM.Storage</span></span>
* <span data-ttu-id="c20a0-541">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-541">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c20a0-542">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c20a0-542">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c20a0-543">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-543">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c20a0-544">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c20a0-544">AzureRM.Tags</span></span>
* <span data-ttu-id="c20a0-545">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-545">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c20a0-546">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c20a0-546">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c20a0-547">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-547">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c20a0-548">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c20a0-548">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c20a0-549">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-549">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-550">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-550">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-551">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c20a0-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c20a0-552">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-552">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c20a0-553">Generale</span><span class="sxs-lookup"><span data-stu-id="c20a0-553">General</span></span>
* <span data-ttu-id="c20a0-554">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="c20a0-554">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-555">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-555">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-556">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-556">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c20a0-557">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-557">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c20a0-558">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-558">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-559">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c20a0-559">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c20a0-560">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c20a0-560">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c20a0-561">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c20a0-561">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c20a0-562">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c20a0-562">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c20a0-563">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="c20a0-563">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c20a0-564">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c20a0-564">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c20a0-565">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="c20a0-565">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c20a0-566">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c20a0-566">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c20a0-567">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="c20a0-567">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-568">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-568">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-569">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="c20a0-569">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c20a0-570">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c20a0-570">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c20a0-571">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-571">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c20a0-572">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c20a0-572">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c20a0-573">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="c20a0-573">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c20a0-574">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="c20a0-574">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c20a0-575">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c20a0-575">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c20a0-576">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="c20a0-576">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c20a0-577">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="c20a0-577">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c20a0-578">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="c20a0-578">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c20a0-579">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c20a0-579">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c20a0-580">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="c20a0-580">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c20a0-581">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="c20a0-581">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c20a0-582">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c20a0-582">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c20a0-583">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c20a0-583">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-584">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-584">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-585">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c20a0-585">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c20a0-586">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-586">AzureRM.EventHub</span></span>
* <span data-ttu-id="c20a0-587">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="c20a0-587">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c20a0-588">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-588">AzureRM.Insights</span></span>
* <span data-ttu-id="c20a0-589">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="c20a0-589">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c20a0-590">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="c20a0-590">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-591">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-591">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-592">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-592">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-593">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-594">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="c20a0-594">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-595">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-595">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-596">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c20a0-596">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c20a0-597">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c20a0-597">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-598">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-598">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-599">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="c20a0-599">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c20a0-600">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="c20a0-600">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-601">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-601">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-602">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20a0-602">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c20a0-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-603">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c20a0-604">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20a0-604">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c20a0-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c20a0-605">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c20a0-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c20a0-606">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c20a0-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c20a0-607">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c20a0-608">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c20a0-608">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c20a0-609">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="c20a0-609">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c20a0-610">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-610">AzureRM.Storage</span></span>
* <span data-ttu-id="c20a0-611">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="c20a0-611">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c20a0-612">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="c20a0-612">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c20a0-613">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c20a0-613">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c20a0-614">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c20a0-614">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c20a0-615">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c20a0-615">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c20a0-616">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c20a0-616">AzureRM.Tags</span></span>
* <span data-ttu-id="c20a0-617">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="c20a0-617">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c20a0-618">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-618">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-619">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-619">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-620">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="c20a0-620">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c20a0-621">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-621">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-622">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="c20a0-622">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="c20a0-623">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c20a0-623">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="c20a0-624">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c20a0-624">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c20a0-625">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-625">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c20a0-626">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="c20a0-626">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c20a0-627">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c20a0-627">AzureRM.Automation</span></span>
* <span data-ttu-id="c20a0-628">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="c20a0-628">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-629">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-629">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-630">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c20a0-630">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c20a0-631">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="c20a0-631">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c20a0-632">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="c20a0-632">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c20a0-633">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="c20a0-633">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c20a0-634">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="c20a0-634">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c20a0-635">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-635">AzureRM.EventHub</span></span>
* <span data-ttu-id="c20a0-636">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="c20a0-636">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-637">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-637">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-638">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c20a0-638">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c20a0-639">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c20a0-639">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c20a0-640">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c20a0-640">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-641">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-641">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-642">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c20a0-642">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c20a0-643">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c20a0-643">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c20a0-644">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="c20a0-644">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c20a0-645">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c20a0-645">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c20a0-646">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c20a0-646">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c20a0-647">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="c20a0-647">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c20a0-648">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c20a0-648">AzureRM.Relay</span></span>
* <span data-ttu-id="c20a0-649">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="c20a0-649">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-650">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-651">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="c20a0-651">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c20a0-652">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="c20a0-652">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c20a0-653">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c20a0-653">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c20a0-654">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="c20a0-654">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c20a0-655">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="c20a0-655">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-656">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-656">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-657">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="c20a0-657">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c20a0-658">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="c20a0-658">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c20a0-659">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c20a0-659">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c20a0-660">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c20a0-660">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c20a0-661">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c20a0-661">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c20a0-662">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c20a0-662">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c20a0-663">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c20a0-663">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c20a0-664">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="c20a0-664">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c20a0-665">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c20a0-665">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c20a0-666">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="c20a0-666">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-667">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-667">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-668">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="c20a0-668">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c20a0-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-669">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c20a0-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-670">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-671">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-671">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-672">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="c20a0-672">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c20a0-673">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="c20a0-673">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c20a0-674">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="c20a0-674">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c20a0-675">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-675">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c20a0-676">Generale</span><span class="sxs-lookup"><span data-stu-id="c20a0-676">General</span></span>
* <span data-ttu-id="c20a0-677">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="c20a0-677">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-678">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-678">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-679">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="c20a0-679">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-680">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-680">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-681">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="c20a0-681">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c20a0-682">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="c20a0-682">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c20a0-683">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-683">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c20a0-684">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="c20a0-684">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c20a0-685">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-685">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c20a0-686">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-686">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c20a0-687">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-687">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c20a0-688">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c20a0-688">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c20a0-689">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20a0-689">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c20a0-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-690">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c20a0-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-691">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c20a0-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-692">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-693">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-693">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-694">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c20a0-694">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c20a0-695">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c20a0-695">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c20a0-696">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="c20a0-696">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c20a0-697">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="c20a0-697">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c20a0-698">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c20a0-698">AzureRM.EventHub</span></span>
* <span data-ttu-id="c20a0-699">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c20a0-699">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c20a0-700">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="c20a0-700">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c20a0-701">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="c20a0-701">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c20a0-702">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c20a0-702">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-703">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-703">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-704">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c20a0-704">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-705">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-705">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-706">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="c20a0-706">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c20a0-707">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="c20a0-707">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c20a0-708">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c20a0-708">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c20a0-709">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c20a0-709">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c20a0-710">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c20a0-710">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c20a0-711">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c20a0-711">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c20a0-712">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c20a0-712">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c20a0-713">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-713">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c20a0-714">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c20a0-714">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c20a0-715">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c20a0-715">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c20a0-716">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-716">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c20a0-717">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="c20a0-717">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c20a0-718">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c20a0-718">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c20a0-719">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="c20a0-719">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-720">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-720">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-721">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="c20a0-721">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c20a0-722">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c20a0-722">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c20a0-723">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c20a0-723">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c20a0-724">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="c20a0-724">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c20a0-725">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c20a0-725">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c20a0-726">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="c20a0-726">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c20a0-727">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="c20a0-727">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c20a0-728">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c20a0-728">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c20a0-729">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="c20a0-729">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c20a0-730">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="c20a0-730">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c20a0-731">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c20a0-731">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c20a0-732">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="c20a0-732">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c20a0-733">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="c20a0-733">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c20a0-734">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c20a0-734">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c20a0-735">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c20a0-735">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-736">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-736">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-737">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c20a0-737">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c20a0-738">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="c20a0-738">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c20a0-739">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-739">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-740">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-740">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-741">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="c20a0-741">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c20a0-742">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="c20a0-742">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c20a0-743">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c20a0-743">Azure.Storage</span></span>
* <span data-ttu-id="c20a0-744">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="c20a0-744">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-745">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-745">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-746">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="c20a0-746">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="c20a0-747">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="c20a0-747">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c20a0-748">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c20a0-748">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c20a0-749">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c20a0-749">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c20a0-750">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c20a0-750">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c20a0-751">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="c20a0-751">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c20a0-752">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c20a0-752">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c20a0-753">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c20a0-753">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c20a0-754">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c20a0-754">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c20a0-755">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c20a0-755">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c20a0-756">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c20a0-756">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c20a0-757">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-757">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c20a0-758">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c20a0-758">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c20a0-759">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c20a0-759">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c20a0-760">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-760">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c20a0-761">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-761">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c20a0-762">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-762">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c20a0-763">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c20a0-763">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c20a0-764">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c20a0-764">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c20a0-765">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c20a0-765">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c20a0-766">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c20a0-766">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c20a0-767">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c20a0-767">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c20a0-768">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c20a0-768">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c20a0-769">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c20a0-769">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c20a0-770">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c20a0-770">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c20a0-771">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c20a0-771">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c20a0-772">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c20a0-772">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-773">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-773">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-774">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c20a0-774">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c20a0-775">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-775">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c20a0-776">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-776">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c20a0-777">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="c20a0-777">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c20a0-778">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="c20a0-778">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c20a0-779">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c20a0-779">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c20a0-780">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="c20a0-780">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c20a0-781">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="c20a0-781">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-782">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-782">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-783">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c20a0-783">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c20a0-784">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c20a0-784">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c20a0-785">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-785">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-786">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-786">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-787">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c20a0-787">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c20a0-788">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="c20a0-788">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c20a0-789">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-789">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c20a0-790">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c20a0-790">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c20a0-791">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="c20a0-791">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c20a0-792">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-792">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-793">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-793">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-794">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="c20a0-794">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c20a0-795">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c20a0-795">AzureRM.Compute</span></span>
* <span data-ttu-id="c20a0-796">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="c20a0-796">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c20a0-797">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="c20a0-797">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c20a0-798">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="c20a0-798">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c20a0-799">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c20a0-799">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c20a0-800">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="c20a0-800">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c20a0-801">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="c20a0-801">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c20a0-802">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="c20a0-802">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c20a0-803">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="c20a0-803">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c20a0-804">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="c20a0-804">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c20a0-805">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c20a0-805">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c20a0-806">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="c20a0-806">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-807">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-807">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-808">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="c20a0-808">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c20a0-809">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c20a0-809">AzureRM.Resources</span></span>
* <span data-ttu-id="c20a0-810">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="c20a0-810">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c20a0-811">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c20a0-811">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c20a0-812">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c20a0-812">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c20a0-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-813">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-814">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="c20a0-814">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c20a0-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c20a0-815">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c20a0-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c20a0-816">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c20a0-817">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c20a0-817">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c20a0-818">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c20a0-818">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c20a0-819">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c20a0-819">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c20a0-820">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c20a0-820">AzureRM.Websites</span></span>
* <span data-ttu-id="c20a0-821">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="c20a0-821">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c20a0-822">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="c20a0-822">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c20a0-823">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c20a0-823">AzureRM.Profile</span></span>
* <span data-ttu-id="c20a0-824">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="c20a0-824">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c20a0-825">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c20a0-825">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c20a0-826">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="c20a0-826">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c20a0-827">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c20a0-827">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c20a0-828">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="c20a0-828">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c20a0-829">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c20a0-829">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c20a0-830">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="c20a0-830">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c20a0-831">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="c20a0-831">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c20a0-832">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="c20a0-832">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c20a0-833">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="c20a0-833">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c20a0-834">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="c20a0-834">Added support for MSI identity</span></span>
* <span data-ttu-id="c20a0-835">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="c20a0-835">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c20a0-836">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c20a0-836">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c20a0-837">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-837">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c20a0-838">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c20a0-838">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c20a0-839">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c20a0-839">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c20a0-840">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c20a0-840">AzureRM.Batch</span></span>
* <span data-ttu-id="c20a0-841">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c20a0-841">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c20a0-842">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c20a0-842">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c20a0-843">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c20a0-843">AzureRM.Consumption</span></span>
* <span data-ttu-id="c20a0-844">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c20a0-844">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c20a0-845">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c20a0-845">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c20a0-846">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c20a0-846">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c20a0-847">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-847">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="c20a0-848">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c20a0-848">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="c20a0-849">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c20a0-849">AzureRM.Network</span></span>
* <span data-ttu-id="c20a0-850">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="c20a0-850">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c20a0-851">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="c20a0-851">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c20a0-852">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c20a0-852">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c20a0-853">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="c20a0-853">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c20a0-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-854">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c20a0-855">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="c20a0-855">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c20a0-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-856">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c20a0-857">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="c20a0-857">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c20a0-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c20a0-858">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c20a0-859">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c20a0-859">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c20a0-860">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="c20a0-860">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c20a0-861">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c20a0-861">AzureRM.Sql</span></span>
* <span data-ttu-id="c20a0-862">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="c20a0-862">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c20a0-863">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="c20a0-863">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c20a0-864">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="c20a0-864">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c20a0-865">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="c20a0-865">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c20a0-866">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="c20a0-866">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="c20a0-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c20a0-867">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c20a0-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c20a0-868">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c20a0-869">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c20a0-869">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c20a0-870">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c20a0-870">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c20a0-871">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c20a0-871">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c20a0-872">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c20a0-872">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c20a0-873">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="c20a0-873">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>