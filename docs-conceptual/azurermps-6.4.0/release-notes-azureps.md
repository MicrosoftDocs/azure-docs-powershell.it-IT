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
ms.openlocfilehash: 255e26aea5ea3cea866faa0d095cdf643c8ef0a8
ms.sourcegitcommit: de0e60800df1add9f3400166faacca202ef567d9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/03/2018
ms.locfileid: "37406484"
---
# <a name="release-notes"></a><span data-ttu-id="52398-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="52398-103">Release notes</span></span>

<span data-ttu-id="52398-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="52398-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="640---july-2018"></a><span data-ttu-id="52398-105">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="52398-105">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="52398-106">Generale</span><span class="sxs-lookup"><span data-stu-id="52398-106">General</span></span>
* <span data-ttu-id="52398-107">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="52398-107">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="52398-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52398-108">AzureRM.Profile</span></span>
* <span data-ttu-id="52398-109">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="52398-109">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52398-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52398-110">AzureRM.Compute</span></span>
* <span data-ttu-id="52398-111">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="52398-111">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="52398-112">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="52398-112">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="52398-113">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="52398-113">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="52398-114">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="52398-114">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="52398-115">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-115">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="52398-116">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="52398-116">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="52398-117">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-117">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="52398-118">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="52398-118">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="52398-119">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="52398-119">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="52398-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52398-120">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="52398-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52398-121">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="52398-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52398-122">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52398-123">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52398-123">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52398-124">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="52398-124">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="52398-125">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="52398-125">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="52398-126">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="52398-126">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="52398-127">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="52398-127">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="52398-128">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="52398-128">AzureRM.EventHub</span></span>
* <span data-ttu-id="52398-129">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="52398-129">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="52398-130">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="52398-130">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="52398-131">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="52398-131">Provided Default Parameter set.</span></span>
* <span data-ttu-id="52398-132">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="52398-132">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52398-133">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52398-133">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52398-134">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="52398-134">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="52398-135">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52398-135">AzureRM.Network</span></span>
* <span data-ttu-id="52398-136">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="52398-136">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="52398-137">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="52398-137">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="52398-138">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="52398-138">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="52398-139">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="52398-139">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="52398-140">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52398-140">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52398-141">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52398-141">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52398-142">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="52398-142">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="52398-143">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="52398-143">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="52398-144">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="52398-144">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="52398-145">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="52398-145">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="52398-146">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="52398-146">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="52398-147">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="52398-147">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="52398-148">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="52398-148">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="52398-149">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="52398-149">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52398-150">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52398-150">AzureRM.Resources</span></span>
* <span data-ttu-id="52398-151">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="52398-151">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="52398-152">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="52398-152">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="52398-153">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="52398-153">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="52398-154">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="52398-154">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="52398-155">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52398-155">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="52398-156">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="52398-156">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="52398-157">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="52398-157">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="52398-158">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="52398-158">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="52398-159">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="52398-159">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="52398-160">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="52398-160">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="52398-161">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="52398-161">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="52398-162">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="52398-162">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="52398-163">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="52398-163">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="52398-164">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="52398-164">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="52398-165">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="52398-165">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52398-166">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52398-166">AzureRM.Sql</span></span>
* <span data-ttu-id="52398-167">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="52398-167">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="52398-168">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="52398-168">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="52398-169">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="52398-169">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52398-170">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52398-170">AzureRM.Profile</span></span>
* <span data-ttu-id="52398-171">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="52398-171">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="52398-172">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="52398-172">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="52398-173">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="52398-173">Azure.Storage</span></span>
* <span data-ttu-id="52398-174">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="52398-174">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52398-175">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52398-175">AzureRM.Compute</span></span>
* <span data-ttu-id="52398-176">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="52398-176">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="52398-177">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="52398-177">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="52398-178">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="52398-178">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="52398-179">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="52398-179">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="52398-180">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="52398-180">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="52398-181">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="52398-181">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="52398-182">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52398-182">Start-AzureRmVM</span></span>
    - <span data-ttu-id="52398-183">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52398-183">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="52398-184">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52398-184">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="52398-185">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="52398-185">Set-AzureRmVM</span></span>
    - <span data-ttu-id="52398-186">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="52398-186">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="52398-187">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-187">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="52398-188">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="52398-188">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="52398-189">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="52398-189">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="52398-190">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-190">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="52398-191">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-191">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="52398-192">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-192">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="52398-193">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="52398-193">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="52398-194">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="52398-194">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="52398-195">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="52398-195">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="52398-196">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="52398-196">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="52398-197">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="52398-197">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="52398-198">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="52398-198">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="52398-199">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="52398-199">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="52398-200">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="52398-200">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="52398-201">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="52398-201">AzureRM.EventGrid</span></span>
* <span data-ttu-id="52398-202">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="52398-202">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="52398-203">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52398-203">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52398-204">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="52398-204">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="52398-205">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="52398-205">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="52398-206">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="52398-206">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="52398-207">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="52398-207">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="52398-208">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="52398-208">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="52398-209">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="52398-209">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="52398-210">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="52398-210">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="52398-211">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="52398-211">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52398-212">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52398-212">AzureRM.Sql</span></span>
* <span data-ttu-id="52398-213">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="52398-213">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="52398-214">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="52398-214">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="52398-215">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="52398-215">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52398-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52398-216">AzureRM.Websites</span></span>
* <span data-ttu-id="52398-217">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="52398-217">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="52398-218">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="52398-218">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="52398-219">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="52398-219">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="52398-220">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="52398-220">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="52398-221">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="52398-221">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="52398-222">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="52398-222">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52398-223">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52398-223">AzureRM.Profile</span></span>
* <span data-ttu-id="52398-224">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="52398-224">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="52398-225">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="52398-225">AzureRM.Compute</span></span>
* <span data-ttu-id="52398-226">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="52398-226">VMSS VM Update feature</span></span>
    - <span data-ttu-id="52398-227">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="52398-227">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="52398-228">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="52398-228">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="52398-229">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="52398-229">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="52398-230">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="52398-230">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="52398-231">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="52398-231">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="52398-232">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="52398-232">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="52398-233">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="52398-233">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="52398-234">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="52398-234">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="52398-235">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="52398-235">AzureRM.KeyVault</span></span>
* <span data-ttu-id="52398-236">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="52398-236">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="52398-237">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52398-237">AzureRM.Network</span></span>
* <span data-ttu-id="52398-238">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="52398-238">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="52398-239">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="52398-239">AzureRM.Resources</span></span>
* <span data-ttu-id="52398-240">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="52398-240">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="52398-241">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="52398-241">AzureRM.Scheduler</span></span>
* <span data-ttu-id="52398-242">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="52398-242">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="52398-243">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52398-243">AzureRM.Sql</span></span>
* <span data-ttu-id="52398-244">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="52398-244">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="52398-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52398-245">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="52398-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="52398-246">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="52398-247">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="52398-247">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="52398-248">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="52398-248">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="52398-249">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52398-249">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="52398-250">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="52398-250">AzureRM.Websites</span></span>
* <span data-ttu-id="52398-251">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="52398-251">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="52398-252">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="52398-252">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="52398-253">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="52398-253">AzureRM.Profile</span></span>
* <span data-ttu-id="52398-254">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="52398-254">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="52398-255">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="52398-255">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="52398-256">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="52398-256">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="52398-257">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="52398-257">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="52398-258">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="52398-258">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="52398-259">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="52398-259">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="52398-260">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="52398-260">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="52398-261">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="52398-261">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="52398-262">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="52398-262">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="52398-263">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="52398-263">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="52398-264">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="52398-264">Added support for MSI identity</span></span>
* <span data-ttu-id="52398-265">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="52398-265">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="52398-266">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="52398-266">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="52398-267">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="52398-267">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="52398-268">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="52398-268">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="52398-269">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="52398-269">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="52398-270">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="52398-270">AzureRM.Batch</span></span>
* <span data-ttu-id="52398-271">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="52398-271">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="52398-272">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="52398-272">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="52398-273">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="52398-273">AzureRM.Consumption</span></span>
* <span data-ttu-id="52398-274">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="52398-274">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="52398-275">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="52398-275">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="52398-276">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="52398-276">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="52398-277">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52398-277">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="52398-278">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="52398-278">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="52398-279">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="52398-279">AzureRM.Network</span></span>
* <span data-ttu-id="52398-280">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="52398-280">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="52398-281">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="52398-281">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="52398-282">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="52398-282">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="52398-283">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="52398-283">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="52398-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52398-284">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="52398-285">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="52398-285">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="52398-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52398-286">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="52398-287">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="52398-287">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="52398-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="52398-288">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="52398-289">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="52398-289">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="52398-290">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="52398-290">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="52398-291">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="52398-291">AzureRM.Sql</span></span>
* <span data-ttu-id="52398-292">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="52398-292">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="52398-293">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="52398-293">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="52398-294">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="52398-294">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="52398-295">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="52398-295">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="52398-296">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="52398-296">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="52398-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52398-297">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="52398-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="52398-298">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="52398-299">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="52398-299">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="52398-300">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="52398-300">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="52398-301">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="52398-301">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="52398-302">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="52398-302">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="52398-303">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="52398-303">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>