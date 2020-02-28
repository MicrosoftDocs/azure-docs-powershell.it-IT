---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 81afcd63e5ca7a776965849de9090b833f49acc7
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477234"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="23c11-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="23c11-103">Azure PowerShell release notes</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="23c11-104">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="23c11-104">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-105">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-105">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-106">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="23c11-106">Updated client side telemetry.</span></span>
* <span data-ttu-id="23c11-107">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="23c11-107">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="23c11-108">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="23c11-108">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-109">Az.Accounts</span></span>
* <span data-ttu-id="23c11-110">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="23c11-110">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-111">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-111">Az.Automation</span></span>
* <span data-ttu-id="23c11-112">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="23c11-112">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-113">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-113">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-114">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="23c11-114">Updated SDK to 7.0</span></span>
* <span data-ttu-id="23c11-115">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="23c11-115">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-116">Az.Compute</span></span>
* <span data-ttu-id="23c11-117">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="23c11-117">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-118">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-119">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="23c11-119">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-120">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-120">Az.IotHub</span></span>
* <span data-ttu-id="23c11-121">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="23c11-121">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="23c11-122">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="23c11-122">New Cmdlets are:</span></span>
    - <span data-ttu-id="23c11-123">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="23c11-123">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="23c11-124">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="23c11-124">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="23c11-125">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="23c11-125">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="23c11-126">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="23c11-126">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-127">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-127">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-128">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="23c11-128">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-129">Az.Monitor</span></span>
* <span data-ttu-id="23c11-130">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="23c11-130">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="23c11-131">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="23c11-131">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="23c11-132">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="23c11-132">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-133">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-133">Az.Network</span></span>
* <span data-ttu-id="23c11-134">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="23c11-134">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="23c11-135">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="23c11-135">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="23c11-136">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="23c11-136">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="23c11-137">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-137">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="23c11-138">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="23c11-138">No new cmdlets are added.</span></span> <span data-ttu-id="23c11-139">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-139">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-140">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-140">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-141">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="23c11-141">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-142">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-142">Az.Resources</span></span>
* <span data-ttu-id="23c11-143">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="23c11-143">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="23c11-144">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="23c11-144">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="23c11-145">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="23c11-145">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="23c11-146">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="23c11-146">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="23c11-147">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="23c11-147">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="23c11-148">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="23c11-148">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="23c11-149">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="23c11-149">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="23c11-150">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-150">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-151">Az.Sql</span></span>
* <span data-ttu-id="23c11-152">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="23c11-152">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="23c11-153">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="23c11-153">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="23c11-154">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="23c11-154">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="23c11-155">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="23c11-155">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="23c11-156">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="23c11-156">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="23c11-157">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="23c11-157">Az.StorageSync</span></span>
* <span data-ttu-id="23c11-158">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="23c11-158">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="23c11-159">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="23c11-159">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-160">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-160">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-161">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="23c11-161">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="23c11-162">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="23c11-162">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-163">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-163">Az.Accounts</span></span>
* <span data-ttu-id="23c11-164">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="23c11-164">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="23c11-165">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="23c11-165">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="23c11-166">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-166">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-167">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="23c11-167">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="23c11-168">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="23c11-168">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="23c11-169">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="23c11-169">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="23c11-170">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-170">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-171">Az.Compute</span></span>
* <span data-ttu-id="23c11-172">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23c11-172">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="23c11-173">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="23c11-173">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="23c11-174">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c11-174">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="23c11-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-175">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="23c11-176">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="23c11-176">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-177">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-177">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-178">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="23c11-178">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="23c11-179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="23c11-179">Az.DeploymentManager</span></span>
* <span data-ttu-id="23c11-180">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="23c11-180">Adds LIST operations for resources</span></span>
* <span data-ttu-id="23c11-181">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="23c11-181">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="23c11-182">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-182">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-183">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="23c11-183">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-184">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-184">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-185">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="23c11-185">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-186">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-186">Az.Network</span></span>
* <span data-ttu-id="23c11-187">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="23c11-187">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="23c11-188">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="23c11-188">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="23c11-189">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="23c11-189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="23c11-190">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="23c11-190">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="23c11-191">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="23c11-191">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="23c11-192">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="23c11-192">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="23c11-193">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="23c11-193">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="23c11-194">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="23c11-194">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="23c11-195">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-195">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-196">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="23c11-197">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-197">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="23c11-198">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="23c11-198">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="23c11-199">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="23c11-199">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="23c11-200">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-200">Az.PolicyInsights</span></span>
* <span data-ttu-id="23c11-201">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="23c11-201">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="23c11-202">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="23c11-202">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="23c11-203">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="23c11-203">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="23c11-204">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="23c11-204">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-205">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-205">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-206">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="23c11-206">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="23c11-207">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="23c11-207">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-208">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-208">Az.Resources</span></span>
* <span data-ttu-id="23c11-209">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="23c11-209">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="23c11-210">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="23c11-210">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-211">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-211">Az.Sql</span></span>
<span data-ttu-id="23c11-212">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="23c11-212">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-213">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-213">Az.Storage</span></span>
* <span data-ttu-id="23c11-214">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23c11-214">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="23c11-215">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-215">New-AzStorageAccount</span></span>
* <span data-ttu-id="23c11-216">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="23c11-216">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="23c11-217">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-217">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-218">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-218">Az.Websites</span></span>
* <span data-ttu-id="23c11-219">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="23c11-219">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="23c11-220">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="23c11-220">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="23c11-221">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="23c11-221">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-222">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-222">Az.Accounts</span></span>
* <span data-ttu-id="23c11-223">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="23c11-223">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-224">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-224">Az.Cdn</span></span>
* <span data-ttu-id="23c11-225">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-225">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-226">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-226">Az.Compute</span></span>
* <span data-ttu-id="23c11-227">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="23c11-227">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="23c11-228">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-228">Az.ContainerInstance</span></span>
* <span data-ttu-id="23c11-229">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-229">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="23c11-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="23c11-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="23c11-231">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="23c11-231">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="23c11-232">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-232">Get the Edge Storage Container</span></span>
* <span data-ttu-id="23c11-233">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="23c11-233">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="23c11-234">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-234">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="23c11-235">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="23c11-235">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="23c11-236">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-236">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="23c11-237">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="23c11-237">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="23c11-238">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-238">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="23c11-239">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="23c11-239">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="23c11-240">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-240">Get the Edge Storage Account</span></span>
* <span data-ttu-id="23c11-241">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="23c11-241">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="23c11-242">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-242">Create new Edge Storage Account</span></span>
* <span data-ttu-id="23c11-243">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="23c11-243">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="23c11-244">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="23c11-244">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="23c11-245">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="23c11-245">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="23c11-246">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="23c11-246">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="23c11-247">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="23c11-247">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="23c11-248">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="23c11-248">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-249">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-250">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="23c11-250">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="23c11-251">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="23c11-251">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="23c11-252">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="23c11-252">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="23c11-253">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="23c11-253">Az.DevTestLabs</span></span>
* <span data-ttu-id="23c11-254">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="23c11-254">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-255">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-255">Az.EventHub</span></span>
* <span data-ttu-id="23c11-256">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="23c11-256">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="23c11-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-257">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-258">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="23c11-258">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="23c11-259">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="23c11-259">Az.MachineLearning</span></span>
* <span data-ttu-id="23c11-260">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="23c11-260">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="23c11-261">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="23c11-261">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="23c11-262">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="23c11-262">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="23c11-263">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="23c11-263">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="23c11-264">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="23c11-264">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="23c11-265">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="23c11-265">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="23c11-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="23c11-266">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="23c11-267">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="23c11-267">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-268">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-268">Az.Network</span></span>
* <span data-ttu-id="23c11-269">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="23c11-269">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-270">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-270">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-271">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-271">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="23c11-272">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-272">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="23c11-273">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-273">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="23c11-274">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-274">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-275">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-275">Az.Resources</span></span>
* <span data-ttu-id="23c11-276">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="23c11-276">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-277">Az.Sql</span></span>
* <span data-ttu-id="23c11-278">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="23c11-278">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="23c11-279">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="23c11-279">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="23c11-280">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="23c11-280">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="23c11-281">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="23c11-281">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-282">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-282">Az.Storage</span></span>
* <span data-ttu-id="23c11-283">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="23c11-283">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="23c11-284">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-284">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="23c11-285">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="23c11-285">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="23c11-286">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-286">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="23c11-287">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-287">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="23c11-288">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-288">General</span></span>
* <span data-ttu-id="23c11-289">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="23c11-289">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-290">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-290">Az.Accounts</span></span>
* <span data-ttu-id="23c11-291">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="23c11-291">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="23c11-292">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="23c11-292">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="23c11-293">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-293">Az.Batch</span></span>
* <span data-ttu-id="23c11-294">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="23c11-294">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-295">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-295">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-296">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="23c11-296">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-297">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-297">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-298">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="23c11-298">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="23c11-299">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="23c11-299">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="23c11-300">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="23c11-300">Az.HealthcareApis</span></span>
* <span data-ttu-id="23c11-301">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="23c11-301">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-302">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-302">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-303">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="23c11-303">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="23c11-304">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="23c11-304">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="23c11-305">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="23c11-305">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-306">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-306">Az.Monitor</span></span>
* <span data-ttu-id="23c11-307">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="23c11-307">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="23c11-308">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="23c11-308">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="23c11-309">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="23c11-309">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-310">Az.Network</span></span>
* <span data-ttu-id="23c11-311">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="23c11-311">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-312">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-312">Az.Resources</span></span>
* <span data-ttu-id="23c11-313">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="23c11-313">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="23c11-314">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="23c11-314">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-315">Az.Sql</span></span>
* <span data-ttu-id="23c11-316">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="23c11-316">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-317">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-317">Az.Storage</span></span>
* <span data-ttu-id="23c11-318">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="23c11-318">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="23c11-319">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="23c11-319">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="23c11-320">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="23c11-320">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="23c11-321">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="23c11-321">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="23c11-322">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="23c11-322">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="23c11-323">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="23c11-323">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="23c11-324">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="23c11-324">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="23c11-325">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-325">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="23c11-326">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-326">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="23c11-327">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="23c11-327">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="23c11-328">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="23c11-328">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="23c11-329">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="23c11-329">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="23c11-330">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="23c11-330">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="23c11-331">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-331">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-332">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-332">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-333">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-333">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="23c11-334">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-334">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-335">Az.Compute</span></span>
* <span data-ttu-id="23c11-336">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-336">VM Reapply feature</span></span>
    - <span data-ttu-id="23c11-337">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="23c11-337">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="23c11-338">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="23c11-338">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="23c11-339">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-339">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="23c11-340">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="23c11-340">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="23c11-341">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-341">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="23c11-342">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="23c11-342">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="23c11-343">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="23c11-343">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="23c11-344">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="23c11-344">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="23c11-345">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="23c11-345">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="23c11-346">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-346">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="23c11-347">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="23c11-347">Az.DataBoxEdge</span></span>
* <span data-ttu-id="23c11-348">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="23c11-348">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="23c11-349">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="23c11-349">Get the Order</span></span>
* <span data-ttu-id="23c11-350">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="23c11-350">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="23c11-351">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="23c11-351">Create new Order</span></span>
* <span data-ttu-id="23c11-352">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="23c11-352">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="23c11-353">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="23c11-353">Remove the Order</span></span>
* <span data-ttu-id="23c11-354">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="23c11-354">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="23c11-355">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="23c11-355">Now creates Local Share</span></span>
* <span data-ttu-id="23c11-356">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="23c11-356">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="23c11-357">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="23c11-357">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="23c11-358">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="23c11-358">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="23c11-359">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="23c11-359">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="23c11-360">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="23c11-360">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="23c11-361">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="23c11-361">Gets the information about Triggers</span></span>
* <span data-ttu-id="23c11-362">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="23c11-362">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="23c11-363">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="23c11-363">Create new Triggers</span></span>
* <span data-ttu-id="23c11-364">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="23c11-364">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="23c11-365">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="23c11-365">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-366">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-366">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-367">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="23c11-367">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="23c11-368">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="23c11-368">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-369">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-369">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-370">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="23c11-370">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-371">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-371">Az.EventHub</span></span>
* <span data-ttu-id="23c11-372">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="23c11-372">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-373">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-374">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="23c11-374">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="23c11-375">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="23c11-375">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="23c11-376">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="23c11-376">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="23c11-377">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="23c11-377">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-378">Az.Network</span></span>
* <span data-ttu-id="23c11-379">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="23c11-379">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="23c11-380">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="23c11-380">Az.PrivateDns</span></span>
* <span data-ttu-id="23c11-381">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-381">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-382">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-382">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-383">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="23c11-383">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="23c11-384">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="23c11-384">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="23c11-385">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-385">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="23c11-386">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="23c11-386">Az.RedisCache</span></span>
* <span data-ttu-id="23c11-387">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="23c11-387">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="23c11-388">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="23c11-388">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="23c11-389">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="23c11-389">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-390">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-390">Az.Resources</span></span>
- <span data-ttu-id="23c11-391">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="23c11-391">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="23c11-392">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="23c11-392">Updated create policy definition help example</span></span>
- <span data-ttu-id="23c11-393">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="23c11-393">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="23c11-394">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="23c11-394">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="23c11-395">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="23c11-395">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-396">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-396">Az.Sql</span></span>
* <span data-ttu-id="23c11-397">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="23c11-397">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="23c11-398">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="23c11-398">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="23c11-399">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-399">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="23c11-400">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-400">General</span></span>
* <span data-ttu-id="23c11-401">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-401">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-402">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-402">Az.Accounts</span></span>
* <span data-ttu-id="23c11-403">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="23c11-403">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="23c11-404">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="23c11-404">Az.Advisor</span></span>
* <span data-ttu-id="23c11-405">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="23c11-405">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="23c11-406">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-406">Az.Batch</span></span>
* <span data-ttu-id="23c11-407">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="23c11-407">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="23c11-408">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="23c11-408">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="23c11-409">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="23c11-409">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="23c11-410">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="23c11-410">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="23c11-411">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="23c11-411">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="23c11-412">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="23c11-412">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="23c11-413">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="23c11-413">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="23c11-414">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="23c11-414">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="23c11-415">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="23c11-415">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="23c11-416">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="23c11-416">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="23c11-417">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="23c11-417">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="23c11-418">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="23c11-418">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="23c11-419">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="23c11-419">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="23c11-420">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="23c11-420">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="23c11-421">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="23c11-421">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="23c11-422">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="23c11-422">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="23c11-423">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="23c11-423">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="23c11-424">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="23c11-424">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="23c11-425">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="23c11-425">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="23c11-426">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="23c11-426">This operation is no longer supported.</span></span>
* <span data-ttu-id="23c11-427">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="23c11-427">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="23c11-428">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="23c11-428">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="23c11-429">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="23c11-429">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="23c11-430">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="23c11-430">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="23c11-431">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="23c11-431">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="23c11-432">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="23c11-432">New non-verified images are also now returned.</span></span> <span data-ttu-id="23c11-433">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="23c11-433">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="23c11-434">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="23c11-434">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="23c11-435">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="23c11-435">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="23c11-436">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="23c11-436">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="23c11-437">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="23c11-437">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="23c11-438">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="23c11-438">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="23c11-439">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="23c11-439">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="23c11-440">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="23c11-440">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="23c11-441">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="23c11-441">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="23c11-442">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="23c11-442">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-443">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-443">Az.Cdn</span></span>
* <span data-ttu-id="23c11-444">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="23c11-444">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="23c11-445">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="23c11-445">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-446">Az.Compute</span></span>
* <span data-ttu-id="23c11-447">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="23c11-447">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="23c11-448">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="23c11-448">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="23c11-449">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-449">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="23c11-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="23c11-450">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="23c11-451">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-451">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="23c11-452">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-452">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="23c11-453">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="23c11-453">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="23c11-454">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-454">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="23c11-455">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="23c11-455">Breaking changes</span></span>
    - <span data-ttu-id="23c11-456">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="23c11-456">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="23c11-457">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="23c11-457">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-458">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-458">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-459">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="23c11-459">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-460">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-460">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-461">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="23c11-461">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="23c11-462">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="23c11-462">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="23c11-463">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="23c11-463">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="23c11-464">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="23c11-464">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="23c11-465">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="23c11-465">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="23c11-466">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="23c11-466">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-467">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-467">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-468">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="23c11-468">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="23c11-469">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-469">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-470">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="23c11-470">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="23c11-471">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="23c11-471">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="23c11-472">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="23c11-472">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="23c11-473">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-473">Removed five cmdlets:</span></span>
    - <span data-ttu-id="23c11-474">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="23c11-474">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="23c11-475">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="23c11-475">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="23c11-476">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="23c11-476">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="23c11-477">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="23c11-477">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="23c11-478">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="23c11-478">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="23c11-479">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-479">Added three cmdlets:</span></span>
    - <span data-ttu-id="23c11-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="23c11-480">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="23c11-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="23c11-481">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="23c11-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="23c11-482">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="23c11-483">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="23c11-483">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="23c11-484">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="23c11-484">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="23c11-485">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="23c11-485">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="23c11-486">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c11-486">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="23c11-487">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="23c11-487">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="23c11-488">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="23c11-488">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="23c11-489">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="23c11-489">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="23c11-490">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="23c11-490">Added some scenario test cases.</span></span>
* <span data-ttu-id="23c11-491">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="23c11-491">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-492">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-492">Az.IotHub</span></span>
* <span data-ttu-id="23c11-493">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="23c11-493">Breaking changes:</span></span>
    - <span data-ttu-id="23c11-494">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="23c11-494">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="23c11-495">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="23c11-495">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="23c11-496">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="23c11-496">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="23c11-497">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="23c11-497">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="23c11-498">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="23c11-498">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="23c11-499">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="23c11-499">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="23c11-500">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="23c11-500">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="23c11-501">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="23c11-501">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="23c11-502">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="23c11-502">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="23c11-503">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="23c11-503">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="23c11-504">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="23c11-504">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="23c11-505">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="23c11-505">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-506">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-506">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-507">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-507">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-508">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-508">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="23c11-509">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-509">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="23c11-510">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-510">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-511">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-511">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-512">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-512">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-513">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-513">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-514">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-514">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-515">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="23c11-515">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-516">Az.Resources</span></span>
* <span data-ttu-id="23c11-517">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="23c11-517">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-518">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-518">Az.Network</span></span>
* <span data-ttu-id="23c11-519">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="23c11-519">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="23c11-520">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="23c11-520">Updated cmdlet:</span></span>
        - <span data-ttu-id="23c11-521">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-521">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-522">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-522">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-523">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-523">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-524">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-524">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-525">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-525">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="23c11-526">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="23c11-526">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="23c11-527">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-527">New cmdlet:</span></span>
        - <span data-ttu-id="23c11-528">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="23c11-528">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="23c11-529">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="23c11-529">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="23c11-530">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-530">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="23c11-531">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-531">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="23c11-532">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="23c11-532">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="23c11-533">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="23c11-533">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="23c11-534">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-534">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="23c11-535">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="23c11-535">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="23c11-536">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-536">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-537">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="23c11-537">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="23c11-538">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-538">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="23c11-539">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-539">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="23c11-540">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-540">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="23c11-541">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="23c11-541">Set-AzVirtualHub</span></span>
* <span data-ttu-id="23c11-542">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="23c11-542">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="23c11-543">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="23c11-543">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="23c11-544">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="23c11-544">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="23c11-545">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="23c11-545">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="23c11-546">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="23c11-546">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="23c11-547">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="23c11-547">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="23c11-548">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-548">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="23c11-549">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-549">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-550">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-550">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="23c11-551">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="23c11-551">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="23c11-552">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="23c11-552">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="23c11-553">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="23c11-553">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="23c11-554">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="23c11-554">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="23c11-555">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="23c11-555">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="23c11-556">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="23c11-556">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="23c11-557">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="23c11-557">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="23c11-558">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-558">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-559">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="23c11-559">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="23c11-560">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="23c11-560">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="23c11-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="23c11-561">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="23c11-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="23c11-562">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="23c11-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="23c11-563">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="23c11-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-564">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="23c11-565">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="23c11-565">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="23c11-566">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="23c11-566">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="23c11-567">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="23c11-567">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="23c11-568">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="23c11-568">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="23c11-569">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="23c11-569">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="23c11-570">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="23c11-570">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="23c11-571">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="23c11-571">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="23c11-572">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="23c11-572">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="23c11-573">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="23c11-573">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="23c11-574">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-574">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="23c11-575">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-575">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="23c11-576">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-576">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-577">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-577">New-AzIpGroup</span></span>
        - <span data-ttu-id="23c11-578">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-578">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="23c11-579">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-579">Get-AzIpGroup</span></span>
        - <span data-ttu-id="23c11-580">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-580">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-581">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-581">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-582">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="23c11-582">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-583">Az.Sql</span></span>
* <span data-ttu-id="23c11-584">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="23c11-584">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="23c11-585">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="23c11-585">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="23c11-586">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="23c11-586">Removed deprecated aliases:</span></span>
* <span data-ttu-id="23c11-587">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="23c11-587">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="23c11-588">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="23c11-588">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="23c11-589">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-589">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="23c11-590">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="23c11-590">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="23c11-591">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="23c11-591">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="23c11-592">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="23c11-592">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-593">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-593">Az.Storage</span></span>
* <span data-ttu-id="23c11-594">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23c11-594">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="23c11-595">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-595">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="23c11-596">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-596">Set-AzStorageAccount</span></span>
* <span data-ttu-id="23c11-597">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="23c11-597">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="23c11-598">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="23c11-598">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="23c11-599">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="23c11-599">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="23c11-600">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-600">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="23c11-601">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-601">General</span></span>
* <span data-ttu-id="23c11-602">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-602">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-603">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-603">Az.Accounts</span></span>
* <span data-ttu-id="23c11-604">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="23c11-604">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="23c11-605">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-605">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-606">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="23c11-606">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="23c11-607">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="23c11-607">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-608">Az.Automation</span></span>
* <span data-ttu-id="23c11-609">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="23c11-609">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="23c11-610">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-610">Az.Batch</span></span>
* <span data-ttu-id="23c11-611">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="23c11-611">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-612">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-612">Az.Compute</span></span>
* <span data-ttu-id="23c11-613">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-613">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="23c11-614">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="23c11-614">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="23c11-615">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="23c11-615">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="23c11-616">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="23c11-616">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-617">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-618">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="23c11-618">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="23c11-619">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="23c11-619">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="23c11-620">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="23c11-620">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-622">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="23c11-622">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="23c11-623">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="23c11-623">Az.HealthcareApis</span></span>
* <span data-ttu-id="23c11-624">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-624">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="23c11-625">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="23c11-625">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="23c11-626">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="23c11-626">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="23c11-627">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="23c11-627">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-628">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-628">Az.IotHub</span></span>
* <span data-ttu-id="23c11-629">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="23c11-629">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="23c11-630">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="23c11-630">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="23c11-631">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-631">Az.Monitor</span></span>
* <span data-ttu-id="23c11-632">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="23c11-632">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="23c11-633">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="23c11-633">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="23c11-634">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="23c11-634">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="23c11-635">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="23c11-635">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-636">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-636">Az.Network</span></span>
* <span data-ttu-id="23c11-637">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="23c11-637">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="23c11-638">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-638">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="23c11-639">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-639">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-640">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-640">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="23c11-641">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-641">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="23c11-642">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="23c11-642">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="23c11-643">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-643">Updated cmdlets:</span></span>
        - <span data-ttu-id="23c11-644">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-644">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="23c11-645">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-645">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="23c11-646">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-646">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="23c11-647">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="23c11-647">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="23c11-648">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="23c11-648">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="23c11-649">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="23c11-649">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="23c11-650">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="23c11-650">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="23c11-651">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="23c11-651">Az.RedisCache</span></span>
* <span data-ttu-id="23c11-652">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="23c11-652">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-653">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-653">Az.Sql</span></span>
* <span data-ttu-id="23c11-654">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="23c11-654">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-655">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-655">Az.Storage</span></span>
* <span data-ttu-id="23c11-656">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="23c11-656">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="23c11-657">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="23c11-657">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="23c11-658">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="23c11-658">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="23c11-659">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="23c11-659">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="23c11-660">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-660">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="23c11-661">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="23c11-661">Az.StorageSync</span></span>
* <span data-ttu-id="23c11-662">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="23c11-662">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-663">Az.Websites</span></span>
* <span data-ttu-id="23c11-664">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="23c11-664">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="23c11-665">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-665">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="23c11-666">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-666">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-667">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="23c11-667">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="23c11-668">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="23c11-668">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="23c11-669">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="23c11-669">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-670">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-670">Az.Automation</span></span>
* <span data-ttu-id="23c11-671">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="23c11-671">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="23c11-672">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="23c11-672">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="23c11-673">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="23c11-673">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-674">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-674">Az.Compute</span></span>
* <span data-ttu-id="23c11-675">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-675">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="23c11-676">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-676">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="23c11-677">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="23c11-677">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="23c11-678">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="23c11-678">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="23c11-679">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="23c11-679">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="23c11-680">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="23c11-680">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="23c11-681">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="23c11-681">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="23c11-682">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="23c11-682">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="23c11-683">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="23c11-683">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-684">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-684">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-685">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="23c11-685">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="23c11-686">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="23c11-686">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="23c11-687">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-687">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-688">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="23c11-688">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-689">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-689">Az.IotHub</span></span>
* <span data-ttu-id="23c11-690">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="23c11-690">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="23c11-691">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="23c11-691">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="23c11-692">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="23c11-692">New cmdlets are:</span></span>
    - <span data-ttu-id="23c11-693">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="23c11-693">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="23c11-694">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="23c11-694">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="23c11-695">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="23c11-695">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="23c11-696">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="23c11-696">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-697">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-697">Az.Monitor</span></span>
* <span data-ttu-id="23c11-698">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="23c11-698">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="23c11-699">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="23c11-699">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="23c11-700">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="23c11-700">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="23c11-701">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="23c11-701">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="23c11-702">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="23c11-702">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="23c11-703">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="23c11-703">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="23c11-704">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c11-704">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="23c11-705">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="23c11-705">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="23c11-706">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="23c11-706">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="23c11-707">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="23c11-707">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="23c11-708">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="23c11-708">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="23c11-709">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="23c11-709">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="23c11-710">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="23c11-710">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="23c11-711">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="23c11-711">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="23c11-712">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="23c11-712">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="23c11-713">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="23c11-713">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="23c11-714">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="23c11-714">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="23c11-715">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-715">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="23c11-716">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="23c11-716">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="23c11-717">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-717">Overall improved help files</span></span>
* <span data-ttu-id="23c11-718">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="23c11-718">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-719">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-719">Az.Network</span></span>
* <span data-ttu-id="23c11-720">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="23c11-720">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="23c11-721">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="23c11-721">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="23c11-722">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="23c11-722">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="23c11-723">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="23c11-723">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="23c11-724">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="23c11-724">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="23c11-725">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="23c11-725">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="23c11-726">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="23c11-726">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="23c11-727">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="23c11-727">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="23c11-728">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-728">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="23c11-729">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="23c11-729">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="23c11-730">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-730">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="23c11-731">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-731">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="23c11-732">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-732">New cmdlets</span></span>
        - <span data-ttu-id="23c11-733">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="23c11-733">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="23c11-734">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-734">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="23c11-735">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="23c11-735">Updated cmdlet:</span></span>
        - <span data-ttu-id="23c11-736">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="23c11-736">New-VpnSite</span></span>
        - <span data-ttu-id="23c11-737">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="23c11-737">Update-VpnSite</span></span>
        - <span data-ttu-id="23c11-738">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-738">New-VpnConnection</span></span>
        - <span data-ttu-id="23c11-739">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-739">Update-VpnConnection</span></span>
* <span data-ttu-id="23c11-740">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="23c11-740">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-741">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-741">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-742">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="23c11-742">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="23c11-743">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="23c11-743">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-744">Az.Resources</span></span>
* <span data-ttu-id="23c11-745">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="23c11-745">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-746">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-746">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-747">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="23c11-747">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="23c11-748">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="23c11-748">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="23c11-749">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="23c11-749">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="23c11-750">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="23c11-750">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="23c11-751">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="23c11-751">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="23c11-752">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="23c11-752">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="23c11-753">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="23c11-753">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="23c11-754">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="23c11-754">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="23c11-755">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="23c11-755">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="23c11-756">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="23c11-756">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="23c11-757">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="23c11-757">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="23c11-758">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="23c11-758">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="23c11-759">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="23c11-759">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="23c11-760">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="23c11-760">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="23c11-761">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="23c11-761">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="23c11-762">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="23c11-762">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="23c11-763">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="23c11-763">Az.SignalR</span></span>
* <span data-ttu-id="23c11-764">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="23c11-764">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-765">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-765">Az.Sql</span></span>
* <span data-ttu-id="23c11-766">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="23c11-766">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="23c11-767">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="23c11-767">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="23c11-768">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-768">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="23c11-769">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="23c11-769">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="23c11-770">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="23c11-770">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-771">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-771">Az.Storage</span></span>
* <span data-ttu-id="23c11-772">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="23c11-772">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="23c11-773">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="23c11-773">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="23c11-774">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="23c11-774">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="23c11-775">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="23c11-775">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="23c11-776">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="23c11-776">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="23c11-777">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="23c11-777">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="23c11-778">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="23c11-778">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="23c11-779">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-779">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="23c11-780">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-780">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="23c11-781">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-781">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="23c11-782">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="23c11-782">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-783">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-783">Az.Websites</span></span>
* <span data-ttu-id="23c11-784">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="23c11-784">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="23c11-785">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="23c11-785">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="23c11-786">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="23c11-786">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="23c11-787">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-787">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="23c11-788">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-788">General</span></span>
* <span data-ttu-id="23c11-789">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="23c11-789">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-790">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-790">Az.Accounts</span></span>
* <span data-ttu-id="23c11-791">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="23c11-791">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="23c11-792">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="23c11-792">Az.Aks</span></span>
* <span data-ttu-id="23c11-793">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="23c11-793">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="23c11-794">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="23c11-794">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="23c11-795">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-795">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-796">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="23c11-796">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="23c11-797">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="23c11-797">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="23c11-798">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="23c11-798">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="23c11-799">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="23c11-799">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="23c11-800">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="23c11-800">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="23c11-801">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-801">Az.Batch</span></span>
* <span data-ttu-id="23c11-802">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="23c11-802">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-803">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-803">Az.Cdn</span></span>
* <span data-ttu-id="23c11-804">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="23c11-804">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-805">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-805">Az.Compute</span></span>
* <span data-ttu-id="23c11-806">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-806">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="23c11-807">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-807">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="23c11-808">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-808">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="23c11-809">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-809">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="23c11-810">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="23c11-810">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="23c11-811">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="23c11-811">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="23c11-812">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="23c11-812">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="23c11-813">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="23c11-813">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-814">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-814">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-815">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="23c11-815">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="23c11-816">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="23c11-816">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="23c11-817">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="23c11-817">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="23c11-818">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="23c11-818">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-819">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-819">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-820">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="23c11-820">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-821">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-821">Az.EventHub</span></span>
* <span data-ttu-id="23c11-822">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-822">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="23c11-823">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="23c11-823">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="23c11-824">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="23c11-824">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="23c11-825">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="23c11-825">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="23c11-826">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="23c11-826">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="23c11-827">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="23c11-827">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-828">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-828">Az.Monitor</span></span>
* <span data-ttu-id="23c11-829">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-829">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-830">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-830">Az.Network</span></span>
* <span data-ttu-id="23c11-831">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-831">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="23c11-832">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="23c11-832">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="23c11-833">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="23c11-833">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="23c11-834">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="23c11-834">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="23c11-835">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="23c11-835">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="23c11-836">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="23c11-836">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="23c11-837">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="23c11-837">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-838">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-838">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-839">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="23c11-839">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="23c11-840">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="23c11-840">Added example</span></span>
    - <span data-ttu-id="23c11-841">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="23c11-841">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="23c11-842">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="23c11-842">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="23c11-843">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="23c11-843">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-844">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-844">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-845">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-845">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-846">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-846">Az.Resources</span></span>
* <span data-ttu-id="23c11-847">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="23c11-847">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="23c11-848">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="23c11-848">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="23c11-849">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="23c11-849">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="23c11-850">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-850">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-851">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-851">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-852">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-852">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="23c11-853">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="23c11-853">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="23c11-854">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="23c11-854">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-855">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-855">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-856">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="23c11-856">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="23c11-857">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="23c11-857">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="23c11-858">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="23c11-858">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="23c11-859">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="23c11-859">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="23c11-860">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="23c11-860">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="23c11-861">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="23c11-861">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-862">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-862">Az.Sql</span></span>
* <span data-ttu-id="23c11-863">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="23c11-863">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-864">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-864">Az.Storage</span></span>
* <span data-ttu-id="23c11-865">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="23c11-865">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="23c11-866">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="23c11-866">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="23c11-867">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="23c11-867">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="23c11-868">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-868">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="23c11-869">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="23c11-869">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="23c11-870">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-870">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-871">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-871">Az.Websites</span></span>
* <span data-ttu-id="23c11-872">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23c11-872">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="23c11-873">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-873">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-874">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-874">Az.Accounts</span></span>
* <span data-ttu-id="23c11-875">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="23c11-875">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="23c11-876">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-876">Az.ApplicationInsights</span></span>
* <span data-ttu-id="23c11-877">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="23c11-877">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="23c11-878">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-878">Az.Automation</span></span>
* <span data-ttu-id="23c11-879">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="23c11-879">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-880">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-880">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-881">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="23c11-881">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-882">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-882">Az.Compute</span></span>
* <span data-ttu-id="23c11-883">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="23c11-883">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="23c11-884">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23c11-884">Az.ContainerRegistry</span></span>
* <span data-ttu-id="23c11-885">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="23c11-885">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="23c11-886">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="23c11-886">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-887">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-887">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-888">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="23c11-888">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="23c11-889">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="23c11-889">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-890">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-890">Az.EventHub</span></span>
* <span data-ttu-id="23c11-891">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="23c11-891">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="23c11-892">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="23c11-892">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-893">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-893">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-894">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="23c11-894">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="23c11-895">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="23c11-895">Az.LogicApp</span></span>
* <span data-ttu-id="23c11-896">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="23c11-896">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="23c11-897">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="23c11-897">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="23c11-898">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="23c11-898">Az.ManagedServices</span></span>
* <span data-ttu-id="23c11-899">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="23c11-899">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-900">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-900">Az.Network</span></span>
* <span data-ttu-id="23c11-901">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="23c11-901">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="23c11-902">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-902">New cmdlets</span></span>
        - <span data-ttu-id="23c11-903">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-903">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="23c11-904">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-904">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="23c11-905">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-905">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-906">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-906">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-907">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-907">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-908">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-908">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="23c11-909">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="23c11-909">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="23c11-910">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-910">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="23c11-911">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="23c11-911">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="23c11-912">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-912">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="23c11-913">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="23c11-913">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="23c11-914">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="23c11-914">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="23c11-915">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="23c11-915">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="23c11-916">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="23c11-916">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="23c11-917">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-917">Updated cmdlets</span></span>
        - <span data-ttu-id="23c11-918">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-918">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="23c11-919">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-919">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="23c11-920">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-920">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="23c11-921">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-921">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="23c11-922">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-922">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="23c11-923">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="23c11-923">Updated cmdlet:</span></span>
        - <span data-ttu-id="23c11-924">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-924">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="23c11-925">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-925">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="23c11-926">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-926">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="23c11-927">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="23c11-927">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="23c11-928">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="23c11-928">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="23c11-929">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="23c11-929">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-930">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-930">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-931">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="23c11-931">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="23c11-932">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="23c11-932">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-933">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-933">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-934">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-934">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="23c11-935">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-935">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="23c11-936">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-936">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="23c11-937">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-937">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="23c11-938">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-938">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="23c11-939">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-939">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="23c11-940">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-940">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="23c11-941">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-941">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="23c11-942">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-942">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="23c11-943">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="23c11-943">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-944">Az.Resources</span></span>
- <span data-ttu-id="23c11-945">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="23c11-945">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="23c11-946">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="23c11-946">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-947">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-947">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-948">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="23c11-948">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="23c11-949">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="23c11-949">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-950">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-950">Az.Sql</span></span>
* <span data-ttu-id="23c11-951">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="23c11-951">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="23c11-952">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="23c11-952">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="23c11-953">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="23c11-953">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-954">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-954">Az.Storage</span></span>
* <span data-ttu-id="23c11-955">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="23c11-955">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="23c11-956">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="23c11-956">Az.StorageSync</span></span>
* <span data-ttu-id="23c11-957">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="23c11-957">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="23c11-958">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="23c11-958">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-959">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-959">Az.Websites</span></span>
* <span data-ttu-id="23c11-960">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="23c11-960">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="23c11-961">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="23c11-961">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="23c11-962">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="23c11-962">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="23c11-963">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-963">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-964">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-964">Az.Accounts</span></span>
* <span data-ttu-id="23c11-965">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="23c11-965">Add support for profile cmdlets</span></span>
* <span data-ttu-id="23c11-966">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="23c11-966">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="23c11-967">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="23c11-967">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="23c11-968">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="23c11-968">Az.Advisor</span></span>
* <span data-ttu-id="23c11-969">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="23c11-969">GA release of Az.Advisor</span></span>
* <span data-ttu-id="23c11-970">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="23c11-970">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="23c11-971">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-971">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-972">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="23c11-972">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="23c11-973">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="23c11-973">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="23c11-974">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="23c11-974">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="23c11-975">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="23c11-975">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="23c11-976">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="23c11-976">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="23c11-977">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="23c11-977">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="23c11-978">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="23c11-978">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-979">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-979">Az.Automation</span></span>
* <span data-ttu-id="23c11-980">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="23c11-980">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-981">Az.Compute</span></span>
* <span data-ttu-id="23c11-982">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-982">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-983">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-983">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-984">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="23c11-984">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="23c11-985">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="23c11-985">Az.EventGrid</span></span>
* <span data-ttu-id="23c11-986">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="23c11-986">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-987">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-987">Az.IotHub</span></span>
* <span data-ttu-id="23c11-988">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="23c11-988">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-989">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-989">Az.Network</span></span>
* <span data-ttu-id="23c11-990">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="23c11-990">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="23c11-991">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="23c11-991">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="23c11-992">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-992">Az.PolicyInsights</span></span>
* <span data-ttu-id="23c11-993">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="23c11-993">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="23c11-994">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="23c11-994">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-995">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-995">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-996">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="23c11-996">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-997">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-997">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-998">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="23c11-998">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-999">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-999">Az.Resources</span></span>
    - <span data-ttu-id="23c11-1000">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="23c11-1000">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="23c11-1001">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="23c11-1001">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="23c11-1002">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="23c11-1002">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="23c11-1003">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="23c11-1003">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-1004">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-1004">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-1005">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="23c11-1005">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1006">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1006">Az.Sql</span></span>
* <span data-ttu-id="23c11-1007">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="23c11-1007">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="23c11-1008">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1008">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="23c11-1009">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1009">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="23c11-1010">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1010">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="23c11-1011">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1011">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="23c11-1012">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1012">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="23c11-1013">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1013">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="23c11-1014">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="23c11-1014">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="23c11-1015">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="23c11-1015">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1016">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1016">Az.Storage</span></span>
* <span data-ttu-id="23c11-1017">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-1017">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="23c11-1018">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="23c11-1018">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="23c11-1019">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="23c11-1019">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="23c11-1020">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="23c11-1020">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="23c11-1021">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1021">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="23c11-1022">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1022">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="23c11-1023">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1023">Set-AzStorageAccount</span></span>
* <span data-ttu-id="23c11-1024">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="23c11-1024">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="23c11-1025">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="23c11-1025">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="23c11-1026">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="23c11-1026">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="23c11-1027">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="23c11-1027">Az.StorageSync</span></span>
* <span data-ttu-id="23c11-1028">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="23c11-1028">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="23c11-1029">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1029">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1030">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1030">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1031">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="23c11-1031">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="23c11-1032">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="23c11-1032">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="23c11-1033">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="23c11-1033">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="23c11-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="23c11-1034">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="23c11-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="23c11-1035">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1036">Az.Compute</span></span>
* <span data-ttu-id="23c11-1037">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1037">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="23c11-1038">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="23c11-1038">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="23c11-1039">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="23c11-1039">Az.Dns</span></span>
* <span data-ttu-id="23c11-1040">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1040">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="23c11-1041">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="23c11-1041">Az.EventGrid</span></span>
* <span data-ttu-id="23c11-1042">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="23c11-1042">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="23c11-1043">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-1043">New cmdlets:</span></span>
    - <span data-ttu-id="23c11-1044">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="23c11-1044">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="23c11-1045">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1045">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="23c11-1046">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="23c11-1046">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="23c11-1047">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1047">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="23c11-1048">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="23c11-1048">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="23c11-1049">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1049">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="23c11-1050">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="23c11-1050">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="23c11-1051">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1051">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="23c11-1052">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="23c11-1052">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="23c11-1053">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="23c11-1053">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="23c11-1054">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="23c11-1054">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="23c11-1055">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1055">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="23c11-1056">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="23c11-1056">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="23c11-1057">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1057">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="23c11-1058">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="23c11-1058">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="23c11-1059">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="23c11-1059">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="23c11-1060">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-1060">Updated cmdlets:</span></span>
    - <span data-ttu-id="23c11-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="23c11-1061">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="23c11-1062">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="23c11-1062">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="23c11-1063">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="23c11-1063">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="23c11-1064">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="23c11-1064">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="23c11-1065">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="23c11-1065">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="23c11-1066">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="23c11-1066">Event subscription expiration date,</span></span>
            - <span data-ttu-id="23c11-1067">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1067">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="23c11-1068">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1068">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="23c11-1069">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1069">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="23c11-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="23c11-1070">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="23c11-1071">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1071">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="23c11-1072">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="23c11-1072">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="23c11-1073">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="23c11-1073">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="23c11-1074">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="23c11-1074">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-1075">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-1075">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-1076">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="23c11-1076">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="23c11-1077">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="23c11-1077">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="23c11-1078">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="23c11-1078">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="23c11-1079">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="23c11-1079">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1080">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1080">Az.Network</span></span>
* <span data-ttu-id="23c11-1081">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-1081">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="23c11-1082">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-1082">New cmdlets</span></span>
        - <span data-ttu-id="23c11-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="23c11-1083">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="23c11-1084">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="23c11-1084">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="23c11-1085">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-1085">New cmdlets</span></span> 
        - <span data-ttu-id="23c11-1086">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="23c11-1086">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="23c11-1087">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-1087">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="23c11-1088">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-1088">New cmdlets</span></span> 
        - <span data-ttu-id="23c11-1089">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-1089">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="23c11-1090">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-1090">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="23c11-1091">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="23c11-1091">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="23c11-1092">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-1092">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="23c11-1093">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-1093">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="23c11-1094">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-1094">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="23c11-1095">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-1095">New cmdlets</span></span>
        - <span data-ttu-id="23c11-1096">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-1096">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="23c11-1097">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-1097">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="23c11-1098">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c11-1098">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="23c11-1099">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-1099">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="23c11-1100">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="23c11-1100">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="23c11-1101">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="23c11-1101">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="23c11-1102">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="23c11-1102">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="23c11-1103">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23c11-1103">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="23c11-1104">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="23c11-1104">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="23c11-1105">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="23c11-1105">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="23c11-1106">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1106">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="23c11-1107">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="23c11-1107">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="23c11-1108">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1108">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="23c11-1109">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="23c11-1109">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="23c11-1110">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1110">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="23c11-1111">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1111">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="23c11-1112">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="23c11-1112">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="23c11-1113">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1113">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="23c11-1114">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="23c11-1114">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="23c11-1115">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="23c11-1115">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="23c11-1116">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-1116">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="23c11-1117">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="23c11-1117">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="23c11-1118">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="23c11-1118">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="23c11-1119">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="23c11-1119">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="23c11-1120">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1120">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="23c11-1121">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1121">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="23c11-1122">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1122">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-1123">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1123">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-1124">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="23c11-1124">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1125">Az.Resources</span></span>
* <span data-ttu-id="23c11-1126">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="23c11-1126">Support for additional Template Export options</span></span>
    - <span data-ttu-id="23c11-1127">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1127">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="23c11-1128">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1128">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="23c11-1129">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="23c11-1129">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-1130">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1130">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-1131">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="23c11-1131">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1132">Az.Sql</span></span>
* <span data-ttu-id="23c11-1133">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="23c11-1133">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="23c11-1134">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="23c11-1134">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="23c11-1135">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="23c11-1135">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="23c11-1136">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23c11-1136">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="23c11-1137">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23c11-1137">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="23c11-1138">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23c11-1138">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="23c11-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="23c11-1139">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="23c11-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="23c11-1140">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1141">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1141">Az.Storage</span></span>
* <span data-ttu-id="23c11-1142">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1142">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="23c11-1143">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1143">New-AzStorageAccount</span></span>
* <span data-ttu-id="23c11-1144">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="23c11-1144">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="23c11-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1145">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1146">Az.Websites</span></span>
* <span data-ttu-id="23c11-1147">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="23c11-1147">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="23c11-1148">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="23c11-1148">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="23c11-1149">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1149">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="23c11-1150">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-1150">Az.Cdn</span></span>
* <span data-ttu-id="23c11-1151">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="23c11-1151">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1152">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1152">Az.Compute</span></span>
* <span data-ttu-id="23c11-1153">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1153">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="23c11-1154">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="23c11-1154">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-1155">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1155">Az.EventHub</span></span>
* <span data-ttu-id="23c11-1156">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="23c11-1156">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="23c11-1157">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c11-1157">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1158">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1158">Az.Network</span></span>
* <span data-ttu-id="23c11-1159">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="23c11-1159">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="23c11-1160">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="23c11-1160">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="23c11-1161">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1161">Az.PolicyInsights</span></span>
* <span data-ttu-id="23c11-1162">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="23c11-1162">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1163">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1163">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1164">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="23c11-1164">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-1165">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-1165">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-1166">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23c11-1166">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-1167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1167">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-1168">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="23c11-1168">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="23c11-1169">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1169">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1170">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1170">Az.Sql</span></span>
* <span data-ttu-id="23c11-1171">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="23c11-1171">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="23c11-1172">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1172">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="23c11-1173">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="23c11-1173">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="23c11-1174">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="23c11-1174">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1175">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1175">Az.Websites</span></span>
* <span data-ttu-id="23c11-1176">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="23c11-1176">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="23c11-1177">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1177">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="23c11-1178">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-1178">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-1179">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="23c11-1179">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="23c11-1180">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1180">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="23c11-1181">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1181">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="23c11-1182">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="23c11-1182">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="23c11-1183">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1183">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="23c11-1184">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="23c11-1184">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="23c11-1185">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1185">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="23c11-1186">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1186">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="23c11-1187">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-1187">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="23c11-1188">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="23c11-1188">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="23c11-1189">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1189">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="23c11-1190">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="23c11-1190">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="23c11-1191">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="23c11-1191">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="23c11-1192">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1192">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="23c11-1193">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1193">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="23c11-1194">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1194">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="23c11-1195">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1195">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="23c11-1196">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="23c11-1196">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="23c11-1197">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="23c11-1197">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="23c11-1198">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1198">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="23c11-1199">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="23c11-1199">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="23c11-1200">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="23c11-1200">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="23c11-1201">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="23c11-1201">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="23c11-1202">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-1202">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="23c11-1203">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="23c11-1203">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="23c11-1204">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="23c11-1204">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="23c11-1205">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1205">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="23c11-1206">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="23c11-1206">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="23c11-1207">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="23c11-1207">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="23c11-1208">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="23c11-1208">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="23c11-1209">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="23c11-1209">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="23c11-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="23c11-1210">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="23c11-1211">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="23c11-1211">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="23c11-1212">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="23c11-1212">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="23c11-1213">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="23c11-1213">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="23c11-1214">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="23c11-1214">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="23c11-1215">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="23c11-1215">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="23c11-1216">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="23c11-1216">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="23c11-1217">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="23c11-1217">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="23c11-1218">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="23c11-1218">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="23c11-1219">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1219">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="23c11-1220">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="23c11-1220">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="23c11-1221">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1221">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="23c11-1222">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="23c11-1222">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="23c11-1223">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="23c11-1223">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="23c11-1224">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1224">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="23c11-1225">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="23c11-1225">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="23c11-1226">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="23c11-1226">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="23c11-1227">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="23c11-1227">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="23c11-1228">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1228">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="23c11-1229">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="23c11-1229">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="23c11-1230">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="23c11-1230">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="23c11-1231">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="23c11-1231">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="23c11-1232">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="23c11-1232">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="23c11-1233">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="23c11-1233">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="23c11-1234">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="23c11-1234">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="23c11-1235">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="23c11-1235">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="23c11-1236">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="23c11-1236">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="23c11-1237">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="23c11-1237">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="23c11-1238">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1238">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="23c11-1239">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="23c11-1239">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="23c11-1240">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="23c11-1240">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="23c11-1241">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="23c11-1241">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="23c11-1242">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1242">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="23c11-1243">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="23c11-1243">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="23c11-1244">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="23c11-1244">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="23c11-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="23c11-1245">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="23c11-1246">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="23c11-1246">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="23c11-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="23c11-1247">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="23c11-1248">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="23c11-1248">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="23c11-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="23c11-1249">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="23c11-1250">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="23c11-1250">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="23c11-1251">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="23c11-1251">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="23c11-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1252">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="23c11-1253">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="23c11-1253">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="23c11-1254">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="23c11-1254">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="23c11-1255">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="23c11-1255">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1256">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1256">Az.Automation</span></span>
* <span data-ttu-id="23c11-1257">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="23c11-1257">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="23c11-1258">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="23c11-1258">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="23c11-1259">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="23c11-1259">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="23c11-1260">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="23c11-1260">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="23c11-1261">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="23c11-1261">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="23c11-1262">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="23c11-1262">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="23c11-1263">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="23c11-1263">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1264">Az.Compute</span></span>
* <span data-ttu-id="23c11-1265">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="23c11-1265">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="23c11-1266">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="23c11-1266">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1267">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1268">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1268">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-1269">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-1269">Az.Monitor</span></span>
* <span data-ttu-id="23c11-1270">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-1270">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1271">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1271">Az.Network</span></span>
* <span data-ttu-id="23c11-1272">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="23c11-1272">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="23c11-1273">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="23c11-1273">Updated cmdlet:</span></span>
        - <span data-ttu-id="23c11-1274">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-1274">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="23c11-1275">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="23c11-1275">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1276">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1276">Az.Resources</span></span>
* <span data-ttu-id="23c11-1277">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="23c11-1277">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1278">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1278">Az.Sql</span></span>
* <span data-ttu-id="23c11-1279">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="23c11-1279">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="23c11-1280">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1280">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1281">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1281">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1282">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="23c11-1282">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-1283">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1283">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-1284">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="23c11-1284">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="23c11-1285">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="23c11-1285">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1286">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1286">Az.Compute</span></span>
* <span data-ttu-id="23c11-1287">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="23c11-1287">Proximity placement group feature.</span></span>
    - <span data-ttu-id="23c11-1288">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1288">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="23c11-1289">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-1289">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="23c11-1290">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="23c11-1290">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="23c11-1291">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="23c11-1291">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="23c11-1292">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-1292">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="23c11-1293">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="23c11-1293">Breaking changes</span></span>
    - <span data-ttu-id="23c11-1294">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="23c11-1294">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="23c11-1295">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="23c11-1295">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="23c11-1296">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="23c11-1296">Az.DeploymentManager</span></span>
* <span data-ttu-id="23c11-1297">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="23c11-1297">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="23c11-1298">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="23c11-1298">Az.Dns</span></span>
* <span data-ttu-id="23c11-1299">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="23c11-1299">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="23c11-1300">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="23c11-1300">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="23c11-1301">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="23c11-1301">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="23c11-1302">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-1302">Az.FrontDoor</span></span>
* <span data-ttu-id="23c11-1303">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1303">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="23c11-1304">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="23c11-1304">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="23c11-1305">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-1305">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-1306">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-1306">Removed two cmdlets:</span></span>
    - <span data-ttu-id="23c11-1307">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="23c11-1307">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="23c11-1308">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="23c11-1308">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="23c11-1309">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="23c11-1309">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="23c11-1310">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="23c11-1310">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="23c11-1311">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="23c11-1311">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="23c11-1312">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1312">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-1313">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-1313">Az.Monitor</span></span>
* <span data-ttu-id="23c11-1314">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="23c11-1314">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="23c11-1315">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="23c11-1315">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="23c11-1316">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1316">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="23c11-1317">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="23c11-1317">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="23c11-1318">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="23c11-1318">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="23c11-1319">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="23c11-1319">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="23c11-1320">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="23c11-1320">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="23c11-1321">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1321">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="23c11-1322">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1322">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="23c11-1323">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1323">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="23c11-1324">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1324">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="23c11-1325">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1325">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="23c11-1326">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="23c11-1326">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="23c11-1327">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="23c11-1327">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1328">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1328">Az.Network</span></span>
* <span data-ttu-id="23c11-1329">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="23c11-1329">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="23c11-1330">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-1330">New cmdlets</span></span>
        - <span data-ttu-id="23c11-1331">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1331">New-AzNatGateway</span></span>
        - <span data-ttu-id="23c11-1332">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1332">Get-AzNatGateway</span></span>
        - <span data-ttu-id="23c11-1333">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1333">Set-AzNatGateway</span></span>
        - <span data-ttu-id="23c11-1334">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1334">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="23c11-1335">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="23c11-1335">Updated cmdlets</span></span>
        - <span data-ttu-id="23c11-1336">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="23c11-1336">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="23c11-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="23c11-1337">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="23c11-1338">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1338">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="23c11-1339">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1339">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="23c11-1340">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="23c11-1340">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="23c11-1341">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1341">Az.PolicyInsights</span></span>
* <span data-ttu-id="23c11-1342">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="23c11-1342">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="23c11-1343">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="23c11-1343">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="23c11-1344">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1344">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1345">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1345">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1346">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="23c11-1346">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="23c11-1347">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="23c11-1347">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="23c11-1348">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="23c11-1348">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="23c11-1349">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1349">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="23c11-1350">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="23c11-1350">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="23c11-1351">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="23c11-1351">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="23c11-1352">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="23c11-1352">Az.Relay</span></span>
* <span data-ttu-id="23c11-1353">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="23c11-1353">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-1354">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-1354">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-1355">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23c11-1355">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1356">Az.Storage</span></span>
* <span data-ttu-id="23c11-1357">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="23c11-1357">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="23c11-1358">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="23c11-1358">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="23c11-1359">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="23c11-1359">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="23c11-1360">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1360">New-AzStorageAccount</span></span>
* <span data-ttu-id="23c11-1361">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="23c11-1361">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="23c11-1362">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1362">New-AzStorageAccount</span></span>
    - <span data-ttu-id="23c11-1363">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1363">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="23c11-1364">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1364">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1365">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1365">Az.Websites</span></span>
* <span data-ttu-id="23c11-1366">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="23c11-1366">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="23c11-1367">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="23c11-1367">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="23c11-1368">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1368">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-1369">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-1369">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-1370">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="23c11-1370">General availability of `Az` module</span></span>
* <span data-ttu-id="23c11-1371">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="23c11-1371">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="23c11-1372">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="23c11-1372">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="23c11-1373">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1373">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="23c11-1374">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="23c11-1374">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="23c11-1375">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1375">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="23c11-1376">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="23c11-1376">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-1377">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1377">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1378">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="23c11-1378">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="23c11-1379">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-1379">Az.Batch</span></span>
* <span data-ttu-id="23c11-1380">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1380">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-1381">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-1381">Az.Cdn</span></span>
* <span data-ttu-id="23c11-1382">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1382">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-1383">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1383">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-1384">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1384">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1385">Az.Compute</span></span>
* <span data-ttu-id="23c11-1386">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="23c11-1386">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="23c11-1387">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1387">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1388">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="23c11-1388">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-1389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-1389">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-1390">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="23c11-1390">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1391">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1391">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1392">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1392">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="23c11-1393">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="23c11-1393">Az.EventGrid</span></span>
* <span data-ttu-id="23c11-1394">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="23c11-1394">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-1395">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1395">Az.EventHub</span></span>
* <span data-ttu-id="23c11-1396">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="23c11-1396">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="23c11-1397">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="23c11-1397">Az.HDInsight</span></span>
* <span data-ttu-id="23c11-1398">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1398">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-1399">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1399">Az.IotHub</span></span>
* <span data-ttu-id="23c11-1400">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1400">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-1401">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1401">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-1402">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1402">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1403">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="23c11-1403">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="23c11-1404">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="23c11-1404">Az.MachineLearning</span></span>
* <span data-ttu-id="23c11-1405">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1405">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="23c11-1406">Az.Media</span><span class="sxs-lookup"><span data-stu-id="23c11-1406">Az.Media</span></span>
* <span data-ttu-id="23c11-1407">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1407">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-1408">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-1408">Az.Monitor</span></span>
  * <span data-ttu-id="23c11-1409">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="23c11-1409">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="23c11-1410">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="23c11-1410">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="23c11-1411">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="23c11-1411">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="23c11-1412">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="23c11-1412">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="23c11-1413">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="23c11-1413">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="23c11-1414">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="23c11-1414">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="23c11-1415">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="23c11-1415">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1416">Az.Network</span></span>
* <span data-ttu-id="23c11-1417">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1417">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1418">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="23c11-1418">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="23c11-1419">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="23c11-1419">Az.NotificationHubs</span></span>
* <span data-ttu-id="23c11-1420">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1420">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-1421">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1421">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-1422">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1422">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="23c11-1423">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="23c11-1423">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="23c11-1424">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1424">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1425">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1425">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1426">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1426">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1427">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1427">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="23c11-1428">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="23c11-1428">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="23c11-1429">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="23c11-1429">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="23c11-1430">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="23c11-1430">Az.RedisCache</span></span>
* <span data-ttu-id="23c11-1431">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1432">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1432">Az.Resources</span></span>
* <span data-ttu-id="23c11-1433">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="23c11-1433">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1434">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1434">Az.Sql</span></span>
* <span data-ttu-id="23c11-1435">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="23c11-1435">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="23c11-1436">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1437">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="23c11-1437">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="23c11-1438">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="23c11-1438">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="23c11-1439">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="23c11-1439">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="23c11-1440">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="23c11-1440">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="23c11-1441">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="23c11-1441">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1442">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1442">Az.Websites</span></span>
* <span data-ttu-id="23c11-1443">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="23c11-1443">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="23c11-1444">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="23c11-1444">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="23c11-1445">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="23c11-1445">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="23c11-1446">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="23c11-1446">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="23c11-1447">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1447">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-1448">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-1448">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-1449">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="23c11-1449">General availability of `Az` module</span></span>
* <span data-ttu-id="23c11-1450">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="23c11-1450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="23c11-1451">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="23c11-1451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="23c11-1452">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="23c11-1453">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="23c11-1453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="23c11-1454">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="23c11-1455">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="23c11-1455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="23c11-1456">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1456">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1457">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="23c11-1457">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="23c11-1458">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1458">Az.AnalysisServices</span></span>
* <span data-ttu-id="23c11-1459">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="23c11-1459">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="23c11-1460">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="23c11-1460">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1461">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1461">Az.Automation</span></span>
* <span data-ttu-id="23c11-1462">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="23c11-1462">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="23c11-1463">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="23c11-1463">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="23c11-1464">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1464">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1465">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1465">Az.Compute</span></span>
* <span data-ttu-id="23c11-1466">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-1466">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="23c11-1467">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="23c11-1467">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="23c11-1468">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1468">Az.ContainerInstance</span></span>
* <span data-ttu-id="23c11-1469">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="23c11-1469">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-1470">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-1470">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-1471">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="23c11-1471">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="23c11-1472">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="23c11-1472">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1473">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1473">Az.Resources</span></span>
* <span data-ttu-id="23c11-1474">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="23c11-1474">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="23c11-1475">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="23c11-1475">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="23c11-1476">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="23c11-1476">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="23c11-1477">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="23c11-1477">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="23c11-1478">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="23c11-1478">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="23c11-1479">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="23c11-1479">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1480">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1480">Az.Sql</span></span>
* <span data-ttu-id="23c11-1481">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="23c11-1481">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1482">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1482">Az.Storage</span></span>
* <span data-ttu-id="23c11-1483">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="23c11-1483">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="23c11-1484">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="23c11-1484">New-AzStorageContext</span></span>
* <span data-ttu-id="23c11-1485">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="23c11-1485">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="23c11-1486">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="23c11-1486">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="23c11-1487">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="23c11-1487">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="23c11-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1488">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="23c11-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1489">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="23c11-1490">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="23c11-1490">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="23c11-1491">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="23c11-1491">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="23c11-1492">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="23c11-1492">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="23c11-1493">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="23c11-1493">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="23c11-1494">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="23c11-1494">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="23c11-1495">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1495">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="23c11-1496">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="23c11-1496">Highlights since the last major release</span></span>
* <span data-ttu-id="23c11-1497">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="23c11-1497">General availability of `Az` module</span></span>
* <span data-ttu-id="23c11-1498">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="23c11-1498">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="23c11-1499">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="23c11-1499">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="23c11-1500">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1500">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="23c11-1501">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="23c11-1501">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="23c11-1502">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1502">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="23c11-1503">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="23c11-1503">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1504">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1504">Az.Automation</span></span>
* <span data-ttu-id="23c11-1505">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c11-1505">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="23c11-1506">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="23c11-1506">Dynamic grouping</span></span>
    * <span data-ttu-id="23c11-1507">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="23c11-1507">Pre-Post script</span></span>
    * <span data-ttu-id="23c11-1508">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="23c11-1508">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1509">Az.Compute</span></span>
* <span data-ttu-id="23c11-1510">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="23c11-1510">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="23c11-1511">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="23c11-1511">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-1512">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1512">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-1513">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1513">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1514">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1514">Az.Network</span></span>
* <span data-ttu-id="23c11-1515">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1515">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="23c11-1516">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="23c11-1516">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1517">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1517">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1518">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="23c11-1518">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="23c11-1519">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="23c11-1519">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1520">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1520">Az.Resources</span></span>
* <span data-ttu-id="23c11-1521">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1521">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="23c11-1522">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="23c11-1522">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1523">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1523">Az.Sql</span></span>
* <span data-ttu-id="23c11-1524">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="23c11-1524">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1525">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1525">Az.Storage</span></span>
* <span data-ttu-id="23c11-1526">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1526">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="23c11-1527">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1527">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="23c11-1528">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1528">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="23c11-1529">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1529">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="23c11-1530">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="23c11-1530">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="23c11-1531">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="23c11-1531">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="23c11-1532">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1532">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1533">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1533">Az.Websites</span></span>
* <span data-ttu-id="23c11-1534">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="23c11-1534">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="23c11-1535">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1535">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1536">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1536">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1537">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="23c11-1537">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="23c11-1538">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1538">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1539">Az.Automation</span></span>
* <span data-ttu-id="23c11-1540">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1540">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="23c11-1541">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="23c11-1541">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="23c11-1542">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="23c11-1542">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-1543">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-1543">Az.Cdn</span></span>
* <span data-ttu-id="23c11-1544">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="23c11-1544">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1545">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1545">Az.Compute</span></span>
* <span data-ttu-id="23c11-1546">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="23c11-1546">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-1547">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-1547">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-1548">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="23c11-1548">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="23c11-1549">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="23c11-1549">Az.LogicApp</span></span>
* <span data-ttu-id="23c11-1550">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="23c11-1550">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1551">Az.Network</span></span>
* <span data-ttu-id="23c11-1552">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1552">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1553">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1553">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1554">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1554">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="23c11-1555">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="23c11-1555">SDK Update</span></span>
* <span data-ttu-id="23c11-1556">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="23c11-1556">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="23c11-1557">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="23c11-1557">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1558">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1558">Az.Resources</span></span>
* <span data-ttu-id="23c11-1559">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="23c11-1559">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="23c11-1560">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="23c11-1560">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="23c11-1561">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="23c11-1561">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="23c11-1562">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="23c11-1562">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="23c11-1563">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="23c11-1563">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="23c11-1564">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="23c11-1564">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1565">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1565">Az.Sql</span></span>
* <span data-ttu-id="23c11-1566">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="23c11-1566">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="23c11-1567">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="23c11-1567">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1568">Az.Storage</span></span>
* <span data-ttu-id="23c11-1569">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1569">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="23c11-1570">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1570">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="23c11-1571">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1571">Az.AnalysisServices</span></span>
* <span data-ttu-id="23c11-1572">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="23c11-1572">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1573">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1573">Az.Automation</span></span>
* <span data-ttu-id="23c11-1574">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1574">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="23c11-1575">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1575">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="23c11-1576">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1576">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-1577">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1577">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-1578">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="23c11-1578">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1579">Az.Compute</span></span>
* <span data-ttu-id="23c11-1580">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="23c11-1580">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="23c11-1581">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="23c11-1581">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="23c11-1582">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="23c11-1582">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="23c11-1583">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="23c11-1583">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1584">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1584">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1585">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="23c11-1585">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="23c11-1586">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1586">Az.EventHub</span></span>
* <span data-ttu-id="23c11-1587">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="23c11-1587">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1588">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-1589">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23c11-1589">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="23c11-1590">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="23c11-1590">Az.LogicApp</span></span>
* <span data-ttu-id="23c11-1591">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1591">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="23c11-1592">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="23c11-1592">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="23c11-1593">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1593">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="23c11-1594">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="23c11-1594">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="23c11-1595">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="23c11-1595">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="23c11-1596">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="23c11-1596">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="23c11-1597">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="23c11-1597">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="23c11-1598">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1598">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="23c11-1599">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1599">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="23c11-1600">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1600">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="23c11-1601">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1601">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="23c11-1602">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1602">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="23c11-1603">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="23c11-1603">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="23c11-1604">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-1604">Az.Monitor</span></span>
* <span data-ttu-id="23c11-1605">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="23c11-1605">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1606">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1606">Az.Network</span></span>
* <span data-ttu-id="23c11-1607">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="23c11-1607">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-1608">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1608">Az.OperationalInsights</span></span>
* <span data-ttu-id="23c11-1609">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="23c11-1609">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="23c11-1610">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="23c11-1610">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="23c11-1611">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="23c11-1611">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="23c11-1612">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1612">Az.Resources</span></span>
* <span data-ttu-id="23c11-1613">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="23c11-1613">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="23c11-1614">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="23c11-1614">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="23c11-1615">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="23c11-1615">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="23c11-1616">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="23c11-1616">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1617">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1617">Az.Sql</span></span>
* <span data-ttu-id="23c11-1618">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="23c11-1618">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="23c11-1619">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="23c11-1619">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1620">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1620">Az.Websites</span></span>
* <span data-ttu-id="23c11-1621">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="23c11-1621">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="23c11-1622">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1622">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1623">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1623">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1624">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="23c11-1624">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="23c11-1625">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1625">Az.AnalysisServices</span></span>
<span data-ttu-id="23c11-1626">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="23c11-1626">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1627">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1627">Az.Compute</span></span>
* <span data-ttu-id="23c11-1628">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="23c11-1628">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="23c11-1629">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="23c11-1629">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="23c11-1630">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="23c11-1630">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1631">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1631">Az.RecoveryServices</span></span>
<span data-ttu-id="23c11-1632">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="23c11-1632">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1633">Az.Resources</span></span>
* <span data-ttu-id="23c11-1634">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="23c11-1634">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="23c11-1635">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="23c11-1635">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="23c11-1636">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="23c11-1636">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="23c11-1637">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="23c11-1637">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1638">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1638">Az.Sql</span></span>
* <span data-ttu-id="23c11-1639">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="23c11-1639">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="23c11-1640">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="23c11-1640">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="23c11-1641">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="23c11-1641">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="23c11-1642">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1642">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1643">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1643">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1644">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1644">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="23c11-1645">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1645">Az.AnalysisServices</span></span>
* <span data-ttu-id="23c11-1646">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1646">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1647">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1647">Az.RecoveryServices</span></span>
* <span data-ttu-id="23c11-1648">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1648">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="23c11-1649">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1649">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1650">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1650">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1651">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="23c11-1651">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="23c11-1652">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="23c11-1653">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="23c11-1653">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="23c11-1654">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="23c11-1654">Az.Aks</span></span>
* <span data-ttu-id="23c11-1655">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1655">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="23c11-1656">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1656">Az.Automation</span></span>
* <span data-ttu-id="23c11-1657">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="23c11-1657">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="23c11-1658">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1658">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="23c11-1659">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="23c11-1659">Az.Cdn</span></span>
* <span data-ttu-id="23c11-1660">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1660">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1661">Az.Compute</span></span>
* <span data-ttu-id="23c11-1662">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="23c11-1662">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="23c11-1663">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="23c11-1663">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="23c11-1664">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="23c11-1664">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="23c11-1665">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="23c11-1665">Az.ContainerRegistry</span></span>
* <span data-ttu-id="23c11-1666">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1666">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="23c11-1667">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="23c11-1667">Az.DataFactory</span></span>
* <span data-ttu-id="23c11-1668">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="23c11-1668">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1669">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1670">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="23c11-1670">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="23c11-1671">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="23c11-1671">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="23c11-1672">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1672">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-1673">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1673">Az.IotHub</span></span>
* <span data-ttu-id="23c11-1674">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="23c11-1674">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="23c11-1675">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1675">Az.KeyVault</span></span>
* <span data-ttu-id="23c11-1676">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1676">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1677">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1677">Az.Network</span></span>
* <span data-ttu-id="23c11-1678">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1678">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1679">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1679">Az.Resources</span></span>
* <span data-ttu-id="23c11-1680">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="23c11-1680">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="23c11-1681">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="23c11-1681">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="23c11-1682">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="23c11-1682">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="23c11-1683">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="23c11-1683">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="23c11-1684">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="23c11-1684">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="23c11-1685">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="23c11-1685">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="23c11-1686">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="23c11-1686">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-1687">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1687">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-1688">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="23c11-1688">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="23c11-1689">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="23c11-1689">Fix some error messages.</span></span>
* <span data-ttu-id="23c11-1690">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="23c11-1690">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="23c11-1691">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1691">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="23c11-1692">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="23c11-1692">Az.SignalR</span></span>
* <span data-ttu-id="23c11-1693">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1693">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1694">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1694">Az.Sql</span></span>
* <span data-ttu-id="23c11-1695">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1695">Update incorrect online help URLs</span></span>
* <span data-ttu-id="23c11-1696">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="23c11-1696">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="23c11-1697">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="23c11-1697">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="23c11-1698">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="23c11-1698">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1699">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1699">Az.Storage</span></span>
* <span data-ttu-id="23c11-1700">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1700">Update incorrect online help URLs</span></span>
* <span data-ttu-id="23c11-1701">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="23c11-1701">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="23c11-1702">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="23c11-1702">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="23c11-1703">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="23c11-1703">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="23c11-1704">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="23c11-1704">Az.TrafficManager</span></span>
* <span data-ttu-id="23c11-1705">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1705">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1706">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1706">Az.Websites</span></span>
* <span data-ttu-id="23c11-1707">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="23c11-1707">Update incorrect online help URLs</span></span>
* <span data-ttu-id="23c11-1708">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1708">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="23c11-1709">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="23c11-1709">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="23c11-1710">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="23c11-1710">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="23c11-1711">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1711">Az.Accounts</span></span>
* <span data-ttu-id="23c11-1712">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="23c11-1712">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1713">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1713">Az.Compute</span></span>
* <span data-ttu-id="23c11-1714">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="23c11-1714">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="23c11-1715">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="23c11-1715">Updated the description of ID in help files</span></span>
* <span data-ttu-id="23c11-1716">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1716">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1717">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1717">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1718">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="23c11-1718">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="23c11-1719">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="23c11-1719">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="23c11-1720">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="23c11-1720">Az.EventGrid</span></span>
* <span data-ttu-id="23c11-1721">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="23c11-1721">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="23c11-1722">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="23c11-1722">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="23c11-1723">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="23c11-1723">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="23c11-1724">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="23c11-1724">Event Time-To-Live,</span></span>
        - <span data-ttu-id="23c11-1725">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="23c11-1725">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="23c11-1726">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="23c11-1726">Dead letter endpoint.</span></span>
    - <span data-ttu-id="23c11-1727">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="23c11-1727">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="23c11-1728">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="23c11-1728">Event Time-To-Live,</span></span>
        - <span data-ttu-id="23c11-1729">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="23c11-1729">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="23c11-1730">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="23c11-1730">Dead letter endpoint.</span></span>
* <span data-ttu-id="23c11-1731">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="23c11-1731">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="23c11-1732">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="23c11-1732">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="23c11-1733">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1733">Az.IotHub</span></span>
* <span data-ttu-id="23c11-1734">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="23c11-1734">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="23c11-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="23c11-1735">Az.LogicApp</span></span>
* <span data-ttu-id="23c11-1736">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="23c11-1736">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1737">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1737">Az.Resources</span></span>
* <span data-ttu-id="23c11-1738">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="23c11-1738">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="23c11-1739">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="23c11-1739">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="23c11-1740">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23c11-1740">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="23c11-1741">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="23c11-1741">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="23c11-1742">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="23c11-1742">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="23c11-1743">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="23c11-1743">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="23c11-1744">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="23c11-1744">Az.SignalR</span></span>
* <span data-ttu-id="23c11-1745">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1745">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-1746">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1746">Az.Sql</span></span>
* <span data-ttu-id="23c11-1747">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="23c11-1747">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="23c11-1748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1748">Az.Storage</span></span>
* <span data-ttu-id="23c11-1749">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="23c11-1749">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="23c11-1750">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="23c11-1750">New-AzStorageContext</span></span>
* <span data-ttu-id="23c11-1751">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="23c11-1751">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="23c11-1752">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="23c11-1752">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-1753">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1753">Az.Websites</span></span>
* <span data-ttu-id="23c11-1754">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="23c11-1754">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="23c11-1755">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1755">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="23c11-1756">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1756">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="23c11-1757">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-1757">General</span></span>

- <span data-ttu-id="23c11-1758">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="23c11-1758">General Availability of Az Module</span></span>
- <span data-ttu-id="23c11-1759">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="23c11-1759">Online help for each module</span></span>
- <span data-ttu-id="23c11-1760">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="23c11-1760">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="23c11-1761">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="23c11-1761">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="23c11-1762">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1762">Az.Accounts</span></span>
- <span data-ttu-id="23c11-1763">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="23c11-1763">Changed from Az.Profile</span></span>
- <span data-ttu-id="23c11-1764">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="23c11-1764">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="23c11-1765">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-1765">Az.ApiManagement</span></span>
- <span data-ttu-id="23c11-1766">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="23c11-1766">Fixes for #7002</span></span>
- <span data-ttu-id="23c11-1767">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="23c11-1768">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="23c11-1768">Az.Batch</span></span>
- <span data-ttu-id="23c11-1769">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="23c11-1769">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="23c11-1770">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="23c11-1770">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="23c11-1771">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1771">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="23c11-1772">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="23c11-1772">Az.Billing</span></span>
- <span data-ttu-id="23c11-1773">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1773">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="23c11-1774">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1774">Az.CognitivServices</span></span>
- <span data-ttu-id="23c11-1775">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1775">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="23c11-1776">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="23c11-1776">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="23c11-1777">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1777">Az.ContainerInstance</span></span>
- <span data-ttu-id="23c11-1778">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="23c11-1778">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="23c11-1779">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="23c11-1779">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="23c11-1780">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1781">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1781">Az.DataLakeStore</span></span>
- <span data-ttu-id="23c11-1782">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1782">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="23c11-1783">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="23c11-1783">Az.Monitor</span></span>
- <span data-ttu-id="23c11-1784">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1784">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="23c11-1785">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="23c11-1785">Az.KeyVault</span></span>
- <span data-ttu-id="23c11-1786">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="23c11-1786">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="23c11-1787">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="23c11-1787">Az.MachineLearning</span></span>
- <span data-ttu-id="23c11-1788">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="23c11-1788">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="23c11-1789">Az.Media</span><span class="sxs-lookup"><span data-stu-id="23c11-1789">Az.Media</span></span>
- <span data-ttu-id="23c11-1790">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="23c11-1790">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="23c11-1791">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1791">Az.Network</span></span>
<span data-ttu-id="23c11-1792">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1792">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="23c11-1793">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="23c11-1793">New cmdlets added:</span></span>
        - <span data-ttu-id="23c11-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1794">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1795">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1796">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1797">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1798">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1799">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1799">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="23c11-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1800">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="23c11-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="23c11-1801">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="23c11-1802">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="23c11-1802">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="23c11-1803">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23c11-1803">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="23c11-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1804">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="23c11-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="23c11-1805">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="23c11-1806">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-1806">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="23c11-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-1807">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="23c11-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="23c11-1808">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="23c11-1809">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="23c11-1809">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="23c11-1810">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23c11-1810">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="23c11-1811">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23c11-1811">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="23c11-1812">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="23c11-1812">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="23c11-1813">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="23c11-1813">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="23c11-1814">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1814">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="23c11-1815">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1815">Az.OperationalInsights</span></span>
- <span data-ttu-id="23c11-1816">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="23c11-1817">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="23c11-1817">Az.Profile</span></span>
- <span data-ttu-id="23c11-1818">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="23c11-1818">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1819">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1819">Az.RecoveryServices</span></span>
- <span data-ttu-id="23c11-1820">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="23c11-1821">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1821">Az.Resources</span></span>
- <span data-ttu-id="23c11-1822">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1822">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="23c11-1823">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1823">Az.ServiceFabric</span></span>
- <span data-ttu-id="23c11-1824">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="23c11-1824">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="23c11-1825">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1825">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="23c11-1826">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="23c11-1826">Az.SIgnalR</span></span>
- <span data-ttu-id="23c11-1827">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="23c11-1827">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="23c11-1828">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1828">Az.Sql</span></span>
- <span data-ttu-id="23c11-1829">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="23c11-1829">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="23c11-1830">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1830">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="23c11-1831">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="23c11-1832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1832">Az.Storage</span></span>
- <span data-ttu-id="23c11-1833">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1833">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="23c11-1834">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1834">Az.Websites</span></span>
- <span data-ttu-id="23c11-1835">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="23c11-1835">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="23c11-1836">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1836">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="23c11-1837">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-1837">General</span></span>

* <span data-ttu-id="23c11-1838">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="23c11-1838">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="23c11-1839">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1839">Az.Compute</span></span>

* <span data-ttu-id="23c11-1840">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="23c11-1840">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1841">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1841">Az.DataLakeStore</span></span>

* <span data-ttu-id="23c11-1842">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="23c11-1842">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="23c11-1843">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="23c11-1843">Az.FrontDoor</span></span>

* <span data-ttu-id="23c11-1844">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="23c11-1844">Fixed some broken links</span></span>
    - <span data-ttu-id="23c11-1845">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="23c11-1845">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="23c11-1846">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="23c11-1846">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="23c11-1847">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1847">Az.RecoveryServices</span></span>

* <span data-ttu-id="23c11-1848">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1848">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="23c11-1849">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="23c11-1849">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="23c11-1850">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1850">Az.Resources</span></span>

* <span data-ttu-id="23c11-1851">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="23c11-1851">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="23c11-1852">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="23c11-1852">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="23c11-1853">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1853">Az.Sql</span></span>

* <span data-ttu-id="23c11-1854">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="23c11-1854">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="23c11-1855">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="23c11-1855">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="23c11-1856">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="23c11-1856">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="23c11-1857">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1857">Az.Storage</span></span>

* <span data-ttu-id="23c11-1858">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1858">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="23c11-1859">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="23c11-1859">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="23c11-1860">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-1860">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="23c11-1861">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="23c11-1861">Support Static Website configuration</span></span>
    - <span data-ttu-id="23c11-1862">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="23c11-1862">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="23c11-1863">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="23c11-1863">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="23c11-1864">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-1864">Az.Websites</span></span>

* <span data-ttu-id="23c11-1865">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="23c11-1865">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="23c11-1866">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="23c11-1866">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="23c11-1867">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="23c11-1867">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="23c11-1868">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1868">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="23c11-1869">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="23c11-1869">Az.ApiManagement</span></span>
* <span data-ttu-id="23c11-1870">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="23c11-1870">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="23c11-1871">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="23c11-1871">Az.Automation</span></span>
* <span data-ttu-id="23c11-1872">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="23c11-1872">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="23c11-1873">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="23c11-1873">Added Update Management cmdlets</span></span>
* <span data-ttu-id="23c11-1874">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="23c11-1874">Added Source Control cmdlets</span></span>
* <span data-ttu-id="23c11-1875">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="23c11-1875">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="23c11-1876">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="23c11-1876">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="23c11-1877">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1877">Az.Compute</span></span>
* <span data-ttu-id="23c11-1878">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="23c11-1878">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="23c11-1879">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="23c11-1879">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="23c11-1880">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1880">Az.ContainerInstance</span></span>
* <span data-ttu-id="23c11-1881">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="23c11-1881">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="23c11-1882">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="23c11-1882">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="23c11-1883">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="23c11-1883">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="23c11-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1884">Az.Network</span></span>
* <span data-ttu-id="23c11-1885">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="23c11-1885">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="23c11-1886">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="23c11-1886">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="23c11-1887">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1887">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="23c11-1888">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="23c11-1888">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="23c11-1889">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="23c11-1889">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="23c11-1890">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="23c11-1890">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="23c11-1891">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="23c11-1891">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="23c11-1892">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="23c11-1892">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="23c11-1893">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="23c11-1893">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="23c11-1894">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="23c11-1894">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="23c11-1895">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="23c11-1895">Az.Relay</span></span>
* <span data-ttu-id="23c11-1896">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="23c11-1896">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="23c11-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1897">Az.Resources</span></span>
* <span data-ttu-id="23c11-1898">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="23c11-1898">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="23c11-1899">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="23c11-1899">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="23c11-1900">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="23c11-1900">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="23c11-1901">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1901">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-1902">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="23c11-1902">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="23c11-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-1903">Az.Sql</span></span>
* <span data-ttu-id="23c11-1904">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="23c11-1904">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="23c11-1905">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1905">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="23c11-1906">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1906">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="23c11-1907">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1907">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="23c11-1908">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="23c11-1908">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="23c11-1909">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="23c11-1909">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="23c11-1910">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="23c11-1910">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="23c11-1911">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="23c11-1911">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="23c11-1912">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="23c11-1912">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="23c11-1913">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="23c11-1913">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="23c11-1914">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="23c11-1914">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="23c11-1915">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="23c11-1915">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="23c11-1916">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="23c11-1916">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="23c11-1917">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="23c11-1917">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="23c11-1918">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="23c11-1918">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="23c11-1919">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="23c11-1919">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="23c11-1920">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1920">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="23c11-1921">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1921">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="23c11-1922">Generale</span><span class="sxs-lookup"><span data-stu-id="23c11-1922">General</span></span>
* <span data-ttu-id="23c11-1923">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="23c11-1923">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="23c11-1924">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="23c11-1924">Az.Profile</span></span>
* <span data-ttu-id="23c11-1925">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="23c11-1925">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="23c11-1926">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="23c11-1926">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="23c11-1927">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="23c11-1927">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="23c11-1928">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="23c11-1928">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="23c11-1929">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="23c11-1929">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="23c11-1930">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="23c11-1930">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="23c11-1931">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="23c11-1931">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-1932">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1932">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-1933">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="23c11-1933">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1934">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1934">Az.Compute</span></span>
* <span data-ttu-id="23c11-1935">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="23c11-1935">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="23c11-1936">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="23c11-1936">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="23c11-1937">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="23c11-1937">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1938">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1938">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1939">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="23c11-1939">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="23c11-1940">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="23c11-1940">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="23c11-1941">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="23c11-1941">Az.Insights</span></span>
* <span data-ttu-id="23c11-1942">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="23c11-1942">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="23c11-1943">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="23c11-1943">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="23c11-1944">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1944">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="23c11-1945">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="23c11-1945">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1946">Az.Network</span></span>
* <span data-ttu-id="23c11-1947">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="23c11-1947">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="23c11-1948">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-1948">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="23c11-1949">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="23c11-1949">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="23c11-1950">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="23c11-1950">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="23c11-1951">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="23c11-1951">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="23c11-1952">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="23c11-1952">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="23c11-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="23c11-1953">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="23c11-1954">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="23c11-1954">Az.PolicyInsights</span></span>
* <span data-ttu-id="23c11-1955">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="23c11-1955">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1956">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1956">Az.Resources</span></span>
* <span data-ttu-id="23c11-1957">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="23c11-1957">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="23c11-1958">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="23c11-1958">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="23c11-1959">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="23c11-1959">Az.ServiceBus</span></span>
* <span data-ttu-id="23c11-1960">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="23c11-1960">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="23c11-1961">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c11-1961">Az.ServiceFabric</span></span>
* <span data-ttu-id="23c11-1962">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="23c11-1962">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="23c11-1963">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="23c11-1963">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="23c11-1964">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="23c11-1964">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="23c11-1965">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="23c11-1965">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="23c11-1966">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="23c11-1966">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="23c11-1967">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1967">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="23c11-1968">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="23c11-1968">Az.Profile</span></span>
* <span data-ttu-id="23c11-1969">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="23c11-1969">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="23c11-1970">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="23c11-1970">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1971">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1971">Az.Compute</span></span>
* <span data-ttu-id="23c11-1972">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="23c11-1972">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="23c11-1973">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c11-1973">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="23c11-1974">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="23c11-1974">Az.DataLakeStore</span></span>
* <span data-ttu-id="23c11-1975">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="23c11-1975">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="23c11-1976">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23c11-1976">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="23c11-1977">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="23c11-1977">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="23c11-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="23c11-1978">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="23c11-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="23c11-1979">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-1980">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-1980">Az.Network</span></span>
* <span data-ttu-id="23c11-1981">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="23c11-1981">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="23c11-1982">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23c11-1982">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-1983">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-1983">Az.Resources</span></span>
* <span data-ttu-id="23c11-1984">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="23c11-1984">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="23c11-1985">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="23c11-1985">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="23c11-1986">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-1986">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="23c11-1987">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="23c11-1987">Azure.Storage</span></span>
* <span data-ttu-id="23c11-1988">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="23c11-1988">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="23c11-1989">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-1989">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="23c11-1990">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="23c11-1990">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="23c11-1991">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="23c11-1991">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="23c11-1992">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="23c11-1992">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="23c11-1993">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="23c11-1993">Az.CognitiveServices</span></span>
* <span data-ttu-id="23c11-1994">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="23c11-1994">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="23c11-1995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="23c11-1995">Az.Compute</span></span>
* <span data-ttu-id="23c11-1996">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="23c11-1996">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="23c11-1997">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="23c11-1997">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="23c11-1998">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="23c11-1998">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="23c11-1999">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="23c11-1999">Az.DataFactoryV2</span></span>
* <span data-ttu-id="23c11-2000">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="23c11-2000">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="23c11-2001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="23c11-2001">Az.Network</span></span>
* <span data-ttu-id="23c11-2002">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-2002">Added NetworkProfile functionality.</span></span> <span data-ttu-id="23c11-2003">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="23c11-2003">new cmdlets added</span></span>
    - <span data-ttu-id="23c11-2004">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-2004">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="23c11-2005">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-2005">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="23c11-2006">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-2006">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="23c11-2007">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="23c11-2007">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="23c11-2008">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-2008">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="23c11-2009">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-2009">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="23c11-2010">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="23c11-2010">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="23c11-2011">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="23c11-2011">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="23c11-2012">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="23c11-2012">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="23c11-2013">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="23c11-2013">Az.RedisCache</span></span>
* <span data-ttu-id="23c11-2014">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="23c11-2014">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="23c11-2015">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="23c11-2015">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="23c11-2016">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="23c11-2016">Az.Resources</span></span>
* <span data-ttu-id="23c11-2017">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23c11-2017">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="23c11-2018">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="23c11-2018">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="23c11-2019">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="23c11-2019">Az.Sql</span></span>
* <span data-ttu-id="23c11-2020">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="23c11-2020">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="23c11-2021">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="23c11-2021">Az.Websites</span></span>
* <span data-ttu-id="23c11-2022">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="23c11-2022">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="23c11-2023">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="23c11-2023">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="23c11-2024">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="23c11-2024">0.2.0 - September 2018</span></span>
 <span data-ttu-id="23c11-2025">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="23c11-2025">Initial Release</span></span>
