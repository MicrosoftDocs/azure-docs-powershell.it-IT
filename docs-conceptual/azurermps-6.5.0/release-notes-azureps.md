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
ms.openlocfilehash: e9fa2d75c1c4e6ffaa2f7dd8e400f5b13dd4527d
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110484"
---
# <a name="release-notes"></a><span data-ttu-id="5a3b6-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="5a3b6-103">Release notes</span></span>

<span data-ttu-id="5a3b6-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="650---july-2018"></a><span data-ttu-id="5a3b6-105">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-105">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5a3b6-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5a3b6-106">AzureRM.Profile</span></span>
* <span data-ttu-id="5a3b6-107">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-107">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="5a3b6-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5a3b6-108">Azure.Storage</span></span>
* <span data-ttu-id="5a3b6-109">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="5a3b6-109">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="5a3b6-110">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="5a3b6-110">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="5a3b6-111">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="5a3b6-111">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="5a3b6-112">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a3b6-112">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="5a3b6-113">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-113">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="5a3b6-114">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="5a3b6-114">AzureRM.Automation</span></span>
* <span data-ttu-id="5a3b6-115">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-115">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5a3b6-116">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5a3b6-116">AzureRM.Compute</span></span>
* <span data-ttu-id="5a3b6-117">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5a3b6-117">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="5a3b6-118">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-118">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="5a3b6-119">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-119">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="5a3b6-120">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-120">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="5a3b6-121">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-121">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="5a3b6-122">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a3b6-122">AzureRM.EventHub</span></span>
* <span data-ttu-id="5a3b6-123">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="5a3b6-123">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5a3b6-124">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a3b6-124">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5a3b6-125">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5a3b6-125">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="5a3b6-126">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="5a3b6-126">AzureRM.LogicApp</span></span>
* <span data-ttu-id="5a3b6-127">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="5a3b6-127">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="5a3b6-128">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5a3b6-128">AzureRM.Network</span></span>
* <span data-ttu-id="5a3b6-129">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5a3b6-129">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="5a3b6-130">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5a3b6-130">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="5a3b6-131">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="5a3b6-131">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="5a3b6-132">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="5a3b6-132">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="5a3b6-133">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="5a3b6-133">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="5a3b6-134">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="5a3b6-134">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="5a3b6-135">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="5a3b6-135">AzureRM.Relay</span></span>
* <span data-ttu-id="5a3b6-136">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="5a3b6-136">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5a3b6-137">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5a3b6-137">AzureRM.Resources</span></span>
* <span data-ttu-id="5a3b6-138">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-138">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="5a3b6-139">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-139">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="5a3b6-140">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="5a3b6-140">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="5a3b6-141">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="5a3b6-141">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="5a3b6-142">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="5a3b6-142">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="5a3b6-143">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a3b6-143">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="5a3b6-144">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="5a3b6-144">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="5a3b6-145">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-145">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="5a3b6-146">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-146">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="5a3b6-147">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-147">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="5a3b6-148">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-148">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="5a3b6-149">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-149">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="5a3b6-150">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-150">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="5a3b6-151">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="5a3b6-151">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="5a3b6-152">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a3b6-152">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5a3b6-153">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-153">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5a3b6-154">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5a3b6-154">AzureRM.Sql</span></span>
* <span data-ttu-id="5a3b6-155">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="5a3b6-155">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="5a3b6-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="5a3b6-156">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="5a3b6-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="5a3b6-157">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5a3b6-158">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5a3b6-158">AzureRM.Websites</span></span>
* <span data-ttu-id="5a3b6-159">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-159">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="5a3b6-160">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="5a3b6-160">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="5a3b6-161">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="5a3b6-161">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="5a3b6-162">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-162">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="5a3b6-163">Generale</span><span class="sxs-lookup"><span data-stu-id="5a3b6-163">General</span></span>
* <span data-ttu-id="5a3b6-164">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="5a3b6-164">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="5a3b6-165">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5a3b6-165">AzureRM.Profile</span></span>
* <span data-ttu-id="5a3b6-166">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="5a3b6-166">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5a3b6-167">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5a3b6-167">AzureRM.Compute</span></span>
* <span data-ttu-id="5a3b6-168">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="5a3b6-168">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="5a3b6-169">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-169">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="5a3b6-170">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="5a3b6-170">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="5a3b6-171">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="5a3b6-171">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="5a3b6-172">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-172">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="5a3b6-173">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-173">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="5a3b6-174">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-174">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="5a3b6-175">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="5a3b6-175">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="5a3b6-176">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-176">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="5a3b6-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a3b6-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5a3b6-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a3b6-178">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="5a3b6-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a3b6-179">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5a3b6-180">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a3b6-180">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5a3b6-181">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="5a3b6-181">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="5a3b6-182">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="5a3b6-182">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5a3b6-183">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="5a3b6-183">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="5a3b6-184">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="5a3b6-184">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="5a3b6-185">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="5a3b6-185">AzureRM.EventHub</span></span>
* <span data-ttu-id="5a3b6-186">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="5a3b6-186">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="5a3b6-187">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-187">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="5a3b6-188">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-188">Provided Default Parameter set.</span></span>
* <span data-ttu-id="5a3b6-189">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-189">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5a3b6-190">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a3b6-190">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5a3b6-191">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="5a3b6-191">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="5a3b6-192">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5a3b6-192">AzureRM.Network</span></span>
* <span data-ttu-id="5a3b6-193">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="5a3b6-193">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="5a3b6-194">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-194">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="5a3b6-195">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5a3b6-195">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5a3b6-196">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5a3b6-196">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="5a3b6-197">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5a3b6-197">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5a3b6-198">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5a3b6-198">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5a3b6-199">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="5a3b6-199">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="5a3b6-200">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="5a3b6-200">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="5a3b6-201">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="5a3b6-201">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="5a3b6-202">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="5a3b6-202">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5a3b6-203">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5a3b6-203">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5a3b6-204">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-204">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="5a3b6-205">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-205">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="5a3b6-206">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-206">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5a3b6-207">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5a3b6-207">AzureRM.Resources</span></span>
* <span data-ttu-id="5a3b6-208">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-208">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="5a3b6-209">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a3b6-209">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="5a3b6-210">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a3b6-210">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="5a3b6-211">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="5a3b6-211">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="5a3b6-212">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5a3b6-212">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="5a3b6-213">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="5a3b6-213">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5a3b6-214">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="5a3b6-214">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5a3b6-215">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="5a3b6-215">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="5a3b6-216">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="5a3b6-216">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="5a3b6-217">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="5a3b6-217">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="5a3b6-218">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-218">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="5a3b6-219">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="5a3b6-219">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="5a3b6-220">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="5a3b6-220">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="5a3b6-221">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="5a3b6-221">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="5a3b6-222">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-222">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5a3b6-223">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5a3b6-223">AzureRM.Sql</span></span>
* <span data-ttu-id="5a3b6-224">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="5a3b6-224">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="5a3b6-225">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="5a3b6-225">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="5a3b6-226">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-226">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5a3b6-227">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5a3b6-227">AzureRM.Profile</span></span>
* <span data-ttu-id="5a3b6-228">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="5a3b6-228">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="5a3b6-229">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="5a3b6-229">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="5a3b6-230">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="5a3b6-230">Azure.Storage</span></span>
* <span data-ttu-id="5a3b6-231">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-231">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5a3b6-232">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5a3b6-232">AzureRM.Compute</span></span>
* <span data-ttu-id="5a3b6-233">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="5a3b6-233">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="5a3b6-234">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="5a3b6-234">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="5a3b6-235">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5a3b6-235">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5a3b6-236">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5a3b6-236">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5a3b6-237">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="5a3b6-237">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="5a3b6-238">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="5a3b6-238">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="5a3b6-239">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-239">Start-AzureRmVM</span></span>
    - <span data-ttu-id="5a3b6-240">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-240">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="5a3b6-241">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-241">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="5a3b6-242">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-242">Set-AzureRmVM</span></span>
    - <span data-ttu-id="5a3b6-243">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="5a3b6-243">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="5a3b6-244">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-244">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="5a3b6-245">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a3b6-245">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="5a3b6-246">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="5a3b6-246">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="5a3b6-247">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-247">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="5a3b6-248">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-248">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="5a3b6-249">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-249">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="5a3b6-250">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5a3b6-250">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="5a3b6-251">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="5a3b6-251">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="5a3b6-252">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="5a3b6-252">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="5a3b6-253">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="5a3b6-253">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="5a3b6-254">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="5a3b6-254">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="5a3b6-255">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="5a3b6-255">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="5a3b6-256">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="5a3b6-256">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="5a3b6-257">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="5a3b6-257">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="5a3b6-258">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="5a3b6-258">AzureRM.EventGrid</span></span>
* <span data-ttu-id="5a3b6-259">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-259">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="5a3b6-260">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a3b6-260">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5a3b6-261">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="5a3b6-261">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="5a3b6-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="5a3b6-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="5a3b6-263">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="5a3b6-263">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="5a3b6-264">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="5a3b6-264">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="5a3b6-265">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="5a3b6-265">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="5a3b6-266">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="5a3b6-266">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="5a3b6-267">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-267">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="5a3b6-268">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-268">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5a3b6-269">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5a3b6-269">AzureRM.Sql</span></span>
* <span data-ttu-id="5a3b6-270">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="5a3b6-270">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5a3b6-271">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5a3b6-271">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5a3b6-272">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5a3b6-272">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5a3b6-273">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5a3b6-273">AzureRM.Websites</span></span>
* <span data-ttu-id="5a3b6-274">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5a3b6-274">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="5a3b6-275">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="5a3b6-275">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="5a3b6-276">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-276">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="5a3b6-277">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="5a3b6-277">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="5a3b6-278">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="5a3b6-278">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="5a3b6-279">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-279">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5a3b6-280">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5a3b6-280">AzureRM.Profile</span></span>
* <span data-ttu-id="5a3b6-281">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="5a3b6-281">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="5a3b6-282">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="5a3b6-282">AzureRM.Compute</span></span>
* <span data-ttu-id="5a3b6-283">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="5a3b6-283">VMSS VM Update feature</span></span>
    - <span data-ttu-id="5a3b6-284">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="5a3b6-284">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="5a3b6-285">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="5a3b6-285">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="5a3b6-286">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="5a3b6-286">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="5a3b6-287">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-287">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="5a3b6-288">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="5a3b6-288">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="5a3b6-289">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="5a3b6-289">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="5a3b6-290">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="5a3b6-290">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="5a3b6-291">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="5a3b6-291">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="5a3b6-292">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="5a3b6-292">AzureRM.KeyVault</span></span>
* <span data-ttu-id="5a3b6-293">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="5a3b6-293">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="5a3b6-294">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5a3b6-294">AzureRM.Network</span></span>
* <span data-ttu-id="5a3b6-295">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="5a3b6-295">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="5a3b6-296">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="5a3b6-296">AzureRM.Resources</span></span>
* <span data-ttu-id="5a3b6-297">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="5a3b6-297">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="5a3b6-298">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="5a3b6-298">AzureRM.Scheduler</span></span>
* <span data-ttu-id="5a3b6-299">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="5a3b6-299">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="5a3b6-300">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5a3b6-300">AzureRM.Sql</span></span>
* <span data-ttu-id="5a3b6-301">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="5a3b6-301">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="5a3b6-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5a3b6-302">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5a3b6-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5a3b6-303">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5a3b6-304">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5a3b6-304">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5a3b6-305">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a3b6-305">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5a3b6-306">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5a3b6-306">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="5a3b6-307">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="5a3b6-307">AzureRM.Websites</span></span>
* <span data-ttu-id="5a3b6-308">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="5a3b6-308">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="5a3b6-309">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="5a3b6-309">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="5a3b6-310">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="5a3b6-310">AzureRM.Profile</span></span>
* <span data-ttu-id="5a3b6-311">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="5a3b6-311">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="5a3b6-312">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="5a3b6-312">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="5a3b6-313">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-313">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="5a3b6-314">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5a3b6-314">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="5a3b6-315">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="5a3b6-315">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="5a3b6-316">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="5a3b6-316">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="5a3b6-317">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="5a3b6-317">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="5a3b6-318">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="5a3b6-318">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="5a3b6-319">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="5a3b6-319">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="5a3b6-320">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="5a3b6-320">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="5a3b6-321">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="5a3b6-321">Added support for MSI identity</span></span>
* <span data-ttu-id="5a3b6-322">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="5a3b6-322">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="5a3b6-323">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="5a3b6-323">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="5a3b6-324">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-324">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="5a3b6-325">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="5a3b6-325">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="5a3b6-326">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5a3b6-326">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="5a3b6-327">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="5a3b6-327">AzureRM.Batch</span></span>
* <span data-ttu-id="5a3b6-328">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="5a3b6-328">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="5a3b6-329">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="5a3b6-329">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="5a3b6-330">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="5a3b6-330">AzureRM.Consumption</span></span>
* <span data-ttu-id="5a3b6-331">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="5a3b6-331">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="5a3b6-332">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5a3b6-332">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="5a3b6-333">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="5a3b6-333">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="5a3b6-334">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a3b6-334">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="5a3b6-335">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="5a3b6-335">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="5a3b6-336">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="5a3b6-336">AzureRM.Network</span></span>
* <span data-ttu-id="5a3b6-337">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="5a3b6-337">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="5a3b6-338">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="5a3b6-338">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="5a3b6-339">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a3b6-339">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="5a3b6-340">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-340">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="5a3b6-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5a3b6-341">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5a3b6-342">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-342">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="5a3b6-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5a3b6-343">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="5a3b6-344">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="5a3b6-344">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="5a3b6-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="5a3b6-345">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="5a3b6-346">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="5a3b6-346">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="5a3b6-347">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="5a3b6-347">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="5a3b6-348">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="5a3b6-348">AzureRM.Sql</span></span>
* <span data-ttu-id="5a3b6-349">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="5a3b6-349">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="5a3b6-350">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-350">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="5a3b6-351">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-351">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="5a3b6-352">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-352">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="5a3b6-353">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="5a3b6-353">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="5a3b6-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5a3b6-354">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="5a3b6-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5a3b6-355">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="5a3b6-356">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="5a3b6-356">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="5a3b6-357">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5a3b6-357">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="5a3b6-358">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5a3b6-358">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="5a3b6-359">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="5a3b6-359">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="5a3b6-360">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="5a3b6-360">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>