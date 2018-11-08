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
ms.openlocfilehash: eec8b5960f787fa9ca1130b4f8b49c9d896aa99e
ms.sourcegitcommit: 1f699b72bf544d92459da9d888cc0091f9415b65
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2018
ms.locfileid: "50971976"
---
# <a name="release-notes"></a><span data-ttu-id="8cc01-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="8cc01-103">Release notes</span></span>

<span data-ttu-id="8cc01-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6110---october-2018"></a><span data-ttu-id="8cc01-105">6.11.0 - ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-105">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-106">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-107">Risoluzione del problema con Get-AzureRmSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="8cc01-107">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="8cc01-108">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="8cc01-108">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="8cc01-109">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc01-109">AzureRM.Backup</span></span>
* <span data-ttu-id="8cc01-110">Cmdlet di Backup di Azure deprecati.</span><span class="sxs-lookup"><span data-stu-id="8cc01-110">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-111">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-112">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzureRmVm'.</span><span class="sxs-lookup"><span data-stu-id="8cc01-112">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="8cc01-113">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc01-113">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc01-114">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc01-114">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc01-115">Aggiunta del supporto per le regole della rete virtuale</span><span class="sxs-lookup"><span data-stu-id="8cc01-115">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="8cc01-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: ottiene o elenca le regole di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8cc01-116">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="8cc01-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="8cc01-117">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8cc01-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: modifica la regola di rete virtuale specificata nell'account Data Lake Store indicato.</span><span class="sxs-lookup"><span data-stu-id="8cc01-118">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="8cc01-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8cc01-119">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-120">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-121">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="8cc01-121">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="8cc01-122">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc01-122">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-123">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-123">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-124">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzureRMRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="8cc01-124">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="8cc01-125">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="8cc01-125">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="8cc01-126">6.10.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-126">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="8cc01-127">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-127">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-128">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="8cc01-128">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="8cc01-129">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="8cc01-129">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="8cc01-130">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="8cc01-130">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="8cc01-131">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-131">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="8cc01-132">Supporto di Get-AzureRmCognitiveServicesAccountSkus senza un account esistente</span><span class="sxs-lookup"><span data-stu-id="8cc01-132">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-133">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-133">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-134">Correzione di Get-AzureRmVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="8cc01-134">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="8cc01-135">Aggiunta di un esempio di SimpleParameterSet alla Guida del cmdlet New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-135">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="8cc01-136">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="8cc01-136">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc01-137">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc01-137">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc01-138">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="8cc01-138">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-139">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-139">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-140">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-140">Added NetworkProfile functionality.</span></span> <span data-ttu-id="8cc01-141">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cc01-141">new cmdlets added</span></span>
    - <span data-ttu-id="8cc01-142">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-142">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="8cc01-143">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-143">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="8cc01-144">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-144">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="8cc01-145">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-145">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="8cc01-146">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-146">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="8cc01-147">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-147">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="8cc01-148">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-148">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="8cc01-149">Aggiunta dei cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap e Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="8cc01-149">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="8cc01-150">Aggiunta dei cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig e Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-150">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8cc01-151">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8cc01-151">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8cc01-152">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="8cc01-152">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="8cc01-153">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="8cc01-153">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-154">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-154">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-155">Aggiunta del parametro -Mode mancante a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8cc01-155">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="8cc01-156">Correzione del bug del cmdlet Get-AzureRmProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="8cc01-156">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-157">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-157">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-158">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="8cc01-158">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc01-159">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-159">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc01-160">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="8cc01-160">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="8cc01-161">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="8cc01-161">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-162">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-162">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-163">Nuovo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="8cc01-163">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="8cc01-164">Nuovi cmdlet New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="8cc01-164">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="8cc01-165">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-165">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc01-166">Generale</span><span class="sxs-lookup"><span data-stu-id="8cc01-166">General</span></span>
* <span data-ttu-id="8cc01-167">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="8cc01-167">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-168">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-168">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-169">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8cc01-169">Minor changes to the storage common code</span></span>
* <span data-ttu-id="8cc01-170">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="8cc01-170">Updated help files to include full parameter types.</span></span>
- <span data-ttu-id="8cc01-171">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8cc01-171">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="8cc01-172">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-172">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-173">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="8cc01-173">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="8cc01-174">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="8cc01-174">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="8cc01-175">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="8cc01-175">AzureRM.Cdn</span></span>
* <span data-ttu-id="8cc01-176">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="8cc01-176">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-177">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-177">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-178">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="8cc01-178">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="8cc01-179">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="8cc01-179">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="8cc01-180">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-180">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8cc01-181">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cc01-181">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="8cc01-182">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8cc01-182">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="8cc01-183">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="8cc01-183">AzureRM.Dns</span></span>
* <span data-ttu-id="8cc01-184">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="8cc01-184">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8cc01-185">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8cc01-185">AzureRM.Insights</span></span>
* <span data-ttu-id="8cc01-186">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="8cc01-186">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="8cc01-187">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="8cc01-187">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="8cc01-188">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="8cc01-188">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="8cc01-189">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="8cc01-189">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="8cc01-190">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="8cc01-190">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-191">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-191">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-192">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cc01-192">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="8cc01-193">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8cc01-193">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="8cc01-194">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8cc01-194">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="8cc01-195">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="8cc01-195">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="8cc01-196">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="8cc01-196">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="8cc01-197">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8cc01-197">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="8cc01-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-198">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="8cc01-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-199">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="8cc01-200">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-200">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="8cc01-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-201">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="8cc01-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-202">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="8cc01-203">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8cc01-203">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="8cc01-204">Aggiunta di nuovi cmdlet per la funzionalità Firewall di Azure tramite ARM</span><span class="sxs-lookup"><span data-stu-id="8cc01-204">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="8cc01-205">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8cc01-205">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="8cc01-206">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8cc01-206">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="8cc01-207">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8cc01-207">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="8cc01-208">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8cc01-208">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="8cc01-209">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8cc01-209">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="8cc01-210">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="8cc01-210">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="8cc01-211">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8cc01-211">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="8cc01-212">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="8cc01-212">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="8cc01-213">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="8cc01-213">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="8cc01-214">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8cc01-214">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="8cc01-215">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="8cc01-215">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="8cc01-216">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8cc01-216">New Cmdlets added:</span></span>
      - <span data-ttu-id="8cc01-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-217">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-218">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-219">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-220">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-221">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-222">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="8cc01-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-223">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="8cc01-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-224">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="8cc01-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-225">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="8cc01-226">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-226">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="8cc01-227">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-227">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="8cc01-228">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-228">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="8cc01-229">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8cc01-229">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="8cc01-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="8cc01-230">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="8cc01-231">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-231">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="8cc01-232">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-232">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="8cc01-233">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-233">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="8cc01-234">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-234">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="8cc01-235">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="8cc01-235">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="8cc01-236">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8cc01-236">Updated cmdlets:</span></span>
  - <span data-ttu-id="8cc01-237">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-237">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="8cc01-238">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-238">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="8cc01-239">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-239">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="8cc01-240">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-240">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="8cc01-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-241">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="8cc01-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-242">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="8cc01-243">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-243">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="8cc01-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-244">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="8cc01-245">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-245">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="8cc01-246">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-246">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="8cc01-247">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-247">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="8cc01-248">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-248">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="8cc01-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-249">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="8cc01-250">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-250">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="8cc01-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-251">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="8cc01-252">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-252">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="8cc01-253">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-253">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="8cc01-254">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-254">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="8cc01-255">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="8cc01-255">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="8cc01-256">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="8cc01-256">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="8cc01-257">New-AzureRmDelegation: crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-257">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="8cc01-258">Remove-AzureRmDelegation: acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-258">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="8cc01-259">Add-AzureRmDelegation: acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-259">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="8cc01-260">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="8cc01-260">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="8cc01-261">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="8cc01-261">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="8cc01-262">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8cc01-262">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8cc01-263">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="8cc01-263">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8cc01-264">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8cc01-264">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8cc01-265">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="8cc01-265">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-266">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-266">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-267">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="8cc01-267">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="8cc01-268">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="8cc01-268">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="8cc01-269">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="8cc01-269">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="8cc01-270">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="8cc01-270">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="8cc01-271">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="8cc01-271">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-272">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-272">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-273">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="8cc01-273">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="8cc01-274">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="8cc01-274">AzureRM.SignalR</span></span>
* <span data-ttu-id="8cc01-275">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="8cc01-275">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="8cc01-276">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="8cc01-276">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc01-277">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-277">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc01-278">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-278">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="8cc01-279">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8cc01-279">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="8cc01-280">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8cc01-280">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="8cc01-281">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8cc01-281">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="8cc01-282">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8cc01-282">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="8cc01-283">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8cc01-283">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="8cc01-284">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="8cc01-284">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="8cc01-285">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="8cc01-285">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="8cc01-286">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-286">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="8cc01-287">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-287">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="8cc01-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-288">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="8cc01-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-289">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-290">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-290">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-291">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="8cc01-291">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="8cc01-292">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="8cc01-292">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="8cc01-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="8cc01-293">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="8cc01-294">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-294">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc01-295">Generale</span><span class="sxs-lookup"><span data-stu-id="8cc01-295">General</span></span>
* <span data-ttu-id="8cc01-296">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-296">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8cc01-297">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="8cc01-297">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc01-298">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc01-298">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc01-299">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-299">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8cc01-300">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="8cc01-300">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="8cc01-301">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="8cc01-301">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="8cc01-302">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="8cc01-302">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="8cc01-303">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="8cc01-303">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="8cc01-304">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="8cc01-304">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="8cc01-305">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="8cc01-305">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="8cc01-306">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="8cc01-306">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="8cc01-307">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="8cc01-307">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="8cc01-308">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="8cc01-308">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="8cc01-309">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="8cc01-309">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-310">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-310">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-311">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="8cc01-311">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="8cc01-312">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="8cc01-312">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="8cc01-313">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-313">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="8cc01-314">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="8cc01-314">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-315">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-315">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-316">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cc01-316">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8cc01-317">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8cc01-317">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8cc01-318">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="8cc01-318">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="8cc01-319">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-319">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-320">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8cc01-320">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-321">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-321">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-322">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="8cc01-322">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc01-323">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc01-323">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc01-324">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc01-324">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="8cc01-325">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc01-325">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="8cc01-326">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-326">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="8cc01-327">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-327">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="8cc01-328">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="8cc01-328">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="8cc01-329">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="8cc01-329">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="8cc01-330">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-330">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="8cc01-331">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-331">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc01-332">Generale</span><span class="sxs-lookup"><span data-stu-id="8cc01-332">General</span></span>
* <span data-ttu-id="8cc01-333">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-333">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-334">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-334">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-335">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="8cc01-335">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-336">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-336">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-337">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="8cc01-337">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="8cc01-338">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="8cc01-338">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="8cc01-339">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="8cc01-339">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8cc01-340">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-340">AzureRM.IotHub</span></span>
* <span data-ttu-id="8cc01-341">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="8cc01-341">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-342">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-342">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-343">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="8cc01-343">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8cc01-344">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8cc01-344">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8cc01-345">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="8cc01-345">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-346">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-346">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-347">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8cc01-347">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-348">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-348">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-349">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="8cc01-349">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc01-350">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc01-350">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc01-351">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc01-351">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="8cc01-352">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="8cc01-352">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="8cc01-353">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="8cc01-353">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="8cc01-354">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-354">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="8cc01-355">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="8cc01-355">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="8cc01-356">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="8cc01-356">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="8cc01-357">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-357">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-358">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-358">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-359">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="8cc01-359">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="8cc01-360">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-360">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-361">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-361">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-362">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-362">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc01-363">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="8cc01-363">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="8cc01-364">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="8cc01-364">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="8cc01-365">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="8cc01-365">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="8cc01-366">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-366">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-367">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="8cc01-367">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="8cc01-368">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="8cc01-368">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc01-369">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-369">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc01-370">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-370">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="8cc01-371">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-371">Azure.AnalysisServices</span></span>
* <span data-ttu-id="8cc01-372">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-372">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc01-373">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc01-373">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc01-374">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-374">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="8cc01-375">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="8cc01-375">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="8cc01-376">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-376">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8cc01-377">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8cc01-377">AzureRM.Automation</span></span>
* <span data-ttu-id="8cc01-378">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-378">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="8cc01-379">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc01-379">AzureRM.Backup</span></span>
* <span data-ttu-id="8cc01-380">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-380">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8cc01-381">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8cc01-381">AzureRM.Batch</span></span>
* <span data-ttu-id="8cc01-382">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-382">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="8cc01-383">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="8cc01-383">AzureRM.Billing</span></span>
* <span data-ttu-id="8cc01-384">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-384">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="8cc01-385">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="8cc01-385">AzureRM.Cdn</span></span>
* <span data-ttu-id="8cc01-386">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-386">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="8cc01-387">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-387">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="8cc01-388">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-388">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-389">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-389">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-390">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-390">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc01-391">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-391">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="8cc01-392">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-392">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="8cc01-393">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8cc01-393">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8cc01-394">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="8cc01-394">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8cc01-395">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8cc01-395">AzureRM.Consumption</span></span>
* <span data-ttu-id="8cc01-396">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-396">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="8cc01-397">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="8cc01-397">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="8cc01-398">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-398">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="8cc01-399">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="8cc01-399">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="8cc01-400">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-400">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="8cc01-401">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="8cc01-401">AzureRM.DataFactories</span></span>
* <span data-ttu-id="8cc01-402">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-402">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc01-403">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc01-403">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc01-404">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-404">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8cc01-405">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc01-405">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8cc01-406">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-406">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc01-407">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc01-407">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc01-408">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="8cc01-408">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="8cc01-409">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="8cc01-409">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8cc01-410">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-410">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc01-411">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-411">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="8cc01-412">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="8cc01-412">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="8cc01-413">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-413">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="8cc01-414">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="8cc01-414">AzureRM.Dns</span></span>
* <span data-ttu-id="8cc01-415">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-415">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8cc01-416">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc01-416">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8cc01-417">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-417">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc01-418">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-418">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc01-419">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-419">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="8cc01-420">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="8cc01-420">AzureRM.HDInsight</span></span>
* <span data-ttu-id="8cc01-421">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-421">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8cc01-422">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8cc01-422">AzureRM.Insights</span></span>
* <span data-ttu-id="8cc01-423">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-423">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="8cc01-424">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-424">AzureRM.IotHub</span></span>
* <span data-ttu-id="8cc01-425">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-425">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-426">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-426">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-427">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-427">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8cc01-428">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc01-428">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8cc01-429">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-429">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="8cc01-430">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="8cc01-430">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="8cc01-431">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-431">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="8cc01-432">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="8cc01-432">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="8cc01-433">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-433">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="8cc01-434">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="8cc01-434">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="8cc01-435">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-435">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="8cc01-436">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="8cc01-436">AzureRM.Media</span></span>
* <span data-ttu-id="8cc01-437">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-437">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-438">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-438">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-439">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-439">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="8cc01-440">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8cc01-440">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8cc01-441">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="8cc01-441">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="8cc01-442">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8cc01-442">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8cc01-443">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="8cc01-443">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="8cc01-444">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="8cc01-444">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="8cc01-445">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="8cc01-445">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="8cc01-446">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="8cc01-446">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="8cc01-447">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="8cc01-447">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="8cc01-448">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-448">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="8cc01-449">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8cc01-449">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8cc01-450">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-450">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8cc01-451">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8cc01-451">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8cc01-452">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-452">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="8cc01-453">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="8cc01-453">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="8cc01-454">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-454">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="8cc01-455">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-455">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="8cc01-456">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-456">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc01-457">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc01-457">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc01-458">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="8cc01-458">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="8cc01-459">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="8cc01-459">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="8cc01-460">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="8cc01-460">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="8cc01-461">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-461">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="8cc01-462">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="8cc01-462">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="8cc01-463">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-463">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="8cc01-464">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="8cc01-464">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="8cc01-465">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="8cc01-465">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="8cc01-466">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-466">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="8cc01-467">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="8cc01-467">AzureRM.RedisCache</span></span>
* <span data-ttu-id="8cc01-468">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-468">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8cc01-469">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8cc01-469">AzureRM.Relay</span></span>
* <span data-ttu-id="8cc01-470">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-470">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-471">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-471">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-472">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-472">Support template deployment at subscription scope.</span></span> <span data-ttu-id="8cc01-473">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="8cc01-473">Add new Cmdlets:</span></span>
    - <span data-ttu-id="8cc01-474">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-474">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc01-475">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-475">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc01-476">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-476">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc01-477">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-477">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc01-478">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-478">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="8cc01-479">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="8cc01-479">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="8cc01-480">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="8cc01-480">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="8cc01-481">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="8cc01-481">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="8cc01-482">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-482">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="8cc01-483">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8cc01-484">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8cc01-484">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8cc01-485">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-486">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-486">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-487">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc01-488">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc01-488">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc01-489">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-490">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-490">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-491">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc01-492">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-492">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc01-493">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-493">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="8cc01-494">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc01-494">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="8cc01-495">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-495">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8cc01-496">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8cc01-496">AzureRM.Tags</span></span>
* <span data-ttu-id="8cc01-497">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-497">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc01-498">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc01-498">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc01-499">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="8cc01-500">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="8cc01-500">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="8cc01-501">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-502">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-502">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-503">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cc01-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="8cc01-504">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-504">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc01-505">Generale</span><span class="sxs-lookup"><span data-stu-id="8cc01-505">General</span></span>
* <span data-ttu-id="8cc01-506">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="8cc01-506">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-507">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-507">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-508">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-508">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="8cc01-509">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-509">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc01-510">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-510">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-511">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cc01-511">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="8cc01-512">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cc01-512">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc01-513">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc01-513">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc01-514">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="8cc01-514">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="8cc01-515">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="8cc01-515">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="8cc01-516">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="8cc01-516">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="8cc01-517">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="8cc01-517">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="8cc01-518">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="8cc01-518">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="8cc01-519">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="8cc01-519">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-520">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-520">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-521">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="8cc01-521">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="8cc01-522">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="8cc01-522">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="8cc01-523">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-523">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="8cc01-524">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8cc01-524">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="8cc01-525">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="8cc01-525">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="8cc01-526">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="8cc01-526">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="8cc01-527">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8cc01-527">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="8cc01-528">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="8cc01-528">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="8cc01-529">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="8cc01-529">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="8cc01-530">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="8cc01-530">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc01-531">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc01-531">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc01-532">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="8cc01-532">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="8cc01-533">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="8cc01-533">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="8cc01-534">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc01-534">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="8cc01-535">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="8cc01-535">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc01-536">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc01-536">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc01-537">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="8cc01-537">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc01-538">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-538">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc01-539">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="8cc01-539">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="8cc01-540">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="8cc01-540">AzureRM.Insights</span></span>
* <span data-ttu-id="8cc01-541">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="8cc01-541">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="8cc01-542">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="8cc01-542">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-543">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-543">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-544">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-544">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-545">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-545">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-546">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="8cc01-546">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-547">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-547">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-548">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="8cc01-548">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="8cc01-549">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="8cc01-549">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-550">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-550">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-551">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="8cc01-551">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="8cc01-552">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="8cc01-552">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-553">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-553">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-554">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc01-554">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="8cc01-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-555">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="8cc01-556">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc01-556">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="8cc01-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="8cc01-557">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="8cc01-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="8cc01-558">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="8cc01-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="8cc01-559">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="8cc01-560">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8cc01-560">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="8cc01-561">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="8cc01-561">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="8cc01-562">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-562">AzureRM.Storage</span></span>
* <span data-ttu-id="8cc01-563">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cc01-563">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="8cc01-564">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="8cc01-564">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="8cc01-565">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc01-565">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8cc01-566">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc01-566">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="8cc01-567">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cc01-567">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="8cc01-568">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="8cc01-568">AzureRM.Tags</span></span>
* <span data-ttu-id="8cc01-569">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="8cc01-569">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="8cc01-570">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-570">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-571">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-571">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-572">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="8cc01-572">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc01-573">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-573">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-574">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="8cc01-574">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="8cc01-575">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="8cc01-575">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="8cc01-576">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="8cc01-576">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc01-577">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-577">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc01-578">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="8cc01-578">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="8cc01-579">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="8cc01-579">AzureRM.Automation</span></span>
* <span data-ttu-id="8cc01-580">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="8cc01-580">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-581">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-581">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-582">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8cc01-582">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="8cc01-583">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="8cc01-583">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8cc01-584">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="8cc01-584">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="8cc01-585">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="8cc01-585">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="8cc01-586">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="8cc01-586">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc01-587">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-587">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc01-588">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="8cc01-588">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-589">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-589">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-590">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8cc01-590">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="8cc01-591">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc01-591">AzureRM.LogicApp</span></span>
* <span data-ttu-id="8cc01-592">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="8cc01-592">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-593">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-593">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-594">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="8cc01-594">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="8cc01-595">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="8cc01-595">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="8cc01-596">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="8cc01-596">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="8cc01-597">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8cc01-597">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="8cc01-598">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="8cc01-598">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="8cc01-599">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="8cc01-599">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="8cc01-600">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="8cc01-600">AzureRM.Relay</span></span>
* <span data-ttu-id="8cc01-601">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="8cc01-601">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-602">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-602">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-603">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="8cc01-603">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="8cc01-604">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="8cc01-604">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="8cc01-605">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="8cc01-605">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="8cc01-606">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="8cc01-606">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="8cc01-607">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="8cc01-607">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-608">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-608">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-609">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="8cc01-609">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="8cc01-610">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="8cc01-610">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="8cc01-611">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc01-611">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc01-612">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc01-612">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc01-613">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc01-613">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc01-614">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc01-614">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="8cc01-615">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="8cc01-615">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="8cc01-616">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="8cc01-616">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc01-617">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc01-617">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc01-618">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="8cc01-618">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-619">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-619">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-620">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="8cc01-620">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="8cc01-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-621">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="8cc01-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-622">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-623">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-623">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-624">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="8cc01-624">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="8cc01-625">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="8cc01-625">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="8cc01-626">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="8cc01-626">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="8cc01-627">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-627">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="8cc01-628">Generale</span><span class="sxs-lookup"><span data-stu-id="8cc01-628">General</span></span>
* <span data-ttu-id="8cc01-629">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="8cc01-629">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-630">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-630">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-631">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="8cc01-631">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-632">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-632">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-633">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="8cc01-633">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="8cc01-634">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="8cc01-634">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="8cc01-635">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-635">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="8cc01-636">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="8cc01-636">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="8cc01-637">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-637">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="8cc01-638">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-638">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="8cc01-639">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-639">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="8cc01-640">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="8cc01-640">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="8cc01-641">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc01-641">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="8cc01-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-642">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8cc01-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-643">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="8cc01-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-644">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc01-645">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc01-645">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc01-646">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="8cc01-646">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="8cc01-647">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8cc01-647">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8cc01-648">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="8cc01-648">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="8cc01-649">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="8cc01-649">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="8cc01-650">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="8cc01-650">AzureRM.EventHub</span></span>
* <span data-ttu-id="8cc01-651">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="8cc01-651">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="8cc01-652">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="8cc01-652">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="8cc01-653">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="8cc01-653">Provided Default Parameter set.</span></span>
* <span data-ttu-id="8cc01-654">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8cc01-654">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-655">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-655">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-656">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="8cc01-656">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-657">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-657">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-658">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="8cc01-658">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="8cc01-659">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="8cc01-659">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="8cc01-660">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8cc01-660">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8cc01-661">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="8cc01-661">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="8cc01-662">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc01-662">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc01-663">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc01-663">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc01-664">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="8cc01-664">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="8cc01-665">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="8cc01-665">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="8cc01-666">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="8cc01-666">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="8cc01-667">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="8cc01-667">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc01-668">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc01-668">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc01-669">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="8cc01-669">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="8cc01-670">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8cc01-670">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="8cc01-671">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="8cc01-671">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-672">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-672">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-673">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="8cc01-673">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="8cc01-674">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8cc01-674">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="8cc01-675">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="8cc01-675">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="8cc01-676">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="8cc01-676">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="8cc01-677">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8cc01-677">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="8cc01-678">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="8cc01-678">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8cc01-679">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="8cc01-679">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8cc01-680">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8cc01-680">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="8cc01-681">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="8cc01-681">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="8cc01-682">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="8cc01-682">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="8cc01-683">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="8cc01-683">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="8cc01-684">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="8cc01-684">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="8cc01-685">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="8cc01-685">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="8cc01-686">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="8cc01-686">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="8cc01-687">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="8cc01-687">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-688">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-688">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-689">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="8cc01-689">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="8cc01-690">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="8cc01-690">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="8cc01-691">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-691">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-692">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-692">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-693">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="8cc01-693">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="8cc01-694">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="8cc01-694">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="8cc01-695">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="8cc01-695">Azure.Storage</span></span>
* <span data-ttu-id="8cc01-696">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="8cc01-696">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-697">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-697">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-698">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="8cc01-698">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="8cc01-699">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="8cc01-699">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="8cc01-700">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8cc01-700">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8cc01-701">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8cc01-701">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8cc01-702">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="8cc01-702">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="8cc01-703">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="8cc01-703">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="8cc01-704">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc01-704">Start-AzureRmVM</span></span>
    - <span data-ttu-id="8cc01-705">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc01-705">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="8cc01-706">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc01-706">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="8cc01-707">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc01-707">Set-AzureRmVM</span></span>
    - <span data-ttu-id="8cc01-708">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="8cc01-708">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="8cc01-709">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-709">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc01-710">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="8cc01-710">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="8cc01-711">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="8cc01-711">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="8cc01-712">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-712">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc01-713">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-713">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc01-714">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-714">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc01-715">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="8cc01-715">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="8cc01-716">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="8cc01-716">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="8cc01-717">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="8cc01-717">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="8cc01-718">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="8cc01-718">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="8cc01-719">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8cc01-719">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="8cc01-720">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="8cc01-720">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="8cc01-721">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="8cc01-721">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="8cc01-722">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="8cc01-722">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="8cc01-723">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="8cc01-723">AzureRM.EventGrid</span></span>
* <span data-ttu-id="8cc01-724">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="8cc01-724">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-725">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-725">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-726">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="8cc01-726">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="8cc01-727">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="8cc01-727">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="8cc01-728">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="8cc01-728">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="8cc01-729">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="8cc01-729">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="8cc01-730">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="8cc01-730">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="8cc01-731">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="8cc01-731">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="8cc01-732">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="8cc01-732">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="8cc01-733">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="8cc01-733">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-734">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-734">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-735">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="8cc01-735">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc01-736">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc01-736">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc01-737">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-737">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-738">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-738">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-739">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8cc01-739">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="8cc01-740">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="8cc01-740">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="8cc01-741">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-741">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="8cc01-742">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="8cc01-742">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="8cc01-743">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="8cc01-743">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="8cc01-744">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-744">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-745">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-745">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-746">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="8cc01-746">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="8cc01-747">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="8cc01-747">AzureRM.Compute</span></span>
* <span data-ttu-id="8cc01-748">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="8cc01-748">VMSS VM Update feature</span></span>
    - <span data-ttu-id="8cc01-749">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="8cc01-749">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="8cc01-750">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="8cc01-750">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="8cc01-751">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="8cc01-751">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="8cc01-752">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="8cc01-752">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="8cc01-753">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="8cc01-753">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="8cc01-754">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="8cc01-754">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="8cc01-755">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="8cc01-755">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="8cc01-756">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="8cc01-756">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="8cc01-757">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="8cc01-757">AzureRM.KeyVault</span></span>
* <span data-ttu-id="8cc01-758">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="8cc01-758">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-759">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-759">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-760">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="8cc01-760">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="8cc01-761">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="8cc01-761">AzureRM.Resources</span></span>
* <span data-ttu-id="8cc01-762">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="8cc01-762">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="8cc01-763">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="8cc01-763">AzureRM.Scheduler</span></span>
* <span data-ttu-id="8cc01-764">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="8cc01-764">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="8cc01-765">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-765">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-766">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="8cc01-766">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="8cc01-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc01-767">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8cc01-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cc01-768">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8cc01-769">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8cc01-769">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8cc01-770">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8cc01-770">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8cc01-771">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc01-771">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="8cc01-772">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="8cc01-772">AzureRM.Websites</span></span>
* <span data-ttu-id="8cc01-773">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="8cc01-773">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="8cc01-774">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="8cc01-774">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="8cc01-775">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="8cc01-775">AzureRM.Profile</span></span>
* <span data-ttu-id="8cc01-776">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="8cc01-776">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="8cc01-777">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="8cc01-777">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="8cc01-778">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="8cc01-778">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="8cc01-779">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="8cc01-779">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="8cc01-780">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="8cc01-780">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="8cc01-781">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="8cc01-781">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="8cc01-782">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="8cc01-782">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="8cc01-783">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="8cc01-783">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="8cc01-784">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="8cc01-784">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="8cc01-785">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="8cc01-785">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="8cc01-786">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="8cc01-786">Added support for MSI identity</span></span>
* <span data-ttu-id="8cc01-787">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="8cc01-787">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="8cc01-788">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="8cc01-788">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="8cc01-789">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-789">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="8cc01-790">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="8cc01-790">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="8cc01-791">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="8cc01-791">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="8cc01-792">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="8cc01-792">AzureRM.Batch</span></span>
* <span data-ttu-id="8cc01-793">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="8cc01-793">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="8cc01-794">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="8cc01-794">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="8cc01-795">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="8cc01-795">AzureRM.Consumption</span></span>
* <span data-ttu-id="8cc01-796">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="8cc01-796">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="8cc01-797">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="8cc01-797">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="8cc01-798">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="8cc01-798">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="8cc01-799">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-799">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="8cc01-800">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="8cc01-800">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="8cc01-801">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="8cc01-801">AzureRM.Network</span></span>
* <span data-ttu-id="8cc01-802">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="8cc01-802">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="8cc01-803">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="8cc01-803">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="8cc01-804">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cc01-804">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="8cc01-805">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="8cc01-805">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="8cc01-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-806">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8cc01-807">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="8cc01-807">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="8cc01-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-808">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="8cc01-809">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="8cc01-809">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="8cc01-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="8cc01-810">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="8cc01-811">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="8cc01-811">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="8cc01-812">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="8cc01-812">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="8cc01-813">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="8cc01-813">AzureRM.Sql</span></span>
* <span data-ttu-id="8cc01-814">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="8cc01-814">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="8cc01-815">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="8cc01-815">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="8cc01-816">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="8cc01-816">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="8cc01-817">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="8cc01-817">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="8cc01-818">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="8cc01-818">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="8cc01-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc01-819">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="8cc01-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cc01-820">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="8cc01-821">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="8cc01-821">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="8cc01-822">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8cc01-822">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="8cc01-823">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8cc01-823">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="8cc01-824">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="8cc01-824">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="8cc01-825">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="8cc01-825">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
