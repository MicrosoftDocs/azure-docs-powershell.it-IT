---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 694439934afb41b465a89188d59bc964db3c0032
ms.sourcegitcommit: 9181f20c2c5eaa271150de9e25b9cb30ba5e6cb0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2020
ms.locfileid: "77002674"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="daa2e-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="daa2e-103">Azure PowerShell release notes</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="daa2e-104">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="daa2e-104">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="daa2e-105">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="daa2e-105">Highlights since the last major release</span></span>
* <span data-ttu-id="daa2e-106">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="daa2e-106">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="daa2e-107">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="daa2e-107">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-108">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-108">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-109">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="daa2e-109">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="daa2e-110">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="daa2e-110">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-111">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-111">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-112">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="daa2e-112">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="daa2e-113">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="daa2e-113">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="daa2e-114">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="daa2e-114">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="daa2e-115">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-115">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-116">Az.Compute</span></span>
* <span data-ttu-id="daa2e-117">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-117">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="daa2e-118">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-118">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="daa2e-119">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-119">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="daa2e-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-120">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="daa2e-121">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="daa2e-121">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-122">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-123">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-123">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="daa2e-124">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="daa2e-124">Az.DeploymentManager</span></span>
* <span data-ttu-id="daa2e-125">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="daa2e-125">Adds LIST operations for resources</span></span>
* <span data-ttu-id="daa2e-126">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="daa2e-126">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-127">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-127">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-128">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="daa2e-128">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-129">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-130">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="daa2e-130">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-131">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-131">Az.Network</span></span>
* <span data-ttu-id="daa2e-132">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="daa2e-132">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="daa2e-133">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="daa2e-133">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="daa2e-134">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="daa2e-134">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="daa2e-135">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="daa2e-135">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="daa2e-136">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="daa2e-136">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="daa2e-137">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="daa2e-137">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="daa2e-138">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="daa2e-138">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="daa2e-139">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-139">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="daa2e-140">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-140">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-141">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="daa2e-142">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-142">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="daa2e-143">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-143">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="daa2e-144">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="daa2e-144">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="daa2e-145">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-145">Az.PolicyInsights</span></span>
* <span data-ttu-id="daa2e-146">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="daa2e-146">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="daa2e-147">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="daa2e-147">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="daa2e-148">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="daa2e-148">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="daa2e-149">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="daa2e-149">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-150">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-150">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-151">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="daa2e-151">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="daa2e-152">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="daa2e-152">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-153">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-153">Az.Resources</span></span>
* <span data-ttu-id="daa2e-154">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="daa2e-154">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="daa2e-155">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="daa2e-155">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-156">Az.Sql</span></span>
<span data-ttu-id="daa2e-157">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="daa2e-157">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-158">Az.Storage</span></span>
* <span data-ttu-id="daa2e-159">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-159">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="daa2e-160">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-160">New-AzStorageAccount</span></span>
* <span data-ttu-id="daa2e-161">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="daa2e-161">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="daa2e-162">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-162">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-163">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-163">Az.Websites</span></span>
* <span data-ttu-id="daa2e-164">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="daa2e-164">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="daa2e-165">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="daa2e-165">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="daa2e-166">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="daa2e-166">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-167">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-167">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-168">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="daa2e-168">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-169">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-169">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-170">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-170">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-171">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-171">Az.Compute</span></span>
* <span data-ttu-id="daa2e-172">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="daa2e-172">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="daa2e-173">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-173">Az.ContainerInstance</span></span>
* <span data-ttu-id="daa2e-174">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-174">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="daa2e-175">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="daa2e-175">Az.DataBoxEdge</span></span>
* <span data-ttu-id="daa2e-176">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-176">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="daa2e-177">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-177">Get the Edge Storage Container</span></span>
* <span data-ttu-id="daa2e-178">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-178">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="daa2e-179">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-179">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="daa2e-180">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-180">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="daa2e-181">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-181">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="daa2e-182">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-182">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="daa2e-183">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-183">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="daa2e-184">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="daa2e-184">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="daa2e-185">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-185">Get the Edge Storage Account</span></span>
* <span data-ttu-id="daa2e-186">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="daa2e-186">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="daa2e-187">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-187">Create new Edge Storage Account</span></span>
* <span data-ttu-id="daa2e-188">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="daa2e-188">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="daa2e-189">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="daa2e-189">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="daa2e-190">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="daa2e-190">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="daa2e-191">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="daa2e-191">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="daa2e-192">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="daa2e-192">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="daa2e-193">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="daa2e-193">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-194">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-194">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-195">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="daa2e-195">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="daa2e-196">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-196">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="daa2e-197">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="daa2e-197">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="daa2e-198">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="daa2e-198">Az.DevTestLabs</span></span>
* <span data-ttu-id="daa2e-199">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="daa2e-199">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-200">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-200">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-201">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="daa2e-201">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-202">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-202">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-203">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="daa2e-203">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="daa2e-204">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="daa2e-204">Az.MachineLearning</span></span>
* <span data-ttu-id="daa2e-205">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="daa2e-205">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="daa2e-206">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="daa2e-206">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="daa2e-207">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-207">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="daa2e-208">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="daa2e-208">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="daa2e-209">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="daa2e-209">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="daa2e-210">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="daa2e-210">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="daa2e-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="daa2e-211">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="daa2e-212">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="daa2e-212">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-213">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-213">Az.Network</span></span>
* <span data-ttu-id="daa2e-214">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="daa2e-214">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-215">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-215">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-216">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-216">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="daa2e-217">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-217">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="daa2e-218">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-218">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="daa2e-219">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-219">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-220">Az.Resources</span></span>
* <span data-ttu-id="daa2e-221">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-221">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-222">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-222">Az.Sql</span></span>
* <span data-ttu-id="daa2e-223">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="daa2e-223">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="daa2e-224">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="daa2e-224">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="daa2e-225">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="daa2e-225">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="daa2e-226">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="daa2e-226">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-227">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-227">Az.Storage</span></span>
* <span data-ttu-id="daa2e-228">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="daa2e-228">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="daa2e-229">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-229">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="daa2e-230">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="daa2e-230">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="daa2e-231">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-231">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="daa2e-232">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-232">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="daa2e-233">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-233">General</span></span>
* <span data-ttu-id="daa2e-234">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="daa2e-234">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-235">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-235">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-236">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-236">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="daa2e-237">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-237">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="daa2e-238">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-238">Az.Batch</span></span>
* <span data-ttu-id="daa2e-239">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="daa2e-239">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-240">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-240">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-241">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-241">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-242">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-242">Az.FrontDoor</span></span>
* <span data-ttu-id="daa2e-243">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="daa2e-243">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="daa2e-244">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="daa2e-244">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="daa2e-245">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="daa2e-245">Az.HealthcareApis</span></span>
* <span data-ttu-id="daa2e-246">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="daa2e-246">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-247">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-247">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-248">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="daa2e-248">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="daa2e-249">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="daa2e-249">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="daa2e-250">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="daa2e-250">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-251">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-251">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-252">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="daa2e-252">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="daa2e-253">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="daa2e-253">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="daa2e-254">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="daa2e-254">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-255">Az.Network</span></span>
* <span data-ttu-id="daa2e-256">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="daa2e-256">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-257">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-257">Az.Resources</span></span>
* <span data-ttu-id="daa2e-258">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="daa2e-258">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="daa2e-259">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="daa2e-259">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-260">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-260">Az.Sql</span></span>
* <span data-ttu-id="daa2e-261">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="daa2e-261">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-262">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-262">Az.Storage</span></span>
* <span data-ttu-id="daa2e-263">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="daa2e-263">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="daa2e-264">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="daa2e-264">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="daa2e-265">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="daa2e-265">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="daa2e-266">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="daa2e-266">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="daa2e-267">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="daa2e-267">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="daa2e-268">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="daa2e-268">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="daa2e-269">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-269">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="daa2e-270">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-270">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="daa2e-271">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-271">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="daa2e-272">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="daa2e-272">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="daa2e-273">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="daa2e-273">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="daa2e-274">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="daa2e-274">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="daa2e-275">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="daa2e-275">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="daa2e-276">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-276">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="daa2e-277">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="daa2e-277">Highlights since the last major release</span></span>
* <span data-ttu-id="daa2e-278">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-278">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="daa2e-279">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-279">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-280">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-280">Az.Compute</span></span>
* <span data-ttu-id="daa2e-281">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-281">VM Reapply feature</span></span>
    - <span data-ttu-id="daa2e-282">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-282">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="daa2e-283">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="daa2e-283">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="daa2e-284">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-284">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="daa2e-285">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-285">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="daa2e-286">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-286">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="daa2e-287">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="daa2e-287">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="daa2e-288">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="daa2e-288">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="daa2e-289">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="daa2e-289">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="daa2e-290">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="daa2e-290">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="daa2e-291">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-291">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="daa2e-292">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="daa2e-292">Az.DataBoxEdge</span></span>
* <span data-ttu-id="daa2e-293">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="daa2e-293">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="daa2e-294">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="daa2e-294">Get the Order</span></span>
* <span data-ttu-id="daa2e-295">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="daa2e-295">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="daa2e-296">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="daa2e-296">Create new Order</span></span>
* <span data-ttu-id="daa2e-297">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="daa2e-297">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="daa2e-298">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="daa2e-298">Remove the Order</span></span>
* <span data-ttu-id="daa2e-299">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="daa2e-299">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="daa2e-300">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="daa2e-300">Now creates Local Share</span></span>
* <span data-ttu-id="daa2e-301">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="daa2e-301">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="daa2e-302">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="daa2e-302">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="daa2e-303">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="daa2e-303">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="daa2e-304">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="daa2e-304">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="daa2e-305">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="daa2e-305">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="daa2e-306">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="daa2e-306">Gets the information about Triggers</span></span>
* <span data-ttu-id="daa2e-307">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="daa2e-307">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="daa2e-308">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="daa2e-308">Create new Triggers</span></span>
* <span data-ttu-id="daa2e-309">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="daa2e-309">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="daa2e-310">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="daa2e-310">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-311">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-311">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-312">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-312">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="daa2e-313">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="daa2e-313">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-314">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-314">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-315">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="daa2e-315">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-316">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-316">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-317">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="daa2e-317">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-318">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-318">Az.FrontDoor</span></span>
* <span data-ttu-id="daa2e-319">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-319">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="daa2e-320">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-320">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="daa2e-321">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-321">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="daa2e-322">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-322">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-323">Az.Network</span></span>
* <span data-ttu-id="daa2e-324">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-324">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="daa2e-325">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="daa2e-325">Az.PrivateDns</span></span>
* <span data-ttu-id="daa2e-326">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-326">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-327">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-327">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-328">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-328">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="daa2e-329">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="daa2e-329">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="daa2e-330">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-330">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="daa2e-331">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="daa2e-331">Az.RedisCache</span></span>
* <span data-ttu-id="daa2e-332">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-332">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="daa2e-333">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-333">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="daa2e-334">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="daa2e-334">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-335">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-335">Az.Resources</span></span>
- <span data-ttu-id="daa2e-336">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="daa2e-336">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="daa2e-337">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-337">Updated create policy definition help example</span></span>
- <span data-ttu-id="daa2e-338">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="daa2e-338">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="daa2e-339">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="daa2e-339">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="daa2e-340">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="daa2e-340">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-341">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-341">Az.Sql</span></span>
* <span data-ttu-id="daa2e-342">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="daa2e-342">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="daa2e-343">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="daa2e-343">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="daa2e-344">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-344">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="daa2e-345">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-345">General</span></span>
* <span data-ttu-id="daa2e-346">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-346">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-347">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-348">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-348">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="daa2e-349">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="daa2e-349">Az.Advisor</span></span>
* <span data-ttu-id="daa2e-350">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="daa2e-350">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="daa2e-351">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-351">Az.Batch</span></span>
* <span data-ttu-id="daa2e-352">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-352">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="daa2e-353">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-353">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="daa2e-354">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-354">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="daa2e-355">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-355">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="daa2e-356">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-356">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="daa2e-357">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-357">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="daa2e-358">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="daa2e-358">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="daa2e-359">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="daa2e-359">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="daa2e-360">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="daa2e-360">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="daa2e-361">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-361">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="daa2e-362">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-362">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="daa2e-363">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-363">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="daa2e-364">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-364">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="daa2e-365">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-365">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="daa2e-366">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-366">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="daa2e-367">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-367">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="daa2e-368">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-368">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="daa2e-369">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-369">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="daa2e-370">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-370">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="daa2e-371">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="daa2e-371">This operation is no longer supported.</span></span>
* <span data-ttu-id="daa2e-372">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-372">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="daa2e-373">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-373">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="daa2e-374">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-374">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="daa2e-375">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-375">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="daa2e-376">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="daa2e-376">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="daa2e-377">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="daa2e-377">New non-verified images are also now returned.</span></span> <span data-ttu-id="daa2e-378">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="daa2e-378">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="daa2e-379">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-379">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="daa2e-380">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="daa2e-380">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="daa2e-381">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-381">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="daa2e-382">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="daa2e-382">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="daa2e-383">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-383">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="daa2e-384">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-384">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="daa2e-385">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-385">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="daa2e-386">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="daa2e-386">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="daa2e-387">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="daa2e-387">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-388">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-388">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-389">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="daa2e-389">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="daa2e-390">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="daa2e-390">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-391">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-391">Az.Compute</span></span>
* <span data-ttu-id="daa2e-392">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="daa2e-392">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="daa2e-393">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-393">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="daa2e-394">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-394">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="daa2e-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="daa2e-395">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="daa2e-396">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-396">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="daa2e-397">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-397">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="daa2e-398">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="daa2e-398">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="daa2e-399">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-399">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="daa2e-400">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="daa2e-400">Breaking changes</span></span>
    - <span data-ttu-id="daa2e-401">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="daa2e-401">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="daa2e-402">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="daa2e-402">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-403">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-403">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-404">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-404">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-405">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-405">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-406">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="daa2e-406">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="daa2e-407">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="daa2e-407">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="daa2e-408">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="daa2e-408">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="daa2e-409">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="daa2e-409">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="daa2e-410">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="daa2e-410">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="daa2e-411">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="daa2e-411">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-412">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-412">Az.FrontDoor</span></span>
* <span data-ttu-id="daa2e-413">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="daa2e-413">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-414">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-414">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-415">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="daa2e-415">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="daa2e-416">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="daa2e-416">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="daa2e-417">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-417">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="daa2e-418">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-418">Removed five cmdlets:</span></span>
    - <span data-ttu-id="daa2e-419">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="daa2e-419">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="daa2e-420">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="daa2e-420">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="daa2e-421">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="daa2e-421">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="daa2e-422">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="daa2e-422">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="daa2e-423">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="daa2e-423">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="daa2e-424">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-424">Added three cmdlets:</span></span>
    - <span data-ttu-id="daa2e-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="daa2e-425">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="daa2e-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="daa2e-426">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="daa2e-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="daa2e-427">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="daa2e-428">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="daa2e-428">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="daa2e-429">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="daa2e-429">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="daa2e-430">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="daa2e-430">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="daa2e-431">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-431">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="daa2e-432">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="daa2e-432">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="daa2e-433">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="daa2e-433">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="daa2e-434">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="daa2e-434">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="daa2e-435">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="daa2e-435">Added some scenario test cases.</span></span>
* <span data-ttu-id="daa2e-436">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-436">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-437">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-438">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="daa2e-438">Breaking changes:</span></span>
    - <span data-ttu-id="daa2e-439">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-439">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="daa2e-440">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="daa2e-440">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="daa2e-441">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-441">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="daa2e-442">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="daa2e-442">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="daa2e-443">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="daa2e-443">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="daa2e-444">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="daa2e-444">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="daa2e-445">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-445">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="daa2e-446">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-446">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="daa2e-447">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-447">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="daa2e-448">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="daa2e-448">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="daa2e-449">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-449">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="daa2e-450">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="daa2e-450">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-451">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-451">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-452">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-452">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-453">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-453">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="daa2e-454">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-454">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="daa2e-455">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-455">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-456">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-456">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-457">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-457">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-458">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-458">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-459">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-459">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-460">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="daa2e-460">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-461">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-461">Az.Resources</span></span>
* <span data-ttu-id="daa2e-462">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="daa2e-462">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-463">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-463">Az.Network</span></span>
* <span data-ttu-id="daa2e-464">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="daa2e-464">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="daa2e-465">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="daa2e-465">Updated cmdlet:</span></span>
        - <span data-ttu-id="daa2e-466">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-466">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-467">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-467">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-468">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-468">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-469">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-469">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-470">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-470">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="daa2e-471">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="daa2e-471">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="daa2e-472">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-472">New cmdlet:</span></span>
        - <span data-ttu-id="daa2e-473">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="daa2e-473">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="daa2e-474">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="daa2e-474">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="daa2e-475">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-475">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="daa2e-476">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-476">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="daa2e-477">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="daa2e-477">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="daa2e-478">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="daa2e-478">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="daa2e-479">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-479">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="daa2e-480">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-480">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="daa2e-481">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-481">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-482">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="daa2e-482">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="daa2e-483">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-483">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="daa2e-484">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-484">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="daa2e-485">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-485">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="daa2e-486">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-486">Set-AzVirtualHub</span></span>
* <span data-ttu-id="daa2e-487">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="daa2e-487">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="daa2e-488">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="daa2e-488">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="daa2e-489">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="daa2e-489">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="daa2e-490">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="daa2e-490">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="daa2e-491">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="daa2e-491">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="daa2e-492">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="daa2e-492">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="daa2e-493">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-493">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="daa2e-494">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-494">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-495">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-495">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="daa2e-496">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="daa2e-496">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="daa2e-497">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="daa2e-497">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="daa2e-498">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="daa2e-498">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="daa2e-499">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="daa2e-499">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="daa2e-500">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="daa2e-500">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="daa2e-501">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="daa2e-501">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="daa2e-502">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="daa2e-502">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="daa2e-503">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-503">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-504">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="daa2e-504">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="daa2e-505">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="daa2e-505">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="daa2e-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="daa2e-506">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="daa2e-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="daa2e-507">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="daa2e-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-508">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="daa2e-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-509">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="daa2e-510">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="daa2e-510">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="daa2e-511">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-511">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="daa2e-512">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-512">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="daa2e-513">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="daa2e-513">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="daa2e-514">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="daa2e-514">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="daa2e-515">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="daa2e-515">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="daa2e-516">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="daa2e-516">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="daa2e-517">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="daa2e-517">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="daa2e-518">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="daa2e-518">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="daa2e-519">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-519">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="daa2e-520">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-520">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="daa2e-521">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-521">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-522">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-522">New-AzIpGroup</span></span>
        - <span data-ttu-id="daa2e-523">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-523">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="daa2e-524">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-524">Get-AzIpGroup</span></span>
        - <span data-ttu-id="daa2e-525">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-525">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-526">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-526">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-527">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="daa2e-527">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-528">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-528">Az.Sql</span></span>
* <span data-ttu-id="daa2e-529">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="daa2e-529">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="daa2e-530">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="daa2e-530">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="daa2e-531">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="daa2e-531">Removed deprecated aliases:</span></span>
* <span data-ttu-id="daa2e-532">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="daa2e-532">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="daa2e-533">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="daa2e-533">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="daa2e-534">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-534">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="daa2e-535">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="daa2e-535">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="daa2e-536">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="daa2e-536">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="daa2e-537">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="daa2e-537">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-538">Az.Storage</span></span>
* <span data-ttu-id="daa2e-539">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-539">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="daa2e-540">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-540">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="daa2e-541">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-541">Set-AzStorageAccount</span></span>
* <span data-ttu-id="daa2e-542">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="daa2e-542">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="daa2e-543">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="daa2e-543">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="daa2e-544">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="daa2e-544">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="daa2e-545">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-545">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="daa2e-546">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-546">General</span></span>
* <span data-ttu-id="daa2e-547">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-547">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-548">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-549">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="daa2e-549">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-550">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-550">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-551">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-551">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="daa2e-552">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="daa2e-552">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-553">Az.Automation</span></span>
* <span data-ttu-id="daa2e-554">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="daa2e-554">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="daa2e-555">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-555">Az.Batch</span></span>
* <span data-ttu-id="daa2e-556">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="daa2e-556">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-557">Az.Compute</span></span>
* <span data-ttu-id="daa2e-558">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-558">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="daa2e-559">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-559">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="daa2e-560">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="daa2e-560">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="daa2e-561">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-561">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-562">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-562">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-563">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="daa2e-563">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="daa2e-564">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="daa2e-564">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="daa2e-565">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-565">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-566">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-566">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-567">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="daa2e-567">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="daa2e-568">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="daa2e-568">Az.HealthcareApis</span></span>
* <span data-ttu-id="daa2e-569">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-569">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="daa2e-570">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="daa2e-570">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="daa2e-571">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="daa2e-571">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="daa2e-572">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="daa2e-572">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-573">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-573">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-574">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="daa2e-574">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="daa2e-575">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="daa2e-575">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-576">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-576">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-577">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="daa2e-577">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="daa2e-578">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="daa2e-578">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="daa2e-579">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="daa2e-579">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="daa2e-580">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="daa2e-580">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-581">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-581">Az.Network</span></span>
* <span data-ttu-id="daa2e-582">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="daa2e-582">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="daa2e-583">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-583">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="daa2e-584">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-584">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-585">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-585">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="daa2e-586">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-586">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="daa2e-587">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="daa2e-587">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="daa2e-588">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-588">Updated cmdlets:</span></span>
        - <span data-ttu-id="daa2e-589">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-589">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="daa2e-590">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-590">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="daa2e-591">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-591">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="daa2e-592">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="daa2e-592">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="daa2e-593">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="daa2e-593">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="daa2e-594">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="daa2e-594">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="daa2e-595">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="daa2e-595">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="daa2e-596">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="daa2e-596">Az.RedisCache</span></span>
* <span data-ttu-id="daa2e-597">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="daa2e-597">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-598">Az.Sql</span></span>
* <span data-ttu-id="daa2e-599">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="daa2e-599">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-600">Az.Storage</span></span>
* <span data-ttu-id="daa2e-601">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-601">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="daa2e-602">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="daa2e-602">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="daa2e-603">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="daa2e-603">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="daa2e-604">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="daa2e-604">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="daa2e-605">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-605">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="daa2e-606">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="daa2e-606">Az.StorageSync</span></span>
* <span data-ttu-id="daa2e-607">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="daa2e-607">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-608">Az.Websites</span></span>
* <span data-ttu-id="daa2e-609">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="daa2e-609">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="daa2e-610">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-610">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-611">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-612">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="daa2e-612">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="daa2e-613">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="daa2e-613">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="daa2e-614">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-614">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-615">Az.Automation</span></span>
* <span data-ttu-id="daa2e-616">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="daa2e-616">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="daa2e-617">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="daa2e-617">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="daa2e-618">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="daa2e-618">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-619">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-619">Az.Compute</span></span>
* <span data-ttu-id="daa2e-620">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-620">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="daa2e-621">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-621">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="daa2e-622">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="daa2e-622">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="daa2e-623">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="daa2e-623">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="daa2e-624">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="daa2e-624">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="daa2e-625">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-625">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="daa2e-626">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="daa2e-626">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="daa2e-627">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="daa2e-627">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="daa2e-628">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="daa2e-628">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-629">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-629">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-630">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="daa2e-630">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="daa2e-631">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="daa2e-631">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-632">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-632">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-633">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="daa2e-633">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-634">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-634">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-635">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="daa2e-635">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="daa2e-636">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="daa2e-636">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="daa2e-637">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="daa2e-637">New cmdlets are:</span></span>
    - <span data-ttu-id="daa2e-638">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="daa2e-638">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="daa2e-639">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="daa2e-639">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="daa2e-640">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="daa2e-640">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="daa2e-641">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="daa2e-641">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-642">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-642">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-643">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="daa2e-643">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="daa2e-644">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="daa2e-644">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="daa2e-645">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="daa2e-645">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="daa2e-646">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-646">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="daa2e-647">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="daa2e-647">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="daa2e-648">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="daa2e-648">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="daa2e-649">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-649">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="daa2e-650">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-650">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="daa2e-651">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-651">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="daa2e-652">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="daa2e-652">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="daa2e-653">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-653">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="daa2e-654">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="daa2e-654">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="daa2e-655">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="daa2e-655">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="daa2e-656">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="daa2e-656">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="daa2e-657">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="daa2e-657">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="daa2e-658">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="daa2e-658">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="daa2e-659">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="daa2e-659">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="daa2e-660">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-660">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="daa2e-661">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="daa2e-661">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="daa2e-662">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-662">Overall improved help files</span></span>
* <span data-ttu-id="daa2e-663">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="daa2e-663">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-664">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-664">Az.Network</span></span>
* <span data-ttu-id="daa2e-665">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="daa2e-665">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="daa2e-666">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="daa2e-666">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="daa2e-667">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="daa2e-667">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="daa2e-668">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="daa2e-668">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="daa2e-669">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="daa2e-669">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="daa2e-670">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="daa2e-670">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="daa2e-671">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="daa2e-671">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="daa2e-672">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="daa2e-672">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="daa2e-673">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-673">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="daa2e-674">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="daa2e-674">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="daa2e-675">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-675">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="daa2e-676">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-676">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="daa2e-677">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-677">New cmdlets</span></span>
        - <span data-ttu-id="daa2e-678">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="daa2e-678">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="daa2e-679">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-679">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="daa2e-680">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="daa2e-680">Updated cmdlet:</span></span>
        - <span data-ttu-id="daa2e-681">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="daa2e-681">New-VpnSite</span></span>
        - <span data-ttu-id="daa2e-682">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="daa2e-682">Update-VpnSite</span></span>
        - <span data-ttu-id="daa2e-683">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-683">New-VpnConnection</span></span>
        - <span data-ttu-id="daa2e-684">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-684">Update-VpnConnection</span></span>
* <span data-ttu-id="daa2e-685">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="daa2e-685">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-686">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-686">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-687">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="daa2e-687">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="daa2e-688">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="daa2e-688">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-689">Az.Resources</span></span>
* <span data-ttu-id="daa2e-690">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="daa2e-690">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-691">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-691">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-692">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="daa2e-692">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="daa2e-693">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="daa2e-693">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="daa2e-694">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="daa2e-694">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="daa2e-695">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="daa2e-695">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="daa2e-696">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="daa2e-696">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="daa2e-697">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="daa2e-697">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="daa2e-698">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="daa2e-698">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="daa2e-699">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="daa2e-699">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="daa2e-700">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="daa2e-700">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="daa2e-701">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="daa2e-701">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="daa2e-702">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="daa2e-702">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="daa2e-703">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="daa2e-703">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="daa2e-704">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="daa2e-704">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="daa2e-705">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="daa2e-705">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="daa2e-706">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="daa2e-706">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="daa2e-707">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="daa2e-707">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="daa2e-708">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="daa2e-708">Az.SignalR</span></span>
* <span data-ttu-id="daa2e-709">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="daa2e-709">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-710">Az.Sql</span></span>
* <span data-ttu-id="daa2e-711">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="daa2e-711">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="daa2e-712">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="daa2e-712">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="daa2e-713">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-713">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="daa2e-714">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="daa2e-714">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="daa2e-715">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="daa2e-715">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-716">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-716">Az.Storage</span></span>
* <span data-ttu-id="daa2e-717">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="daa2e-717">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="daa2e-718">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-718">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="daa2e-719">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-719">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="daa2e-720">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-720">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="daa2e-721">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="daa2e-721">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="daa2e-722">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-722">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="daa2e-723">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="daa2e-723">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="daa2e-724">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-724">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="daa2e-725">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-725">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="daa2e-726">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-726">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="daa2e-727">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-727">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-728">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-728">Az.Websites</span></span>
* <span data-ttu-id="daa2e-729">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="daa2e-729">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="daa2e-730">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="daa2e-730">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="daa2e-731">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="daa2e-731">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="daa2e-732">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-732">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="daa2e-733">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-733">General</span></span>
* <span data-ttu-id="daa2e-734">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="daa2e-734">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-735">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-735">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-736">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="daa2e-736">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="daa2e-737">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="daa2e-737">Az.Aks</span></span>
* <span data-ttu-id="daa2e-738">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="daa2e-738">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="daa2e-739">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="daa2e-739">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-740">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-740">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-741">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="daa2e-741">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="daa2e-742">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="daa2e-742">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="daa2e-743">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="daa2e-743">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="daa2e-744">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="daa2e-744">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="daa2e-745">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-745">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="daa2e-746">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-746">Az.Batch</span></span>
* <span data-ttu-id="daa2e-747">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="daa2e-747">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-748">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-748">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-749">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="daa2e-749">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-750">Az.Compute</span></span>
* <span data-ttu-id="daa2e-751">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-751">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="daa2e-752">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-752">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="daa2e-753">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-753">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="daa2e-754">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-754">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="daa2e-755">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="daa2e-755">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="daa2e-756">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-756">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="daa2e-757">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="daa2e-757">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="daa2e-758">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="daa2e-758">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-759">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-760">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="daa2e-760">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="daa2e-761">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="daa2e-761">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="daa2e-762">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="daa2e-762">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="daa2e-763">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="daa2e-763">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-764">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-764">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-765">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="daa2e-765">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-766">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-766">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-767">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-767">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="daa2e-768">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="daa2e-768">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="daa2e-769">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="daa2e-769">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="daa2e-770">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="daa2e-770">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="daa2e-771">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="daa2e-771">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="daa2e-772">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="daa2e-772">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-773">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-774">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-774">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-775">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-775">Az.Network</span></span>
* <span data-ttu-id="daa2e-776">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-776">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="daa2e-777">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="daa2e-777">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="daa2e-778">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="daa2e-778">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="daa2e-779">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="daa2e-779">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="daa2e-780">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="daa2e-780">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="daa2e-781">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-781">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="daa2e-782">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="daa2e-782">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-783">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-783">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-784">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="daa2e-784">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="daa2e-785">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="daa2e-785">Added example</span></span>
    - <span data-ttu-id="daa2e-786">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="daa2e-786">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="daa2e-787">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="daa2e-787">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="daa2e-788">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="daa2e-788">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-789">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-789">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-790">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-790">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-791">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-791">Az.Resources</span></span>
* <span data-ttu-id="daa2e-792">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="daa2e-792">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="daa2e-793">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="daa2e-793">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="daa2e-794">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="daa2e-794">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="daa2e-795">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-795">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-796">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-796">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-797">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-797">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="daa2e-798">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="daa2e-798">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="daa2e-799">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="daa2e-799">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-800">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-800">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-801">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="daa2e-801">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="daa2e-802">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="daa2e-802">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="daa2e-803">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="daa2e-803">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="daa2e-804">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="daa2e-804">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="daa2e-805">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="daa2e-805">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="daa2e-806">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="daa2e-806">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-807">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-807">Az.Sql</span></span>
* <span data-ttu-id="daa2e-808">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-808">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-809">Az.Storage</span></span>
* <span data-ttu-id="daa2e-810">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="daa2e-810">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="daa2e-811">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="daa2e-811">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="daa2e-812">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-812">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="daa2e-813">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-813">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="daa2e-814">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="daa2e-814">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="daa2e-815">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-815">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-816">Az.Websites</span></span>
* <span data-ttu-id="daa2e-817">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="daa2e-817">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="daa2e-818">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-818">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-819">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-819">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-820">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="daa2e-820">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="daa2e-821">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-821">Az.ApplicationInsights</span></span>
* <span data-ttu-id="daa2e-822">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="daa2e-822">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="daa2e-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-823">Az.Automation</span></span>
* <span data-ttu-id="daa2e-824">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="daa2e-824">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-825">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-825">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-826">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-826">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-827">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-827">Az.Compute</span></span>
* <span data-ttu-id="daa2e-828">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-828">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="daa2e-829">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="daa2e-829">Az.ContainerRegistry</span></span>
* <span data-ttu-id="daa2e-830">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="daa2e-830">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="daa2e-831">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="daa2e-831">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-832">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-832">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-833">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-833">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="daa2e-834">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="daa2e-834">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-835">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-835">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-836">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="daa2e-836">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="daa2e-837">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="daa2e-837">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-838">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-838">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-839">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="daa2e-839">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="daa2e-840">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-840">Az.LogicApp</span></span>
* <span data-ttu-id="daa2e-841">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="daa2e-841">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="daa2e-842">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="daa2e-842">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="daa2e-843">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-843">Az.ManagedServices</span></span>
* <span data-ttu-id="daa2e-844">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="daa2e-844">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-845">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-845">Az.Network</span></span>
* <span data-ttu-id="daa2e-846">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="daa2e-846">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="daa2e-847">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-847">New cmdlets</span></span>
        - <span data-ttu-id="daa2e-848">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-848">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="daa2e-849">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-849">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="daa2e-850">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-850">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-851">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-851">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-852">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-852">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-853">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-853">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="daa2e-854">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="daa2e-854">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="daa2e-855">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-855">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="daa2e-856">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="daa2e-856">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="daa2e-857">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-857">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="daa2e-858">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-858">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="daa2e-859">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-859">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="daa2e-860">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="daa2e-860">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="daa2e-861">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="daa2e-861">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="daa2e-862">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-862">Updated cmdlets</span></span>
        - <span data-ttu-id="daa2e-863">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-863">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="daa2e-864">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-864">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="daa2e-865">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-865">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="daa2e-866">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-866">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="daa2e-867">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-867">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="daa2e-868">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="daa2e-868">Updated cmdlet:</span></span>
        - <span data-ttu-id="daa2e-869">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-869">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="daa2e-870">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-870">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="daa2e-871">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-871">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="daa2e-872">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="daa2e-872">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="daa2e-873">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="daa2e-873">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="daa2e-874">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="daa2e-874">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-875">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-875">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-876">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="daa2e-876">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="daa2e-877">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="daa2e-877">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-878">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-878">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-879">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-879">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="daa2e-880">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-880">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="daa2e-881">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-881">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="daa2e-882">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-882">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="daa2e-883">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-883">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="daa2e-884">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-884">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="daa2e-885">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-885">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="daa2e-886">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-886">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="daa2e-887">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-887">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="daa2e-888">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="daa2e-888">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-889">Az.Resources</span></span>
- <span data-ttu-id="daa2e-890">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="daa2e-890">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="daa2e-891">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="daa2e-891">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-892">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-892">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-893">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="daa2e-893">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="daa2e-894">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="daa2e-894">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-895">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-895">Az.Sql</span></span>
* <span data-ttu-id="daa2e-896">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="daa2e-896">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="daa2e-897">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="daa2e-897">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="daa2e-898">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="daa2e-898">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-899">Az.Storage</span></span>
* <span data-ttu-id="daa2e-900">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="daa2e-900">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="daa2e-901">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="daa2e-901">Az.StorageSync</span></span>
* <span data-ttu-id="daa2e-902">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="daa2e-902">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="daa2e-903">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="daa2e-903">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-904">Az.Websites</span></span>
* <span data-ttu-id="daa2e-905">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-905">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="daa2e-906">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-906">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="daa2e-907">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="daa2e-907">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="daa2e-908">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-908">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-909">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-909">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-910">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="daa2e-910">Add support for profile cmdlets</span></span>
* <span data-ttu-id="daa2e-911">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="daa2e-911">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="daa2e-912">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="daa2e-912">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="daa2e-913">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="daa2e-913">Az.Advisor</span></span>
* <span data-ttu-id="daa2e-914">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="daa2e-914">GA release of Az.Advisor</span></span>
* <span data-ttu-id="daa2e-915">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="daa2e-915">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-916">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-916">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-917">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="daa2e-917">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="daa2e-918">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="daa2e-918">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="daa2e-919">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="daa2e-919">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="daa2e-920">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="daa2e-920">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="daa2e-921">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="daa2e-921">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="daa2e-922">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="daa2e-922">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="daa2e-923">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="daa2e-923">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-924">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-924">Az.Automation</span></span>
* <span data-ttu-id="daa2e-925">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="daa2e-925">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-926">Az.Compute</span></span>
* <span data-ttu-id="daa2e-927">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-927">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-928">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-928">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-929">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="daa2e-929">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="daa2e-930">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="daa2e-930">Az.EventGrid</span></span>
* <span data-ttu-id="daa2e-931">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="daa2e-931">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-932">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-932">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-933">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-933">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-934">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-934">Az.Network</span></span>
* <span data-ttu-id="daa2e-935">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="daa2e-935">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="daa2e-936">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="daa2e-936">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="daa2e-937">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-937">Az.PolicyInsights</span></span>
* <span data-ttu-id="daa2e-938">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="daa2e-938">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="daa2e-939">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="daa2e-939">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-940">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-940">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-941">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="daa2e-941">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-942">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-942">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-943">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="daa2e-943">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-944">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-944">Az.Resources</span></span>
    - <span data-ttu-id="daa2e-945">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="daa2e-945">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="daa2e-946">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="daa2e-946">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="daa2e-947">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-947">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="daa2e-948">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="daa2e-948">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-949">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-949">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-950">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="daa2e-950">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-951">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-951">Az.Sql</span></span>
* <span data-ttu-id="daa2e-952">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="daa2e-952">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="daa2e-953">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-953">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="daa2e-954">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-954">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="daa2e-955">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-955">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="daa2e-956">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-956">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="daa2e-957">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-957">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="daa2e-958">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-958">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="daa2e-959">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="daa2e-959">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="daa2e-960">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="daa2e-960">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-961">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-961">Az.Storage</span></span>
* <span data-ttu-id="daa2e-962">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-962">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="daa2e-963">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="daa2e-963">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="daa2e-964">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="daa2e-964">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="daa2e-965">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="daa2e-965">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="daa2e-966">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-966">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="daa2e-967">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-967">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="daa2e-968">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-968">Set-AzStorageAccount</span></span>
* <span data-ttu-id="daa2e-969">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="daa2e-969">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="daa2e-970">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="daa2e-970">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="daa2e-971">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="daa2e-971">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="daa2e-972">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="daa2e-972">Az.StorageSync</span></span>
* <span data-ttu-id="daa2e-973">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="daa2e-973">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="daa2e-974">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-974">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-975">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-975">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-976">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="daa2e-976">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="daa2e-977">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="daa2e-977">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="daa2e-978">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="daa2e-978">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="daa2e-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="daa2e-979">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="daa2e-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="daa2e-980">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-981">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-981">Az.Compute</span></span>
* <span data-ttu-id="daa2e-982">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-982">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="daa2e-983">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="daa2e-983">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="daa2e-984">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="daa2e-984">Az.Dns</span></span>
* <span data-ttu-id="daa2e-985">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-985">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="daa2e-986">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="daa2e-986">Az.EventGrid</span></span>
* <span data-ttu-id="daa2e-987">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="daa2e-987">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="daa2e-988">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-988">New cmdlets:</span></span>
    - <span data-ttu-id="daa2e-989">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="daa2e-989">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="daa2e-990">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-990">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="daa2e-991">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="daa2e-991">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="daa2e-992">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-992">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="daa2e-993">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="daa2e-993">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="daa2e-994">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-994">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="daa2e-995">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-995">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="daa2e-996">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-996">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="daa2e-997">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-997">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="daa2e-998">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-998">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="daa2e-999">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="daa2e-999">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="daa2e-1000">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1000">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="daa2e-1001">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="daa2e-1001">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="daa2e-1002">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1002">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="daa2e-1003">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="daa2e-1003">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="daa2e-1004">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1004">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="daa2e-1005">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1005">Updated cmdlets:</span></span>
    - <span data-ttu-id="daa2e-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="daa2e-1006">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="daa2e-1007">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1007">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="daa2e-1008">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1008">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="daa2e-1009">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1009">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="daa2e-1010">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1010">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="daa2e-1011">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1011">Event subscription expiration date,</span></span>
            - <span data-ttu-id="daa2e-1012">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1012">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="daa2e-1013">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1013">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="daa2e-1014">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1014">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="daa2e-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="daa2e-1015">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="daa2e-1016">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1016">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="daa2e-1017">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="daa2e-1017">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="daa2e-1018">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1018">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="daa2e-1019">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1019">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-1020">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1020">Az.FrontDoor</span></span>
* <span data-ttu-id="daa2e-1021">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-1021">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="daa2e-1022">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1022">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="daa2e-1023">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-1023">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="daa2e-1024">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="daa2e-1024">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1025">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1025">Az.Network</span></span>
* <span data-ttu-id="daa2e-1026">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1026">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="daa2e-1027">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1027">New cmdlets</span></span>
        - <span data-ttu-id="daa2e-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="daa2e-1028">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="daa2e-1029">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="daa2e-1029">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="daa2e-1030">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1030">New cmdlets</span></span> 
        - <span data-ttu-id="daa2e-1031">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="daa2e-1031">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="daa2e-1032">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-1032">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="daa2e-1033">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1033">New cmdlets</span></span> 
        - <span data-ttu-id="daa2e-1034">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-1034">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="daa2e-1035">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-1035">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="daa2e-1036">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="daa2e-1036">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="daa2e-1037">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1037">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="daa2e-1038">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1038">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="daa2e-1039">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-1039">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="daa2e-1040">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1040">New cmdlets</span></span>
        - <span data-ttu-id="daa2e-1041">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-1041">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="daa2e-1042">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-1042">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="daa2e-1043">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="daa2e-1043">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="daa2e-1044">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1044">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="daa2e-1045">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1045">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="daa2e-1046">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1046">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="daa2e-1047">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1047">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="daa2e-1048">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1048">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="daa2e-1049">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1049">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="daa2e-1050">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="daa2e-1050">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="daa2e-1051">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1051">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="daa2e-1052">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1052">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="daa2e-1053">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1053">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="daa2e-1054">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="daa2e-1054">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="daa2e-1055">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1055">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="daa2e-1056">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1056">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="daa2e-1057">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="daa2e-1057">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="daa2e-1058">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1058">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="daa2e-1059">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1059">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="daa2e-1060">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="daa2e-1060">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="daa2e-1061">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1061">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="daa2e-1062">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="daa2e-1062">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="daa2e-1063">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="daa2e-1063">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="daa2e-1064">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1064">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="daa2e-1065">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1065">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="daa2e-1066">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1066">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="daa2e-1067">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1067">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-1068">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1068">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-1069">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1069">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1070">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1070">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1071">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="daa2e-1071">Support for additional Template Export options</span></span>
    - <span data-ttu-id="daa2e-1072">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1072">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="daa2e-1073">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1073">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="daa2e-1074">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1074">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1075">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1075">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-1076">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="daa2e-1076">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1077">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1077">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1078">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1078">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="daa2e-1079">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1079">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="daa2e-1080">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="daa2e-1080">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="daa2e-1081">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-1081">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="daa2e-1082">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-1082">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="daa2e-1083">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="daa2e-1083">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="daa2e-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="daa2e-1084">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="daa2e-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="daa2e-1085">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1086">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1086">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1087">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1087">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="daa2e-1088">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1088">New-AzStorageAccount</span></span>
* <span data-ttu-id="daa2e-1089">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="daa2e-1089">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="daa2e-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1090">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1091">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1091">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1092">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="daa2e-1092">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="daa2e-1093">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="daa2e-1093">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="daa2e-1094">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1094">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="daa2e-1095">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-1095">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-1096">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1096">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1097">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1097">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1098">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1098">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="daa2e-1099">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-1099">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-1100">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1100">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-1101">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="daa2e-1101">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="daa2e-1102">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa2e-1102">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1103">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1103">Az.Network</span></span>
* <span data-ttu-id="daa2e-1104">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="daa2e-1104">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="daa2e-1105">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="daa2e-1105">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="daa2e-1106">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1106">Az.PolicyInsights</span></span>
* <span data-ttu-id="daa2e-1107">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="daa2e-1107">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1108">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1108">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1109">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-1109">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-1110">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-1110">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-1111">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daa2e-1111">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1112">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1112">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-1113">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1113">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="daa2e-1114">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1114">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1115">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1115">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1116">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1116">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="daa2e-1117">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1117">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="daa2e-1118">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1118">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="daa2e-1119">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1119">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1120">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1120">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1121">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1121">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="daa2e-1122">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1122">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="daa2e-1123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-1123">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-1124">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1124">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="daa2e-1125">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1125">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="daa2e-1126">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1126">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="daa2e-1127">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="daa2e-1127">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="daa2e-1128">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1128">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="daa2e-1129">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="daa2e-1129">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="daa2e-1130">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1130">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="daa2e-1131">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1131">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="daa2e-1132">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-1132">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="daa2e-1133">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="daa2e-1133">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="daa2e-1134">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1134">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="daa2e-1135">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="daa2e-1135">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="daa2e-1136">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="daa2e-1136">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="daa2e-1137">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1137">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="daa2e-1138">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1138">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="daa2e-1139">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1139">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="daa2e-1140">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1140">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="daa2e-1141">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="daa2e-1141">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="daa2e-1142">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1142">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="daa2e-1143">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1143">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="daa2e-1144">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="daa2e-1144">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="daa2e-1145">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1145">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="daa2e-1146">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1146">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="daa2e-1147">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-1147">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="daa2e-1148">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1148">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="daa2e-1149">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1149">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="daa2e-1150">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1150">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="daa2e-1151">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1151">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="daa2e-1152">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1152">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="daa2e-1153">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1153">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="daa2e-1154">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="daa2e-1154">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="daa2e-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="daa2e-1155">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="daa2e-1156">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1156">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="daa2e-1157">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1157">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="daa2e-1158">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1158">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="daa2e-1159">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="daa2e-1159">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="daa2e-1160">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1160">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="daa2e-1161">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1161">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="daa2e-1162">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1162">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="daa2e-1163">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1163">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="daa2e-1164">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1164">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="daa2e-1165">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1165">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="daa2e-1166">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1166">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="daa2e-1167">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1167">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="daa2e-1168">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1168">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="daa2e-1169">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1169">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="daa2e-1170">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1170">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="daa2e-1171">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1171">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="daa2e-1172">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1172">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="daa2e-1173">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1173">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="daa2e-1174">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1174">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="daa2e-1175">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1175">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="daa2e-1176">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1176">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="daa2e-1177">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1177">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="daa2e-1178">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1178">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="daa2e-1179">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1179">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="daa2e-1180">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1180">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="daa2e-1181">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1181">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="daa2e-1182">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1182">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="daa2e-1183">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1183">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="daa2e-1184">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="daa2e-1184">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="daa2e-1185">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1185">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="daa2e-1186">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1186">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="daa2e-1187">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1187">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="daa2e-1188">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1188">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="daa2e-1189">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1189">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="daa2e-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="daa2e-1190">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="daa2e-1191">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1191">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="daa2e-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="daa2e-1192">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="daa2e-1193">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1193">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="daa2e-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="daa2e-1194">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="daa2e-1195">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1195">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="daa2e-1196">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1196">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="daa2e-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1197">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="daa2e-1198">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1198">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="daa2e-1199">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1199">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="daa2e-1200">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1200">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1201">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1201">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1202">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1202">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="daa2e-1203">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="daa2e-1203">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="daa2e-1204">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="daa2e-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="daa2e-1205">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1205">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="daa2e-1206">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="daa2e-1206">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="daa2e-1207">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1207">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="daa2e-1208">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1208">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1209">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1210">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1210">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="daa2e-1211">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="daa2e-1211">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1212">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1212">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1213">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1213">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-1214">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1214">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-1215">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-1215">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1216">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1216">Az.Network</span></span>
* <span data-ttu-id="daa2e-1217">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="daa2e-1217">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="daa2e-1218">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1218">Updated cmdlet:</span></span>
        - <span data-ttu-id="daa2e-1219">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-1219">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="daa2e-1220">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1220">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1221">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1221">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1222">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="daa2e-1222">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1223">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1223">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1224">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="daa2e-1224">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="daa2e-1225">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1225">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1226">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1226">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1227">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="daa2e-1227">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-1228">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1228">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-1229">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1229">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="daa2e-1230">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1230">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1231">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1231">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1232">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1232">Proximity placement group feature.</span></span>
    - <span data-ttu-id="daa2e-1233">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1233">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="daa2e-1234">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1234">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="daa2e-1235">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1235">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="daa2e-1236">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1236">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="daa2e-1237">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-1237">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="daa2e-1238">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="daa2e-1238">Breaking changes</span></span>
    - <span data-ttu-id="daa2e-1239">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1239">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="daa2e-1240">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1240">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="daa2e-1241">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="daa2e-1241">Az.DeploymentManager</span></span>
* <span data-ttu-id="daa2e-1242">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="daa2e-1242">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="daa2e-1243">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="daa2e-1243">Az.Dns</span></span>
* <span data-ttu-id="daa2e-1244">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="daa2e-1244">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="daa2e-1245">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1245">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="daa2e-1246">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1246">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-1247">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1247">Az.FrontDoor</span></span>
* <span data-ttu-id="daa2e-1248">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1248">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="daa2e-1249">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1249">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-1250">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-1250">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-1251">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1251">Removed two cmdlets:</span></span>
    - <span data-ttu-id="daa2e-1252">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="daa2e-1252">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="daa2e-1253">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="daa2e-1253">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="daa2e-1254">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="daa2e-1254">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="daa2e-1255">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1255">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="daa2e-1256">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1256">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="daa2e-1257">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1257">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-1258">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1258">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-1259">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1259">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="daa2e-1260">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="daa2e-1260">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="daa2e-1261">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1261">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="daa2e-1262">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="daa2e-1262">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="daa2e-1263">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1263">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="daa2e-1264">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="daa2e-1264">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="daa2e-1265">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="daa2e-1265">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="daa2e-1266">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1266">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="daa2e-1267">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1267">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="daa2e-1268">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1268">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="daa2e-1269">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1269">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="daa2e-1270">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1270">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="daa2e-1271">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="daa2e-1271">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="daa2e-1272">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1272">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1273">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1273">Az.Network</span></span>
* <span data-ttu-id="daa2e-1274">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="daa2e-1274">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="daa2e-1275">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1275">New cmdlets</span></span>
        - <span data-ttu-id="daa2e-1276">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1276">New-AzNatGateway</span></span>
        - <span data-ttu-id="daa2e-1277">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1277">Get-AzNatGateway</span></span>
        - <span data-ttu-id="daa2e-1278">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1278">Set-AzNatGateway</span></span>
        - <span data-ttu-id="daa2e-1279">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1279">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="daa2e-1280">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1280">Updated cmdlets</span></span>
        - <span data-ttu-id="daa2e-1281">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="daa2e-1281">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="daa2e-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="daa2e-1282">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="daa2e-1283">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1283">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="daa2e-1284">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1284">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="daa2e-1285">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1285">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="daa2e-1286">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1286">Az.PolicyInsights</span></span>
* <span data-ttu-id="daa2e-1287">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1287">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="daa2e-1288">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1288">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="daa2e-1289">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1289">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1290">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1290">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1291">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1291">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="daa2e-1292">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1292">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="daa2e-1293">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1293">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="daa2e-1294">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1294">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="daa2e-1295">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1295">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="daa2e-1296">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1296">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="daa2e-1297">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="daa2e-1297">Az.Relay</span></span>
* <span data-ttu-id="daa2e-1298">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="daa2e-1298">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-1299">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-1299">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-1300">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1300">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1301">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1301">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1302">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="daa2e-1302">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="daa2e-1303">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1303">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="daa2e-1304">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1304">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="daa2e-1305">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1305">New-AzStorageAccount</span></span>
* <span data-ttu-id="daa2e-1306">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1306">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="daa2e-1307">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1307">New-AzStorageAccount</span></span>
    - <span data-ttu-id="daa2e-1308">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1308">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="daa2e-1309">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1309">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1310">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1310">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1311">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-1311">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="daa2e-1312">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1312">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="daa2e-1313">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1313">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="daa2e-1314">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1314">Highlights since the last major release</span></span>
* <span data-ttu-id="daa2e-1315">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1315">General availability of `Az` module</span></span>
* <span data-ttu-id="daa2e-1316">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="daa2e-1316">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="daa2e-1317">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="daa2e-1317">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="daa2e-1318">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1318">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="daa2e-1319">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="daa2e-1319">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="daa2e-1320">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1320">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="daa2e-1321">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-1321">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1322">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1322">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1323">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="daa2e-1323">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="daa2e-1324">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-1324">Az.Batch</span></span>
* <span data-ttu-id="daa2e-1325">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1325">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-1326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-1326">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-1327">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-1328">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1328">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-1329">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1329">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1330">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1330">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1331">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="daa2e-1331">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="daa2e-1332">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1333">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1333">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-1334">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-1334">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-1335">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1335">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1336">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1336">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1337">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1337">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="daa2e-1338">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="daa2e-1338">Az.EventGrid</span></span>
* <span data-ttu-id="daa2e-1339">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1339">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-1340">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1340">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-1341">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1341">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="daa2e-1342">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="daa2e-1342">Az.HDInsight</span></span>
* <span data-ttu-id="daa2e-1343">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1343">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-1344">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1344">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-1345">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1345">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-1346">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1346">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-1347">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1347">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1348">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1348">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="daa2e-1349">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="daa2e-1349">Az.MachineLearning</span></span>
* <span data-ttu-id="daa2e-1350">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="daa2e-1351">Az.Media</span><span class="sxs-lookup"><span data-stu-id="daa2e-1351">Az.Media</span></span>
* <span data-ttu-id="daa2e-1352">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-1353">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1353">Az.Monitor</span></span>
  * <span data-ttu-id="daa2e-1354">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1354">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="daa2e-1355">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="daa2e-1355">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="daa2e-1356">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="daa2e-1356">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="daa2e-1357">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1357">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="daa2e-1358">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1358">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="daa2e-1359">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1359">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="daa2e-1360">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="daa2e-1360">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1361">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1361">Az.Network</span></span>
* <span data-ttu-id="daa2e-1362">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1362">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1363">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1363">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="daa2e-1364">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="daa2e-1364">Az.NotificationHubs</span></span>
* <span data-ttu-id="daa2e-1365">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1365">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-1366">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1366">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-1367">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1367">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="daa2e-1368">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="daa2e-1368">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="daa2e-1369">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1370">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1370">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1371">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1371">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1372">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1372">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="daa2e-1373">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="daa2e-1373">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="daa2e-1374">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="daa2e-1374">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="daa2e-1375">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="daa2e-1375">Az.RedisCache</span></span>
* <span data-ttu-id="daa2e-1376">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1377">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1377">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1378">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1378">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1379">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1379">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1380">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="daa2e-1380">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="daa2e-1381">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1381">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1382">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1382">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="daa2e-1383">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1383">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="daa2e-1384">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1384">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="daa2e-1385">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1385">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="daa2e-1386">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1386">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1387">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1387">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1388">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1388">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="daa2e-1389">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1389">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="daa2e-1390">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1390">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="daa2e-1391">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1391">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="daa2e-1392">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1392">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="daa2e-1393">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1393">Highlights since the last major release</span></span>
* <span data-ttu-id="daa2e-1394">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1394">General availability of `Az` module</span></span>
* <span data-ttu-id="daa2e-1395">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="daa2e-1395">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="daa2e-1396">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="daa2e-1396">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="daa2e-1397">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1397">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="daa2e-1398">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="daa2e-1398">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="daa2e-1399">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1399">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="daa2e-1400">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-1400">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1401">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1401">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1402">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="daa2e-1402">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="daa2e-1403">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1403">Az.AnalysisServices</span></span>
* <span data-ttu-id="daa2e-1404">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1404">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="daa2e-1405">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1405">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1406">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1406">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1407">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1407">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="daa2e-1408">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1408">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="daa2e-1409">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1409">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1410">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1410">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1411">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1411">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="daa2e-1412">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1412">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="daa2e-1413">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1413">Az.ContainerInstance</span></span>
* <span data-ttu-id="daa2e-1414">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="daa2e-1414">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-1415">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-1415">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-1416">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1416">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="daa2e-1417">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1417">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1418">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1419">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1419">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="daa2e-1420">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1420">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="daa2e-1421">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="daa2e-1421">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="daa2e-1422">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="daa2e-1422">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="daa2e-1423">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1423">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="daa2e-1424">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="daa2e-1424">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1425">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1426">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1426">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1427">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1428">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="daa2e-1428">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="daa2e-1429">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="daa2e-1429">New-AzStorageContext</span></span>
* <span data-ttu-id="daa2e-1430">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1430">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="daa2e-1431">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="daa2e-1431">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="daa2e-1432">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="daa2e-1432">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="daa2e-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1433">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="daa2e-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1434">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="daa2e-1435">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="daa2e-1435">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="daa2e-1436">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-1436">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="daa2e-1437">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-1437">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="daa2e-1438">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-1438">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="daa2e-1439">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="daa2e-1439">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="daa2e-1440">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1440">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="daa2e-1441">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1441">Highlights since the last major release</span></span>
* <span data-ttu-id="daa2e-1442">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1442">General availability of `Az` module</span></span>
* <span data-ttu-id="daa2e-1443">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="daa2e-1443">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="daa2e-1444">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="daa2e-1444">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="daa2e-1445">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1445">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="daa2e-1446">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="daa2e-1446">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="daa2e-1447">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1447">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="daa2e-1448">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-1448">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1449">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1449">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1450">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1450">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="daa2e-1451">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="daa2e-1451">Dynamic grouping</span></span>
    * <span data-ttu-id="daa2e-1452">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="daa2e-1452">Pre-Post script</span></span>
    * <span data-ttu-id="daa2e-1453">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="daa2e-1453">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1454">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1454">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1455">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="daa2e-1455">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="daa2e-1456">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1456">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-1457">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1457">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-1458">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1458">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1459">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1459">Az.Network</span></span>
* <span data-ttu-id="daa2e-1460">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1460">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="daa2e-1461">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1461">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1462">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1462">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1463">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="daa2e-1463">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="daa2e-1464">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="daa2e-1464">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1465">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1465">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1466">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1466">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="daa2e-1467">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="daa2e-1467">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1468">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1468">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1469">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1469">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1470">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1470">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1471">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1471">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="daa2e-1472">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1472">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="daa2e-1473">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1473">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="daa2e-1474">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1474">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="daa2e-1475">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="daa2e-1475">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="daa2e-1476">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="daa2e-1476">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="daa2e-1477">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1477">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1478">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1479">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="daa2e-1479">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="daa2e-1480">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1480">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1481">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1481">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1482">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="daa2e-1482">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="daa2e-1483">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1483">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1484">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1485">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1485">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="daa2e-1486">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1486">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="daa2e-1487">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1487">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-1488">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-1488">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-1489">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1489">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1490">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1491">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="daa2e-1491">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-1492">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-1492">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-1493">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="daa2e-1493">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="daa2e-1494">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-1494">Az.LogicApp</span></span>
* <span data-ttu-id="daa2e-1495">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1495">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1496">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1496">Az.Network</span></span>
* <span data-ttu-id="daa2e-1497">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1497">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1498">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1498">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1499">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1499">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="daa2e-1500">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="daa2e-1500">SDK Update</span></span>
* <span data-ttu-id="daa2e-1501">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="daa2e-1501">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="daa2e-1502">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="daa2e-1502">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1503">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1503">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1504">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1504">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="daa2e-1505">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="daa2e-1505">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="daa2e-1506">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1506">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="daa2e-1507">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="daa2e-1507">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="daa2e-1508">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1508">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="daa2e-1509">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="daa2e-1509">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1510">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1511">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1511">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="daa2e-1512">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1512">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1513">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1513">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1514">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1514">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="daa2e-1515">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1515">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="daa2e-1516">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1516">Az.AnalysisServices</span></span>
* <span data-ttu-id="daa2e-1517">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="daa2e-1517">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1518">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1518">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1519">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1519">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="daa2e-1520">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1520">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="daa2e-1521">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1521">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-1522">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1522">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-1523">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1523">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1524">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1524">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1525">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="daa2e-1525">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="daa2e-1526">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="daa2e-1526">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="daa2e-1527">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1527">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="daa2e-1528">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1528">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1529">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1529">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1530">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1530">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="daa2e-1531">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1531">Az.EventHub</span></span>
* <span data-ttu-id="daa2e-1532">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1532">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-1533">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1533">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-1534">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="daa2e-1534">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="daa2e-1535">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-1535">Az.LogicApp</span></span>
* <span data-ttu-id="daa2e-1536">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1536">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="daa2e-1537">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="daa2e-1537">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="daa2e-1538">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1538">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="daa2e-1539">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1539">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="daa2e-1540">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1540">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="daa2e-1541">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1541">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="daa2e-1542">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="daa2e-1542">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="daa2e-1543">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1543">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="daa2e-1544">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1544">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="daa2e-1545">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1545">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="daa2e-1546">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1546">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="daa2e-1547">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1547">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="daa2e-1548">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-1548">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="daa2e-1549">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1549">Az.Monitor</span></span>
* <span data-ttu-id="daa2e-1550">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1550">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1551">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1551">Az.Network</span></span>
* <span data-ttu-id="daa2e-1552">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="daa2e-1552">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-1553">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1553">Az.OperationalInsights</span></span>
* <span data-ttu-id="daa2e-1554">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1554">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="daa2e-1555">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1555">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="daa2e-1556">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1556">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="daa2e-1557">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1557">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1558">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="daa2e-1558">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="daa2e-1559">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="daa2e-1559">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="daa2e-1560">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="daa2e-1560">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="daa2e-1561">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="daa2e-1561">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1562">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1563">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="daa2e-1563">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="daa2e-1564">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="daa2e-1564">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1565">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1565">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1566">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="daa2e-1566">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="daa2e-1567">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1567">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1568">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1568">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1569">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="daa2e-1569">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="daa2e-1570">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1570">Az.AnalysisServices</span></span>
<span data-ttu-id="daa2e-1571">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1571">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1572">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1572">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1573">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="daa2e-1573">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="daa2e-1574">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="daa2e-1574">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="daa2e-1575">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1575">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1576">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1576">Az.RecoveryServices</span></span>
<span data-ttu-id="daa2e-1577">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1577">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1578">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1578">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1579">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="daa2e-1579">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="daa2e-1580">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="daa2e-1580">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="daa2e-1581">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="daa2e-1581">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="daa2e-1582">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="daa2e-1582">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1583">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1583">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1584">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1584">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="daa2e-1585">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="daa2e-1585">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="daa2e-1586">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="daa2e-1586">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="daa2e-1587">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1587">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1588">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1588">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1589">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1589">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="daa2e-1590">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1590">Az.AnalysisServices</span></span>
* <span data-ttu-id="daa2e-1591">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1591">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="daa2e-1593">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1593">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="daa2e-1594">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1594">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1595">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1596">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="daa2e-1596">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="daa2e-1597">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1597">Update incorrect online help URLs</span></span>
* <span data-ttu-id="daa2e-1598">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="daa2e-1598">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="daa2e-1599">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="daa2e-1599">Az.Aks</span></span>
* <span data-ttu-id="daa2e-1600">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1600">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="daa2e-1601">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1601">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1602">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1602">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="daa2e-1603">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1603">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="daa2e-1604">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="daa2e-1604">Az.Cdn</span></span>
* <span data-ttu-id="daa2e-1605">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1605">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1606">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1606">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1607">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1607">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="daa2e-1608">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="daa2e-1608">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="daa2e-1609">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="daa2e-1609">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="daa2e-1610">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="daa2e-1610">Az.ContainerRegistry</span></span>
* <span data-ttu-id="daa2e-1611">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1611">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="daa2e-1612">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="daa2e-1612">Az.DataFactory</span></span>
* <span data-ttu-id="daa2e-1613">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-1613">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1614">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1614">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1615">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="daa2e-1615">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="daa2e-1616">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="daa2e-1616">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="daa2e-1617">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1617">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-1618">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1618">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-1619">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1619">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="daa2e-1620">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1620">Az.KeyVault</span></span>
* <span data-ttu-id="daa2e-1621">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1621">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1622">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1622">Az.Network</span></span>
* <span data-ttu-id="daa2e-1623">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1623">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1624">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1624">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1625">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="daa2e-1625">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="daa2e-1626">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="daa2e-1626">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="daa2e-1627">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="daa2e-1627">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="daa2e-1628">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="daa2e-1628">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="daa2e-1629">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="daa2e-1629">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="daa2e-1630">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="daa2e-1630">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="daa2e-1631">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="daa2e-1631">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1632">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1632">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-1633">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="daa2e-1633">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="daa2e-1634">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1634">Fix some error messages.</span></span>
* <span data-ttu-id="daa2e-1635">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1635">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="daa2e-1636">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1636">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="daa2e-1637">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="daa2e-1637">Az.SignalR</span></span>
* <span data-ttu-id="daa2e-1638">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1638">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1639">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1639">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1640">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1640">Update incorrect online help URLs</span></span>
* <span data-ttu-id="daa2e-1641">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="daa2e-1641">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="daa2e-1642">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="daa2e-1642">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="daa2e-1643">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="daa2e-1643">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1644">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1645">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1645">Update incorrect online help URLs</span></span>
* <span data-ttu-id="daa2e-1646">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1646">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="daa2e-1647">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="daa2e-1647">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="daa2e-1648">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="daa2e-1648">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="daa2e-1649">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="daa2e-1649">Az.TrafficManager</span></span>
* <span data-ttu-id="daa2e-1650">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1650">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1651">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1651">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1652">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="daa2e-1652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="daa2e-1653">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1653">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="daa2e-1654">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="daa2e-1654">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="daa2e-1655">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="daa2e-1655">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="daa2e-1656">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1656">Az.Accounts</span></span>
* <span data-ttu-id="daa2e-1657">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="daa2e-1657">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1658">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1658">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1659">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1659">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="daa2e-1660">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="daa2e-1660">Updated the description of ID in help files</span></span>
* <span data-ttu-id="daa2e-1661">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1661">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1662">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1662">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1663">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1663">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="daa2e-1664">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="daa2e-1664">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="daa2e-1665">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="daa2e-1665">Az.EventGrid</span></span>
* <span data-ttu-id="daa2e-1666">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1666">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="daa2e-1667">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="daa2e-1667">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="daa2e-1668">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1668">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="daa2e-1669">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="daa2e-1669">Event Time-To-Live,</span></span>
        - <span data-ttu-id="daa2e-1670">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1670">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="daa2e-1671">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="daa2e-1671">Dead letter endpoint.</span></span>
    - <span data-ttu-id="daa2e-1672">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1672">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="daa2e-1673">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="daa2e-1673">Event Time-To-Live,</span></span>
        - <span data-ttu-id="daa2e-1674">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1674">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="daa2e-1675">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="daa2e-1675">Dead letter endpoint.</span></span>
* <span data-ttu-id="daa2e-1676">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1676">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="daa2e-1677">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1677">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="daa2e-1678">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1678">Az.IotHub</span></span>
* <span data-ttu-id="daa2e-1679">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="daa2e-1679">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="daa2e-1680">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="daa2e-1680">Az.LogicApp</span></span>
* <span data-ttu-id="daa2e-1681">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="daa2e-1681">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1682">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1683">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1683">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="daa2e-1684">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="daa2e-1684">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="daa2e-1685">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="daa2e-1685">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="daa2e-1686">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="daa2e-1686">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="daa2e-1687">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1687">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="daa2e-1688">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="daa2e-1688">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="daa2e-1689">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="daa2e-1689">Az.SignalR</span></span>
* <span data-ttu-id="daa2e-1690">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1690">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1691">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1691">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1692">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1692">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="daa2e-1693">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1693">Az.Storage</span></span>
* <span data-ttu-id="daa2e-1694">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="daa2e-1694">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="daa2e-1695">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="daa2e-1695">New-AzStorageContext</span></span>
* <span data-ttu-id="daa2e-1696">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="daa2e-1696">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="daa2e-1697">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="daa2e-1697">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1698">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1698">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1699">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1699">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="daa2e-1700">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1700">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="daa2e-1701">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1701">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="daa2e-1702">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1702">General</span></span>

- <span data-ttu-id="daa2e-1703">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="daa2e-1703">General Availability of Az Module</span></span>
- <span data-ttu-id="daa2e-1704">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="daa2e-1704">Online help for each module</span></span>
- <span data-ttu-id="daa2e-1705">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1705">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="daa2e-1706">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="daa2e-1706">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="daa2e-1707">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1707">Az.Accounts</span></span>
- <span data-ttu-id="daa2e-1708">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1708">Changed from Az.Profile</span></span>
- <span data-ttu-id="daa2e-1709">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="daa2e-1709">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="daa2e-1710">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-1710">Az.ApiManagement</span></span>
- <span data-ttu-id="daa2e-1711">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="daa2e-1711">Fixes for #7002</span></span>
- <span data-ttu-id="daa2e-1712">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1712">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="daa2e-1713">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="daa2e-1713">Az.Batch</span></span>
- <span data-ttu-id="daa2e-1714">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1714">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="daa2e-1715">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1715">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="daa2e-1716">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="daa2e-1717">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="daa2e-1717">Az.Billing</span></span>
- <span data-ttu-id="daa2e-1718">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1718">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="daa2e-1719">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1719">Az.CognitivServices</span></span>
- <span data-ttu-id="daa2e-1720">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1720">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="daa2e-1721">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="daa2e-1721">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="daa2e-1722">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1722">Az.ContainerInstance</span></span>
- <span data-ttu-id="daa2e-1723">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="daa2e-1723">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="daa2e-1724">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="daa2e-1724">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="daa2e-1725">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1725">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1726">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1726">Az.DataLakeStore</span></span>
- <span data-ttu-id="daa2e-1727">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1727">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="daa2e-1728">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1728">Az.Monitor</span></span>
- <span data-ttu-id="daa2e-1729">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1729">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="daa2e-1730">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="daa2e-1730">Az.KeyVault</span></span>
- <span data-ttu-id="daa2e-1731">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="daa2e-1731">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="daa2e-1732">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="daa2e-1732">Az.MachineLearning</span></span>
- <span data-ttu-id="daa2e-1733">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1733">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="daa2e-1734">Az.Media</span><span class="sxs-lookup"><span data-stu-id="daa2e-1734">Az.Media</span></span>
- <span data-ttu-id="daa2e-1735">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="daa2e-1735">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="daa2e-1736">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1736">Az.Network</span></span>
<span data-ttu-id="daa2e-1737">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1737">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="daa2e-1738">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1738">New cmdlets added:</span></span>
        - <span data-ttu-id="daa2e-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1739">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1740">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1741">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1742">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1743">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1744">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1744">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="daa2e-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1745">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="daa2e-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="daa2e-1746">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="daa2e-1747">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1747">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="daa2e-1748">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="daa2e-1748">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="daa2e-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1749">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="daa2e-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="daa2e-1750">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="daa2e-1751">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1751">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="daa2e-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1752">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="daa2e-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1753">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="daa2e-1754">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="daa2e-1754">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="daa2e-1755">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1755">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="daa2e-1756">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1756">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="daa2e-1757">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="daa2e-1757">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="daa2e-1758">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="daa2e-1758">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="daa2e-1759">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1759">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="daa2e-1760">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1760">Az.OperationalInsights</span></span>
- <span data-ttu-id="daa2e-1761">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1761">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="daa2e-1762">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1762">Az.Profile</span></span>
- <span data-ttu-id="daa2e-1763">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="daa2e-1763">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1764">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1764">Az.RecoveryServices</span></span>
- <span data-ttu-id="daa2e-1765">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1765">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="daa2e-1766">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1766">Az.Resources</span></span>
- <span data-ttu-id="daa2e-1767">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1767">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1768">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1768">Az.ServiceFabric</span></span>
- <span data-ttu-id="daa2e-1769">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1769">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="daa2e-1770">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1770">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="daa2e-1771">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="daa2e-1771">Az.SIgnalR</span></span>
- <span data-ttu-id="daa2e-1772">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="daa2e-1772">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="daa2e-1773">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1773">Az.Sql</span></span>
- <span data-ttu-id="daa2e-1774">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="daa2e-1774">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="daa2e-1775">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1775">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="daa2e-1776">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1776">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="daa2e-1777">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1777">Az.Storage</span></span>
- <span data-ttu-id="daa2e-1778">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1778">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="daa2e-1779">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1779">Az.Websites</span></span>
- <span data-ttu-id="daa2e-1780">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1780">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="daa2e-1781">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1781">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="daa2e-1782">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1782">General</span></span>

* <span data-ttu-id="daa2e-1783">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="daa2e-1783">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="daa2e-1784">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1784">Az.Compute</span></span>

* <span data-ttu-id="daa2e-1785">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1785">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1786">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1786">Az.DataLakeStore</span></span>

* <span data-ttu-id="daa2e-1787">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="daa2e-1787">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="daa2e-1788">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="daa2e-1788">Az.FrontDoor</span></span>

* <span data-ttu-id="daa2e-1789">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="daa2e-1789">Fixed some broken links</span></span>
    - <span data-ttu-id="daa2e-1790">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1790">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="daa2e-1791">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1791">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="daa2e-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1792">Az.RecoveryServices</span></span>

* <span data-ttu-id="daa2e-1793">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1793">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="daa2e-1794">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1794">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="daa2e-1795">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1795">Az.Resources</span></span>

* <span data-ttu-id="daa2e-1796">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="daa2e-1796">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="daa2e-1797">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1797">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="daa2e-1798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1798">Az.Sql</span></span>

* <span data-ttu-id="daa2e-1799">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="daa2e-1799">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="daa2e-1800">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="daa2e-1800">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="daa2e-1801">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1801">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="daa2e-1802">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1802">Az.Storage</span></span>

* <span data-ttu-id="daa2e-1803">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1803">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="daa2e-1804">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="daa2e-1804">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="daa2e-1805">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1805">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="daa2e-1806">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="daa2e-1806">Support Static Website configuration</span></span>
    - <span data-ttu-id="daa2e-1807">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="daa2e-1807">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="daa2e-1808">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="daa2e-1808">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="daa2e-1809">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1809">Az.Websites</span></span>

* <span data-ttu-id="daa2e-1810">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="daa2e-1810">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="daa2e-1811">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1811">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="daa2e-1812">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1812">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="daa2e-1813">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1813">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="daa2e-1814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="daa2e-1814">Az.ApiManagement</span></span>
* <span data-ttu-id="daa2e-1815">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1815">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="daa2e-1816">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="daa2e-1816">Az.Automation</span></span>
* <span data-ttu-id="daa2e-1817">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="daa2e-1817">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="daa2e-1818">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="daa2e-1818">Added Update Management cmdlets</span></span>
* <span data-ttu-id="daa2e-1819">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="daa2e-1819">Added Source Control cmdlets</span></span>
* <span data-ttu-id="daa2e-1820">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1820">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="daa2e-1821">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="daa2e-1821">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="daa2e-1822">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1822">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1823">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="daa2e-1823">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="daa2e-1824">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1824">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="daa2e-1825">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1825">Az.ContainerInstance</span></span>
* <span data-ttu-id="daa2e-1826">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1826">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="daa2e-1827">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="daa2e-1827">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="daa2e-1828">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="daa2e-1828">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="daa2e-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1829">Az.Network</span></span>
* <span data-ttu-id="daa2e-1830">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="daa2e-1830">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="daa2e-1831">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1831">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="daa2e-1832">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1832">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="daa2e-1833">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="daa2e-1833">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="daa2e-1834">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="daa2e-1834">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="daa2e-1835">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1835">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="daa2e-1836">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1836">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="daa2e-1837">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="daa2e-1837">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="daa2e-1838">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="daa2e-1838">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="daa2e-1839">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="daa2e-1839">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="daa2e-1840">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="daa2e-1840">Az.Relay</span></span>
* <span data-ttu-id="daa2e-1841">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1841">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="daa2e-1842">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1842">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1843">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="daa2e-1843">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="daa2e-1844">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="daa2e-1844">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="daa2e-1845">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="daa2e-1845">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1846">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1846">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-1847">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1847">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="daa2e-1848">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1848">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1849">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="daa2e-1849">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="daa2e-1850">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1850">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="daa2e-1851">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1851">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="daa2e-1852">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1852">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="daa2e-1853">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="daa2e-1853">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="daa2e-1854">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="daa2e-1854">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="daa2e-1855">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="daa2e-1855">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="daa2e-1856">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="daa2e-1856">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="daa2e-1857">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="daa2e-1857">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="daa2e-1858">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1858">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="daa2e-1859">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1859">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="daa2e-1860">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1860">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="daa2e-1861">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1861">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="daa2e-1862">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1862">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="daa2e-1863">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1863">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="daa2e-1864">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1864">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="daa2e-1865">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1865">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="daa2e-1866">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1866">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="daa2e-1867">Generale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1867">General</span></span>
* <span data-ttu-id="daa2e-1868">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="daa2e-1868">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="daa2e-1869">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1869">Az.Profile</span></span>
* <span data-ttu-id="daa2e-1870">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="daa2e-1870">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="daa2e-1871">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="daa2e-1871">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="daa2e-1872">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="daa2e-1872">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="daa2e-1873">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="daa2e-1873">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="daa2e-1874">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="daa2e-1874">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="daa2e-1875">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="daa2e-1875">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="daa2e-1876">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="daa2e-1876">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-1877">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1877">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-1878">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1878">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1879">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1879">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1880">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="daa2e-1880">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="daa2e-1881">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="daa2e-1881">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="daa2e-1882">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1882">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1883">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1883">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1884">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1884">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="daa2e-1885">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1885">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="daa2e-1886">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1886">Az.Insights</span></span>
* <span data-ttu-id="daa2e-1887">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="daa2e-1887">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="daa2e-1888">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="daa2e-1888">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="daa2e-1889">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1889">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="daa2e-1890">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="daa2e-1890">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1891">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1891">Az.Network</span></span>
* <span data-ttu-id="daa2e-1892">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="daa2e-1892">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="daa2e-1893">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-1893">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="daa2e-1894">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-1894">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="daa2e-1895">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="daa2e-1895">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="daa2e-1896">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-1896">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="daa2e-1897">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="daa2e-1897">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="daa2e-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="daa2e-1898">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="daa2e-1899">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="daa2e-1899">Az.PolicyInsights</span></span>
* <span data-ttu-id="daa2e-1900">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="daa2e-1900">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1901">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1901">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1902">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="daa2e-1902">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="daa2e-1903">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1903">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="daa2e-1904">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="daa2e-1904">Az.ServiceBus</span></span>
* <span data-ttu-id="daa2e-1905">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1905">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="daa2e-1906">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="daa2e-1906">Az.ServiceFabric</span></span>
* <span data-ttu-id="daa2e-1907">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1907">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="daa2e-1908">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1908">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="daa2e-1909">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="daa2e-1909">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="daa2e-1910">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="daa2e-1910">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="daa2e-1911">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1911">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="daa2e-1912">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1912">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="daa2e-1913">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1913">Az.Profile</span></span>
* <span data-ttu-id="daa2e-1914">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="daa2e-1914">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="daa2e-1915">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="daa2e-1915">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1916">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1916">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1917">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="daa2e-1917">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="daa2e-1918">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1918">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="daa2e-1919">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="daa2e-1919">Az.DataLakeStore</span></span>
* <span data-ttu-id="daa2e-1920">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1920">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="daa2e-1921">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1921">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="daa2e-1922">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1922">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="daa2e-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1923">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="daa2e-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1924">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1925">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1925">Az.Network</span></span>
* <span data-ttu-id="daa2e-1926">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1926">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="daa2e-1927">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1927">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1928">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1928">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1929">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1929">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="daa2e-1930">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1930">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="daa2e-1931">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1931">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="daa2e-1932">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1932">Azure.Storage</span></span>
* <span data-ttu-id="daa2e-1933">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="daa2e-1933">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="daa2e-1934">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1934">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="daa2e-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="daa2e-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="daa2e-1936">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="daa2e-1936">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="daa2e-1937">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="daa2e-1937">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="daa2e-1938">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="daa2e-1938">Az.CognitiveServices</span></span>
* <span data-ttu-id="daa2e-1939">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1939">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="daa2e-1940">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="daa2e-1940">Az.Compute</span></span>
* <span data-ttu-id="daa2e-1941">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="daa2e-1941">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="daa2e-1942">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1942">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="daa2e-1943">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="daa2e-1943">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="daa2e-1944">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="daa2e-1944">Az.DataFactoryV2</span></span>
* <span data-ttu-id="daa2e-1945">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="daa2e-1945">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="daa2e-1946">Az.Network</span><span class="sxs-lookup"><span data-stu-id="daa2e-1946">Az.Network</span></span>
* <span data-ttu-id="daa2e-1947">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1947">Added NetworkProfile functionality.</span></span> <span data-ttu-id="daa2e-1948">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1948">new cmdlets added</span></span>
    - <span data-ttu-id="daa2e-1949">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1949">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="daa2e-1950">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1950">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="daa2e-1951">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1951">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="daa2e-1952">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="daa2e-1952">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="daa2e-1953">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1953">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="daa2e-1954">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1954">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="daa2e-1955">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="daa2e-1955">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="daa2e-1956">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="daa2e-1956">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="daa2e-1957">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="daa2e-1957">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="daa2e-1958">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="daa2e-1958">Az.RedisCache</span></span>
* <span data-ttu-id="daa2e-1959">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="daa2e-1959">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="daa2e-1960">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="daa2e-1960">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="daa2e-1961">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="daa2e-1961">Az.Resources</span></span>
* <span data-ttu-id="daa2e-1962">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="daa2e-1962">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="daa2e-1963">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="daa2e-1963">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="daa2e-1964">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="daa2e-1964">Az.Sql</span></span>
* <span data-ttu-id="daa2e-1965">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="daa2e-1965">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="daa2e-1966">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="daa2e-1966">Az.Websites</span></span>
* <span data-ttu-id="daa2e-1967">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="daa2e-1967">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="daa2e-1968">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="daa2e-1968">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="daa2e-1969">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="daa2e-1969">0.2.0 - September 2018</span></span>
 <span data-ttu-id="daa2e-1970">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="daa2e-1970">Initial Release</span></span>
