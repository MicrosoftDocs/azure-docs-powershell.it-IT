---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 189b360f8825b7de93b67b0b2cbe670d00187327
ms.sourcegitcommit: 6071038ed955107220a01156550a541bf68d0266
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2020
ms.locfileid: "89241356"
---
# <a name="release-notes"></a><span data-ttu-id="c24d7-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="c24d7-103">Release notes</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="c24d7-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="6130---november-2018"></a><span data-ttu-id="c24d7-105">6.13.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-105">6.13.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-106">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-107">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c24d7-107">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c24d7-108">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c24d7-108">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c24d7-109">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c24d7-109">Update dependencies for type mapping issue</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c24d7-110">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c24d7-110">AzureRM.Automation</span></span>
* <span data-ttu-id="c24d7-111">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="c24d7-111">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="c24d7-112">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="c24d7-112">Added Update Management cmdlets</span></span>
* <span data-ttu-id="c24d7-113">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="c24d7-113">Added Source Control cmdlets</span></span>
* <span data-ttu-id="c24d7-114">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="c24d7-114">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="c24d7-115">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="c24d7-115">Fixed the DSC Register Node command</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-116">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-117">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="c24d7-117">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="c24d7-118">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c24d7-118">Update dependencies for type mapping issue</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c24d7-119">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-119">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c24d7-120">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c24d7-120">Update dependencies for type mapping issue</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c24d7-121">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c24d7-121">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c24d7-122">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="c24d7-122">update the examples description for marketplace cmdlets</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-123">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-123">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-124">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="c24d7-124">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="c24d7-125">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="c24d7-125">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="c24d7-126">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-126">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="c24d7-127">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c24d7-127">Fix issues with memory usage in VirtualNetwork map</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c24d7-128">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-128">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c24d7-129">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="c24d7-129">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="c24d7-130">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="c24d7-130">Converted policy timezone to uppercase.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c24d7-131">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c24d7-131">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c24d7-132">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="c24d7-132">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="c24d7-133">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="c24d7-133">Update dependencies for type mapping issue</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c24d7-134">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c24d7-134">AzureRM.Relay</span></span>
* <span data-ttu-id="c24d7-135">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c24d7-135">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-136">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-136">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-137">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="c24d7-137">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="c24d7-138">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="c24d7-138">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="c24d7-139">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="c24d7-139">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c24d7-140">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-140">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c24d7-141">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="c24d7-141">Add deprecation messages for upcoming breaking changes</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-142">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-142">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-143">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="c24d7-143">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="c24d7-144">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-144">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c24d7-145">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-145">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c24d7-146">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-146">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c24d7-147">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-147">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="c24d7-148">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-148">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c24d7-149">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-149">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c24d7-150">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-150">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="c24d7-151">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-151">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="c24d7-152">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="c24d7-152">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="c24d7-153">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="c24d7-153">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="c24d7-154">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="c24d7-154">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="c24d7-155">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c24d7-155">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c24d7-156">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="c24d7-156">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="c24d7-157">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c24d7-157">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="c24d7-158">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="c24d7-158">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="c24d7-159">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-159">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="6120---november-2018"></a><span data-ttu-id="c24d7-160">6.12.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-160">6.12.0 - November 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-161">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-162">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c24d7-162">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="c24d7-163">Parametro TenantId nel cmdlet Connect-AzureRmAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="c24d7-163">Rename param TenantId in cmdlet Connect-AzureRmAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="c24d7-164">Aggiornamento della descrizione di TenantId per Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c24d7-164">Updated TenantId description for Connect-AzureRmAccount</span></span>
* <span data-ttu-id="c24d7-165">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="c24d7-165">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="c24d7-166">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="c24d7-166">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="c24d7-167">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="c24d7-167">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="c24d7-168">Risoluzione del problema per il quale 'Disconnect-AzureRmAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="c24d7-168">Fix issue where 'Disconnect-AzureRmAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azurermautomation"></a><span data-ttu-id="c24d7-169">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c24d7-169">AzureRM.Automation</span></span>
* <span data-ttu-id="c24d7-170">Cmdlet DLL filename rinominato in Microsoft.Azure.Commands.Automation.dll</span><span class="sxs-lookup"><span data-stu-id="c24d7-170">Renamed cmdlet DLL filename to Microsoft.Azure.Commands.Automation.dll</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c24d7-171">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-171">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c24d7-172">Aggiunta dell'operazione Get-AzureRmCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="c24d7-172">Add Get-AzureRmCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-173">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-173">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-174">Aggiunta dei cmdlet Add-AzureRmVmssVMDataDisk e Remove-AzureRmVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="c24d7-174">Add Add-AzureRmVmssVMDataDisk and Remove-AzureRmVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="c24d7-175">Get-AzureRmVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="c24d7-175">Get-AzureRmVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="c24d7-176">Correzione dei valori di opzione di SetAzureRmVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="c24d7-176">Fixed SetAzureRmVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-177">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-177">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-178">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="c24d7-178">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="c24d7-179">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="c24d7-179">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c24d7-180">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-180">AzureRM.Insights</span></span>
* <span data-ttu-id="c24d7-181">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="c24d7-181">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="c24d7-182">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="c24d7-182">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="c24d7-183">Correzione del problema numero 7513 [Insights] per il quale Set-AzureRMDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-183">Fixed issue #7513 [Insights] Set-AzureRMDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="c24d7-184">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="c24d7-184">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-185">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-185">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-186">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c24d7-186">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="c24d7-187">Get-AzureRmExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-187">Get-AzureRmExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="c24d7-188">Get-AzureRmExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-188">Get-AzureRmExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="c24d7-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c24d7-189">Get-AzureRmExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="c24d7-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-190">Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c24d7-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-191">Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c24d7-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c24d7-192">Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c24d7-193">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-193">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c24d7-194">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="c24d7-194">Added policy remediation cmdlets</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c24d7-195">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-195">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c24d7-196">Aggiunta del supporto per le condivisioni di File di Azure nei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c24d7-196">Added support for azure file shares in recovery services.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-197">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-197">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-198">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="c24d7-198">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="c24d7-199">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c24d7-199">Allow listing resources using the '-ResourceId' parameter for 'Get-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-200">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-200">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-201">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-201">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c24d7-202">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-202">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c24d7-203">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="c24d7-203">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="c24d7-204">Correzione di 'Add-AzureRmServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="c24d7-204">Fix 'Add-AzureRmServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="c24d7-205">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="c24d7-205">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="c24d7-206">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="c24d7-206">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="c24d7-207">Correzione di 'Update-AzureRmServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="c24d7-207">Fix 'Update-AzureRmServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="6110---october-2018"></a><span data-ttu-id="c24d7-208">6.11.0 - ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-208">6.11.0 - October 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-209">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-209">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-210">Risoluzione del problema con Get-AzureRmSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="c24d7-210">Fix issue with Get-AzureRmSubscription in CloudShell</span></span>
* <span data-ttu-id="c24d7-211">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="c24d7-211">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c24d7-212">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-212">AzureRM.Backup</span></span>
* <span data-ttu-id="c24d7-213">Cmdlet di Backup di Azure deprecati.</span><span class="sxs-lookup"><span data-stu-id="c24d7-213">Deprecated Azure Backup cmdlets.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-214">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-214">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-215">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzureRmVm'.</span><span class="sxs-lookup"><span data-stu-id="c24d7-215">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzureRmVm'</span></span>
* <span data-ttu-id="c24d7-216">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c24d7-216">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-217">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-217">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-218">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="c24d7-218">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="c24d7-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c24d7-219">Get-AzureRmDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="c24d7-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c24d7-220">Add-AzureRmDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c24d7-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="c24d7-221">Set-AzureRmDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="c24d7-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c24d7-222">Remove-AzureRmDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-223">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-223">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-224">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="c24d7-224">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="c24d7-225">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c24d7-225">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-226">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-226">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-227">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzureRMRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="c24d7-227">Fix isssue where Get-AzureRMRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="c24d7-228">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="c24d7-228">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="6100---october-2018"></a><span data-ttu-id="c24d7-229">6.10.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-229">6.10.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="c24d7-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-230">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-231">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-231">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="c24d7-232">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="c24d7-232">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="c24d7-233">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="c24d7-233">Start-AzureStorageFileCopy</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c24d7-234">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-234">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c24d7-235">Supporto di Get-AzureRmCognitiveServicesAccountSkus senza un account esistente</span><span class="sxs-lookup"><span data-stu-id="c24d7-235">Support Get-AzureRmCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-236">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-236">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-237">Correzione di Get-AzureRmVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="c24d7-237">Fix Get-AzureRmVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="c24d7-238">Aggiunta di un esempio di SimpleParameterSet alla Guida del cmdlet New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-238">Added an example of the 'SimpleParameterSet' to New-AzureRmVmss cmdlet help.</span></span>
* <span data-ttu-id="c24d7-239">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="c24d7-239">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c24d7-240">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c24d7-240">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c24d7-241">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="c24d7-241">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-242">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-242">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-243">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-243">Added NetworkProfile functionality.</span></span> <span data-ttu-id="c24d7-244">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24d7-244">new cmdlets added</span></span>
    - <span data-ttu-id="c24d7-245">Get-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-245">Get-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c24d7-246">New-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-246">New-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c24d7-247">Remove-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-247">Remove-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c24d7-248">Set-AzureRMNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-248">Set-AzureRMNetworkProfile</span></span>
    - <span data-ttu-id="c24d7-249">New-AzureRMContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-249">New-AzureRMContainerNicConfig</span></span>
    - <span data-ttu-id="c24d7-250">New-AzureRmContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-250">New-AzureRmContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="c24d7-251">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-251">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="c24d7-252">Aggiunta dei cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap e Remove-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c24d7-252">Added cmdlet New-AzureRmVirtualNetworkTap, Get-AzureRmVirtualNetworkTap, Set-AzureRmVirtualNetworkTap, Remove-AzureRmVirtualNetworkTap</span></span>
* <span data-ttu-id="c24d7-253">Aggiunta dei cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig e Remove-AzureRmNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-253">Added cmdlet Set-AzureRmNEtworkInterfaceTapConfig, Get-AzureRmNEtworkInterfaceTapConfig, Remove-AzureRmNEtworkInterfaceTapConfig</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c24d7-254">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c24d7-254">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c24d7-255">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="c24d7-255">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="c24d7-256">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="c24d7-256">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-257">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-257">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-258">Aggiunta del parametro -Mode mancante a Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c24d7-258">Add missing -Mode parameter to Set-AzureRmPolicyDefinition</span></span>
* <span data-ttu-id="c24d7-259">Correzione del bug del cmdlet Get-AzureRmProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="c24d7-259">Fix Get-AzureRmProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-260">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-260">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-261">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="c24d7-261">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c24d7-262">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-262">AzureRM.Storage</span></span>
* <span data-ttu-id="c24d7-263">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="c24d7-263">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="c24d7-264">Get-AzureRmStorageUsage</span><span class="sxs-lookup"><span data-stu-id="c24d7-264">Get-AzureRmStorageUsage</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-265">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-265">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-266">Nuovo cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="c24d7-266">New Cmdlet Get-AzureRMWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="c24d7-267">Nuovi cmdlet New-AzureRMWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c24d7-267">New Cmdlets New-AzureRMWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="690---september-2018"></a><span data-ttu-id="c24d7-268">6.9.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-268">6.9.0 - September 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c24d7-269">Generale</span><span class="sxs-lookup"><span data-stu-id="c24d7-269">General</span></span>
* <span data-ttu-id="c24d7-270">Aggiunta di AzureRM.SignalR al modulo di rollup AzureRM</span><span class="sxs-lookup"><span data-stu-id="c24d7-270">AzureRM.SignalR was added to the AzureRM rollup module</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-271">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-271">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-272">Modifiche minori al codice comune di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-272">Minor changes to the storage common code</span></span>
* <span data-ttu-id="c24d7-273">Aggiornamento dei file della Guida per includere tipi di parametri completi.</span><span class="sxs-lookup"><span data-stu-id="c24d7-273">Updated help files to include full parameter types.</span></span>
* <span data-ttu-id="c24d7-274">Modifica di -ServicePrincipal in non obbligatorio nel set di parametri ServicePrincipalCertificateWithSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c24d7-274">Changed -ServicePrincipal to non-mandatory in the ServicePrincipalCertificateWithSubscriptionId parameter set</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c24d7-275">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-275">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-276">Supporto della creazione del contesto di archiviazione con OAuth.</span><span class="sxs-lookup"><span data-stu-id="c24d7-276">Support create Storage Context with OAuth.</span></span>
    - <span data-ttu-id="c24d7-277">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="c24d7-277">New-AzureStorageContext</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c24d7-278">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c24d7-278">AzureRM.Cdn</span></span>
* <span data-ttu-id="c24d7-279">Aggiunta di Standard_Microsoft nello SKU del piano tariffario per la rete CDN.</span><span class="sxs-lookup"><span data-stu-id="c24d7-279">Added Standard_Microsoft in Cdn pricing sku.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-280">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-280">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-281">Trasferimento delle dipendenze da Key Vault e Archiviazione a dipendenze comuni</span><span class="sxs-lookup"><span data-stu-id="c24d7-281">Move dependencies on Keyvault and Storage to the common dependencies</span></span>
* <span data-ttu-id="c24d7-282">Aggiunta del supporto per altre dimensioni delle macchine virtuali ai cmdlet AEM</span><span class="sxs-lookup"><span data-stu-id="c24d7-282">Add support for more virutal machine sizes to AEM cmdlets</span></span>
* <span data-ttu-id="c24d7-283">Aggiunta del parametro PublicIPPrefix a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-283">Add PublicIPPrefix parameter to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c24d7-284">Aggiunta del parametro ResourceId a Invoke-AzureRmVMRunCommand cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24d7-284">Add ResourceId parameter to Invoke-AzureRmVMRunCommand cmdelt</span></span>
* <span data-ttu-id="c24d7-285">Aggiunta del cmdlet Invoke-AzureRmVmVmssVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c24d7-285">Add Invoke-AzureRmVmssVMRunCommand cmdlet</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c24d7-286">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c24d7-286">AzureRM.Dns</span></span>
* <span data-ttu-id="c24d7-287">Aggiunta del supporto per record alias durante la creazione del record DNS</span><span class="sxs-lookup"><span data-stu-id="c24d7-287">Added support for alias record during dns record creation</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c24d7-288">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-288">AzureRM.Insights</span></span>
* <span data-ttu-id="c24d7-289">Risoluzione dei problemi 6833 e 7102 (area Impostazioni di diagnostica)</span><span class="sxs-lookup"><span data-stu-id="c24d7-289">Fixed issues #6833 and #7102 (Diagnostic Settings area)</span></span>
    - <span data-ttu-id="c24d7-290">Problemi con il nome predefinito, ovvero 'service', durante la creazione e l'elencazione/ottenimento delle impostazioni di diagnostica</span><span class="sxs-lookup"><span data-stu-id="c24d7-290">Issues with the default name, i.e. 'service', during creation and listing/getting of diagnostic settings</span></span>
    - <span data-ttu-id="c24d7-291">Problemi nella creazione di impostazioni di diagnostica con categorie</span><span class="sxs-lookup"><span data-stu-id="c24d7-291">Issues creating diagnostic settings with categories</span></span>
* <span data-ttu-id="c24d7-292">Aggiunta del messaggio di funzione deprecata per i parametri degli intervalli di tempo delle metriche</span><span class="sxs-lookup"><span data-stu-id="c24d7-292">Added deprecation message for metrics time grains parameters</span></span>
    - <span data-ttu-id="c24d7-293">I parametri timegrains vengono ancora accettati (si tratta di una modifica che non causa interruzioni), ma vengono ignorati nel back-end perché solo PT1M è valido</span><span class="sxs-lookup"><span data-stu-id="c24d7-293">Timegrains parameters are still being accepted (this is a non-breaking change,) but they are ignored in the backend since only PT1M is valid</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-294">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-295">Modifiche ai cmdlet LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c24d7-295">Changes to LoadBalancer cmdlets</span></span>
  - <span data-ttu-id="c24d7-296">LoadBalancerInboundNatPoolConfig: aggiunta dei parametri IdleTimeoutInMinutes, EnableFloatingIp ed EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c24d7-296">LoadBalancerInboundNatPoolConfig: added parameters IdleTimeoutInMinutes, EnableFloatingIp and EnableTcpReset</span></span>
  - <span data-ttu-id="c24d7-297">LoadBalancerInboundNatRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c24d7-297">LoadBalancerInboundNatRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c24d7-298">LoadBalancerRuleConfig: aggiunta del parametro EnableTcpReset</span><span class="sxs-lookup"><span data-stu-id="c24d7-298">LoadBalancerRuleConfig: added parameter EnableTcpReset</span></span>
  - <span data-ttu-id="c24d7-299">LoadBalancerProbeConfig: aggiunta del supporto del valore "Https" per il parametro Protocol</span><span class="sxs-lookup"><span data-stu-id="c24d7-299">LoadBalancerProbeConfig: added support for value "Https" for parameter Protocol</span></span>
* <span data-ttu-id="c24d7-300">Aggiunta di nuovi comandi per la nuova OutboundRule delle sottorisorse di LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c24d7-300">Added new commands for new LoadBalancer's subresource OutboundRule</span></span>
  - <span data-ttu-id="c24d7-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-301">Add-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c24d7-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-302">Get-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c24d7-303">New-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-303">New-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c24d7-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-304">Set-AzureRmLoadBalancerOutboundRuleConfig</span></span>
  - <span data-ttu-id="c24d7-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-305">Remove-AzureRmLoadBalancerOutboundRuleConfig</span></span>
* <span data-ttu-id="c24d7-306">Aggiunta della nuova proprietà HostedWorkloads per PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c24d7-306">Added new HostedWorkloads property for PSNetworkInterface</span></span>
* <span data-ttu-id="c24d7-307">Aggiunta di nuovi cmdlet per la funzionalità: Firewall di Azure tramite Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="c24d7-307">Added new cmdlets for feature: Azure Firewall via ARM</span></span>
  - <span data-ttu-id="c24d7-308">Aggiunta di Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c24d7-308">Added Get-AzureRmFirewall</span></span>
  - <span data-ttu-id="c24d7-309">Aggiunta di Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c24d7-309">Added Set-AzureRmFirewall</span></span>
  - <span data-ttu-id="c24d7-310">Aggiunta di New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c24d7-310">Added New-AzureRmFirewall</span></span>
  - <span data-ttu-id="c24d7-311">Aggiunta di Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="c24d7-311">Added Remove-AzureRmFirewall</span></span>
  - <span data-ttu-id="c24d7-312">Aggiunta di New-AzureRmFirewallApplicationRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c24d7-312">Added New-AzureRmFirewallApplicationRuleCollection</span></span>
  - <span data-ttu-id="c24d7-313">Aggiunta di New-AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="c24d7-313">Added New-AzureRmFirewallApplicationRule</span></span>
  - <span data-ttu-id="c24d7-314">Aggiunta di New-AzureRmFirewallNatRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c24d7-314">Added New-AzureRmFirewallNatRuleCollection</span></span>
  - <span data-ttu-id="c24d7-315">Aggiunta di New-AzureRmFirewallNatRule</span><span class="sxs-lookup"><span data-stu-id="c24d7-315">Added New-AzureRmFirewallNatRule</span></span>
  - <span data-ttu-id="c24d7-316">Aggiunta di New-AzureRmFirewallNetworkRuleCollection</span><span class="sxs-lookup"><span data-stu-id="c24d7-316">Added New-AzureRmFirewallNetworkRuleCollection</span></span>
  - <span data-ttu-id="c24d7-317">Aggiunta di New-AzureRmFirewallNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c24d7-317">Added New-AzureRmFirewallNetworkRule</span></span>
* <span data-ttu-id="c24d7-318">Aggiunta del supporto per il certificato radice attendibile e la configurazione della scalabilità automatica nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-318">Added support for Trusted Root certificate and Autoscale configuration in Application Gateway</span></span>
  - <span data-ttu-id="c24d7-319">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c24d7-319">New Cmdlets added:</span></span>
      - <span data-ttu-id="c24d7-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-320">Add-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-321">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-322">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-323">Remove-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-324">Set-AzureRmApplicationGatewayTrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-325">Get-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c24d7-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-326">New-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c24d7-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-327">Remove-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
      - <span data-ttu-id="c24d7-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-328">Set-AzureRmApplicationGatewayAutoscaleConfiguration</span></span>
  - <span data-ttu-id="c24d7-329">Aggiornamento dei cmdlet con il parametro facoltativo -TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-329">Cmdlets updated with optonal parameter -TrustedRootCertificate</span></span>
      - <span data-ttu-id="c24d7-330">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-330">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c24d7-331">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-331">Set-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c24d7-332">New-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c24d7-332">New-AzureRmApplicationGatewayBackendHttpSetting</span></span>
      - <span data-ttu-id="c24d7-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="c24d7-333">Set-AzureRmApplicationGatewayBackendHttpSetting</span></span>
  - <span data-ttu-id="c24d7-334">Aggiornamento dei cmdlet con il parametro facoltativo -AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-334">Cmdlets updated with optonal parameter -AutoscaleConfiguration</span></span>
      - <span data-ttu-id="c24d7-335">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-335">New-AzureRmApplicationGateway</span></span>
      - <span data-ttu-id="c24d7-336">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-336">Set-AzureRmApplicationGateway</span></span>
* <span data-ttu-id="c24d7-337">Aggiunta di un cmdlet per l'endpoint di interfaccia Get-AzureInterfaceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-337">Add cmdlet for Interface Endpoint Get-AzureInterfaceEndpoint</span></span>
* <span data-ttu-id="c24d7-338">Aggiunta del supporto per più prefissi di indirizzi in una sottorete.</span><span class="sxs-lookup"><span data-stu-id="c24d7-338">Added support for multiple address prefixes in a subnet.</span></span> <span data-ttu-id="c24d7-339">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c24d7-339">Updated cmdlets:</span></span>
  - <span data-ttu-id="c24d7-340">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-340">New-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c24d7-341">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-341">Set-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c24d7-342">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-342">Add-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c24d7-343">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-343">Get-AzureRmVirtualNetworkSubnetConfig</span></span>
  - <span data-ttu-id="c24d7-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-344">Add-AzureRmApplicationGatewayAuthenticationCertificate</span></span>
  - <span data-ttu-id="c24d7-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-345">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c24d7-346">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-346">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c24d7-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-347">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>
  - <span data-ttu-id="c24d7-348">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-348">Add-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c24d7-349">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-349">New-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c24d7-350">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-350">Set-AzureRmApplicationGatewayIPConfiguration</span></span>
  - <span data-ttu-id="c24d7-351">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-351">Add-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c24d7-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-352">New-AzureRmNetworkInterfaceIpConfig  - Set-AzureRmNetworkInterfaceIpConfig</span></span>
  - <span data-ttu-id="c24d7-353">New-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-353">New-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c24d7-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-354">Add-AzureRmVirtualNetworkGatewayIpConfig</span></span>
  - <span data-ttu-id="c24d7-355">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-355">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c24d7-356">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-356">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c24d7-357">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-357">New-AzureRmLoadBalancerFrontendIpConfig</span></span>
  - <span data-ttu-id="c24d7-358">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c24d7-358">New-AzureRmNetworkInterface</span></span>
* <span data-ttu-id="c24d7-359">Aggiunta di cmdlet per la delega di subnet.</span><span class="sxs-lookup"><span data-stu-id="c24d7-359">Adding cmdlets for subnet delegation.</span></span>
  - <span data-ttu-id="c24d7-360">New-AzureRmDelegation: Crea una nuova delega che può essere aggiunta a una subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-360">New-AzureRmDelegation: Creates a new delegation, which can be added to a subnet</span></span>
  - <span data-ttu-id="c24d7-361">Remove-AzureRmDelegation: Acquisisce una subnet e rimuove il nome di delega fornito da tale subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-361">Remove-AzureRmDelegation: Takes in a subnet and removes the provided delegation name from that subnet</span></span>
  - <span data-ttu-id="c24d7-362">Add-AzureRmDelegation: Acquisisce una subnet e aggiunge il nome servizio specificato come delega a tale subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-362">Add-AzureRmDelegation: Takes in a subnet and adds the provided service name as a delegation to that subnet</span></span>
  - <span data-ttu-id="c24d7-363">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="c24d7-363">Get-AzureRmDelegation</span></span>
  - <span data-ttu-id="c24d7-364">Get-AzureRmAvailableServiceDelegations</span><span class="sxs-lookup"><span data-stu-id="c24d7-364">Get-AzureRmAvailableServiceDelegations</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c24d7-365">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c24d7-365">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c24d7-366">Supporto per dischi gestiti</span><span class="sxs-lookup"><span data-stu-id="c24d7-366">Support for managed Managed disk</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c24d7-367">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c24d7-367">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c24d7-368">Aggiornamento della dipendenza di Insights.</span><span class="sxs-lookup"><span data-stu-id="c24d7-368">Updated Insights dependency.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-369">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-369">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-370">Aggiornamento di New-AzureRmResourceGroupDeployment con il nuovo parametro RollbackAction</span><span class="sxs-lookup"><span data-stu-id="c24d7-370">Update New-AzureRmResourceGroupDeployment with new parameter RollbackAction</span></span>
    - <span data-ttu-id="c24d7-371">Aggiunta del supporto per OnErrorDeployment con il nuovo parametro.</span><span class="sxs-lookup"><span data-stu-id="c24d7-371">Add support for OnErrorDeployment with the new parameter.</span></span>
* <span data-ttu-id="c24d7-372">Supporto dell'identità gestita per le assegnazioni dei criteri.</span><span class="sxs-lookup"><span data-stu-id="c24d7-372">Support managed identity on policy assignments.</span></span>
* <span data-ttu-id="c24d7-373">Non sono più necessari parametri con valori predefiniti durante l'assegnazione di criteri con 'New-AzureRmPolicyAssignment'</span><span class="sxs-lookup"><span data-stu-id="c24d7-373">Parameters with default values are no longer requred when assigning a policy with 'New-AzureRmPolicyAssignment'</span></span>
* <span data-ttu-id="c24d7-374">Aggiunta del nuovo cmdlet Get-AzureRmPolicyAlias per il recupero di alias dei criteri</span><span class="sxs-lookup"><span data-stu-id="c24d7-374">Add new cmdlet Get-AzureRmPolicyAlias for retrieving policy aliases</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-375">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-375">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-376">Risoluzione del problema #7161</span><span class="sxs-lookup"><span data-stu-id="c24d7-376">Fixed issue #7161</span></span>

#### <a name="azurermsignalr"></a><span data-ttu-id="c24d7-377">AzureRM.SignalR</span><span class="sxs-lookup"><span data-stu-id="c24d7-377">AzureRM.SignalR</span></span>
* <span data-ttu-id="c24d7-378">Aggiornamento dei nomi SKU in Free_F1 e Standard_S1</span><span class="sxs-lookup"><span data-stu-id="c24d7-378">Update SKU names to Free_F1 and Standard_S1</span></span>
* <span data-ttu-id="c24d7-379">Aggiunta del campo di versione all'oggetto PSSignalRResource e della stringa di connessione all'oggetto PSSignalRKeys.</span><span class="sxs-lookup"><span data-stu-id="c24d7-379">Add version field to the PSSignalRResource object and connection string to the PSSignalRKeys object.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c24d7-380">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-380">AzureRM.Storage</span></span>
* <span data-ttu-id="c24d7-381">Supporto dei criteri di immutabilità in AzureRm.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-381">Support Immutability Policy in AzureRm.Storage</span></span>
    - <span data-ttu-id="c24d7-382">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c24d7-382">Remove-AzureRmStorageAccountNetworkRule</span></span>
    - <span data-ttu-id="c24d7-383">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c24d7-383">Get-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c24d7-384">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c24d7-384">Update-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c24d7-385">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c24d7-385">New-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c24d7-386">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c24d7-386">Remove-AzureRmStorageContainer</span></span>
    - <span data-ttu-id="c24d7-387">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c24d7-387">Add-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c24d7-388">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="c24d7-388">Remove-AzureRmStorageContainerLegalHold</span></span>
    - <span data-ttu-id="c24d7-389">Set-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-389">Set-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c24d7-390">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-390">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c24d7-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-391">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>
    - <span data-ttu-id="c24d7-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-392">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-393">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-393">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-394">Aggiunta di due nuovi cmdlet: Get-AzureRmDeletedWebApp e Restore-AzureRmDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="c24d7-394">Added two new cmdlets: Get-AzureRmDeletedWebApp and Restore-AzureRmDeletedWebApp</span></span>
* <span data-ttu-id="c24d7-395">New-AzureRmAppServicePlan - Aggiunta dello switch HyperV per la creazione di un piano del servizio app con il contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c24d7-395">New-AzureRmAppServicePlan -HyperV switch is added for create app service plan with windows container</span></span>
* <span data-ttu-id="c24d7-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - Aggiunta di nuovi parametri (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) per la creazione e la gestione di app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="c24d7-396">New-AzureRmWebApp/ New-AzureRmWebAppSlot/ Set-AzureRmWebApp/ Set-AzureRmWebAppSlot - New parameters (–ContainerRegistryUser string -ContainerRegistryPassword secureString -EnableContainerContinuousDeployment) added for creating and managing windows container app</span></span>

## <a name="681---august-2018"></a><span data-ttu-id="c24d7-397">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-397">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c24d7-398">Generale</span><span class="sxs-lookup"><span data-stu-id="c24d7-398">General</span></span>
* <span data-ttu-id="c24d7-399">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-399">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c24d7-400">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="c24d7-400">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c24d7-401">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c24d7-401">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c24d7-402">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-402">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c24d7-403">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="c24d7-403">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="c24d7-404">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="c24d7-404">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="c24d7-405">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="c24d7-405">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="c24d7-406">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c24d7-406">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="c24d7-407">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="c24d7-407">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="c24d7-408">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="c24d7-408">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="c24d7-409">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="c24d7-409">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="c24d7-410">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="c24d7-410">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="c24d7-411">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="c24d7-411">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="c24d7-412">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="c24d7-412">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-413">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-413">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-414">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c24d7-414">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c24d7-415">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="c24d7-415">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c24d7-416">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-416">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="c24d7-417">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="c24d7-417">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-418">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-418">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-419">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24d7-419">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c24d7-420">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c24d7-420">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c24d7-421">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="c24d7-421">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="c24d7-422">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-422">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-423">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c24d7-423">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-424">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-424">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-425">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="c24d7-425">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c24d7-426">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c24d7-426">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c24d7-427">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c24d7-427">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c24d7-428">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c24d7-428">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c24d7-429">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-429">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c24d7-430">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-430">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c24d7-431">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="c24d7-431">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c24d7-432">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="c24d7-432">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c24d7-433">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-433">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="c24d7-434">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-434">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c24d7-435">Generale</span><span class="sxs-lookup"><span data-stu-id="c24d7-435">General</span></span>
* <span data-ttu-id="c24d7-436">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-436">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-437">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-438">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c24d7-438">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-439">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-439">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-440">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="c24d7-440">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="c24d7-441">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="c24d7-441">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="c24d7-442">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="c24d7-442">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c24d7-443">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-443">AzureRM.IotHub</span></span>
* <span data-ttu-id="c24d7-444">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="c24d7-444">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-445">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-445">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-446">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="c24d7-446">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c24d7-447">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c24d7-447">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c24d7-448">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="c24d7-448">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-449">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-449">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-450">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="c24d7-450">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-451">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-451">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-452">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="c24d7-452">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c24d7-453">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c24d7-453">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c24d7-454">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c24d7-454">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="c24d7-455">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="c24d7-455">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="c24d7-456">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="c24d7-456">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="c24d7-457">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-457">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="c24d7-458">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="c24d7-458">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="c24d7-459">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="c24d7-459">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="c24d7-460">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-460">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-461">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-461">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-462">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="c24d7-462">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="c24d7-463">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-463">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-464">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-464">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-465">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-465">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c24d7-466">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="c24d7-466">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="c24d7-467">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="c24d7-467">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="c24d7-468">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="c24d7-468">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="c24d7-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-469">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-470">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="c24d7-470">Remove the 5TB limitation for Azure File Share quota</span></span>
* <span data-ttu-id="c24d7-471">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="c24d7-471">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c24d7-472">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-472">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c24d7-473">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-473">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="c24d7-474">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-474">Azure.AnalysisServices</span></span>
* <span data-ttu-id="c24d7-475">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-475">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c24d7-476">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c24d7-476">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c24d7-477">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-477">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="c24d7-478">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-478">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="c24d7-479">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-479">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c24d7-480">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c24d7-480">AzureRM.Automation</span></span>
* <span data-ttu-id="c24d7-481">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-481">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="c24d7-482">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-482">AzureRM.Backup</span></span>
* <span data-ttu-id="c24d7-483">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-483">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c24d7-484">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c24d7-484">AzureRM.Batch</span></span>
* <span data-ttu-id="c24d7-485">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-485">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="c24d7-486">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="c24d7-486">AzureRM.Billing</span></span>
* <span data-ttu-id="c24d7-487">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-487">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="c24d7-488">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="c24d7-488">AzureRM.Cdn</span></span>
* <span data-ttu-id="c24d7-489">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-489">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="c24d7-490">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-490">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="c24d7-491">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-491">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-492">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-493">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-493">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c24d7-494">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-494">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="c24d7-495">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-495">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="c24d7-496">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c24d7-496">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c24d7-497">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="c24d7-497">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c24d7-498">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c24d7-498">AzureRM.Consumption</span></span>
* <span data-ttu-id="c24d7-499">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-499">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="c24d7-500">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="c24d7-500">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="c24d7-501">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-501">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="c24d7-502">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c24d7-502">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="c24d7-503">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-503">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="c24d7-504">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="c24d7-504">AzureRM.DataFactories</span></span>
* <span data-ttu-id="c24d7-505">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-505">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c24d7-506">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c24d7-506">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c24d7-507">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-507">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c24d7-508">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c24d7-508">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c24d7-509">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-509">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-510">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-510">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-511">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="c24d7-511">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="c24d7-512">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c24d7-512">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c24d7-513">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-513">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c24d7-514">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-514">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="c24d7-515">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="c24d7-515">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="c24d7-516">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-516">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="c24d7-517">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="c24d7-517">AzureRM.Dns</span></span>
* <span data-ttu-id="c24d7-518">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-518">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c24d7-519">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c24d7-519">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c24d7-520">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-520">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c24d7-521">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-521">AzureRM.EventHub</span></span>
* <span data-ttu-id="c24d7-522">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-522">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="c24d7-523">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="c24d7-523">AzureRM.HDInsight</span></span>
* <span data-ttu-id="c24d7-524">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-524">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c24d7-525">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-525">AzureRM.Insights</span></span>
* <span data-ttu-id="c24d7-526">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-526">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="c24d7-527">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-527">AzureRM.IotHub</span></span>
* <span data-ttu-id="c24d7-528">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-528">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-529">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-529">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-530">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-530">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c24d7-531">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c24d7-531">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c24d7-532">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-532">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="c24d7-533">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="c24d7-533">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="c24d7-534">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-534">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="c24d7-535">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="c24d7-535">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="c24d7-536">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-536">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="c24d7-537">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="c24d7-537">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="c24d7-538">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-538">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="c24d7-539">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="c24d7-539">AzureRM.Media</span></span>
* <span data-ttu-id="c24d7-540">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-540">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-541">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-541">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-542">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-542">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="c24d7-543">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c24d7-543">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c24d7-544">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c24d7-544">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="c24d7-545">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c24d7-545">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c24d7-546">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="c24d7-546">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="c24d7-547">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="c24d7-547">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="c24d7-548">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="c24d7-548">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="c24d7-549">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="c24d7-549">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="c24d7-550">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="c24d7-550">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="c24d7-551">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-551">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="c24d7-552">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-552">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c24d7-553">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-553">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c24d7-554">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-554">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c24d7-555">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-555">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="c24d7-556">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="c24d7-556">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="c24d7-557">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-557">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="c24d7-558">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-558">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="c24d7-559">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-559">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c24d7-560">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-560">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c24d7-561">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="c24d7-561">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="c24d7-562">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="c24d7-562">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="c24d7-563">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="c24d7-563">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="c24d7-564">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-564">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="c24d7-565">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="c24d7-565">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="c24d7-566">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-566">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="c24d7-567">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="c24d7-567">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="c24d7-568">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="c24d7-568">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="c24d7-569">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-569">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="c24d7-570">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="c24d7-570">AzureRM.RedisCache</span></span>
* <span data-ttu-id="c24d7-571">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-571">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c24d7-572">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c24d7-572">AzureRM.Relay</span></span>
* <span data-ttu-id="c24d7-573">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-573">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-574">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-574">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-575">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-575">Support template deployment at subscription scope.</span></span> <span data-ttu-id="c24d7-576">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="c24d7-576">Add new Cmdlets:</span></span>
    - <span data-ttu-id="c24d7-577">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-577">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="c24d7-578">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-578">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="c24d7-579">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-579">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="c24d7-580">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-580">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="c24d7-581">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-581">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="c24d7-582">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="c24d7-582">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="c24d7-583">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="c24d7-583">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="c24d7-584">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="c24d7-584">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="c24d7-585">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-585">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="c24d7-586">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-586">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c24d7-587">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c24d7-587">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c24d7-588">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-588">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-589">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-589">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-590">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-590">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c24d7-591">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-591">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c24d7-592">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-592">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-593">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-593">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-594">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-594">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c24d7-595">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-595">AzureRM.Storage</span></span>
* <span data-ttu-id="c24d7-596">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-596">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="c24d7-597">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="c24d7-597">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="c24d7-598">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-598">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c24d7-599">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c24d7-599">AzureRM.Tags</span></span>
* <span data-ttu-id="c24d7-600">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-600">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c24d7-601">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c24d7-601">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c24d7-602">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-602">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="c24d7-603">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="c24d7-603">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="c24d7-604">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-604">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-605">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-605">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-606">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="c24d7-606">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="c24d7-607">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-607">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c24d7-608">Generale</span><span class="sxs-lookup"><span data-stu-id="c24d7-608">General</span></span>
* <span data-ttu-id="c24d7-609">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="c24d7-609">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-610">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-610">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-611">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-611">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="c24d7-612">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-612">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c24d7-613">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-613">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-614">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24d7-614">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="c24d7-615">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c24d7-615">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c24d7-616">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c24d7-616">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c24d7-617">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="c24d7-617">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="c24d7-618">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="c24d7-618">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="c24d7-619">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="c24d7-619">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="c24d7-620">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="c24d7-620">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="c24d7-621">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="c24d7-621">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="c24d7-622">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="c24d7-622">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-623">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-623">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-624">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="c24d7-624">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="c24d7-625">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="c24d7-625">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="c24d7-626">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-626">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="c24d7-627">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c24d7-627">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="c24d7-628">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="c24d7-628">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="c24d7-629">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="c24d7-629">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="c24d7-630">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c24d7-630">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="c24d7-631">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="c24d7-631">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="c24d7-632">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="c24d7-632">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="c24d7-633">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="c24d7-633">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c24d7-634">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c24d7-634">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c24d7-635">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="c24d7-635">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="c24d7-636">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="c24d7-636">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="c24d7-637">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c24d7-637">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="c24d7-638">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="c24d7-638">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-639">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-639">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-640">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="c24d7-640">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c24d7-641">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-641">AzureRM.EventHub</span></span>
* <span data-ttu-id="c24d7-642">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="c24d7-642">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="c24d7-643">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-643">AzureRM.Insights</span></span>
* <span data-ttu-id="c24d7-644">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="c24d7-644">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="c24d7-645">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="c24d7-645">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-646">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-646">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-647">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-647">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-648">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-648">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-649">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="c24d7-649">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-650">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-650">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-651">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c24d7-651">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="c24d7-652">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="c24d7-652">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-653">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-653">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-654">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="c24d7-654">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="c24d7-655">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="c24d7-655">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-656">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-656">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-657">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c24d7-657">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="c24d7-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-658">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="c24d7-659">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="c24d7-659">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="c24d7-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="c24d7-660">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="c24d7-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="c24d7-661">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="c24d7-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="c24d7-662">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="c24d7-663">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c24d7-663">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="c24d7-664">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="c24d7-664">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="c24d7-665">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-665">AzureRM.Storage</span></span>
* <span data-ttu-id="c24d7-666">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24d7-666">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="c24d7-667">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="c24d7-667">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="c24d7-668">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c24d7-668">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c24d7-669">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c24d7-669">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="c24d7-670">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c24d7-670">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="c24d7-671">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="c24d7-671">AzureRM.Tags</span></span>
* <span data-ttu-id="c24d7-672">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="c24d7-672">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="c24d7-673">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-673">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-674">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-674">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-675">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="c24d7-675">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c24d7-676">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-676">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-677">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="c24d7-677">Support Upload Blob or File with write only Sas token</span></span>
* <span data-ttu-id="c24d7-678">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="c24d7-678">Set-AzureStorageBlobContent</span></span>
* <span data-ttu-id="c24d7-679">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="c24d7-679">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c24d7-680">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-680">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c24d7-681">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="c24d7-681">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="c24d7-682">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="c24d7-682">AzureRM.Automation</span></span>
* <span data-ttu-id="c24d7-683">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="c24d7-683">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-684">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-684">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-685">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c24d7-685">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="c24d7-686">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="c24d7-686">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c24d7-687">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="c24d7-687">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="c24d7-688">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="c24d7-688">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="c24d7-689">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="c24d7-689">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c24d7-690">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-690">AzureRM.EventHub</span></span>
* <span data-ttu-id="c24d7-691">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="c24d7-691">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-692">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-692">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-693">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c24d7-693">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="c24d7-694">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="c24d7-694">AzureRM.LogicApp</span></span>
* <span data-ttu-id="c24d7-695">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c24d7-695">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-696">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-696">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-697">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="c24d7-697">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="c24d7-698">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="c24d7-698">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="c24d7-699">New-AzureRmApplicationGateway: Aggiunta del flag EnableFIPS e del supporto per le zone</span><span class="sxs-lookup"><span data-stu-id="c24d7-699">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="c24d7-700">New-AzureRmApplicationGatewaySku: Aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c24d7-700">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="c24d7-701">Set-AzureRmApplicationGatewaySku : Aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="c24d7-701">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="c24d7-702">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="c24d7-702">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="c24d7-703">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="c24d7-703">AzureRM.Relay</span></span>
* <span data-ttu-id="c24d7-704">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="c24d7-704">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-705">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-705">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-706">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="c24d7-706">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="c24d7-707">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="c24d7-707">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="c24d7-708">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c24d7-708">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="c24d7-709">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="c24d7-709">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="c24d7-710">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="c24d7-710">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-711">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-711">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-712">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="c24d7-712">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="c24d7-713">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="c24d7-713">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="c24d7-714">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c24d7-714">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c24d7-715">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c24d7-715">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c24d7-716">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c24d7-716">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c24d7-717">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c24d7-717">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="c24d7-718">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="c24d7-718">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="c24d7-719">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="c24d7-719">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c24d7-720">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-720">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c24d7-721">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="c24d7-721">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-722">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-722">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-723">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="c24d7-723">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="c24d7-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-724">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="c24d7-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-725">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-726">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-726">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-727">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="c24d7-727">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="c24d7-728">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="c24d7-728">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="c24d7-729">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="c24d7-729">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="c24d7-730">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-730">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="c24d7-731">Generale</span><span class="sxs-lookup"><span data-stu-id="c24d7-731">General</span></span>
* <span data-ttu-id="c24d7-732">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="c24d7-732">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-733">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-733">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-734">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="c24d7-734">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-735">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-735">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-736">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="c24d7-736">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="c24d7-737">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="c24d7-737">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="c24d7-738">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-738">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="c24d7-739">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="c24d7-739">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="c24d7-740">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-740">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="c24d7-741">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-741">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="c24d7-742">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-742">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="c24d7-743">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="c24d7-743">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="c24d7-744">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="c24d7-744">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="c24d7-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-745">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c24d7-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-746">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="c24d7-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-747">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-748">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-748">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-749">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="c24d7-749">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="c24d7-750">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c24d7-750">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c24d7-751">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="c24d7-751">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="c24d7-752">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="c24d7-752">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="c24d7-753">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="c24d7-753">AzureRM.EventHub</span></span>
* <span data-ttu-id="c24d7-754">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="c24d7-754">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="c24d7-755">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="c24d7-755">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="c24d7-756">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="c24d7-756">Provided Default Parameter set.</span></span>
* <span data-ttu-id="c24d7-757">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c24d7-757">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-758">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-758">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-759">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c24d7-759">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-760">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-760">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-761">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="c24d7-761">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="c24d7-762">Aggiunta di nuovi comandi per la funzione: API Partner ExpressRoute tramite Azure Resource Manager</span><span class="sxs-lookup"><span data-stu-id="c24d7-762">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="c24d7-763">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c24d7-763">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c24d7-764">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="c24d7-764">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="c24d7-765">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c24d7-765">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c24d7-766">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c24d7-766">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c24d7-767">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="c24d7-767">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="c24d7-768">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-768">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="c24d7-769">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="c24d7-769">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="c24d7-770">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="c24d7-770">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c24d7-771">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-771">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c24d7-772">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="c24d7-772">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="c24d7-773">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c24d7-773">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="c24d7-774">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="c24d7-774">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-775">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-775">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-776">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="c24d7-776">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="c24d7-777">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c24d7-777">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="c24d7-778">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="c24d7-778">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="c24d7-779">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="c24d7-779">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="c24d7-780">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c24d7-780">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="c24d7-781">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="c24d7-781">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c24d7-782">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="c24d7-782">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c24d7-783">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c24d7-783">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="c24d7-784">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="c24d7-784">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="c24d7-785">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="c24d7-785">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="c24d7-786">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="c24d7-786">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="c24d7-787">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="c24d7-787">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="c24d7-788">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="c24d7-788">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="c24d7-789">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c24d7-789">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="c24d7-790">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="c24d7-790">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-791">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-791">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-792">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="c24d7-792">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="c24d7-793">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="c24d7-793">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="c24d7-794">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-794">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-795">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-795">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-796">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="c24d7-796">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="c24d7-797">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="c24d7-797">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="c24d7-798">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="c24d7-798">Azure.Storage</span></span>
* <span data-ttu-id="c24d7-799">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="c24d7-799">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-800">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-800">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-801">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="c24d7-801">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span>
* <span data-ttu-id="c24d7-802">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="c24d7-802">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="c24d7-803">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c24d7-803">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c24d7-804">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c24d7-804">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c24d7-805">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c24d7-805">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="c24d7-806">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="c24d7-806">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="c24d7-807">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c24d7-807">Start-AzureRmVM</span></span>
    - <span data-ttu-id="c24d7-808">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c24d7-808">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="c24d7-809">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c24d7-809">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="c24d7-810">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="c24d7-810">Set-AzureRmVM</span></span>
    - <span data-ttu-id="c24d7-811">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="c24d7-811">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="c24d7-812">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-812">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="c24d7-813">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="c24d7-813">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="c24d7-814">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="c24d7-814">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="c24d7-815">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-815">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="c24d7-816">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-816">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="c24d7-817">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-817">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="c24d7-818">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c24d7-818">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="c24d7-819">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="c24d7-819">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="c24d7-820">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="c24d7-820">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="c24d7-821">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="c24d7-821">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="c24d7-822">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="c24d7-822">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="c24d7-823">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c24d7-823">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="c24d7-824">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c24d7-824">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="c24d7-825">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c24d7-825">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="c24d7-826">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="c24d7-826">AzureRM.EventGrid</span></span>
* <span data-ttu-id="c24d7-827">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="c24d7-827">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-828">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-828">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-829">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="c24d7-829">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="c24d7-830">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-830">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="c24d7-831">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-831">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="c24d7-832">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="c24d7-832">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="c24d7-833">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="c24d7-833">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="c24d7-834">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="c24d7-834">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="c24d7-835">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="c24d7-835">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="c24d7-836">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="c24d7-836">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-837">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-837">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-838">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="c24d7-838">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c24d7-839">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c24d7-839">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c24d7-840">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-840">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-841">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-841">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-842">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c24d7-842">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="c24d7-843">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="c24d7-843">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="c24d7-844">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-844">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="c24d7-845">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="c24d7-845">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="c24d7-846">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="c24d7-846">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="c24d7-847">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-847">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-848">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-848">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-849">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="c24d7-849">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="c24d7-850">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="c24d7-850">AzureRM.Compute</span></span>
* <span data-ttu-id="c24d7-851">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="c24d7-851">VMSS VM Update feature</span></span>
    - <span data-ttu-id="c24d7-852">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="c24d7-852">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="c24d7-853">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="c24d7-853">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="c24d7-854">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="c24d7-854">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="c24d7-855">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="c24d7-855">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="c24d7-856">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="c24d7-856">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="c24d7-857">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="c24d7-857">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="c24d7-858">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="c24d7-858">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="c24d7-859">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="c24d7-859">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="c24d7-860">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="c24d7-860">AzureRM.KeyVault</span></span>
* <span data-ttu-id="c24d7-861">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="c24d7-861">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-862">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-862">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-863">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="c24d7-863">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="c24d7-864">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="c24d7-864">AzureRM.Resources</span></span>
* <span data-ttu-id="c24d7-865">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="c24d7-865">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="c24d7-866">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="c24d7-866">AzureRM.Scheduler</span></span>
* <span data-ttu-id="c24d7-867">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="c24d7-867">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="c24d7-868">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-868">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-869">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="c24d7-869">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="c24d7-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-870">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c24d7-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c24d7-871">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c24d7-872">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c24d7-872">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c24d7-873">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c24d7-873">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c24d7-874">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-874">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="c24d7-875">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="c24d7-875">AzureRM.Websites</span></span>
* <span data-ttu-id="c24d7-876">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="c24d7-876">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="c24d7-877">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="c24d7-877">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="c24d7-878">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="c24d7-878">AzureRM.Profile</span></span>
* <span data-ttu-id="c24d7-879">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="c24d7-879">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="c24d7-880">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="c24d7-880">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="c24d7-881">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="c24d7-881">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="c24d7-882">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c24d7-882">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="c24d7-883">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="c24d7-883">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="c24d7-884">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-884">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="c24d7-885">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="c24d7-885">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="c24d7-886">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="c24d7-886">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="c24d7-887">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="c24d7-887">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="c24d7-888">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="c24d7-888">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="c24d7-889">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="c24d7-889">Added support for MSI identity</span></span>
* <span data-ttu-id="c24d7-890">Aggiunta del supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti saranno deprecati nella versione futura</span><span class="sxs-lookup"><span data-stu-id="c24d7-890">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="c24d7-891">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="c24d7-891">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="c24d7-892">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-892">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="c24d7-893">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="c24d7-893">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="c24d7-894">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="c24d7-894">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="c24d7-895">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="c24d7-895">AzureRM.Batch</span></span>
* <span data-ttu-id="c24d7-896">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="c24d7-896">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="c24d7-897">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="c24d7-897">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="c24d7-898">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="c24d7-898">AzureRM.Consumption</span></span>
* <span data-ttu-id="c24d7-899">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="c24d7-899">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="c24d7-900">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="c24d7-900">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="c24d7-901">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="c24d7-901">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="c24d7-902">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-902">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span>
* <span data-ttu-id="c24d7-903">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c24d7-903">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="c24d7-904">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="c24d7-904">AzureRM.Network</span></span>
* <span data-ttu-id="c24d7-905">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="c24d7-905">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="c24d7-906">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="c24d7-906">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="c24d7-907">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24d7-907">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="c24d7-908">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="c24d7-908">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="c24d7-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-909">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c24d7-910">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="c24d7-910">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="c24d7-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-911">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="c24d7-912">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="c24d7-912">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="c24d7-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="c24d7-913">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="c24d7-914">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="c24d7-914">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="c24d7-915">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="c24d7-915">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="c24d7-916">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="c24d7-916">AzureRM.Sql</span></span>
* <span data-ttu-id="c24d7-917">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="c24d7-917">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="c24d7-918">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="c24d7-918">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="c24d7-919">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="c24d7-919">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="c24d7-920">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="c24d7-920">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="c24d7-921">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="c24d7-921">The updated cmdlets including:</span></span>
    - <span data-ttu-id="c24d7-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-922">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="c24d7-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c24d7-923">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="c24d7-924">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="c24d7-924">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="c24d7-925">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c24d7-925">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="c24d7-926">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="c24d7-926">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="c24d7-927">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="c24d7-927">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="c24d7-928">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="c24d7-928">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
