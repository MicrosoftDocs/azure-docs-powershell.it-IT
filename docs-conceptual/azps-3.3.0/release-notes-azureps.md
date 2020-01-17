---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 3806a1c609a71c53c0bddc5bafd51d845c0c296e
ms.sourcegitcommit: 16904e0a72c55fb81248e0252769defb86c50f36
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/10/2020
ms.locfileid: "75831645"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="56e67-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="56e67-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="56e67-104">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="56e67-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-105">Az.Accounts</span></span>
* <span data-ttu-id="56e67-106">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="56e67-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-107">Az.Cdn</span></span>
* <span data-ttu-id="56e67-108">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-108">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-109">Az.Compute</span></span>
* <span data-ttu-id="56e67-110">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="56e67-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="56e67-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="56e67-112">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="56e67-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="56e67-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="56e67-114">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="56e67-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="56e67-115">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-115">Get the Edge Storage Container</span></span>
* <span data-ttu-id="56e67-116">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="56e67-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="56e67-117">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-117">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="56e67-118">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="56e67-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="56e67-119">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-119">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="56e67-120">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="56e67-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="56e67-121">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-121">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="56e67-122">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="56e67-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="56e67-123">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-123">Get the Edge Storage Account</span></span>
* <span data-ttu-id="56e67-124">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="56e67-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="56e67-125">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-125">Create new Edge Storage Account</span></span>
* <span data-ttu-id="56e67-126">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="56e67-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="56e67-127">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="56e67-127">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="56e67-128">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="56e67-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="56e67-129">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="56e67-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="56e67-130">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="56e67-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="56e67-131">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="56e67-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-132">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-133">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="56e67-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="56e67-134">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="56e67-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="56e67-135">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="56e67-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="56e67-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="56e67-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="56e67-137">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="56e67-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-138">Az.EventHub</span></span>
* <span data-ttu-id="56e67-139">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="56e67-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="56e67-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="56e67-140">Az.HDInsight</span></span>
* <span data-ttu-id="56e67-141">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="56e67-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="56e67-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="56e67-142">Az.MachineLearning</span></span>
* <span data-ttu-id="56e67-143">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="56e67-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="56e67-144">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="56e67-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="56e67-145">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="56e67-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="56e67-146">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="56e67-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="56e67-147">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="56e67-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="56e67-148">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="56e67-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="56e67-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="56e67-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="56e67-150">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="56e67-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-151">Az.Network</span></span>
* <span data-ttu-id="56e67-152">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="56e67-152">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-154">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="56e67-155">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="56e67-156">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="56e67-157">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-158">Az.Resources</span></span>
* <span data-ttu-id="56e67-159">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="56e67-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-160">Az.Sql</span></span>
* <span data-ttu-id="56e67-161">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="56e67-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="56e67-162">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="56e67-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="56e67-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="56e67-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="56e67-164">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="56e67-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-165">Az.Storage</span></span>
* <span data-ttu-id="56e67-166">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="56e67-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="56e67-167">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="56e67-168">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="56e67-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="56e67-169">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="56e67-170">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="56e67-171">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-171">General</span></span>
* <span data-ttu-id="56e67-172">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="56e67-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-173">Az.Accounts</span></span>
* <span data-ttu-id="56e67-174">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="56e67-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="56e67-175">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="56e67-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="56e67-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-176">Az.Batch</span></span>
* <span data-ttu-id="56e67-177">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="56e67-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-178">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-179">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="56e67-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="56e67-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-180">Az.FrontDoor</span></span>
* <span data-ttu-id="56e67-181">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="56e67-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="56e67-182">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="56e67-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="56e67-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="56e67-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="56e67-184">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="56e67-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-185">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-186">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="56e67-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="56e67-187">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="56e67-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="56e67-188">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="56e67-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-189">Az.Monitor</span></span>
* <span data-ttu-id="56e67-190">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="56e67-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="56e67-191">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="56e67-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="56e67-192">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="56e67-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-193">Az.Network</span></span>
* <span data-ttu-id="56e67-194">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="56e67-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-195">Az.Resources</span></span>
* <span data-ttu-id="56e67-196">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="56e67-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="56e67-197">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="56e67-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-198">Az.Sql</span></span>
* <span data-ttu-id="56e67-199">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="56e67-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-200">Az.Storage</span></span>
* <span data-ttu-id="56e67-201">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="56e67-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="56e67-202">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="56e67-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="56e67-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="56e67-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="56e67-204">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="56e67-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="56e67-205">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="56e67-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="56e67-206">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="56e67-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="56e67-207">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="56e67-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="56e67-208">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="56e67-209">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="56e67-210">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="56e67-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="56e67-211">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="56e67-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="56e67-212">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="56e67-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="56e67-213">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="56e67-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="56e67-214">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="56e67-215">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="56e67-215">Highlights since the last major release</span></span>
* <span data-ttu-id="56e67-216">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="56e67-217">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-218">Az.Compute</span></span>
* <span data-ttu-id="56e67-219">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-219">VM Reapply feature</span></span>
    - <span data-ttu-id="56e67-220">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="56e67-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="56e67-221">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="56e67-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="56e67-222">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="56e67-223">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="56e67-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="56e67-224">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="56e67-225">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="56e67-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="56e67-226">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="56e67-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="56e67-227">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="56e67-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="56e67-228">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="56e67-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="56e67-229">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="56e67-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="56e67-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="56e67-231">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="56e67-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="56e67-232">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="56e67-232">Get the Order</span></span>
* <span data-ttu-id="56e67-233">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="56e67-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="56e67-234">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="56e67-234">Create new Order</span></span>
* <span data-ttu-id="56e67-235">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="56e67-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="56e67-236">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="56e67-236">Remove the Order</span></span>
* <span data-ttu-id="56e67-237">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="56e67-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="56e67-238">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="56e67-238">Now creates Local Share</span></span>
* <span data-ttu-id="56e67-239">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="56e67-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="56e67-240">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="56e67-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="56e67-241">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="56e67-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="56e67-242">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="56e67-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="56e67-243">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="56e67-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="56e67-244">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="56e67-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="56e67-245">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="56e67-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="56e67-246">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="56e67-246">Create new Triggers</span></span>
* <span data-ttu-id="56e67-247">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="56e67-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="56e67-248">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="56e67-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-249">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-250">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="56e67-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="56e67-251">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="56e67-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-253">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="56e67-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-254">Az.EventHub</span></span>
* <span data-ttu-id="56e67-255">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="56e67-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="56e67-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-256">Az.FrontDoor</span></span>
* <span data-ttu-id="56e67-257">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="56e67-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="56e67-258">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="56e67-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="56e67-259">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="56e67-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="56e67-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="56e67-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-261">Az.Network</span></span>
* <span data-ttu-id="56e67-262">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="56e67-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="56e67-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="56e67-263">Az.PrivateDns</span></span>
* <span data-ttu-id="56e67-264">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-266">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="56e67-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="56e67-267">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="56e67-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="56e67-268">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="56e67-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="56e67-269">Az.RedisCache</span></span>
* <span data-ttu-id="56e67-270">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="56e67-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="56e67-271">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="56e67-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="56e67-272">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="56e67-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-273">Az.Resources</span></span>
- <span data-ttu-id="56e67-274">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="56e67-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="56e67-275">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="56e67-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="56e67-276">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="56e67-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="56e67-277">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="56e67-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="56e67-278">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="56e67-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-279">Az.Sql</span></span>
* <span data-ttu-id="56e67-280">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="56e67-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="56e67-281">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="56e67-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="56e67-282">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="56e67-283">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-283">General</span></span>
* <span data-ttu-id="56e67-284">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-285">Az.Accounts</span></span>
* <span data-ttu-id="56e67-286">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="56e67-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="56e67-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="56e67-287">Az.Advisor</span></span>
* <span data-ttu-id="56e67-288">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="56e67-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="56e67-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-289">Az.Batch</span></span>
* <span data-ttu-id="56e67-290">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="56e67-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="56e67-291">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="56e67-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="56e67-292">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="56e67-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="56e67-293">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="56e67-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="56e67-294">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="56e67-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="56e67-295">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="56e67-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="56e67-296">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="56e67-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="56e67-297">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="56e67-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="56e67-298">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="56e67-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="56e67-299">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="56e67-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="56e67-300">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="56e67-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="56e67-301">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="56e67-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="56e67-302">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="56e67-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="56e67-303">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="56e67-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="56e67-304">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="56e67-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="56e67-305">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="56e67-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="56e67-306">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="56e67-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="56e67-307">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="56e67-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="56e67-308">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="56e67-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="56e67-309">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="56e67-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="56e67-310">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="56e67-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="56e67-311">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="56e67-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="56e67-312">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="56e67-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="56e67-313">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="56e67-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="56e67-314">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="56e67-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="56e67-315">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="56e67-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="56e67-316">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="56e67-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="56e67-317">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="56e67-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="56e67-318">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="56e67-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="56e67-319">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="56e67-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="56e67-320">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="56e67-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="56e67-321">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="56e67-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="56e67-322">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="56e67-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="56e67-323">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="56e67-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="56e67-324">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="56e67-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="56e67-325">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="56e67-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-326">Az.Cdn</span></span>
* <span data-ttu-id="56e67-327">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="56e67-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="56e67-328">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="56e67-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-329">Az.Compute</span></span>
* <span data-ttu-id="56e67-330">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="56e67-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="56e67-331">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="56e67-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="56e67-332">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="56e67-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="56e67-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="56e67-334">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="56e67-335">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="56e67-336">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="56e67-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="56e67-337">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="56e67-338">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="56e67-338">Breaking changes</span></span>
    - <span data-ttu-id="56e67-339">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="56e67-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="56e67-340">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="56e67-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-341">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-342">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="56e67-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-344">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="56e67-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="56e67-345">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="56e67-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="56e67-346">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="56e67-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="56e67-347">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="56e67-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="56e67-348">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="56e67-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="56e67-349">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="56e67-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="56e67-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-350">Az.FrontDoor</span></span>
* <span data-ttu-id="56e67-351">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="56e67-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="56e67-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="56e67-352">Az.HDInsight</span></span>
* <span data-ttu-id="56e67-353">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="56e67-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="56e67-354">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="56e67-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="56e67-355">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="56e67-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="56e67-356">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="56e67-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="56e67-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="56e67-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="56e67-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="56e67-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="56e67-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="56e67-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="56e67-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="56e67-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="56e67-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="56e67-362">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="56e67-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="56e67-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="56e67-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="56e67-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="56e67-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="56e67-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="56e67-366">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="56e67-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="56e67-367">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="56e67-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="56e67-368">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="56e67-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="56e67-369">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="56e67-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="56e67-370">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="56e67-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="56e67-371">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="56e67-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="56e67-372">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="56e67-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="56e67-373">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="56e67-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="56e67-374">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="56e67-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-375">Az.IotHub</span></span>
* <span data-ttu-id="56e67-376">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="56e67-376">Breaking changes:</span></span>
    - <span data-ttu-id="56e67-377">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="56e67-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="56e67-378">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="56e67-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="56e67-379">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="56e67-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="56e67-380">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="56e67-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="56e67-381">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="56e67-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="56e67-382">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="56e67-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="56e67-383">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="56e67-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="56e67-384">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="56e67-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="56e67-385">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="56e67-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="56e67-386">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="56e67-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="56e67-387">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="56e67-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="56e67-388">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="56e67-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-390">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-391">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="56e67-392">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="56e67-393">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-394">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-395">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-396">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-397">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-398">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="56e67-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-399">Az.Resources</span></span>
* <span data-ttu-id="56e67-400">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="56e67-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-401">Az.Network</span></span>
* <span data-ttu-id="56e67-402">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="56e67-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="56e67-403">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="56e67-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="56e67-404">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-405">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-406">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-407">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="56e67-409">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="56e67-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="56e67-410">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-410">New cmdlet:</span></span>
        - <span data-ttu-id="56e67-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="56e67-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="56e67-412">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="56e67-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="56e67-413">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="56e67-414">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="56e67-415">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="56e67-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="56e67-416">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="56e67-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="56e67-417">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="56e67-418">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="56e67-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="56e67-419">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-419">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="56e67-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="56e67-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="56e67-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="56e67-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="56e67-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="56e67-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="56e67-425">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="56e67-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="56e67-426">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="56e67-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="56e67-427">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="56e67-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="56e67-428">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="56e67-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="56e67-429">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="56e67-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="56e67-430">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="56e67-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="56e67-431">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="56e67-432">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-432">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="56e67-434">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="56e67-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="56e67-435">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="56e67-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="56e67-436">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="56e67-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="56e67-437">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="56e67-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="56e67-438">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="56e67-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="56e67-439">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="56e67-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="56e67-440">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="56e67-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="56e67-441">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-441">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="56e67-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="56e67-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="56e67-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="56e67-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="56e67-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="56e67-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="56e67-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="56e67-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="56e67-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="56e67-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="56e67-448">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="56e67-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="56e67-449">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="56e67-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="56e67-450">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="56e67-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="56e67-451">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="56e67-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="56e67-452">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="56e67-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="56e67-453">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="56e67-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="56e67-454">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="56e67-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="56e67-455">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="56e67-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="56e67-456">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="56e67-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="56e67-457">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="56e67-458">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="56e67-459">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-459">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="56e67-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="56e67-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="56e67-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-465">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="56e67-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-466">Az.Sql</span></span>
* <span data-ttu-id="56e67-467">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="56e67-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="56e67-468">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="56e67-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="56e67-469">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="56e67-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="56e67-470">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="56e67-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="56e67-471">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="56e67-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="56e67-472">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="56e67-473">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="56e67-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="56e67-474">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="56e67-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="56e67-475">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="56e67-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-476">Az.Storage</span></span>
* <span data-ttu-id="56e67-477">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="56e67-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="56e67-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="56e67-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="56e67-480">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="56e67-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="56e67-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="56e67-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="56e67-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="56e67-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="56e67-483">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="56e67-484">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-484">General</span></span>
* <span data-ttu-id="56e67-485">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-486">Az.Accounts</span></span>
* <span data-ttu-id="56e67-487">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="56e67-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="56e67-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-488">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-489">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="56e67-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="56e67-490">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="56e67-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-491">Az.Automation</span></span>
* <span data-ttu-id="56e67-492">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="56e67-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="56e67-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-493">Az.Batch</span></span>
* <span data-ttu-id="56e67-494">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="56e67-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-495">Az.Compute</span></span>
* <span data-ttu-id="56e67-496">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="56e67-497">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="56e67-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="56e67-498">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="56e67-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="56e67-499">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="56e67-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-500">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-501">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="56e67-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="56e67-502">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="56e67-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="56e67-503">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="56e67-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-505">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="56e67-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="56e67-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="56e67-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="56e67-507">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="56e67-508">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="56e67-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="56e67-509">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="56e67-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="56e67-510">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="56e67-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-511">Az.IotHub</span></span>
* <span data-ttu-id="56e67-512">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="56e67-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="56e67-513">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="56e67-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="56e67-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-514">Az.Monitor</span></span>
* <span data-ttu-id="56e67-515">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="56e67-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="56e67-516">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="56e67-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="56e67-517">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="56e67-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="56e67-518">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="56e67-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-519">Az.Network</span></span>
* <span data-ttu-id="56e67-520">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="56e67-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="56e67-521">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="56e67-522">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-522">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-523">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="56e67-524">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="56e67-525">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="56e67-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="56e67-526">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="56e67-527">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="56e67-528">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="56e67-529">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="56e67-530">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="56e67-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="56e67-531">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="56e67-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="56e67-532">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="56e67-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="56e67-533">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="56e67-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="56e67-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="56e67-534">Az.RedisCache</span></span>
* <span data-ttu-id="56e67-535">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="56e67-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-536">Az.Sql</span></span>
* <span data-ttu-id="56e67-537">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="56e67-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-538">Az.Storage</span></span>
* <span data-ttu-id="56e67-539">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="56e67-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="56e67-540">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="56e67-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="56e67-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="56e67-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="56e67-542">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="56e67-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="56e67-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="56e67-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="56e67-544">Az.StorageSync</span></span>
* <span data-ttu-id="56e67-545">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="56e67-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-546">Az.Websites</span></span>
* <span data-ttu-id="56e67-547">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="56e67-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="56e67-548">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="56e67-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-549">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-550">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="56e67-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="56e67-551">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="56e67-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="56e67-552">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="56e67-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-553">Az.Automation</span></span>
* <span data-ttu-id="56e67-554">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="56e67-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="56e67-555">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="56e67-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="56e67-556">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="56e67-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-557">Az.Compute</span></span>
* <span data-ttu-id="56e67-558">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="56e67-559">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="56e67-560">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="56e67-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="56e67-561">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="56e67-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="56e67-562">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="56e67-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="56e67-563">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="56e67-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="56e67-564">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="56e67-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="56e67-565">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="56e67-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="56e67-566">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="56e67-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-567">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-568">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="56e67-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="56e67-569">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="56e67-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="56e67-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="56e67-570">Az.HDInsight</span></span>
* <span data-ttu-id="56e67-571">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="56e67-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-572">Az.IotHub</span></span>
* <span data-ttu-id="56e67-573">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="56e67-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="56e67-574">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="56e67-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="56e67-575">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="56e67-575">New cmdlets are:</span></span>
    - <span data-ttu-id="56e67-576">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56e67-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="56e67-577">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56e67-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="56e67-578">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56e67-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="56e67-579">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="56e67-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-580">Az.Monitor</span></span>
* <span data-ttu-id="56e67-581">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="56e67-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="56e67-582">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="56e67-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="56e67-583">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="56e67-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="56e67-584">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="56e67-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="56e67-585">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="56e67-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="56e67-586">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="56e67-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="56e67-587">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e67-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="56e67-588">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="56e67-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="56e67-589">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="56e67-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="56e67-590">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="56e67-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="56e67-591">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="56e67-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="56e67-592">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="56e67-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="56e67-593">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="56e67-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="56e67-594">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="56e67-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="56e67-595">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="56e67-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="56e67-596">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="56e67-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="56e67-597">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="56e67-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="56e67-598">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="56e67-599">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="56e67-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="56e67-600">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-600">Overall improved help files</span></span>
* <span data-ttu-id="56e67-601">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="56e67-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-602">Az.Network</span></span>
* <span data-ttu-id="56e67-603">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="56e67-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="56e67-604">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="56e67-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="56e67-605">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="56e67-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="56e67-606">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="56e67-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="56e67-607">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="56e67-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="56e67-608">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="56e67-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="56e67-609">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="56e67-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="56e67-610">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="56e67-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="56e67-611">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="56e67-612">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="56e67-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="56e67-613">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="56e67-614">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="56e67-615">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-615">New cmdlets</span></span>
        - <span data-ttu-id="56e67-616">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="56e67-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="56e67-617">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="56e67-618">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="56e67-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="56e67-619">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="56e67-619">New-VpnSite</span></span>
        - <span data-ttu-id="56e67-620">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="56e67-620">Update-VpnSite</span></span>
        - <span data-ttu-id="56e67-621">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-621">New-VpnConnection</span></span>
        - <span data-ttu-id="56e67-622">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-622">Update-VpnConnection</span></span>
* <span data-ttu-id="56e67-623">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="56e67-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-625">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="56e67-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="56e67-626">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="56e67-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-627">Az.Resources</span></span>
* <span data-ttu-id="56e67-628">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="56e67-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-630">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="56e67-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="56e67-631">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="56e67-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="56e67-632">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="56e67-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="56e67-633">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="56e67-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="56e67-634">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="56e67-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="56e67-635">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="56e67-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="56e67-636">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="56e67-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="56e67-637">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="56e67-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="56e67-638">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="56e67-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="56e67-639">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="56e67-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="56e67-640">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="56e67-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="56e67-641">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="56e67-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="56e67-642">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="56e67-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="56e67-643">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="56e67-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="56e67-644">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="56e67-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="56e67-645">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="56e67-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="56e67-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="56e67-646">Az.SignalR</span></span>
* <span data-ttu-id="56e67-647">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="56e67-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-648">Az.Sql</span></span>
* <span data-ttu-id="56e67-649">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="56e67-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="56e67-650">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="56e67-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="56e67-651">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="56e67-652">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="56e67-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="56e67-653">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="56e67-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-654">Az.Storage</span></span>
* <span data-ttu-id="56e67-655">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="56e67-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="56e67-656">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="56e67-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="56e67-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="56e67-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="56e67-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="56e67-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="56e67-659">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="56e67-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="56e67-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="56e67-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="56e67-661">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="56e67-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="56e67-662">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="56e67-663">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="56e67-664">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="56e67-665">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="56e67-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-666">Az.Websites</span></span>
* <span data-ttu-id="56e67-667">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="56e67-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="56e67-668">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="56e67-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="56e67-669">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="56e67-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="56e67-670">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="56e67-671">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-671">General</span></span>
* <span data-ttu-id="56e67-672">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="56e67-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-673">Az.Accounts</span></span>
* <span data-ttu-id="56e67-674">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="56e67-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="56e67-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="56e67-675">Az.Aks</span></span>
* <span data-ttu-id="56e67-676">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="56e67-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="56e67-677">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="56e67-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="56e67-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-678">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-679">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="56e67-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="56e67-680">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="56e67-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="56e67-681">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="56e67-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="56e67-682">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="56e67-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="56e67-683">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="56e67-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="56e67-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-684">Az.Batch</span></span>
* <span data-ttu-id="56e67-685">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="56e67-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-686">Az.Cdn</span></span>
* <span data-ttu-id="56e67-687">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="56e67-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-688">Az.Compute</span></span>
* <span data-ttu-id="56e67-689">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="56e67-690">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="56e67-691">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="56e67-692">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="56e67-693">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="56e67-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="56e67-694">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="56e67-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="56e67-695">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="56e67-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="56e67-696">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="56e67-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-697">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-698">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="56e67-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="56e67-699">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="56e67-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="56e67-700">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="56e67-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="56e67-701">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="56e67-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-703">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="56e67-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-704">Az.EventHub</span></span>
* <span data-ttu-id="56e67-705">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="56e67-706">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="56e67-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="56e67-707">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="56e67-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="56e67-708">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="56e67-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="56e67-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="56e67-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="56e67-710">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="56e67-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-711">Az.Monitor</span></span>
* <span data-ttu-id="56e67-712">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-713">Az.Network</span></span>
* <span data-ttu-id="56e67-714">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="56e67-715">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="56e67-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="56e67-716">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="56e67-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="56e67-717">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="56e67-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="56e67-718">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="56e67-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="56e67-719">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="56e67-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="56e67-720">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="56e67-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-722">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="56e67-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="56e67-723">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="56e67-723">Added example</span></span>
    - <span data-ttu-id="56e67-724">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="56e67-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="56e67-725">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="56e67-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="56e67-726">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="56e67-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-728">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-729">Az.Resources</span></span>
* <span data-ttu-id="56e67-730">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="56e67-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="56e67-731">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="56e67-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="56e67-732">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="56e67-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="56e67-733">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-734">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-735">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="56e67-736">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="56e67-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="56e67-737">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="56e67-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-739">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="56e67-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="56e67-740">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="56e67-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="56e67-741">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="56e67-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="56e67-742">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="56e67-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="56e67-743">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="56e67-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="56e67-744">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="56e67-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-745">Az.Sql</span></span>
* <span data-ttu-id="56e67-746">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="56e67-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-747">Az.Storage</span></span>
* <span data-ttu-id="56e67-748">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="56e67-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="56e67-749">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="56e67-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="56e67-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="56e67-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="56e67-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="56e67-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="56e67-752">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="56e67-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="56e67-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="56e67-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-754">Az.Websites</span></span>
* <span data-ttu-id="56e67-755">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56e67-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="56e67-756">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-757">Az.Accounts</span></span>
* <span data-ttu-id="56e67-758">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="56e67-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="56e67-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="56e67-760">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="56e67-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="56e67-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-761">Az.Automation</span></span>
* <span data-ttu-id="56e67-762">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="56e67-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-764">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="56e67-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-765">Az.Compute</span></span>
* <span data-ttu-id="56e67-766">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="56e67-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="56e67-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="56e67-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="56e67-768">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="56e67-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="56e67-769">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="56e67-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-770">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-771">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="56e67-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="56e67-772">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="56e67-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-773">Az.EventHub</span></span>
* <span data-ttu-id="56e67-774">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="56e67-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="56e67-775">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="56e67-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-776">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-777">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="56e67-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="56e67-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="56e67-778">Az.LogicApp</span></span>
* <span data-ttu-id="56e67-779">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="56e67-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="56e67-780">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="56e67-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="56e67-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="56e67-781">Az.ManagedServices</span></span>
* <span data-ttu-id="56e67-782">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="56e67-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-783">Az.Network</span></span>
* <span data-ttu-id="56e67-784">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="56e67-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="56e67-785">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-785">New cmdlets</span></span>
        - <span data-ttu-id="56e67-786">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="56e67-787">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="56e67-788">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-789">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-790">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-791">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="56e67-792">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="56e67-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="56e67-793">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="56e67-794">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="56e67-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="56e67-795">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="56e67-796">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="56e67-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="56e67-797">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="56e67-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="56e67-798">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="56e67-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="56e67-799">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="56e67-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="56e67-800">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-800">Updated cmdlets</span></span>
        - <span data-ttu-id="56e67-801">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="56e67-802">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="56e67-803">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="56e67-804">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="56e67-805">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="56e67-806">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="56e67-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="56e67-807">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="56e67-808">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="56e67-809">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="56e67-810">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="56e67-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="56e67-811">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="56e67-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="56e67-812">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="56e67-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-814">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="56e67-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="56e67-815">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="56e67-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-817">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="56e67-818">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="56e67-819">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="56e67-820">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="56e67-821">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="56e67-822">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="56e67-823">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="56e67-824">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="56e67-825">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="56e67-826">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="56e67-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-827">Az.Resources</span></span>
- <span data-ttu-id="56e67-828">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="56e67-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="56e67-829">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="56e67-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-830">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-831">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="56e67-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="56e67-832">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="56e67-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-833">Az.Sql</span></span>
* <span data-ttu-id="56e67-834">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="56e67-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="56e67-835">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="56e67-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="56e67-836">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="56e67-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-837">Az.Storage</span></span>
* <span data-ttu-id="56e67-838">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="56e67-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="56e67-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="56e67-839">Az.StorageSync</span></span>
* <span data-ttu-id="56e67-840">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="56e67-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="56e67-841">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="56e67-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-842">Az.Websites</span></span>
* <span data-ttu-id="56e67-843">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="56e67-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="56e67-844">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="56e67-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="56e67-845">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="56e67-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="56e67-846">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-847">Az.Accounts</span></span>
* <span data-ttu-id="56e67-848">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="56e67-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="56e67-849">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="56e67-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="56e67-850">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="56e67-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="56e67-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="56e67-851">Az.Advisor</span></span>
* <span data-ttu-id="56e67-852">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="56e67-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="56e67-853">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="56e67-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="56e67-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-854">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-855">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="56e67-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="56e67-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="56e67-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="56e67-857">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="56e67-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="56e67-858">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="56e67-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="56e67-859">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="56e67-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="56e67-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="56e67-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="56e67-861">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="56e67-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-862">Az.Automation</span></span>
* <span data-ttu-id="56e67-863">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="56e67-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-864">Az.Compute</span></span>
* <span data-ttu-id="56e67-865">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-866">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-867">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="56e67-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="56e67-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="56e67-868">Az.EventGrid</span></span>
* <span data-ttu-id="56e67-869">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="56e67-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-870">Az.IotHub</span></span>
* <span data-ttu-id="56e67-871">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="56e67-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-872">Az.Network</span></span>
* <span data-ttu-id="56e67-873">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="56e67-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="56e67-874">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="56e67-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="56e67-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="56e67-876">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="56e67-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="56e67-877">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="56e67-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-879">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="56e67-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-881">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="56e67-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-882">Az.Resources</span></span>
    - <span data-ttu-id="56e67-883">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="56e67-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="56e67-884">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="56e67-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="56e67-885">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="56e67-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="56e67-886">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="56e67-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-887">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-888">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="56e67-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-889">Az.Sql</span></span>
* <span data-ttu-id="56e67-890">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="56e67-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="56e67-891">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="56e67-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="56e67-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="56e67-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="56e67-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="56e67-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="56e67-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="56e67-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="56e67-898">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="56e67-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-899">Az.Storage</span></span>
* <span data-ttu-id="56e67-900">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="56e67-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="56e67-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="56e67-902">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="56e67-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="56e67-903">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="56e67-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="56e67-904">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="56e67-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="56e67-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="56e67-907">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="56e67-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="56e67-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="56e67-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="56e67-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="56e67-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="56e67-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="56e67-910">Az.StorageSync</span></span>
* <span data-ttu-id="56e67-911">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="56e67-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="56e67-912">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-913">Az.Accounts</span></span>
* <span data-ttu-id="56e67-914">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="56e67-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="56e67-915">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="56e67-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="56e67-916">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="56e67-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="56e67-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="56e67-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="56e67-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="56e67-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-919">Az.Compute</span></span>
* <span data-ttu-id="56e67-920">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="56e67-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="56e67-921">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="56e67-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="56e67-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="56e67-922">Az.Dns</span></span>
* <span data-ttu-id="56e67-923">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="56e67-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="56e67-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="56e67-924">Az.EventGrid</span></span>
* <span data-ttu-id="56e67-925">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="56e67-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="56e67-926">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-926">New cmdlets:</span></span>
    - <span data-ttu-id="56e67-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="56e67-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="56e67-928">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="56e67-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="56e67-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="56e67-930">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="56e67-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="56e67-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="56e67-932">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="56e67-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="56e67-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="56e67-934">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="56e67-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="56e67-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="56e67-936">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="56e67-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="56e67-937">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="56e67-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="56e67-938">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="56e67-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="56e67-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="56e67-940">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="56e67-941">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="56e67-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="56e67-942">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="56e67-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="56e67-943">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="56e67-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="56e67-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="56e67-945">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="56e67-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="56e67-946">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="56e67-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="56e67-947">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="56e67-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="56e67-948">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="56e67-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="56e67-949">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="56e67-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="56e67-950">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="56e67-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="56e67-951">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="56e67-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="56e67-952">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="56e67-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="56e67-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="56e67-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="56e67-954">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="56e67-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="56e67-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="56e67-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="56e67-956">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="56e67-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="56e67-957">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="56e67-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="56e67-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-958">Az.FrontDoor</span></span>
* <span data-ttu-id="56e67-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="56e67-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="56e67-960">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="56e67-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="56e67-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="56e67-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="56e67-962">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="56e67-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-963">Az.Network</span></span>
* <span data-ttu-id="56e67-964">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="56e67-965">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-965">New cmdlets</span></span>
        - <span data-ttu-id="56e67-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="56e67-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="56e67-967">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="56e67-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="56e67-968">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-968">New cmdlets</span></span> 
        - <span data-ttu-id="56e67-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="56e67-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="56e67-970">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="56e67-971">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-971">New cmdlets</span></span> 
        - <span data-ttu-id="56e67-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="56e67-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="56e67-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="56e67-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="56e67-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="56e67-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="56e67-977">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="56e67-978">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-978">New cmdlets</span></span>
        - <span data-ttu-id="56e67-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="56e67-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="56e67-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="56e67-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="56e67-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="56e67-983">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="56e67-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="56e67-984">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="56e67-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="56e67-985">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="56e67-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="56e67-986">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56e67-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="56e67-987">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="56e67-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="56e67-988">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="56e67-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="56e67-989">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="56e67-990">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="56e67-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="56e67-991">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="56e67-992">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="56e67-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="56e67-993">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="56e67-994">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="56e67-995">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="56e67-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="56e67-996">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="56e67-997">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="56e67-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="56e67-998">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="56e67-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="56e67-999">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="56e67-1000">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="56e67-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="56e67-1001">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="56e67-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="56e67-1002">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="56e67-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="56e67-1003">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="56e67-1004">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="56e67-1005">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-1007">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="56e67-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1008">Az.Resources</span></span>
* <span data-ttu-id="56e67-1009">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="56e67-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="56e67-1010">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="56e67-1011">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="56e67-1012">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="56e67-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-1014">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="56e67-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1015">Az.Sql</span></span>
* <span data-ttu-id="56e67-1016">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="56e67-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="56e67-1017">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="56e67-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="56e67-1018">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="56e67-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="56e67-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="56e67-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="56e67-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="56e67-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="56e67-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="56e67-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="56e67-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="56e67-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="56e67-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="56e67-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1024">Az.Storage</span></span>
* <span data-ttu-id="56e67-1025">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="56e67-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="56e67-1027">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="56e67-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="56e67-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1029">Az.Websites</span></span>
* <span data-ttu-id="56e67-1030">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="56e67-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="56e67-1031">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="56e67-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="56e67-1032">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="56e67-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-1033">Az.Cdn</span></span>
* <span data-ttu-id="56e67-1034">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="56e67-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1035">Az.Compute</span></span>
* <span data-ttu-id="56e67-1036">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="56e67-1037">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="56e67-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1038">Az.EventHub</span></span>
* <span data-ttu-id="56e67-1039">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="56e67-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="56e67-1040">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e67-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1041">Az.Network</span></span>
* <span data-ttu-id="56e67-1042">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="56e67-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="56e67-1043">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="56e67-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="56e67-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="56e67-1045">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="56e67-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1047">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="56e67-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-1049">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e67-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-1051">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="56e67-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="56e67-1052">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1053">Az.Sql</span></span>
* <span data-ttu-id="56e67-1054">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="56e67-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="56e67-1055">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="56e67-1056">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="56e67-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="56e67-1057">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="56e67-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1058">Az.Websites</span></span>
* <span data-ttu-id="56e67-1059">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="56e67-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="56e67-1060">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="56e67-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-1062">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="56e67-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="56e67-1063">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="56e67-1064">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="56e67-1065">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="56e67-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="56e67-1066">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="56e67-1067">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="56e67-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="56e67-1068">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="56e67-1069">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="56e67-1070">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="56e67-1071">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="56e67-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="56e67-1072">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="56e67-1073">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="56e67-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="56e67-1074">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="56e67-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="56e67-1075">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="56e67-1076">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="56e67-1077">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="56e67-1078">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="56e67-1079">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="56e67-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="56e67-1080">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="56e67-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="56e67-1081">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="56e67-1082">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="56e67-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="56e67-1083">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="56e67-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="56e67-1084">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="56e67-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="56e67-1085">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="56e67-1086">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="56e67-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="56e67-1087">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="56e67-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="56e67-1088">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="56e67-1089">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="56e67-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="56e67-1090">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="56e67-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="56e67-1091">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="56e67-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="56e67-1092">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="56e67-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="56e67-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="56e67-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="56e67-1094">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="56e67-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="56e67-1095">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="56e67-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="56e67-1096">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="56e67-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="56e67-1097">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="56e67-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="56e67-1098">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="56e67-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="56e67-1099">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="56e67-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="56e67-1100">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="56e67-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="56e67-1101">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="56e67-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="56e67-1102">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="56e67-1103">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="56e67-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="56e67-1104">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="56e67-1105">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="56e67-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="56e67-1106">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="56e67-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="56e67-1107">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="56e67-1108">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="56e67-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="56e67-1109">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="56e67-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="56e67-1110">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="56e67-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="56e67-1111">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="56e67-1112">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="56e67-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="56e67-1113">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="56e67-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="56e67-1114">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="56e67-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="56e67-1115">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="56e67-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="56e67-1116">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="56e67-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="56e67-1117">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="56e67-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="56e67-1118">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="56e67-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="56e67-1119">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="56e67-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="56e67-1120">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="56e67-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="56e67-1121">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="56e67-1122">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="56e67-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="56e67-1123">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="56e67-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="56e67-1124">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="56e67-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="56e67-1125">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="56e67-1126">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="56e67-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="56e67-1127">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="56e67-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="56e67-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="56e67-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="56e67-1129">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="56e67-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="56e67-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="56e67-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="56e67-1131">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="56e67-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="56e67-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="56e67-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="56e67-1133">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="56e67-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="56e67-1134">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="56e67-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="56e67-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="56e67-1136">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="56e67-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="56e67-1137">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="56e67-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="56e67-1138">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="56e67-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1139">Az.Automation</span></span>
* <span data-ttu-id="56e67-1140">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="56e67-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="56e67-1141">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="56e67-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="56e67-1142">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="56e67-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="56e67-1143">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="56e67-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="56e67-1144">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="56e67-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="56e67-1145">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="56e67-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="56e67-1146">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="56e67-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1147">Az.Compute</span></span>
* <span data-ttu-id="56e67-1148">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="56e67-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="56e67-1149">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="56e67-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1151">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-1152">Az.Monitor</span></span>
* <span data-ttu-id="56e67-1153">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1154">Az.Network</span></span>
* <span data-ttu-id="56e67-1155">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="56e67-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="56e67-1156">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="56e67-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="56e67-1157">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="56e67-1158">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="56e67-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1159">Az.Resources</span></span>
* <span data-ttu-id="56e67-1160">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="56e67-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1161">Az.Sql</span></span>
* <span data-ttu-id="56e67-1162">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="56e67-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="56e67-1163">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1164">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1165">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="56e67-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-1167">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="56e67-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="56e67-1168">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="56e67-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1169">Az.Compute</span></span>
* <span data-ttu-id="56e67-1170">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="56e67-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="56e67-1171">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="56e67-1172">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="56e67-1173">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="56e67-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="56e67-1174">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="56e67-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="56e67-1175">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="56e67-1176">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="56e67-1176">Breaking changes</span></span>
    - <span data-ttu-id="56e67-1177">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="56e67-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="56e67-1178">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="56e67-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="56e67-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="56e67-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="56e67-1180">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="56e67-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="56e67-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="56e67-1181">Az.Dns</span></span>
* <span data-ttu-id="56e67-1182">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="56e67-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="56e67-1183">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="56e67-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="56e67-1184">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="56e67-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="56e67-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="56e67-1186">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="56e67-1187">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="56e67-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="56e67-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="56e67-1188">Az.HDInsight</span></span>
* <span data-ttu-id="56e67-1189">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="56e67-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="56e67-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="56e67-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="56e67-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="56e67-1192">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="56e67-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="56e67-1193">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="56e67-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="56e67-1194">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="56e67-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="56e67-1195">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-1196">Az.Monitor</span></span>
* <span data-ttu-id="56e67-1197">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="56e67-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="56e67-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="56e67-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="56e67-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="56e67-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="56e67-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="56e67-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="56e67-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="56e67-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="56e67-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="56e67-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="56e67-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="56e67-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="56e67-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="56e67-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="56e67-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="56e67-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="56e67-1209">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="56e67-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="56e67-1210">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="56e67-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1211">Az.Network</span></span>
* <span data-ttu-id="56e67-1212">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="56e67-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="56e67-1213">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-1213">New cmdlets</span></span>
        - <span data-ttu-id="56e67-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="56e67-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="56e67-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="56e67-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="56e67-1218">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="56e67-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="56e67-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="56e67-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="56e67-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="56e67-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="56e67-1221">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="56e67-1222">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="56e67-1223">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="56e67-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="56e67-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="56e67-1225">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="56e67-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="56e67-1226">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="56e67-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="56e67-1227">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1229">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="56e67-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="56e67-1230">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="56e67-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="56e67-1231">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="56e67-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="56e67-1232">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="56e67-1233">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="56e67-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="56e67-1234">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="56e67-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="56e67-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="56e67-1235">Az.Relay</span></span>
* <span data-ttu-id="56e67-1236">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="56e67-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-1238">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56e67-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1239">Az.Storage</span></span>
* <span data-ttu-id="56e67-1240">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="56e67-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="56e67-1241">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="56e67-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="56e67-1242">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="56e67-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="56e67-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="56e67-1244">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="56e67-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="56e67-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="56e67-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="56e67-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1248">Az.Websites</span></span>
* <span data-ttu-id="56e67-1249">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="56e67-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="56e67-1250">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="56e67-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="56e67-1251">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="56e67-1252">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="56e67-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="56e67-1253">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="56e67-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="56e67-1254">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="56e67-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="56e67-1255">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="56e67-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="56e67-1256">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="56e67-1257">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="56e67-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="56e67-1258">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="56e67-1259">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="56e67-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1260">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1261">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="56e67-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="56e67-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-1262">Az.Batch</span></span>
* <span data-ttu-id="56e67-1263">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-1264">Az.Cdn</span></span>
* <span data-ttu-id="56e67-1265">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-1267">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1268">Az.Compute</span></span>
* <span data-ttu-id="56e67-1269">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="56e67-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="56e67-1270">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1271">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="56e67-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-1272">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-1273">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="56e67-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1275">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="56e67-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="56e67-1276">Az.EventGrid</span></span>
* <span data-ttu-id="56e67-1277">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="56e67-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1278">Az.EventHub</span></span>
* <span data-ttu-id="56e67-1279">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="56e67-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="56e67-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="56e67-1280">Az.HDInsight</span></span>
* <span data-ttu-id="56e67-1281">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1282">Az.IotHub</span></span>
* <span data-ttu-id="56e67-1283">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1284">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-1285">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1286">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="56e67-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="56e67-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="56e67-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="56e67-1288">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="56e67-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="56e67-1289">Az.Media</span></span>
* <span data-ttu-id="56e67-1290">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-1291">Az.Monitor</span></span>
  * <span data-ttu-id="56e67-1292">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="56e67-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="56e67-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="56e67-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="56e67-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="56e67-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="56e67-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="56e67-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="56e67-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="56e67-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="56e67-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="56e67-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="56e67-1298">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="56e67-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1299">Az.Network</span></span>
* <span data-ttu-id="56e67-1300">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1301">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="56e67-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="56e67-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="56e67-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="56e67-1303">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-1305">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="56e67-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="56e67-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="56e67-1307">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1309">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1310">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="56e67-1311">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="56e67-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="56e67-1312">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="56e67-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="56e67-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="56e67-1313">Az.RedisCache</span></span>
* <span data-ttu-id="56e67-1314">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1315">Az.Resources</span></span>
* <span data-ttu-id="56e67-1316">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="56e67-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1317">Az.Sql</span></span>
* <span data-ttu-id="56e67-1318">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="56e67-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="56e67-1319">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1320">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="56e67-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="56e67-1321">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="56e67-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="56e67-1322">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="56e67-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="56e67-1323">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="56e67-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="56e67-1324">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="56e67-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1325">Az.Websites</span></span>
* <span data-ttu-id="56e67-1326">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="56e67-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="56e67-1327">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="56e67-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="56e67-1328">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="56e67-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="56e67-1329">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="56e67-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="56e67-1330">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="56e67-1331">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="56e67-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="56e67-1332">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="56e67-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="56e67-1333">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="56e67-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="56e67-1334">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="56e67-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="56e67-1335">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="56e67-1336">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="56e67-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="56e67-1337">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="56e67-1338">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="56e67-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="56e67-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1339">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1340">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="56e67-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="56e67-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="56e67-1342">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="56e67-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="56e67-1343">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="56e67-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1344">Az.Automation</span></span>
* <span data-ttu-id="56e67-1345">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="56e67-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="56e67-1346">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="56e67-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="56e67-1347">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1348">Az.Compute</span></span>
* <span data-ttu-id="56e67-1349">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="56e67-1350">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="56e67-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="56e67-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="56e67-1352">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="56e67-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-1353">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-1354">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="56e67-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="56e67-1355">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="56e67-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1356">Az.Resources</span></span>
* <span data-ttu-id="56e67-1357">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="56e67-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="56e67-1358">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="56e67-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="56e67-1359">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="56e67-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="56e67-1360">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="56e67-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="56e67-1361">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="56e67-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="56e67-1362">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="56e67-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1363">Az.Sql</span></span>
* <span data-ttu-id="56e67-1364">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="56e67-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1365">Az.Storage</span></span>
* <span data-ttu-id="56e67-1366">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="56e67-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="56e67-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="56e67-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="56e67-1368">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="56e67-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="56e67-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="56e67-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="56e67-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="56e67-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="56e67-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="56e67-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="56e67-1373">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="56e67-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="56e67-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="56e67-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="56e67-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="56e67-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="56e67-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="56e67-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="56e67-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="56e67-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="56e67-1378">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="56e67-1379">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="56e67-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="56e67-1380">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="56e67-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="56e67-1381">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="56e67-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="56e67-1382">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="56e67-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="56e67-1383">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="56e67-1384">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="56e67-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="56e67-1385">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="56e67-1386">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="56e67-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1387">Az.Automation</span></span>
* <span data-ttu-id="56e67-1388">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="56e67-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="56e67-1389">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="56e67-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="56e67-1390">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="56e67-1390">Pre-Post script</span></span>
    * <span data-ttu-id="56e67-1391">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="56e67-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1392">Az.Compute</span></span>
* <span data-ttu-id="56e67-1393">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="56e67-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="56e67-1394">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="56e67-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1395">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-1396">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1397">Az.Network</span></span>
* <span data-ttu-id="56e67-1398">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="56e67-1399">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="56e67-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1401">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="56e67-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="56e67-1402">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="56e67-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1403">Az.Resources</span></span>
* <span data-ttu-id="56e67-1404">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="56e67-1405">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="56e67-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1406">Az.Sql</span></span>
* <span data-ttu-id="56e67-1407">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="56e67-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1408">Az.Storage</span></span>
* <span data-ttu-id="56e67-1409">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="56e67-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="56e67-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="56e67-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="56e67-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="56e67-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="56e67-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="56e67-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="56e67-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1416">Az.Websites</span></span>
* <span data-ttu-id="56e67-1417">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="56e67-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="56e67-1418">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1419">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1420">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="56e67-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="56e67-1421">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1422">Az.Automation</span></span>
* <span data-ttu-id="56e67-1423">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="56e67-1424">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="56e67-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="56e67-1425">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="56e67-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-1426">Az.Cdn</span></span>
* <span data-ttu-id="56e67-1427">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="56e67-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1428">Az.Compute</span></span>
* <span data-ttu-id="56e67-1429">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="56e67-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-1430">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-1431">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="56e67-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="56e67-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="56e67-1432">Az.LogicApp</span></span>
* <span data-ttu-id="56e67-1433">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="56e67-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1434">Az.Network</span></span>
* <span data-ttu-id="56e67-1435">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1437">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="56e67-1438">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="56e67-1438">SDK Update</span></span>
* <span data-ttu-id="56e67-1439">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="56e67-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="56e67-1440">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="56e67-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1441">Az.Resources</span></span>
* <span data-ttu-id="56e67-1442">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="56e67-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="56e67-1443">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="56e67-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="56e67-1444">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="56e67-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="56e67-1445">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="56e67-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="56e67-1446">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="56e67-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="56e67-1447">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="56e67-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1448">Az.Sql</span></span>
* <span data-ttu-id="56e67-1449">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="56e67-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="56e67-1450">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="56e67-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1451">Az.Storage</span></span>
* <span data-ttu-id="56e67-1452">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="56e67-1453">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="56e67-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="56e67-1455">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="56e67-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1456">Az.Automation</span></span>
* <span data-ttu-id="56e67-1457">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="56e67-1458">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="56e67-1459">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-1461">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="56e67-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1462">Az.Compute</span></span>
* <span data-ttu-id="56e67-1463">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="56e67-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="56e67-1464">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="56e67-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="56e67-1465">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="56e67-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="56e67-1466">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="56e67-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1468">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="56e67-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="56e67-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1469">Az.EventHub</span></span>
* <span data-ttu-id="56e67-1470">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="56e67-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1471">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-1472">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="56e67-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="56e67-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="56e67-1473">Az.LogicApp</span></span>
* <span data-ttu-id="56e67-1474">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="56e67-1475">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="56e67-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="56e67-1476">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="56e67-1477">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="56e67-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="56e67-1478">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="56e67-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="56e67-1479">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="56e67-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="56e67-1480">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="56e67-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="56e67-1481">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="56e67-1482">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="56e67-1483">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="56e67-1484">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="56e67-1485">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="56e67-1486">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="56e67-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="56e67-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-1487">Az.Monitor</span></span>
* <span data-ttu-id="56e67-1488">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="56e67-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1489">Az.Network</span></span>
* <span data-ttu-id="56e67-1490">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="56e67-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="56e67-1492">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="56e67-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="56e67-1493">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="56e67-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="56e67-1494">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="56e67-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="56e67-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1495">Az.Resources</span></span>
* <span data-ttu-id="56e67-1496">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="56e67-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="56e67-1497">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="56e67-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="56e67-1498">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="56e67-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="56e67-1499">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="56e67-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1500">Az.Sql</span></span>
* <span data-ttu-id="56e67-1501">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="56e67-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="56e67-1502">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="56e67-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1503">Az.Websites</span></span>
* <span data-ttu-id="56e67-1504">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="56e67-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="56e67-1505">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1506">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1507">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="56e67-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="56e67-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="56e67-1509">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="56e67-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1510">Az.Compute</span></span>
* <span data-ttu-id="56e67-1511">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="56e67-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="56e67-1512">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="56e67-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="56e67-1513">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="56e67-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="56e67-1515">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="56e67-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1516">Az.Resources</span></span>
* <span data-ttu-id="56e67-1517">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="56e67-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="56e67-1518">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="56e67-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="56e67-1519">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="56e67-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="56e67-1520">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="56e67-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1521">Az.Sql</span></span>
* <span data-ttu-id="56e67-1522">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="56e67-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="56e67-1523">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="56e67-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="56e67-1524">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="56e67-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="56e67-1525">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1526">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1527">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="56e67-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="56e67-1529">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="56e67-1531">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="56e67-1532">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1533">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1534">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="56e67-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="56e67-1535">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="56e67-1536">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="56e67-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="56e67-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="56e67-1537">Az.Aks</span></span>
* <span data-ttu-id="56e67-1538">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="56e67-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1539">Az.Automation</span></span>
* <span data-ttu-id="56e67-1540">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="56e67-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="56e67-1541">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="56e67-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="56e67-1542">Az.Cdn</span></span>
* <span data-ttu-id="56e67-1543">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1544">Az.Compute</span></span>
* <span data-ttu-id="56e67-1545">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="56e67-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="56e67-1546">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="56e67-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="56e67-1547">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="56e67-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="56e67-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="56e67-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="56e67-1549">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="56e67-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="56e67-1550">Az.DataFactory</span></span>
* <span data-ttu-id="56e67-1551">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="56e67-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1553">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="56e67-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="56e67-1554">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="56e67-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="56e67-1555">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1556">Az.IotHub</span></span>
* <span data-ttu-id="56e67-1557">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56e67-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="56e67-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1558">Az.KeyVault</span></span>
* <span data-ttu-id="56e67-1559">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1560">Az.Network</span></span>
* <span data-ttu-id="56e67-1561">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1562">Az.Resources</span></span>
* <span data-ttu-id="56e67-1563">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="56e67-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="56e67-1564">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="56e67-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="56e67-1565">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="56e67-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="56e67-1566">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="56e67-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="56e67-1567">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="56e67-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="56e67-1568">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="56e67-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="56e67-1569">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="56e67-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-1571">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="56e67-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="56e67-1572">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="56e67-1572">Fix some error messages.</span></span>
* <span data-ttu-id="56e67-1573">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="56e67-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="56e67-1574">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="56e67-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="56e67-1575">Az.SignalR</span></span>
* <span data-ttu-id="56e67-1576">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1577">Az.Sql</span></span>
* <span data-ttu-id="56e67-1578">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="56e67-1579">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="56e67-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="56e67-1580">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="56e67-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="56e67-1581">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="56e67-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1582">Az.Storage</span></span>
* <span data-ttu-id="56e67-1583">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="56e67-1584">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="56e67-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="56e67-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="56e67-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="56e67-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="56e67-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="56e67-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="56e67-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="56e67-1588">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1589">Az.Websites</span></span>
* <span data-ttu-id="56e67-1590">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="56e67-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="56e67-1591">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="56e67-1592">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="56e67-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="56e67-1593">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="56e67-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="56e67-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1594">Az.Accounts</span></span>
* <span data-ttu-id="56e67-1595">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="56e67-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1596">Az.Compute</span></span>
* <span data-ttu-id="56e67-1597">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="56e67-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="56e67-1598">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="56e67-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="56e67-1599">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1601">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="56e67-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="56e67-1602">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="56e67-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="56e67-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="56e67-1603">Az.EventGrid</span></span>
* <span data-ttu-id="56e67-1604">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="56e67-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="56e67-1605">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="56e67-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="56e67-1606">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="56e67-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="56e67-1607">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="56e67-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="56e67-1608">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="56e67-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="56e67-1609">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="56e67-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="56e67-1610">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="56e67-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="56e67-1611">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="56e67-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="56e67-1612">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="56e67-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="56e67-1613">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="56e67-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="56e67-1614">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="56e67-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="56e67-1615">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="56e67-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="56e67-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1616">Az.IotHub</span></span>
* <span data-ttu-id="56e67-1617">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="56e67-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="56e67-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="56e67-1618">Az.LogicApp</span></span>
* <span data-ttu-id="56e67-1619">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="56e67-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1620">Az.Resources</span></span>
* <span data-ttu-id="56e67-1621">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="56e67-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="56e67-1622">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="56e67-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="56e67-1623">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56e67-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="56e67-1624">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="56e67-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="56e67-1625">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="56e67-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="56e67-1626">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="56e67-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="56e67-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="56e67-1627">Az.SignalR</span></span>
* <span data-ttu-id="56e67-1628">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1629">Az.Sql</span></span>
* <span data-ttu-id="56e67-1630">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="56e67-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="56e67-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1631">Az.Storage</span></span>
* <span data-ttu-id="56e67-1632">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="56e67-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="56e67-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="56e67-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="56e67-1634">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="56e67-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="56e67-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="56e67-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1636">Az.Websites</span></span>
* <span data-ttu-id="56e67-1637">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="56e67-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="56e67-1638">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="56e67-1639">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="56e67-1640">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-1640">General</span></span>

- <span data-ttu-id="56e67-1641">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="56e67-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="56e67-1642">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="56e67-1642">Online help for each module</span></span>
- <span data-ttu-id="56e67-1643">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="56e67-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="56e67-1644">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="56e67-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="56e67-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1645">Az.Accounts</span></span>
- <span data-ttu-id="56e67-1646">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="56e67-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="56e67-1647">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="56e67-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="56e67-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="56e67-1649">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="56e67-1649">Fixes for #7002</span></span>
- <span data-ttu-id="56e67-1650">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="56e67-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="56e67-1651">Az.Batch</span></span>
- <span data-ttu-id="56e67-1652">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="56e67-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="56e67-1653">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="56e67-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="56e67-1654">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="56e67-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="56e67-1655">Az.Billing</span></span>
- <span data-ttu-id="56e67-1656">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="56e67-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="56e67-1658">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="56e67-1659">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="56e67-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="56e67-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="56e67-1661">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="56e67-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="56e67-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="56e67-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="56e67-1663">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="56e67-1665">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="56e67-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="56e67-1666">Az.Monitor</span></span>
- <span data-ttu-id="56e67-1667">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="56e67-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="56e67-1668">Az.KeyVault</span></span>
- <span data-ttu-id="56e67-1669">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="56e67-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="56e67-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="56e67-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="56e67-1671">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="56e67-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="56e67-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="56e67-1672">Az.Media</span></span>
- <span data-ttu-id="56e67-1673">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="56e67-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="56e67-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1674">Az.Network</span></span>
<span data-ttu-id="56e67-1675">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="56e67-1676">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="56e67-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="56e67-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="56e67-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="56e67-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="56e67-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="56e67-1685">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="56e67-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="56e67-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="56e67-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="56e67-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="56e67-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="56e67-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="56e67-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="56e67-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="56e67-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="56e67-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="56e67-1692">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="56e67-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="56e67-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="56e67-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="56e67-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="56e67-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="56e67-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="56e67-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="56e67-1696">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="56e67-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="56e67-1697">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="56e67-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="56e67-1699">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="56e67-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="56e67-1700">Az.Profile</span></span>
- <span data-ttu-id="56e67-1701">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="56e67-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="56e67-1703">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="56e67-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1704">Az.Resources</span></span>
- <span data-ttu-id="56e67-1705">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="56e67-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="56e67-1707">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="56e67-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="56e67-1708">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="56e67-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="56e67-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="56e67-1710">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="56e67-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="56e67-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1711">Az.Sql</span></span>
- <span data-ttu-id="56e67-1712">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="56e67-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="56e67-1713">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="56e67-1714">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="56e67-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1715">Az.Storage</span></span>
- <span data-ttu-id="56e67-1716">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="56e67-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1717">Az.Websites</span></span>
- <span data-ttu-id="56e67-1718">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="56e67-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="56e67-1719">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="56e67-1720">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-1720">General</span></span>

* <span data-ttu-id="56e67-1721">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="56e67-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="56e67-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1722">Az.Compute</span></span>

* <span data-ttu-id="56e67-1723">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="56e67-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="56e67-1725">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="56e67-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="56e67-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="56e67-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="56e67-1727">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="56e67-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="56e67-1728">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="56e67-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="56e67-1729">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="56e67-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="56e67-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="56e67-1731">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="56e67-1732">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="56e67-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="56e67-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1733">Az.Resources</span></span>

* <span data-ttu-id="56e67-1734">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="56e67-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="56e67-1735">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="56e67-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="56e67-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1736">Az.Sql</span></span>

* <span data-ttu-id="56e67-1737">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="56e67-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="56e67-1738">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="56e67-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="56e67-1739">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="56e67-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="56e67-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1740">Az.Storage</span></span>

* <span data-ttu-id="56e67-1741">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="56e67-1742">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="56e67-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="56e67-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="56e67-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="56e67-1744">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="56e67-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="56e67-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="56e67-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="56e67-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="56e67-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="56e67-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1747">Az.Websites</span></span>

* <span data-ttu-id="56e67-1748">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="56e67-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="56e67-1749">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="56e67-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="56e67-1750">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="56e67-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="56e67-1751">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="56e67-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="56e67-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="56e67-1753">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="56e67-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="56e67-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="56e67-1754">Az.Automation</span></span>
* <span data-ttu-id="56e67-1755">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="56e67-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="56e67-1756">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="56e67-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="56e67-1757">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="56e67-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="56e67-1758">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="56e67-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="56e67-1759">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="56e67-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="56e67-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1760">Az.Compute</span></span>
* <span data-ttu-id="56e67-1761">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="56e67-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="56e67-1762">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="56e67-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="56e67-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="56e67-1764">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="56e67-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="56e67-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="56e67-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="56e67-1766">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="56e67-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="56e67-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1767">Az.Network</span></span>
* <span data-ttu-id="56e67-1768">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="56e67-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="56e67-1769">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="56e67-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="56e67-1770">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="56e67-1771">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56e67-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="56e67-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="56e67-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="56e67-1773">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="56e67-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="56e67-1774">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="56e67-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="56e67-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="56e67-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="56e67-1776">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="56e67-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="56e67-1777">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="56e67-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="56e67-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="56e67-1778">Az.Relay</span></span>
* <span data-ttu-id="56e67-1779">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="56e67-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="56e67-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1780">Az.Resources</span></span>
* <span data-ttu-id="56e67-1781">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="56e67-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="56e67-1782">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="56e67-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="56e67-1783">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="56e67-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="56e67-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-1785">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="56e67-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="56e67-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1786">Az.Sql</span></span>
* <span data-ttu-id="56e67-1787">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="56e67-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="56e67-1788">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="56e67-1789">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="56e67-1790">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="56e67-1791">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="56e67-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="56e67-1792">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="56e67-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="56e67-1793">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="56e67-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="56e67-1794">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="56e67-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="56e67-1795">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="56e67-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="56e67-1796">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="56e67-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="56e67-1797">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="56e67-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="56e67-1798">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="56e67-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="56e67-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="56e67-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="56e67-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="56e67-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="56e67-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="56e67-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="56e67-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="56e67-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="56e67-1803">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="56e67-1804">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="56e67-1805">Generale</span><span class="sxs-lookup"><span data-stu-id="56e67-1805">General</span></span>
* <span data-ttu-id="56e67-1806">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="56e67-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="56e67-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="56e67-1807">Az.Profile</span></span>
* <span data-ttu-id="56e67-1808">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="56e67-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="56e67-1809">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="56e67-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="56e67-1810">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="56e67-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="56e67-1811">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="56e67-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="56e67-1812">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="56e67-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="56e67-1813">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="56e67-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="56e67-1814">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="56e67-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-1816">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="56e67-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1817">Az.Compute</span></span>
* <span data-ttu-id="56e67-1818">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="56e67-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="56e67-1819">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="56e67-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="56e67-1820">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="56e67-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1822">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="56e67-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="56e67-1823">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="56e67-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="56e67-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="56e67-1824">Az.Insights</span></span>
* <span data-ttu-id="56e67-1825">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="56e67-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="56e67-1826">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="56e67-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="56e67-1827">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="56e67-1828">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="56e67-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1829">Az.Network</span></span>
* <span data-ttu-id="56e67-1830">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="56e67-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="56e67-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="56e67-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="56e67-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="56e67-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="56e67-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="56e67-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="56e67-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="56e67-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="56e67-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="56e67-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="56e67-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="56e67-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="56e67-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="56e67-1838">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="56e67-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1839">Az.Resources</span></span>
* <span data-ttu-id="56e67-1840">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="56e67-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="56e67-1841">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="56e67-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="56e67-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="56e67-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="56e67-1843">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="56e67-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="56e67-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="56e67-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="56e67-1845">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="56e67-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="56e67-1846">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="56e67-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="56e67-1847">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="56e67-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="56e67-1848">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="56e67-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="56e67-1849">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="56e67-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="56e67-1850">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="56e67-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="56e67-1851">Az.Profile</span></span>
* <span data-ttu-id="56e67-1852">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="56e67-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="56e67-1853">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="56e67-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1854">Az.Compute</span></span>
* <span data-ttu-id="56e67-1855">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="56e67-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="56e67-1856">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e67-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="56e67-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="56e67-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="56e67-1858">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="56e67-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="56e67-1859">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56e67-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="56e67-1860">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="56e67-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="56e67-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="56e67-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="56e67-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56e67-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1863">Az.Network</span></span>
* <span data-ttu-id="56e67-1864">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="56e67-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="56e67-1865">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56e67-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1866">Az.Resources</span></span>
* <span data-ttu-id="56e67-1867">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="56e67-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="56e67-1868">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="56e67-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="56e67-1869">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="56e67-1870">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="56e67-1870">Azure.Storage</span></span>
* <span data-ttu-id="56e67-1871">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="56e67-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="56e67-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="56e67-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="56e67-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="56e67-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="56e67-1874">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="56e67-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="56e67-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="56e67-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="56e67-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="56e67-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="56e67-1877">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="56e67-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="56e67-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="56e67-1878">Az.Compute</span></span>
* <span data-ttu-id="56e67-1879">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="56e67-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="56e67-1880">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="56e67-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="56e67-1881">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="56e67-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="56e67-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="56e67-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="56e67-1883">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="56e67-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="56e67-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="56e67-1884">Az.Network</span></span>
* <span data-ttu-id="56e67-1885">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="56e67-1886">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="56e67-1886">new cmdlets added</span></span>
    - <span data-ttu-id="56e67-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="56e67-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="56e67-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="56e67-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="56e67-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="56e67-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="56e67-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="56e67-1893">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="56e67-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="56e67-1894">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="56e67-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="56e67-1895">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="56e67-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="56e67-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="56e67-1896">Az.RedisCache</span></span>
* <span data-ttu-id="56e67-1897">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="56e67-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="56e67-1898">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="56e67-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="56e67-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="56e67-1899">Az.Resources</span></span>
* <span data-ttu-id="56e67-1900">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="56e67-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="56e67-1901">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="56e67-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="56e67-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="56e67-1902">Az.Sql</span></span>
* <span data-ttu-id="56e67-1903">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="56e67-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="56e67-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="56e67-1904">Az.Websites</span></span>
* <span data-ttu-id="56e67-1905">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="56e67-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="56e67-1906">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="56e67-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="56e67-1907">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="56e67-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="56e67-1908">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="56e67-1908">Initial Release</span></span>
