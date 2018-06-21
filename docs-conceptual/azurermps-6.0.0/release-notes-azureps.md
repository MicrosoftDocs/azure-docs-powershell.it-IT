---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
ms.locfileid: "33912004"
---
# <a name="release-notes"></a><span data-ttu-id="86675-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="86675-103">Release notes</span></span>

<span data-ttu-id="86675-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="86675-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---

## <a name="600---may-2018"></a><span data-ttu-id="86675-105">6.0.0 - maggio 2018</span><span class="sxs-lookup"><span data-stu-id="86675-105">6.0.0 - May 2018</span></span>

### <a name="general"></a><span data-ttu-id="86675-106">Generale</span><span class="sxs-lookup"><span data-stu-id="86675-106">General</span></span>
* <span data-ttu-id="86675-107">Impostazione della dipendenza minima dei moduli su PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="86675-107">Set minimum dependency of modules to PowerShell 5.0</span></span>

### <a name="azurestorage"></a><span data-ttu-id="86675-108">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="86675-108">Azure.Storage</span></span>
* <span data-ttu-id="86675-109">Supporto come nodo contenitori BLOB di Archiviazione</span><span class="sxs-lookup"><span data-stu-id="86675-109">Support  as Storage blob container name</span></span>
    - <span data-ttu-id="86675-110">New-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="86675-110">New-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="86675-111">Remove-AzureStorageBlobContainer</span><span class="sxs-lookup"><span data-stu-id="86675-111">Remove-AzureStorageBlobContainer</span></span>
    - <span data-ttu-id="86675-112">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86675-112">Set-AzureStorageBlobContent</span></span>
    - <span data-ttu-id="86675-113">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="86675-113">Get-AzureStorageBlobContent</span></span>
* <span data-ttu-id="86675-114">Correzione del problema per cui l'output degli errori di alcuni cmdlet di Archiviazione non contiene informazioni dettagliate sugli errori</span><span class="sxs-lookup"><span data-stu-id="86675-114">Fix the issue that some Storage cmdlets failure output not contain detail failure information</span></span>

### <a name="azurermapimanagement"></a><span data-ttu-id="86675-115">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="86675-115">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="86675-116">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-116">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-117">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-117">Please refer to the migration guide for more information</span></span>

### <a name="azurermautomation"></a><span data-ttu-id="86675-118">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="86675-118">AzureRM.Automation</span></span>
* <span data-ttu-id="86675-119">Rimozione dell'alias 'Tags' deprecato dai cmdlet</span><span class="sxs-lookup"><span data-stu-id="86675-119">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="86675-120">'Set-AzureRmAutomationRunbook'</span><span class="sxs-lookup"><span data-stu-id="86675-120">'Set-AzureRmAutomationRunbook'</span></span>

### <a name="azurermbatch"></a><span data-ttu-id="86675-121">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="86675-121">AzureRM.Batch</span></span>
* <span data-ttu-id="86675-122">Aggiornamento delle documentazione di New-AzureBatchPool per rimuovere un esempio deprecato</span><span class="sxs-lookup"><span data-stu-id="86675-122">Updated New-AzureBatchPool documentation to remove deprecated example</span></span>

### <a name="azurermcdn"></a><span data-ttu-id="86675-123">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="86675-123">AzureRM.Cdn</span></span>
* <span data-ttu-id="86675-124">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-124">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-125">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-125">Please refer to the migration guide for more information</span></span>

### <a name="azurermcompute"></a><span data-ttu-id="86675-126">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="86675-126">AzureRM.Compute</span></span>
* <span data-ttu-id="86675-127">'New-AzureRmVm' e 'New-AzureRmVmss' supportano l'output dettagliato dei parametri</span><span class="sxs-lookup"><span data-stu-id="86675-127">'New-AzureRmVm' and 'New-AzureRmVmss' support verbose output of parameters</span></span>
* <span data-ttu-id="86675-128">'New-AzureRmVm' e 'New-AzureRmVmss' (set di parametri semplice) supportano l'assegnazione di identità definite dall'utente e/o dal sistema alle macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="86675-128">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support assigning user defined and(or) system defined identities to the VM(s).</span></span>
* <span data-ttu-id="86675-129">Funzionalità Redeploy e PerformMaintenance di VMSS</span><span class="sxs-lookup"><span data-stu-id="86675-129">VMSS Redeploy and PerformMaintenance feature</span></span>
    -  <span data-ttu-id="86675-130">Aggiunta dei nuovi parametri di opzione -Redeploy e -PerformMaintenance a 'Set-AzureRmVmss' e 'Set-AzureRmVmssVM'</span><span class="sxs-lookup"><span data-stu-id="86675-130">Add new switch parameter -Redeploy and -PerformMaintenance to 'Set-AzureRmVmss' and 'Set-AzureRmVmssVM'</span></span>
* <span data-ttu-id="86675-131">Aggiunta del parametro di opzione DisableVMAgent al cmdlet 'Set-AzureRmVMOperatingSystem'</span><span class="sxs-lookup"><span data-stu-id="86675-131">Add DisableVMAgent switch parameter to 'Set-AzureRmVMOperatingSystem' cmdlet</span></span>
* <span data-ttu-id="86675-132">'New-AzureRmVm' e 'New-AzureRmVmss' (set di parametri semplice) supportano un'immagine 'Win10'.</span><span class="sxs-lookup"><span data-stu-id="86675-132">'New-AzureRmVm' and 'New-AzureRmVmss' (simple parameter set) support a 'Win10' image.</span></span>
* <span data-ttu-id="86675-133">Aggiunta del cmdlet 'Repair-AzureRmVmssServiceFabricUpdateDomain'.</span><span class="sxs-lookup"><span data-stu-id="86675-133">'Repair-AzureRmVmssServiceFabricUpdateDomain' cmdlet is added.</span></span>
* <span data-ttu-id="86675-134">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-134">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-135">Per altri dettagli, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-135">Please refer to the migration guide for more details</span></span>
* <span data-ttu-id="86675-136">Con 'Set-AzureRmVmDiskEncryptionExtension' i parametri di AAD diventano facoltativi</span><span class="sxs-lookup"><span data-stu-id="86675-136">'Set-AzureRmVmDiskEncryptionExtension' makes AAD parameters optional</span></span>

### <a name="azurermdatafactories"></a><span data-ttu-id="86675-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="86675-137">AzureRM.DataFactories</span></span>
* <span data-ttu-id="86675-138">Rimozione dell'alias 'Tags' deprecato dai cmdlet</span><span class="sxs-lookup"><span data-stu-id="86675-138">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="86675-139">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="86675-139">New-AzureRmDataFactory</span></span>

### <a name="azurermdatafactoryv2"></a><span data-ttu-id="86675-140">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="86675-140">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="86675-141">Aggiornamento di ADF .Net SDK alla versione 0.7.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="86675-141">Updated the ADF .Net SDK version to 0.7.0-preview containing following changes:</span></span>
    - <span data-ttu-id="86675-142">Aggiunta dei parametri di esecuzione e della proprietà di gestione connessione nell'attività ExecuteSSISPackage</span><span class="sxs-lookup"><span data-stu-id="86675-142">Added execution parameters and connection managers property on ExecuteSSISPackage Activity</span></span>
    - <span data-ttu-id="86675-143">Aggiornamento di PostgreSql, servizio collegato di MySql, per l'uso della stringa di connessione completa invece di server, database, schema, nome utente e password</span><span class="sxs-lookup"><span data-stu-id="86675-143">Updated PostgreSql, MySql llinked service to use full connection string instead of server, database, schema, username and password</span></span>
    - <span data-ttu-id="86675-144">Rimozione dello schema dal servizio collegato DB2</span><span class="sxs-lookup"><span data-stu-id="86675-144">Removed the schema from DB2 linked service</span></span>
    - <span data-ttu-id="86675-145">Rimozione della proprietà dello schema dal servizio collegato Teradata</span><span class="sxs-lookup"><span data-stu-id="86675-145">Removed schema property from Teradata linked service</span></span>
    - <span data-ttu-id="86675-146">Aggiunta di LinkedService, Dataset, CopySource per Responsys</span><span class="sxs-lookup"><span data-stu-id="86675-146">Added LinkedService, Dataset, CopySource for Responsys</span></span>

### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="86675-147">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="86675-147">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="86675-148">Rimozione dell'alias 'Tags' deprecato dai cmdlet</span><span class="sxs-lookup"><span data-stu-id="86675-148">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="86675-149">'New-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="86675-149">'New-AzureRmDataLakeAnalyticsAccount'</span></span>
    - <span data-ttu-id="86675-150">'Set-AzureRmDataLakeAnalyticsAccount'</span><span class="sxs-lookup"><span data-stu-id="86675-150">'Set-AzureRmDataLakeAnalyticsAccount'</span></span>

### <a name="azurermdatalakestore"></a><span data-ttu-id="86675-151">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="86675-151">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="86675-152">Aggiunta della nuova funzionalità di modifica ACL ricorsiva a Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="86675-152">Add new feature of recursive Acl Change to Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="86675-153">Aggiunta del nuovo cmdlet per il recupero del riepilogo del contenuto in una directory</span><span class="sxs-lookup"><span data-stu-id="86675-153">Add new cmdlet for retrieving the content summary under a directory</span></span>
* <span data-ttu-id="86675-154">Aggiunta del nuovo cmdlet per il recupero del dump AVL e dell'utilizzo del disco</span><span class="sxs-lookup"><span data-stu-id="86675-154">Add new cmdlet for retrieving the disk usage and Acl dump</span></span>
* <span data-ttu-id="86675-155">Correzione del tipo restituito di Set-AzureRmDataLakeStoreItemAcl bool in IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="86675-155">Correct return type of Set-AzureRmDataLakeStoreItemAcl bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="86675-156">Correzione del tipo restituito di Set-AzureRmDataLakeStoreItemAclEntry bool in IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="86675-156">Correct return type of Set-AzureRmDataLakeStoreItemAclEntry bool to IEnumerable<DataLakeStoreItemAce></span></span>
* <span data-ttu-id="86675-157">Modifiche di rilievo in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="86675-157">Breaking changes in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem</span></span>

### <a name="azurermdns"></a><span data-ttu-id="86675-158">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="86675-158">AzureRM.Dns</span></span>
* <span data-ttu-id="86675-159">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-159">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-160">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-160">Please refer to the migration guide for more information</span></span>

### <a name="azurermeventhub"></a><span data-ttu-id="86675-161">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="86675-161">AzureRM.EventHub</span></span>
* <span data-ttu-id="86675-162">Aggiornamento della Guida per i cmdlet con esempi mancanti</span><span class="sxs-lookup"><span data-stu-id="86675-162">Updated Help for cmdlets with missing examples</span></span>

### <a name="azurerminsights"></a><span data-ttu-id="86675-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="86675-163">AzureRM.Insights</span></span>
* <span data-ttu-id="86675-164">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-164">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="86675-165">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-165">Please refer to the migration guide for more information</span></span>

### <a name="azurermiothub"></a><span data-ttu-id="86675-166">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="86675-166">AzureRM.IotHub</span></span>
* <span data-ttu-id="86675-167">Abilitazione dei tag e dello SKU Basic nell'hub IoT</span><span class="sxs-lookup"><span data-stu-id="86675-167">Enable tags and Basic Sku to the IotHub</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="86675-168">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="86675-168">AzureRM.KeyVault</span></span>
* <span data-ttu-id="86675-169">Modifiche di rilievo per supportare scenari di piping</span><span class="sxs-lookup"><span data-stu-id="86675-169">Breaking changes to support piping scenarios</span></span>
* <span data-ttu-id="86675-170">Aggiunta di nuovi cmdlet: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval e Undo-AzureKeyVaultManagedStorageAccountRemoval</span><span class="sxs-lookup"><span data-stu-id="86675-170">Added new cmdlets: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval, and Undo-AzureKeyVaultManagedStorageAccountRemoval</span></span>

### <a name="azurermmachinelearning"></a><span data-ttu-id="86675-171">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="86675-171">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="86675-172">Rimozione dell'alias 'Tags' deprecato dai cmdlet</span><span class="sxs-lookup"><span data-stu-id="86675-172">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="86675-173">Update-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="86675-173">Update-AzureRmMlCommitmentPlan</span></span>

### <a name="azurermmedia"></a><span data-ttu-id="86675-174">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="86675-174">AzureRM.Media</span></span>
* <span data-ttu-id="86675-175">Rimozione dell'alias 'Tags' deprecato dai cmdlet</span><span class="sxs-lookup"><span data-stu-id="86675-175">Remove deprecated 'Tags' alias from cmdlets</span></span>
    - <span data-ttu-id="86675-176">'Set-AzureRmMediaService'</span><span class="sxs-lookup"><span data-stu-id="86675-176">'Set-AzureRmMediaService'</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="86675-177">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="86675-177">AzureRM.Network</span></span>
* <span data-ttu-id="86675-178">Aggiunta del supporto per la risorsa del piano di protezione DDoS</span><span class="sxs-lookup"><span data-stu-id="86675-178">Add support for DDoS protection plan resource</span></span>
* <span data-ttu-id="86675-179">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-179">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="86675-180">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-180">Please refer to the migration guide for more information</span></span>

### <a name="azurermnotificationhubs"></a><span data-ttu-id="86675-181">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="86675-181">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="86675-182">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-182">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-183">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-183">Please refer to the migration guide for more information</span></span>

### <a name="azurermoperationalinsights"></a><span data-ttu-id="86675-184">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="86675-184">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="86675-185">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-185">Introduce multiple breaking changes</span></span>
    - <span data-ttu-id="86675-186">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-186">Please refer to the migration guide for more information</span></span>

### <a name="azurermprofile"></a><span data-ttu-id="86675-187">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="86675-187">AzureRM.Profile</span></span>
* <span data-ttu-id="86675-188">Abilitazione del salvataggio automatico del contesto per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="86675-188">Enable context autosave by default</span></span>
* <span data-ttu-id="86675-189">Aggiunta delle proprietà USGovernmentOperationalInsightsEndpoint e USGovernmentOperationalInsightsEndpointResourceId all'ambiente Azure per US Gov.</span><span class="sxs-lookup"><span data-stu-id="86675-189">Add USGovernmentOperationalInsightsEndpoint and USGovernmentOperationalInsightsEndpointResourceId properties to Azure environment for US Gov.</span></span>

### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="86675-190">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="86675-190">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="86675-191">Correzione dell'intestazione di autenticazione in scenari SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="86675-191">Fixed Authentication Header in SiteRecovery scenarios</span></span>

### <a name="azurermrediscache"></a><span data-ttu-id="86675-192">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="86675-192">AzureRM.RedisCache</span></span>
* <span data-ttu-id="86675-193">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-193">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="86675-194">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-194">Please refer to the migration guide for more information</span></span>

### <a name="azurermresources"></a><span data-ttu-id="86675-195">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="86675-195">AzureRM.Resources</span></span>
* <span data-ttu-id="86675-196">Rimozione del parametro obsoleto -AtScopeAndBelow dalla chiamata Get-AzureRmRoledefinition</span><span class="sxs-lookup"><span data-stu-id="86675-196">Remove obsolete parameter -AtScopeAndBelow from Get-AzureRmRoledefinition call</span></span>
* <span data-ttu-id="86675-197">Inclusione delle assegnazioni a utenti/gruppi/entità servizio eliminati nel risultato di Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="86675-197">Include assignments to deleted USers/Groups/ServicePrincipals in Get-AzureRmRoleAssignment result</span></span>
* <span data-ttu-id="86675-198">Aggiunta dei completer di tabulazione per Scope e ResourceType</span><span class="sxs-lookup"><span data-stu-id="86675-198">Add Tab completers for Scope and ResourceType</span></span>
* <span data-ttu-id="86675-199">Aggiunta di un cmdlet pratico per la creazione di entità servizio</span><span class="sxs-lookup"><span data-stu-id="86675-199">Add convenience cmdlet for creating ServicePrincipals</span></span>
* <span data-ttu-id="86675-200">Unione della funzionalità di Get- e Find- in Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="86675-200">Merge Get- and Find- functionality in Get-AzureRmResource</span></span>
* <span data-ttu-id="86675-201">Aggiunta di cmdlet AD:</span><span class="sxs-lookup"><span data-stu-id="86675-201">Add AD Cmdlets:</span></span>
  - <span data-ttu-id="86675-202">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="86675-202">Remove-AzureRmADGroupMember</span></span>
  - <span data-ttu-id="86675-203">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="86675-203">Get-AzureRmADGroup</span></span>
  - <span data-ttu-id="86675-204">New-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="86675-204">New-AzureRmADGroup</span></span>
  - <span data-ttu-id="86675-205">Remove-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="86675-205">Remove-AzureRmADGroup</span></span>
  - <span data-ttu-id="86675-206">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="86675-206">Remove-AzureRmADUser</span></span>
  - <span data-ttu-id="86675-207">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="86675-207">Update-AzureRmADApplication</span></span>
  - <span data-ttu-id="86675-208">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="86675-208">Update-AzureRmADServicePrincipal</span></span>
  - <span data-ttu-id="86675-209">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="86675-209">Update-AzureRmADUser</span></span>

### <a name="azurermservicefabric"></a><span data-ttu-id="86675-210">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="86675-210">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="86675-211">Aggiornamento dello SKU di versione predefinito dell'immagine Linux</span><span class="sxs-lookup"><span data-stu-id="86675-211">Update default Linux image version sku</span></span>
  - <span data-ttu-id="86675-212">Aggiornamento dello SKU UbuntuServer1604 predefinito di NewAzureServiceFabricCluster.cs</span><span class="sxs-lookup"><span data-stu-id="86675-212">NewAzureServiceFabricCluster.cs default UbuntuServer1604 Sku update</span></span>

### <a name="azurermstorage"></a><span data-ttu-id="86675-213">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="86675-213">AzureRM.Storage</span></span>
* <span data-ttu-id="86675-214">Introduzione di numerose modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="86675-214">Introduced multiple breaking changes</span></span>
    - <span data-ttu-id="86675-215">Per altre informazioni, vedere la guida alla migrazione</span><span class="sxs-lookup"><span data-stu-id="86675-215">Please refer to the migration guide for more information</span></span>

### <a name="azurermwebsites"></a><span data-ttu-id="86675-216">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="86675-216">AzureRM.Websites</span></span>
* <span data-ttu-id="86675-217">Aggiornamento alla versione più recente dell'SDK di Siti Web</span><span class="sxs-lookup"><span data-stu-id="86675-217">Upgrade to latest version of the Websites SDK</span></span>
* <span data-ttu-id="86675-218">Aggiunta delle proprietà -AssignIdentity e -Httpsonly per Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86675-218">Added -AssignIdentity & -Httpsonly properties for Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
* <span data-ttu-id="86675-219">Aggiunta di due nuovi cmdlet: Get-AzureRmWebAppSnapshots e Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="86675-219">Added two new cmdlets: Get-AzureRmWebAppSnapshots and Restore-AzureRmWebAppSnapshot</span></span>
