---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 3811e28dda69d194d23934943fb47d562f869fc4
ms.sourcegitcommit: 5a5b6dd216d5f805204244146cf6f88ad2f34fb4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2018
ms.locfileid: "36237814"
---
# <a name="release-notes"></a><span data-ttu-id="435b0-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="435b0-103">Release notes</span></span>

<span data-ttu-id="435b0-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="435b0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="630---june-2018"></a><span data-ttu-id="435b0-105">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="435b0-105">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="435b0-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="435b0-106">AzureRM.Profile</span></span>
* <span data-ttu-id="435b0-107">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="435b0-107">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="435b0-108">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="435b0-108">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="435b0-109">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="435b0-109">Azure.Storage</span></span>
* <span data-ttu-id="435b0-110">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="435b0-110">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="435b0-111">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="435b0-111">AzureRM.Compute</span></span>
* <span data-ttu-id="435b0-112">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="435b0-112">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="435b0-113">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="435b0-113">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="435b0-114">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="435b0-114">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="435b0-115">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="435b0-115">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="435b0-116">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="435b0-116">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="435b0-117">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="435b0-117">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="435b0-118">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="435b0-118">Start-AzureRmVM</span></span>
    - <span data-ttu-id="435b0-119">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="435b0-119">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="435b0-120">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="435b0-120">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="435b0-121">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="435b0-121">Set-AzureRmVM</span></span>
    - <span data-ttu-id="435b0-122">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="435b0-122">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="435b0-123">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="435b0-123">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="435b0-124">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="435b0-124">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="435b0-125">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="435b0-125">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="435b0-126">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="435b0-126">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="435b0-127">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="435b0-127">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="435b0-128">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="435b0-128">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="435b0-129">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="435b0-129">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="435b0-130">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="435b0-130">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="435b0-131">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="435b0-131">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="435b0-132">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="435b0-132">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="435b0-133">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="435b0-133">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="435b0-134">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="435b0-134">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="435b0-135">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="435b0-135">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="435b0-136">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="435b0-136">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="435b0-137">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="435b0-137">AzureRM.EventGrid</span></span>
* <span data-ttu-id="435b0-138">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="435b0-138">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="435b0-139">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="435b0-139">AzureRM.KeyVault</span></span>
* <span data-ttu-id="435b0-140">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="435b0-140">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="435b0-141">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="435b0-141">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="435b0-142">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="435b0-142">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="435b0-143">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="435b0-143">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="435b0-144">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="435b0-144">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="435b0-145">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="435b0-145">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="435b0-146">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="435b0-146">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="435b0-147">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="435b0-147">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="435b0-148">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="435b0-148">AzureRM.Sql</span></span>
* <span data-ttu-id="435b0-149">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="435b0-149">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="435b0-150">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="435b0-150">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="435b0-151">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="435b0-151">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="435b0-152">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="435b0-152">AzureRM.Websites</span></span>
* <span data-ttu-id="435b0-153">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="435b0-153">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="435b0-154">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="435b0-154">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="435b0-155">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="435b0-155">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="435b0-156">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="435b0-156">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="435b0-157">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="435b0-157">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="435b0-158">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="435b0-158">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="435b0-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="435b0-159">AzureRM.Profile</span></span>
* <span data-ttu-id="435b0-160">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="435b0-160">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="435b0-161">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="435b0-161">AzureRM.Compute</span></span>
* <span data-ttu-id="435b0-162">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="435b0-162">VMSS VM Update feature</span></span>
    - <span data-ttu-id="435b0-163">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="435b0-163">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="435b0-164">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="435b0-164">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="435b0-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="435b0-165">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="435b0-166">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="435b0-166">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="435b0-167">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="435b0-167">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="435b0-168">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="435b0-168">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="435b0-169">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="435b0-169">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="435b0-170">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="435b0-170">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="435b0-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="435b0-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="435b0-172">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="435b0-172">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="435b0-173">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="435b0-173">AzureRM.Network</span></span>
* <span data-ttu-id="435b0-174">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="435b0-174">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="435b0-175">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="435b0-175">AzureRM.Resources</span></span>
* <span data-ttu-id="435b0-176">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="435b0-176">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="435b0-177">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="435b0-177">AzureRM.Scheduler</span></span>
* <span data-ttu-id="435b0-178">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="435b0-178">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="435b0-179">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="435b0-179">AzureRM.Sql</span></span>
* <span data-ttu-id="435b0-180">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="435b0-180">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="435b0-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="435b0-181">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="435b0-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="435b0-182">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="435b0-183">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="435b0-183">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="435b0-184">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="435b0-184">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="435b0-185">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="435b0-185">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="435b0-186">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="435b0-186">AzureRM.Websites</span></span>
* <span data-ttu-id="435b0-187">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="435b0-187">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="435b0-188">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="435b0-188">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="435b0-189">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="435b0-189">AzureRM.Profile</span></span>
* <span data-ttu-id="435b0-190">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="435b0-190">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="435b0-191">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="435b0-191">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="435b0-192">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="435b0-192">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="435b0-193">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="435b0-193">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="435b0-194">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="435b0-194">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="435b0-195">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="435b0-195">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="435b0-196">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="435b0-196">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="435b0-197">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="435b0-197">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="435b0-198">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="435b0-198">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="435b0-199">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="435b0-199">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="435b0-200">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="435b0-200">Added support for MSI identity</span></span>
* <span data-ttu-id="435b0-201">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="435b0-201">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="435b0-202">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="435b0-202">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="435b0-203">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="435b0-203">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="435b0-204">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="435b0-204">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="435b0-205">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="435b0-205">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="435b0-206">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="435b0-206">AzureRM.Batch</span></span>
* <span data-ttu-id="435b0-207">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="435b0-207">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="435b0-208">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="435b0-208">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="435b0-209">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="435b0-209">AzureRM.Consumption</span></span>
* <span data-ttu-id="435b0-210">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="435b0-210">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="435b0-211">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="435b0-211">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="435b0-212">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="435b0-212">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="435b0-213">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="435b0-213">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="435b0-214">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="435b0-214">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="435b0-215">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="435b0-215">AzureRM.Network</span></span>
* <span data-ttu-id="435b0-216">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="435b0-216">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="435b0-217">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="435b0-217">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="435b0-218">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="435b0-218">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="435b0-219">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="435b0-219">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="435b0-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="435b0-220">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="435b0-221">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="435b0-221">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="435b0-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="435b0-222">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="435b0-223">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="435b0-223">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="435b0-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="435b0-224">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="435b0-225">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="435b0-225">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="435b0-226">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="435b0-226">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="435b0-227">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="435b0-227">AzureRM.Sql</span></span>
* <span data-ttu-id="435b0-228">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="435b0-228">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="435b0-229">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="435b0-229">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="435b0-230">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="435b0-230">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="435b0-231">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="435b0-231">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="435b0-232">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="435b0-232">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="435b0-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="435b0-233">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="435b0-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="435b0-234">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="435b0-235">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="435b0-235">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="435b0-236">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="435b0-236">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="435b0-237">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="435b0-237">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="435b0-238">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="435b0-238">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="435b0-239">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="435b0-239">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>