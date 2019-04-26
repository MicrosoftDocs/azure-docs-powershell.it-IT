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
ms.openlocfilehash: 7f517f0b3768a2075557b131158ee1264ea9ab3f
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153451"
---
# <a name="release-notes"></a><span data-ttu-id="617a0-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="617a0-103">Release notes</span></span>

<span data-ttu-id="617a0-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="617a0-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="617a0-105">6.13.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-106">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-107">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="617a0-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="617a0-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="617a0-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="617a0-109">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="617a0-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="617a0-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="617a0-110">AzureRM.Automation</span></span>
* <span data-ttu-id="617a0-111">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="617a0-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="617a0-112">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="617a0-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="617a0-113">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="617a0-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="617a0-114">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="617a0-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="617a0-115">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="617a0-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-116">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-117">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="617a0-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="617a0-118">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="617a0-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="617a0-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="617a0-120">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="617a0-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="617a0-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="617a0-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="617a0-122">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="617a0-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-123">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-124">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="617a0-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="617a0-125">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="617a0-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="617a0-126">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="617a0-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="617a0-127">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="617a0-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="617a0-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="617a0-129">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="617a0-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="617a0-130">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="617a0-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="617a0-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="617a0-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="617a0-132">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="617a0-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="617a0-133">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="617a0-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="617a0-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="617a0-134">AzureRM.Relay</span></span>
* <span data-ttu-id="617a0-135">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="617a0-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-136">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-137">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="617a0-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="617a0-138">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="617a0-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="617a0-139">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="617a0-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="617a0-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="617a0-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="617a0-141">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="617a0-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-142">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-143">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="617a0-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="617a0-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="617a0-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="617a0-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="617a0-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="617a0-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="617a0-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="617a0-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="617a0-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="617a0-152">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="617a0-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="617a0-153">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="617a0-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="617a0-154">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="617a0-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="617a0-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="617a0-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="617a0-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="617a0-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="617a0-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="617a0-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="617a0-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="617a0-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="617a0-159">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="617a0-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="617a0-160">6.12.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-161">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-162">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="617a0-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="617a0-163">Parametro TenantId nel cmdlet Connect-AzureRmAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="617a0-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="617a0-164">Aggiornamento della descrizione di TenantId per Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="617a0-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="617a0-165">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="617a0-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="617a0-166">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="617a0-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="617a0-167">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="617a0-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="617a0-168">Risoluzione del problema per il quale 'Disconnect-AzureRmAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="617a0-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="617a0-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="617a0-169">AzureRM.Automation</span></span>
* <span data-ttu-id="617a0-170">Cmdlet DLL filename rinominato in Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="617a0-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="617a0-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="617a0-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="617a0-172">Aggiunta dell'operazione Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="617a0-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-173">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-174">Aggiunta dei cmdlet Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="617a0-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="617a0-175">Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="617a0-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="617a0-176">Correzione dei valori di opzione di SetAzureRmVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="617a0-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-178">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="617a0-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="617a0-179">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="617a0-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="617a0-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-180">AzureRM.Insights</span></span>
* <span data-ttu-id="617a0-181">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="617a0-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="617a0-182">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="617a0-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="617a0-183">Correzione del problema numero 7513 [Insights] per il quale Set-AzureRMDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="617a0-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="617a0-184">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="617a0-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-185">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-186">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a0-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="617a0-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="617a0-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="617a0-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="617a0-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="617a0-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="617a0-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="617a0-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="617a0-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="617a0-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="617a0-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="617a0-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="617a0-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="617a0-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="617a0-194">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="617a0-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="617a0-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="617a0-196">Aggiunta del supporto per le condivisioni di File di Azure nei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="617a0-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-197">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-198">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="617a0-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="617a0-199">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="617a0-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-201">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="617a0-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="617a0-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="617a0-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="617a0-203">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="617a0-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="617a0-204">Correzione di 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="617a0-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="617a0-205">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="617a0-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="617a0-206">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="617a0-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="617a0-207">Correzione di 'Update-AzureRmServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="617a0-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="617a0-208">6.11.0 - ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-209">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-210">Risoluzione del problema con Get-AzureRmSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="617a0-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="617a0-211">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="617a0-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="617a0-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-212">AzureRM.Backup</span></span>
* <span data-ttu-id="617a0-213">Cmdlet di Backup di Azure deprecati.</span><span class="sxs-lookup"><span data-stu-id="617a0-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-214">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-215">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzureRmVm'.</span><span class="sxs-lookup"><span data-stu-id="617a0-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="617a0-216">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="617a0-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-218">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="617a0-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="617a0-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="617a0-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="617a0-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="617a0-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="617a0-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="617a0-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="617a0-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="617a0-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-223">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-224">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="617a0-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="617a0-225">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="617a0-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-226">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-227">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzureRMRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="617a0-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="617a0-228">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="617a0-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="617a0-229">6.10.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="617a0-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-230">Azure.Storage</span></span>
* <span data-ttu-id="617a0-231">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="617a0-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="617a0-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="617a0-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="617a0-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="617a0-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="617a0-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="617a0-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="617a0-235">Supporto di Get-AzureRmCognitiveServicesAccountSkus senza un account esistente</span><span class="sxs-lookup"><span data-stu-id="617a0-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-236">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-237">Correzione di Get-AzureRmVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="617a0-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="617a0-238">Aggiunta di un esempio di SimpleParameterSet alla Guida del cmdlet New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="617a0-239">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="617a0-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="617a0-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="617a0-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="617a0-241">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="617a0-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-242">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-243">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="617a0-244">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-244">new cmdlets added</span></span>
    - <span data-ttu-id="617a0-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="617a0-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="617a0-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="617a0-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="617a0-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="617a0-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="617a0-251">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="617a0-252">Aggiunta dei cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap e Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="617a0-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="617a0-253">Aggiunta dei cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig e Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="617a0-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="617a0-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="617a0-255">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="617a0-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="617a0-256">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="617a0-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-257">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-258">Aggiunta del parametro -Mode mancante a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="617a0-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="617a0-259">Correzione del bug del cmdlet Get-AzureRmProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="617a0-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-260">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-261">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="617a0-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="617a0-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-262">AzureRM.Storage</span></span>
* <span data-ttu-id="617a0-263">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="617a0-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="617a0-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="617a0-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-265">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-266">Nuovo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="617a0-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="617a0-267">Nuovi cmdlet New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="617a0-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="617a0-268">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="617a0-269">Generale</span><span class="sxs-lookup"><span data-stu-id="617a0-269">General</span></span>
* <span data-ttu-id="617a0-270">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="617a0-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="617a0-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-271">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-272">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="617a0-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="617a0-273">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="617a0-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="617a0-274">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="617a0-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span> 

#### <a name="azurestorage"></a><span data-ttu-id="617a0-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-275">Azure.Storage</span></span>
* <span data-ttu-id="617a0-276">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="617a0-276">Support create Storage Context with OAuth.</span></span> 
    - <span data-ttu-id="617a0-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="617a0-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="617a0-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="617a0-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="617a0-279">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="617a0-279">Added Standard_Microsoft in Cdn pricing sku.</span></span> 

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-280">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-281">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="617a0-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="617a0-282">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="617a0-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="617a0-283">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="617a0-284">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="617a0-285">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="617a0-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="617a0-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="617a0-286">AzureRM.Dns</span></span>
* <span data-ttu-id="617a0-287">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="617a0-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="617a0-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-288">AzureRM.Insights</span></span>
* <span data-ttu-id="617a0-289">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="617a0-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="617a0-290">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="617a0-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="617a0-291">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="617a0-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="617a0-292">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="617a0-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="617a0-293">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="617a0-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-294">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-295">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="617a0-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="617a0-296">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="617a0-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="617a0-297">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="617a0-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="617a0-298">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="617a0-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="617a0-299">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="617a0-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="617a0-300">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="617a0-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="617a0-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="617a0-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="617a0-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="617a0-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="617a0-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="617a0-306">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="617a0-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="617a0-307">Aggiunta di nuovi cmdlet per la funzionalità: Firewall di Azure tramite Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="617a0-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="617a0-308">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="617a0-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="617a0-309">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="617a0-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="617a0-310">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="617a0-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="617a0-311">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="617a0-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="617a0-312">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="617a0-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="617a0-313">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="617a0-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="617a0-314">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="617a0-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="617a0-315">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="617a0-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="617a0-316">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="617a0-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="617a0-317">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="617a0-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="617a0-318">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="617a0-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="617a0-319">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="617a0-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="617a0-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="617a0-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="617a0-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="617a0-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="617a0-329">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="617a0-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="617a0-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="617a0-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="617a0-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="617a0-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="617a0-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="617a0-334">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="617a0-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="617a0-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="617a0-337">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="617a0-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="617a0-338">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="617a0-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="617a0-339">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="617a0-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="617a0-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="617a0-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="617a0-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="617a0-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="617a0-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="617a0-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="617a0-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="617a0-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="617a0-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="617a0-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="617a0-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="617a0-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="617a0-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="617a0-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="617a0-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="617a0-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="617a0-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="617a0-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="617a0-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="617a0-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="617a0-359">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="617a0-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="617a0-360">New-AzureRmDelegation: Crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="617a0-361">Remove-AzureRmDelegation: Acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="617a0-362">Add-AzureRmDelegation: Acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="617a0-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="617a0-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="617a0-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="617a0-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="617a0-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="617a0-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="617a0-366">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="617a0-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="617a0-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="617a0-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="617a0-368">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="617a0-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-369">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-370">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="617a0-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="617a0-371">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="617a0-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="617a0-372">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="617a0-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="617a0-373">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="617a0-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="617a0-374">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="617a0-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-376">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="617a0-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="617a0-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="617a0-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="617a0-378">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="617a0-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="617a0-379">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="617a0-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="617a0-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-380">AzureRM.Storage</span></span>
* <span data-ttu-id="617a0-381">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-381">Support Immutability Policy in AzureRm.Storage</span></span> 
    - <span data-ttu-id="617a0-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="617a0-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="617a0-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="617a0-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="617a0-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="617a0-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="617a0-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="617a0-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="617a0-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="617a0-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="617a0-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="617a0-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="617a0-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="617a0-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="617a0-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="617a0-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="617a0-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="617a0-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-393">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-394">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="617a0-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="617a0-395">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="617a0-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="617a0-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="617a0-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="617a0-397">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="617a0-398">Generale</span><span class="sxs-lookup"><span data-stu-id="617a0-398">General</span></span>
* <span data-ttu-id="617a0-399">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="617a0-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="617a0-400">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="617a0-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="617a0-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="617a0-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="617a0-402">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="617a0-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="617a0-403">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="617a0-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="617a0-404">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="617a0-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="617a0-405">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="617a0-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="617a0-406">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="617a0-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="617a0-407">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="617a0-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="617a0-408">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="617a0-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="617a0-409">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="617a0-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="617a0-410">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="617a0-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="617a0-411">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="617a0-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="617a0-412">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="617a0-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="617a0-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-413">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-414">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="617a0-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="617a0-415">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="617a0-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="617a0-416">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="617a0-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="617a0-417">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="617a0-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-418">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-419">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="617a0-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="617a0-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="617a0-421">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="617a0-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="617a0-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-422">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-423">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="617a0-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-425">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="617a0-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="617a0-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="617a0-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="617a0-427">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="617a0-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="617a0-428">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="617a0-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="617a0-429">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="617a0-430">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="617a0-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="617a0-431">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="617a0-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="617a0-432">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="617a0-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="617a0-433">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="617a0-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="617a0-434">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="617a0-435">Generale</span><span class="sxs-lookup"><span data-stu-id="617a0-435">General</span></span>
* <span data-ttu-id="617a0-436">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="617a0-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="617a0-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-437">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-438">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="617a0-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-439">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-440">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="617a0-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="617a0-441">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="617a0-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="617a0-442">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="617a0-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="617a0-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="617a0-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="617a0-444">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="617a0-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-445">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-446">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="617a0-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="617a0-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="617a0-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="617a0-448">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="617a0-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-449">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-450">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="617a0-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-452">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="617a0-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="617a0-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="617a0-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="617a0-454">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="617a0-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="617a0-455">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="617a0-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="617a0-456">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="617a0-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="617a0-457">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="617a0-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="617a0-458">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="617a0-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="617a0-459">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="617a0-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="617a0-460">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="617a0-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-461">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-462">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="617a0-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="617a0-463">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-464">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-465">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="617a0-466">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="617a0-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="617a0-467">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="617a0-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="617a0-468">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="617a0-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="617a0-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-469">Azure.Storage</span></span>
* <span data-ttu-id="617a0-470">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="617a0-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="617a0-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="617a0-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="617a0-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="617a0-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="617a0-473">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="617a0-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="617a0-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="617a0-475">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="617a0-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="617a0-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="617a0-477">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="617a0-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="617a0-479">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="617a0-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="617a0-480">AzureRM.Automation</span></span>
* <span data-ttu-id="617a0-481">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="617a0-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-482">AzureRM.Backup</span></span>
* <span data-ttu-id="617a0-483">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="617a0-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="617a0-484">AzureRM.Batch</span></span>
* <span data-ttu-id="617a0-485">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="617a0-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="617a0-486">AzureRM.Billing</span></span>
* <span data-ttu-id="617a0-487">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="617a0-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="617a0-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="617a0-489">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="617a0-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="617a0-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="617a0-491">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-492">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-493">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="617a0-494">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="617a0-495">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="617a0-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="617a0-496">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="617a0-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="617a0-497">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="617a0-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="617a0-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="617a0-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="617a0-499">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="617a0-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="617a0-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="617a0-501">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="617a0-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="617a0-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="617a0-503">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="617a0-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="617a0-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="617a0-505">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="617a0-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="617a0-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="617a0-507">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="617a0-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="617a0-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="617a0-509">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-511">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="617a0-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="617a0-512">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="617a0-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="617a0-513">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="617a0-514">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="617a0-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="617a0-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="617a0-516">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="617a0-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="617a0-517">AzureRM.Dns</span></span>
* <span data-ttu-id="617a0-518">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="617a0-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="617a0-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="617a0-520">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="617a0-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="617a0-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="617a0-522">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="617a0-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="617a0-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="617a0-524">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="617a0-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-525">AzureRM.Insights</span></span>
* <span data-ttu-id="617a0-526">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="617a0-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="617a0-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="617a0-528">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-530">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="617a0-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="617a0-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="617a0-532">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="617a0-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="617a0-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="617a0-534">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="617a0-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="617a0-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="617a0-536">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="617a0-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="617a0-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="617a0-538">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="617a0-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="617a0-539">AzureRM.Media</span></span>
* <span data-ttu-id="617a0-540">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-541">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-542">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="617a0-543">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="617a0-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="617a0-544">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="617a0-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="617a0-545">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="617a0-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="617a0-546">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="617a0-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="617a0-547">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="617a0-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="617a0-548">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="617a0-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="617a0-549">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="617a0-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="617a0-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="617a0-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="617a0-551">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="617a0-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="617a0-553">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="617a0-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="617a0-555">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="617a0-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="617a0-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="617a0-557">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="617a0-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="617a0-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="617a0-559">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="617a0-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="617a0-561">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="617a0-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="617a0-562">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="617a0-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="617a0-563">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="617a0-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="617a0-564">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="617a0-565">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="617a0-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="617a0-566">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="617a0-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="617a0-567">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="617a0-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="617a0-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="617a0-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="617a0-569">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="617a0-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="617a0-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="617a0-571">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="617a0-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="617a0-572">AzureRM.Relay</span></span>
* <span data-ttu-id="617a0-573">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-574">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-575">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="617a0-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="617a0-576">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="617a0-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="617a0-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="617a0-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="617a0-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="617a0-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="617a0-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="617a0-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="617a0-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="617a0-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="617a0-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="617a0-584">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="617a0-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="617a0-585">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="617a0-586">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="617a0-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="617a0-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="617a0-588">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-590">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="617a0-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="617a0-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="617a0-592">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-593">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-594">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="617a0-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-595">AzureRM.Storage</span></span>
* <span data-ttu-id="617a0-596">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="617a0-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="617a0-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="617a0-598">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="617a0-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="617a0-599">AzureRM.Tags</span></span>
* <span data-ttu-id="617a0-600">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="617a0-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="617a0-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="617a0-602">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="617a0-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="617a0-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="617a0-604">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-605">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-606">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="617a0-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="617a0-607">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="617a0-608">Generale</span><span class="sxs-lookup"><span data-stu-id="617a0-608">General</span></span>
* <span data-ttu-id="617a0-609">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="617a0-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="617a0-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-610">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-611">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="617a0-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="617a0-612">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="617a0-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-613">Azure.Storage</span></span>
* <span data-ttu-id="617a0-614">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="617a0-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="617a0-615">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="617a0-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="617a0-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="617a0-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="617a0-617">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="617a0-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="617a0-618">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="617a0-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="617a0-619">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="617a0-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="617a0-620">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="617a0-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="617a0-621">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="617a0-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="617a0-622">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="617a0-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-623">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-624">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="617a0-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="617a0-625">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="617a0-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="617a0-626">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="617a0-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="617a0-627">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="617a0-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="617a0-628">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="617a0-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="617a0-629">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="617a0-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="617a0-630">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="617a0-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="617a0-631">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="617a0-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="617a0-632">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="617a0-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="617a0-633">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="617a0-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="617a0-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="617a0-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="617a0-635">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="617a0-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="617a0-636">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="617a0-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="617a0-637">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="617a0-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="617a0-638">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="617a0-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-640">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="617a0-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="617a0-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="617a0-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="617a0-642">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="617a0-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="617a0-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-643">AzureRM.Insights</span></span>
* <span data-ttu-id="617a0-644">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="617a0-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="617a0-645">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="617a0-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-647">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-648">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-649">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="617a0-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-650">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-651">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="617a0-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="617a0-652">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="617a0-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-654">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="617a0-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="617a0-655">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="617a0-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="617a0-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-656">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-657">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a0-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="617a0-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="617a0-659">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a0-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="617a0-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="617a0-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="617a0-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="617a0-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="617a0-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="617a0-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="617a0-663">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="617a0-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="617a0-664">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="617a0-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="617a0-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-665">AzureRM.Storage</span></span>
* <span data-ttu-id="617a0-666">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="617a0-667">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="617a0-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="617a0-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="617a0-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="617a0-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="617a0-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="617a0-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="617a0-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="617a0-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="617a0-671">AzureRM.Tags</span></span>
* <span data-ttu-id="617a0-672">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="617a0-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="617a0-673">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-674">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-675">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="617a0-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="617a0-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-676">Azure.Storage</span></span>
* <span data-ttu-id="617a0-677">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="617a0-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="617a0-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="617a0-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="617a0-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="617a0-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="617a0-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="617a0-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="617a0-681">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="617a0-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="617a0-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="617a0-682">AzureRM.Automation</span></span>
* <span data-ttu-id="617a0-683">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="617a0-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-684">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-685">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="617a0-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="617a0-686">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="617a0-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="617a0-687">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="617a0-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="617a0-688">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="617a0-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="617a0-689">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="617a0-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="617a0-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="617a0-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="617a0-691">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="617a0-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-693">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="617a0-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="617a0-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="617a0-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="617a0-695">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="617a0-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-696">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-697">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="617a0-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="617a0-698">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="617a0-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="617a0-699">New-AzureRmApplicationGateway: Aggiunta del flag EnableFIPS e del supporto per le zone</span><span class="sxs-lookup"><span data-stu-id="617a0-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="617a0-700">New-AzureRmApplicationGatewaySku: Aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="617a0-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="617a0-701">Set-AzureRmApplicationGatewaySku : Aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="617a0-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="617a0-702">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="617a0-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="617a0-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="617a0-703">AzureRM.Relay</span></span>
* <span data-ttu-id="617a0-704">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="617a0-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-705">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-706">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="617a0-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="617a0-707">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="617a0-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="617a0-708">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="617a0-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="617a0-709">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="617a0-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="617a0-710">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="617a0-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-712">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="617a0-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="617a0-713">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="617a0-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="617a0-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="617a0-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="617a0-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="617a0-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="617a0-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="617a0-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="617a0-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="617a0-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="617a0-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="617a0-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="617a0-719">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="617a0-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="617a0-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="617a0-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="617a0-721">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="617a0-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-722">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-723">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="617a0-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="617a0-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="617a0-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-726">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-727">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="617a0-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="617a0-728">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="617a0-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="617a0-729">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="617a0-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="617a0-730">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="617a0-731">Generale</span><span class="sxs-lookup"><span data-stu-id="617a0-731">General</span></span>
* <span data-ttu-id="617a0-732">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="617a0-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="617a0-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-733">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-734">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="617a0-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-735">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-736">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="617a0-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="617a0-737">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="617a0-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="617a0-738">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="617a0-739">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="617a0-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="617a0-740">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="617a0-741">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="617a0-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="617a0-742">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="617a0-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="617a0-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="617a0-744">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a0-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="617a0-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="617a0-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="617a0-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-749">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="617a0-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="617a0-750">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="617a0-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="617a0-751">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="617a0-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="617a0-752">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="617a0-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="617a0-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="617a0-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="617a0-754">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="617a0-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="617a0-755">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="617a0-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="617a0-756">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="617a0-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="617a0-757">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="617a0-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-759">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="617a0-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-760">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-761">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="617a0-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="617a0-762">Aggiunta di nuovi comandi per la funzione: API Partner ExpressRoute tramite Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="617a0-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="617a0-763">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="617a0-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="617a0-764">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="617a0-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="617a0-765">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="617a0-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="617a0-766">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="617a0-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="617a0-767">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="617a0-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="617a0-768">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="617a0-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="617a0-769">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="617a0-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="617a0-770">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="617a0-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="617a0-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="617a0-772">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="617a0-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="617a0-773">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="617a0-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="617a0-774">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="617a0-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-775">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-776">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="617a0-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="617a0-777">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="617a0-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="617a0-778">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="617a0-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="617a0-779">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="617a0-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="617a0-780">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="617a0-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="617a0-781">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="617a0-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="617a0-782">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="617a0-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="617a0-783">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="617a0-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="617a0-784">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="617a0-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="617a0-785">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="617a0-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="617a0-786">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="617a0-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="617a0-787">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="617a0-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="617a0-788">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="617a0-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="617a0-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="617a0-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="617a0-790">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="617a0-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-791">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-792">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="617a0-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="617a0-793">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="617a0-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="617a0-794">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-795">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-796">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="617a0-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="617a0-797">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="617a0-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="617a0-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="617a0-798">Azure.Storage</span></span>
* <span data-ttu-id="617a0-799">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="617a0-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-800">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-801">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="617a0-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="617a0-802">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="617a0-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="617a0-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="617a0-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="617a0-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="617a0-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="617a0-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="617a0-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="617a0-806">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="617a0-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="617a0-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="617a0-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="617a0-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="617a0-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="617a0-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="617a0-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="617a0-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="617a0-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="617a0-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="617a0-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="617a0-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="617a0-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="617a0-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="617a0-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="617a0-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="617a0-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="617a0-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="617a0-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="617a0-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="617a0-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="617a0-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="617a0-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="617a0-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="617a0-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="617a0-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="617a0-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="617a0-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="617a0-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="617a0-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="617a0-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="617a0-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="617a0-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="617a0-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="617a0-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="617a0-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="617a0-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="617a0-827">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="617a0-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-829">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="617a0-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="617a0-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="617a0-831">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="617a0-832">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="617a0-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="617a0-833">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="617a0-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="617a0-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="617a0-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="617a0-835">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="617a0-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="617a0-836">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="617a0-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-837">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-838">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="617a0-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="617a0-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="617a0-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="617a0-840">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-841">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-842">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="617a0-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="617a0-843">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="617a0-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="617a0-844">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="617a0-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="617a0-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="617a0-846">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="617a0-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="617a0-847">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-848">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-849">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="617a0-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="617a0-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="617a0-850">AzureRM.Compute</span></span>
* <span data-ttu-id="617a0-851">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="617a0-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="617a0-852">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="617a0-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="617a0-853">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="617a0-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="617a0-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="617a0-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="617a0-855">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="617a0-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="617a0-856">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="617a0-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="617a0-857">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="617a0-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="617a0-858">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="617a0-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="617a0-859">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="617a0-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="617a0-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="617a0-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="617a0-861">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="617a0-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="617a0-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-862">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-863">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="617a0-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="617a0-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="617a0-864">AzureRM.Resources</span></span>
* <span data-ttu-id="617a0-865">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="617a0-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="617a0-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="617a0-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="617a0-867">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="617a0-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="617a0-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-868">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-869">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="617a0-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="617a0-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="617a0-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="617a0-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="617a0-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="617a0-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="617a0-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="617a0-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="617a0-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="617a0-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="617a0-875">AzureRM.Websites</span></span>
* <span data-ttu-id="617a0-876">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="617a0-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="617a0-877">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="617a0-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="617a0-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="617a0-878">AzureRM.Profile</span></span>
* <span data-ttu-id="617a0-879">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="617a0-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="617a0-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="617a0-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="617a0-881">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="617a0-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="617a0-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="617a0-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="617a0-883">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="617a0-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="617a0-884">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="617a0-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="617a0-885">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="617a0-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="617a0-886">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="617a0-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="617a0-887">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="617a0-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="617a0-888">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="617a0-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="617a0-889">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="617a0-889">Added support for MSI identity</span></span>
* <span data-ttu-id="617a0-890">Aggiunta del supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti saranno deprecati nella versione futura</span><span class="sxs-lookup"><span data-stu-id="617a0-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="617a0-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="617a0-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="617a0-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="617a0-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="617a0-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="617a0-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="617a0-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="617a0-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="617a0-895">AzureRM.Batch</span></span>
* <span data-ttu-id="617a0-896">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="617a0-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="617a0-897">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="617a0-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="617a0-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="617a0-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="617a0-899">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="617a0-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="617a0-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="617a0-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="617a0-901">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="617a0-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="617a0-902">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="617a0-903">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="617a0-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="617a0-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="617a0-904">AzureRM.Network</span></span>
* <span data-ttu-id="617a0-905">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="617a0-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="617a0-906">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="617a0-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="617a0-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="617a0-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="617a0-908">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="617a0-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="617a0-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="617a0-910">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="617a0-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="617a0-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="617a0-912">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="617a0-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="617a0-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="617a0-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="617a0-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="617a0-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="617a0-915">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="617a0-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="617a0-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="617a0-916">AzureRM.Sql</span></span>
* <span data-ttu-id="617a0-917">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="617a0-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="617a0-918">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="617a0-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="617a0-919">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="617a0-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="617a0-920">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="617a0-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="617a0-921">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="617a0-921">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="617a0-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="617a0-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="617a0-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="617a0-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="617a0-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="617a0-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="617a0-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="617a0-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="617a0-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="617a0-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="617a0-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="617a0-928">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="617a0-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
