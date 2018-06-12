---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: f90c77d8c9cd78315264fb0a0a58e047aefc5041
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821871"
---
# <a name="release-notes"></a><span data-ttu-id="e61e9-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="e61e9-103">Release notes</span></span>

<span data-ttu-id="e61e9-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="e61e9-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="620---june-2018"></a><span data-ttu-id="e61e9-105">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="e61e9-105">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e61e9-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e61e9-106">AzureRM.Profile</span></span>
* <span data-ttu-id="e61e9-107">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="e61e9-107">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="e61e9-108">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="e61e9-108">AzureRM.Compute</span></span>
* <span data-ttu-id="e61e9-109">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="e61e9-109">VMSS VM Update feature</span></span>
    - <span data-ttu-id="e61e9-110">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="e61e9-110">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="e61e9-111">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="e61e9-111">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="e61e9-112">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="e61e9-112">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="e61e9-113">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e61e9-113">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="e61e9-114">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="e61e9-114">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="e61e9-115">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="e61e9-115">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="e61e9-116">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="e61e9-116">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="e61e9-117">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="e61e9-117">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="e61e9-118">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="e61e9-118">AzureRM.KeyVault</span></span>
* <span data-ttu-id="e61e9-119">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="e61e9-119">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="e61e9-120">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e61e9-120">AzureRM.Network</span></span>
* <span data-ttu-id="e61e9-121">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="e61e9-121">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="e61e9-122">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="e61e9-122">AzureRM.Resources</span></span>
* <span data-ttu-id="e61e9-123">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="e61e9-123">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="e61e9-124">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="e61e9-124">AzureRM.Scheduler</span></span>
* <span data-ttu-id="e61e9-125">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="e61e9-125">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="e61e9-126">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e61e9-126">AzureRM.Sql</span></span>
* <span data-ttu-id="e61e9-127">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="e61e9-127">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="e61e9-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e61e9-128">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e61e9-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e61e9-129">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e61e9-130">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e61e9-130">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e61e9-131">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e61e9-131">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e61e9-132">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e61e9-132">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="e61e9-133">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="e61e9-133">AzureRM.Websites</span></span>
* <span data-ttu-id="e61e9-134">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="e61e9-134">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="e61e9-135">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="e61e9-135">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="e61e9-136">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="e61e9-136">AzureRM.Profile</span></span>
* <span data-ttu-id="e61e9-137">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="e61e9-137">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="e61e9-138">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="e61e9-138">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="e61e9-139">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="e61e9-139">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="e61e9-140">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e61e9-140">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="e61e9-141">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="e61e9-141">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="e61e9-142">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e61e9-142">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="e61e9-143">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="e61e9-143">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="e61e9-144">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="e61e9-144">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="e61e9-145">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="e61e9-145">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="e61e9-146">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="e61e9-146">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="e61e9-147">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="e61e9-147">Added support for MSI identity</span></span>
* <span data-ttu-id="e61e9-148">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="e61e9-148">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="e61e9-149">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e61e9-149">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="e61e9-150">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e61e9-150">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="e61e9-151">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e61e9-151">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="e61e9-152">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="e61e9-152">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="e61e9-153">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="e61e9-153">AzureRM.Batch</span></span>
* <span data-ttu-id="e61e9-154">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="e61e9-154">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="e61e9-155">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="e61e9-155">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="e61e9-156">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="e61e9-156">AzureRM.Consumption</span></span>
* <span data-ttu-id="e61e9-157">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="e61e9-157">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="e61e9-158">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="e61e9-158">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="e61e9-159">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="e61e9-159">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="e61e9-160">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e61e9-160">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="e61e9-161">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e61e9-161">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="e61e9-162">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="e61e9-162">AzureRM.Network</span></span>
* <span data-ttu-id="e61e9-163">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="e61e9-163">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="e61e9-164">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="e61e9-164">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="e61e9-165">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e61e9-165">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="e61e9-166">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="e61e9-166">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="e61e9-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e61e9-167">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e61e9-168">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="e61e9-168">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="e61e9-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e61e9-169">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="e61e9-170">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="e61e9-170">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="e61e9-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="e61e9-171">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="e61e9-172">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e61e9-172">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="e61e9-173">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="e61e9-173">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="e61e9-174">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="e61e9-174">AzureRM.Sql</span></span>
* <span data-ttu-id="e61e9-175">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="e61e9-175">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="e61e9-176">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="e61e9-176">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="e61e9-177">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="e61e9-177">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="e61e9-178">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="e61e9-178">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="e61e9-179">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="e61e9-179">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="e61e9-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e61e9-180">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="e61e9-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e61e9-181">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="e61e9-182">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="e61e9-182">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="e61e9-183">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="e61e9-183">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="e61e9-184">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e61e9-184">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="e61e9-185">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="e61e9-185">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="e61e9-186">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="e61e9-186">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>