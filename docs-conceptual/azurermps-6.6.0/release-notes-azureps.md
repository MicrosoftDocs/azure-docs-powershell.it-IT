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
ms.openlocfilehash: 340c1d2d28e1b97cdd2ec98033361eb00b4302da
ms.sourcegitcommit: 72086f8d368ec84bd403e802305acfc336c08978
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/14/2018
ms.locfileid: "43018910"
---
# <a name="release-notes"></a><span data-ttu-id="b5f62-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="b5f62-103">Release notes</span></span>

<span data-ttu-id="b5f62-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="b5f62-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="660---july-2018"></a><span data-ttu-id="b5f62-105">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-105">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b5f62-106">Generale</span><span class="sxs-lookup"><span data-stu-id="b5f62-106">General</span></span>
* <span data-ttu-id="b5f62-107">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="b5f62-107">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-108">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-109">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b5f62-109">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="b5f62-110">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f62-110">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b5f62-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f62-111">Azure.Storage</span></span>
* <span data-ttu-id="b5f62-112">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5f62-112">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="b5f62-113">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5f62-113">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b5f62-114">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b5f62-114">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b5f62-115">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="b5f62-115">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="b5f62-116">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="b5f62-116">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="b5f62-117">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="b5f62-117">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="b5f62-118">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="b5f62-118">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="b5f62-119">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="b5f62-119">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="b5f62-120">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="b5f62-120">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b5f62-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f62-121">AzureRM.Compute</span></span>
* <span data-ttu-id="b5f62-122">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="b5f62-122">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="b5f62-123">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="b5f62-123">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="b5f62-124">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b5f62-124">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="b5f62-125">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b5f62-125">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="b5f62-126">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="b5f62-126">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="b5f62-127">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="b5f62-127">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="b5f62-128">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b5f62-128">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="b5f62-129">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="b5f62-129">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="b5f62-130">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="b5f62-130">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="b5f62-131">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="b5f62-131">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b5f62-132">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b5f62-132">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b5f62-133">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="b5f62-133">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="b5f62-134">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="b5f62-134">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="b5f62-135">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b5f62-135">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="b5f62-136">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="b5f62-136">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b5f62-137">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b5f62-137">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b5f62-138">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="b5f62-138">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b5f62-139">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b5f62-139">AzureRM.EventHub</span></span>
* <span data-ttu-id="b5f62-140">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="b5f62-140">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="b5f62-141">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="b5f62-141">AzureRM.Insights</span></span>
* <span data-ttu-id="b5f62-142">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="b5f62-142">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="b5f62-143">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="b5f62-143">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b5f62-144">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b5f62-144">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b5f62-145">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5f62-145">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b5f62-146">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b5f62-146">AzureRM.Network</span></span>
* <span data-ttu-id="b5f62-147">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="b5f62-147">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b5f62-148">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b5f62-148">AzureRM.Resources</span></span>
* <span data-ttu-id="b5f62-149">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="b5f62-149">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="b5f62-150">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="b5f62-150">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b5f62-151">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b5f62-151">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b5f62-152">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="b5f62-152">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="b5f62-153">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="b5f62-153">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="b5f62-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-154">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-155">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5f62-155">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="b5f62-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b5f62-156">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="b5f62-157">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5f62-157">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="b5f62-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="b5f62-158">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="b5f62-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="b5f62-159">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="b5f62-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="b5f62-160">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="b5f62-161">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5f62-161">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="b5f62-162">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="b5f62-162">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="b5f62-163">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f62-163">AzureRM.Storage</span></span>
* <span data-ttu-id="b5f62-164">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5f62-164">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="b5f62-165">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="b5f62-165">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="b5f62-166">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5f62-166">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b5f62-167">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5f62-167">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="b5f62-168">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b5f62-168">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="b5f62-169">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="b5f62-169">AzureRM.Tags</span></span>
* <span data-ttu-id="b5f62-170">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="b5f62-170">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="b5f62-171">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-171">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-172">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-173">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="b5f62-173">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b5f62-174">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f62-174">Azure.Storage</span></span>
* <span data-ttu-id="b5f62-175">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="b5f62-175">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="b5f62-176">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b5f62-176">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="b5f62-177">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="b5f62-177">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b5f62-178">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b5f62-178">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b5f62-179">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="b5f62-179">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="b5f62-180">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="b5f62-180">AzureRM.Automation</span></span>
* <span data-ttu-id="b5f62-181">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="b5f62-181">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b5f62-182">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f62-182">AzureRM.Compute</span></span>
* <span data-ttu-id="b5f62-183">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b5f62-183">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="b5f62-184">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="b5f62-184">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b5f62-185">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="b5f62-185">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="b5f62-186">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="b5f62-186">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="b5f62-187">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="b5f62-187">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b5f62-188">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b5f62-188">AzureRM.EventHub</span></span>
* <span data-ttu-id="b5f62-189">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="b5f62-189">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b5f62-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b5f62-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b5f62-191">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b5f62-191">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="b5f62-192">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="b5f62-192">AzureRM.LogicApp</span></span>
* <span data-ttu-id="b5f62-193">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="b5f62-193">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b5f62-194">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b5f62-194">AzureRM.Network</span></span>
* <span data-ttu-id="b5f62-195">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="b5f62-195">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="b5f62-196">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="b5f62-196">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="b5f62-197">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="b5f62-197">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="b5f62-198">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b5f62-198">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="b5f62-199">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="b5f62-199">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="b5f62-200">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="b5f62-200">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="b5f62-201">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="b5f62-201">AzureRM.Relay</span></span>
* <span data-ttu-id="b5f62-202">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="b5f62-202">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b5f62-203">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b5f62-203">AzureRM.Resources</span></span>
* <span data-ttu-id="b5f62-204">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="b5f62-204">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="b5f62-205">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="b5f62-205">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="b5f62-206">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b5f62-206">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="b5f62-207">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="b5f62-207">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="b5f62-208">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="b5f62-208">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="b5f62-209">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b5f62-209">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b5f62-210">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="b5f62-210">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="b5f62-211">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="b5f62-211">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="b5f62-212">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b5f62-212">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b5f62-213">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b5f62-213">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b5f62-214">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b5f62-214">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b5f62-215">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b5f62-215">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="b5f62-216">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="b5f62-216">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="b5f62-217">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="b5f62-217">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b5f62-218">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b5f62-218">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b5f62-219">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="b5f62-219">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b5f62-220">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-220">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-221">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="b5f62-221">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="b5f62-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b5f62-222">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="b5f62-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="b5f62-223">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b5f62-224">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b5f62-224">AzureRM.Websites</span></span>
* <span data-ttu-id="b5f62-225">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="b5f62-225">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="b5f62-226">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="b5f62-226">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="b5f62-227">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="b5f62-227">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="b5f62-228">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-228">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="b5f62-229">Generale</span><span class="sxs-lookup"><span data-stu-id="b5f62-229">General</span></span>
* <span data-ttu-id="b5f62-230">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="b5f62-230">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-231">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-231">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-232">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="b5f62-232">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b5f62-233">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f62-233">AzureRM.Compute</span></span>
* <span data-ttu-id="b5f62-234">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="b5f62-234">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="b5f62-235">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="b5f62-235">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="b5f62-236">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="b5f62-236">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="b5f62-237">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="b5f62-237">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="b5f62-238">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-238">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="b5f62-239">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-239">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="b5f62-240">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-240">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="b5f62-241">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="b5f62-241">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="b5f62-242">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5f62-242">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="b5f62-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b5f62-243">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b5f62-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b5f62-244">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="b5f62-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b5f62-245">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b5f62-246">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b5f62-246">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b5f62-247">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="b5f62-247">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="b5f62-248">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b5f62-248">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b5f62-249">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="b5f62-249">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="b5f62-250">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="b5f62-250">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="b5f62-251">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="b5f62-251">AzureRM.EventHub</span></span>
* <span data-ttu-id="b5f62-252">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b5f62-252">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="b5f62-253">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b5f62-253">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="b5f62-254">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="b5f62-254">Provided Default Parameter set.</span></span>
* <span data-ttu-id="b5f62-255">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b5f62-255">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b5f62-256">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b5f62-256">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b5f62-257">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="b5f62-257">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="b5f62-258">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b5f62-258">AzureRM.Network</span></span>
* <span data-ttu-id="b5f62-259">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="b5f62-259">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="b5f62-260">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="b5f62-260">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="b5f62-261">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b5f62-261">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b5f62-262">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="b5f62-262">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="b5f62-263">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b5f62-263">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b5f62-264">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b5f62-264">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b5f62-265">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="b5f62-265">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="b5f62-266">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="b5f62-266">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="b5f62-267">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="b5f62-267">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="b5f62-268">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="b5f62-268">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b5f62-269">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b5f62-269">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b5f62-270">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="b5f62-270">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="b5f62-271">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b5f62-271">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="b5f62-272">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="b5f62-272">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b5f62-273">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b5f62-273">AzureRM.Resources</span></span>
* <span data-ttu-id="b5f62-274">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="b5f62-274">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="b5f62-275">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="b5f62-275">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="b5f62-276">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="b5f62-276">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="b5f62-277">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="b5f62-277">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="b5f62-278">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b5f62-278">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="b5f62-279">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="b5f62-279">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b5f62-280">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="b5f62-280">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b5f62-281">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b5f62-281">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="b5f62-282">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="b5f62-282">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="b5f62-283">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="b5f62-283">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="b5f62-284">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="b5f62-284">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="b5f62-285">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="b5f62-285">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="b5f62-286">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="b5f62-286">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="b5f62-287">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="b5f62-287">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="b5f62-288">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="b5f62-288">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b5f62-289">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-289">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-290">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="b5f62-290">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="b5f62-291">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="b5f62-291">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="b5f62-292">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-292">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-293">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-293">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-294">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="b5f62-294">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="b5f62-295">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="b5f62-295">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="b5f62-296">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="b5f62-296">Azure.Storage</span></span>
* <span data-ttu-id="b5f62-297">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="b5f62-297">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b5f62-298">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f62-298">AzureRM.Compute</span></span>
* <span data-ttu-id="b5f62-299">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="b5f62-299">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="b5f62-300">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="b5f62-300">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="b5f62-301">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b5f62-301">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b5f62-302">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b5f62-302">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b5f62-303">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="b5f62-303">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="b5f62-304">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="b5f62-304">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="b5f62-305">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b5f62-305">Start-AzureRmVM</span></span>
    - <span data-ttu-id="b5f62-306">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b5f62-306">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="b5f62-307">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b5f62-307">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="b5f62-308">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b5f62-308">Set-AzureRmVM</span></span>
    - <span data-ttu-id="b5f62-309">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="b5f62-309">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="b5f62-310">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-310">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="b5f62-311">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="b5f62-311">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="b5f62-312">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="b5f62-312">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="b5f62-313">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-313">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="b5f62-314">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-314">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="b5f62-315">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-315">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="b5f62-316">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b5f62-316">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="b5f62-317">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="b5f62-317">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="b5f62-318">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="b5f62-318">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="b5f62-319">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="b5f62-319">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="b5f62-320">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="b5f62-320">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="b5f62-321">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="b5f62-321">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="b5f62-322">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b5f62-322">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="b5f62-323">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b5f62-323">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="b5f62-324">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="b5f62-324">AzureRM.EventGrid</span></span>
* <span data-ttu-id="b5f62-325">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="b5f62-325">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="b5f62-326">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b5f62-326">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b5f62-327">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="b5f62-327">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="b5f62-328">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="b5f62-328">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="b5f62-329">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="b5f62-329">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="b5f62-330">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="b5f62-330">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="b5f62-331">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="b5f62-331">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="b5f62-332">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="b5f62-332">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="b5f62-333">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="b5f62-333">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="b5f62-334">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="b5f62-334">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b5f62-335">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-335">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-336">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="b5f62-336">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b5f62-337">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b5f62-337">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b5f62-338">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="b5f62-338">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b5f62-339">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b5f62-339">AzureRM.Websites</span></span>
* <span data-ttu-id="b5f62-340">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b5f62-340">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="b5f62-341">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="b5f62-341">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="b5f62-342">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-342">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="b5f62-343">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="b5f62-343">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="b5f62-344">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="b5f62-344">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="b5f62-345">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-345">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-346">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-346">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-347">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="b5f62-347">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="b5f62-348">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="b5f62-348">AzureRM.Compute</span></span>
* <span data-ttu-id="b5f62-349">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="b5f62-349">VMSS VM Update feature</span></span>
    - <span data-ttu-id="b5f62-350">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="b5f62-350">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="b5f62-351">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="b5f62-351">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="b5f62-352">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="b5f62-352">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="b5f62-353">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="b5f62-353">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="b5f62-354">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="b5f62-354">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="b5f62-355">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="b5f62-355">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="b5f62-356">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="b5f62-356">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="b5f62-357">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="b5f62-357">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="b5f62-358">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="b5f62-358">AzureRM.KeyVault</span></span>
* <span data-ttu-id="b5f62-359">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="b5f62-359">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="b5f62-360">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b5f62-360">AzureRM.Network</span></span>
* <span data-ttu-id="b5f62-361">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="b5f62-361">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="b5f62-362">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="b5f62-362">AzureRM.Resources</span></span>
* <span data-ttu-id="b5f62-363">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="b5f62-363">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="b5f62-364">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="b5f62-364">AzureRM.Scheduler</span></span>
* <span data-ttu-id="b5f62-365">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="b5f62-365">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="b5f62-366">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-366">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-367">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="b5f62-367">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="b5f62-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5f62-368">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b5f62-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b5f62-369">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b5f62-370">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b5f62-370">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b5f62-371">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5f62-371">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b5f62-372">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5f62-372">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="b5f62-373">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="b5f62-373">AzureRM.Websites</span></span>
* <span data-ttu-id="b5f62-374">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="b5f62-374">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="b5f62-375">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="b5f62-375">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="b5f62-376">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="b5f62-376">AzureRM.Profile</span></span>
* <span data-ttu-id="b5f62-377">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="b5f62-377">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="b5f62-378">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="b5f62-378">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="b5f62-379">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="b5f62-379">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="b5f62-380">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b5f62-380">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="b5f62-381">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="b5f62-381">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="b5f62-382">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="b5f62-382">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="b5f62-383">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="b5f62-383">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="b5f62-384">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="b5f62-384">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="b5f62-385">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="b5f62-385">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="b5f62-386">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="b5f62-386">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="b5f62-387">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="b5f62-387">Added support for MSI identity</span></span>
* <span data-ttu-id="b5f62-388">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="b5f62-388">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="b5f62-389">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="b5f62-389">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="b5f62-390">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5f62-390">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="b5f62-391">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="b5f62-391">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="b5f62-392">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="b5f62-392">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="b5f62-393">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="b5f62-393">AzureRM.Batch</span></span>
* <span data-ttu-id="b5f62-394">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="b5f62-394">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="b5f62-395">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="b5f62-395">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="b5f62-396">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="b5f62-396">AzureRM.Consumption</span></span>
* <span data-ttu-id="b5f62-397">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="b5f62-397">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="b5f62-398">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="b5f62-398">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="b5f62-399">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="b5f62-399">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="b5f62-400">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b5f62-400">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="b5f62-401">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b5f62-401">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="b5f62-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="b5f62-402">AzureRM.Network</span></span>
* <span data-ttu-id="b5f62-403">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="b5f62-403">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="b5f62-404">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="b5f62-404">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="b5f62-405">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5f62-405">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="b5f62-406">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="b5f62-406">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="b5f62-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5f62-407">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b5f62-408">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="b5f62-408">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="b5f62-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5f62-409">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="b5f62-410">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="b5f62-410">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="b5f62-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="b5f62-411">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="b5f62-412">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b5f62-412">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="b5f62-413">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="b5f62-413">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="b5f62-414">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="b5f62-414">AzureRM.Sql</span></span>
* <span data-ttu-id="b5f62-415">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="b5f62-415">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="b5f62-416">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="b5f62-416">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="b5f62-417">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="b5f62-417">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="b5f62-418">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="b5f62-418">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="b5f62-419">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="b5f62-419">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="b5f62-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5f62-420">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="b5f62-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="b5f62-421">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="b5f62-422">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b5f62-422">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="b5f62-423">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5f62-423">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="b5f62-424">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="b5f62-424">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="b5f62-425">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b5f62-425">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="b5f62-426">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="b5f62-426">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
