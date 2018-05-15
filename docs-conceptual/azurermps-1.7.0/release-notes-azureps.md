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
ms.date: 05/18/2017
ms.openlocfilehash: 0a3f152751fee569d3ac5fba6bcff8c1737f7b8c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="7ce95-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="7ce95-103">Release notes</span></span>

<span data-ttu-id="7ce95-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="7ce95-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-170"></a><span data-ttu-id="7ce95-105">Versione 1.7.0</span><span class="sxs-lookup"><span data-stu-id="7ce95-105">Version 1.7.0</span></span>

* <span data-ttu-id="7ce95-106">**Modifica comportamentale per i parametri -Force, -Confirm e $ConfirmPreference per tutti i cmdlet. Questa implementazione è in fase di modifica per allinearla alle linee guida di PowerShell. Per la maggior parte dei cmdlet, questo significa rimuovere il parametro Force e per ignorare la richiesta ShouldProcess, gli utenti dovranno includere il parametro‘-Confirm:$false’ negli script di PowerShell.**</span><span class="sxs-lookup"><span data-stu-id="7ce95-106">**Behavioral change for -Force, –Confirm and $ConfirmPreference parameters for all cmdlets. We are changing this implementation to be in line with PowerShell guidelines. For most cmdlets, this means removing the Force parameter and to skip the ShouldProcess prompt, users will need to include the parameter: ‘-Confirm:$false’ in their PowerShell scripts.**</span></span> <span data-ttu-id="7ce95-107">Queste modifiche permettono di risolvere i problemi seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ce95-107">This changes are addressing following issues:</span></span>
  - <span data-ttu-id="7ce95-108">Implementazione corretta della funzionalità -WhatIf, per permettere a un utente di determinare gli effetti di un cmdlet o uno script senza apportare alcuna modifica effettiva</span><span class="sxs-lookup"><span data-stu-id="7ce95-108">Correct implementation of –WhatIf functionality, allowing a user to determine the effects of a cmdlet or script without making any actual changes</span></span>
  - <span data-ttu-id="7ce95-109">Controllo sulle richieste tramite $ConfirmPreference a livello di sessione, in modo che l'utente riceva le richieste in base all'impatto di una potenziale modifica (come indicato nell'impostazione ConfirmImpact nel cmdlet)</span><span class="sxs-lookup"><span data-stu-id="7ce95-109">Control over prompting using a session-wide $ConfirmPreference, so that the user is prompted based on the impact of a prospective change (as reported in the ConfirmImpact setting in the cmdlet)</span></span>
  - <span data-ttu-id="7ce95-110">Controllo specifico dei cmdlet sulle richieste di conferma tramite il parametro -Confirm</span><span class="sxs-lookup"><span data-stu-id="7ce95-110">Cmdlet-specific control over confirmation prompts using the –Confirm parameter</span></span>
  - <span data-ttu-id="7ce95-111">Uso coerente di ShouldContinue e del parametro -Force nei cmdlet, solo per le azioni che richiedono la generazione di richieste all'utente a causa della natura speciale delle modifiche, ad esempio riguardo all'eliminazione di file nascosti</span><span class="sxs-lookup"><span data-stu-id="7ce95-111">Consistent use of ShouldContinue and the –Force parameter across cmdlets, for only those actions that would require prompting from the user due to the special nature of the changes (for example, deleting hidden files)</span></span>
  - <span data-ttu-id="7ce95-112">Coerenza con altri cmdlet di PowerShell, in modo che la conoscenza degli script di PowerShell acquisita da altri cmdlet possa essere immediatamente applicata ai cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7ce95-112">Consistency with other PowerShell cmdlets, so that PowerShell scripting knowledge from other cmdlets is immediately applicable to the Azure PowerShell cmdlets.</span></span>

<span data-ttu-id="7ce95-113">**Si noti che per *ignorare automaticamente tutte le richieste in tutti i casi*, i cmdlet di Azure PowerShell richiedono ora all'utente di fornire due parametri:**</span><span class="sxs-lookup"><span data-stu-id="7ce95-113">**Notice that now to *automatically skip all Prompts in all Circumstances* Azure PowerShell cmdlets require the user to supply two parameters:**</span></span>
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* <span data-ttu-id="7ce95-114">Calcolo di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-114">Azure Compute</span></span>
  - <span data-ttu-id="7ce95-115">Set-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7ce95-115">Set-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="7ce95-116">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="7ce95-116">Get-AzureRmVMADDomainExtension</span></span>
  - <span data-ttu-id="7ce95-117">Parametro -Redeploy per Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="7ce95-117">-Redeploy parameter for Restart-AzureVM</span></span>
  - <span data-ttu-id="7ce95-118">Parametro -Validate per Move-AzureService, Move-AzureStorageAccount e Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7ce95-118">-Validate parameter for Move-AzureService, Move-AzureStorageAccount, and Move-AzureVirtualNetwork</span></span>
  - <span data-ttu-id="7ce95-119">I parametri per nome e versione per i cmdlet di estensione sono facoltativi come nelle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="7ce95-119">Name and version parameters for extension cmdlets are optional as before.</span></span>
  - <span data-ttu-id="7ce95-120">New-AzureVM può ottenere un tipo di licenza dall'oggetto VM.</span><span class="sxs-lookup"><span data-stu-id="7ce95-120">New-AzureVM can get a license type from VM object.</span></span>
* <span data-ttu-id="7ce95-121">Archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-121">Azure Storage</span></span>
  - <span data-ttu-id="7ce95-122">Modifica del parametro Tags in Tag e aggiunta dell'alias di parametro Tags</span><span class="sxs-lookup"><span data-stu-id="7ce95-122">Change Tags Parameter to Tag, and add parameter alias Tags</span></span>
    + <span data-ttu-id="7ce95-123">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-123">New-AzureRmStorageAccount</span></span>
    + <span data-ttu-id="7ce95-124">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-124">Set-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7ce95-125">Azure Network</span><span class="sxs-lookup"><span data-stu-id="7ce95-125">Azure Network</span></span>
  - <span data-ttu-id="7ce95-126">Aggiunta di un nuovo cmdlet per il peering di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="7ce95-126">New cmdlet added for Virtual Network Peering</span></span>
* <span data-ttu-id="7ce95-127">Cache Redis di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-127">Azure Redis Cache</span></span>
  - <span data-ttu-id="7ce95-128">Aggiunta di un nuovo cmdlet per Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ce95-128">New cmdlet added for Reset-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce95-129">Aggiunta di un nuovo cmdlet per Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ce95-129">New cmdlet added for Export-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce95-130">Aggiunta di un nuovo cmdlet per Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7ce95-130">New cmdlet added for Import-AzureRmRedisCache</span></span>
  - <span data-ttu-id="7ce95-131">Modifica del cmdlet New-AzureRmRedisCache per includere una modifica del parametro per vNet</span><span class="sxs-lookup"><span data-stu-id="7ce95-131">Modified cmdlet New-AzureRmRedisCache to include parameter change for vNet</span></span>
* <span data-ttu-id="7ce95-132">Backup/ripristino del database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-132">Azure SQL DB Backup/Restore</span></span>
  - <span data-ttu-id="7ce95-133">Cmdlet per la funzionalità di backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="7ce95-133">Cmdlets for LTR (Long Term Retention) backup feature</span></span>
  - <span data-ttu-id="7ce95-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="7ce95-134">Get-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="7ce95-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce95-135">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="7ce95-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span><span class="sxs-lookup"><span data-stu-id="7ce95-136">Set-AzureRmSqlServerBackupLongTermRetentionVault</span></span>
  - <span data-ttu-id="7ce95-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ce95-137">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>
  - <span data-ttu-id="7ce95-138">Restore-AzureRmSqlDatabase supporta ora il ripristino temporizzato di un database eliminato</span><span class="sxs-lookup"><span data-stu-id="7ce95-138">Restore-AzureRmSqlDatabase now supports point-in-time restore of a deleted database</span></span>
  - <span data-ttu-id="7ce95-139">Restore-AzureRmSqlDatabase supporta ora il ripristino da un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="7ce95-139">Restore-AzureRmSqlDatabase now supports restoring from a Long Term Retention backup</span></span>
* <span data-ttu-id="7ce95-140">Azure LogicApp</span><span class="sxs-lookup"><span data-stu-id="7ce95-140">Azure LogicApp</span></span>
  - <span data-ttu-id="7ce95-141">Aggiunta di cmdlet per gli account di integrazione di LogicApp.</span><span class="sxs-lookup"><span data-stu-id="7ce95-141">Added LogicApp Integration accounts cmdlets.</span></span>
  - <span data-ttu-id="7ce95-142">Get-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7ce95-142">Get-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce95-143">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="7ce95-143">Get-AzureRmIntegrationAccountCallbackUrl</span></span>
  - <span data-ttu-id="7ce95-144">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7ce95-144">Get-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce95-145">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-145">Get-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce95-146">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ce95-146">Get-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce95-147">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce95-147">Get-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce95-148">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7ce95-148">Get-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce95-149">New-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7ce95-149">New-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce95-150">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7ce95-150">New-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce95-151">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-151">New-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce95-152">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ce95-152">New-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce95-153">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce95-153">New-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce95-154">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7ce95-154">New-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce95-155">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7ce95-155">Remove-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce95-156">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7ce95-156">Remove-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce95-157">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-157">Remove-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce95-158">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ce95-158">Remove-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce95-159">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce95-159">Remove-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce95-160">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7ce95-160">Remove-AzureRmIntegrationAccountSchema</span></span>
  - <span data-ttu-id="7ce95-161">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="7ce95-161">Set-AzureRmIntegrationAccountAgreement</span></span>
  - <span data-ttu-id="7ce95-162">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="7ce95-162">Set-AzureRmIntegrationAccountCertificate</span></span>
  - <span data-ttu-id="7ce95-163">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="7ce95-163">Set-AzureRmIntegrationAccount</span></span>
  - <span data-ttu-id="7ce95-164">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="7ce95-164">Set-AzureRmIntegrationAccountMap</span></span>
  - <span data-ttu-id="7ce95-165">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="7ce95-165">Set-AzureRmIntegrationAccountPartner</span></span>
  - <span data-ttu-id="7ce95-166">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="7ce95-166">Set-AzureRmIntegrationAccountSchema</span></span>
* <span data-ttu-id="7ce95-167">Archivio Azure Data Lake</span><span class="sxs-lookup"><span data-stu-id="7ce95-167">Azure Data Lake Store</span></span>
  - <span data-ttu-id="7ce95-168">Drastico miglioramento delle prestazioni di caricamento e download di file e cartelle.</span><span class="sxs-lookup"><span data-stu-id="7ce95-168">Drastically improve performance of file and folder upload and download.</span></span>
  - <span data-ttu-id="7ce95-169">Sono incluse una piccola modifica ai nomi di parametro per il download e l'aggiunta di due nuovi parametri per il caricamento:</span><span class="sxs-lookup"><span data-stu-id="7ce95-169">This includes a slight change to the parameter names for download and inclusion of two new parameters for upload:</span></span>
    + <span data-ttu-id="7ce95-170">NumThreads -> PerFileThreadCount, usato per indicare il numero di thread da usare in un singolo file</span><span class="sxs-lookup"><span data-stu-id="7ce95-170">NumThreads -> PerFileThreadCount, used to indicate the number of threads to use in a single file</span></span>
    + <span data-ttu-id="7ce95-171">ConcurrentFileCount, usato per indicare il numero di file da caricare/scaricare in parallelo per il caricamento/download di cartelle.</span><span class="sxs-lookup"><span data-stu-id="7ce95-171">ConcurrentFileCount, used to indicate the number of files to upload/download in parallel for folder upload/download.</span></span>
  - <span data-ttu-id="7ce95-172">Vengono ora designati i valori di threading predefiniti per offrire una migliore velocità effettiva complessiva per la maggior parte delle dimensioni di file.</span><span class="sxs-lookup"><span data-stu-id="7ce95-172">Default threading values are now designed to give a better all around throughput for most file sizes.</span></span> <span data-ttu-id="7ce95-173">Se le prestazioni sono insufficienti, i valori indicati sopra possono essere modificati per soddisfare i requisiti.</span><span class="sxs-lookup"><span data-stu-id="7ce95-173">If performance is not as desired, the values above can be modified to meet requirements.</span></span>
* <span data-ttu-id="7ce95-174">Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="7ce95-174">Azure Data Lake Analytics</span></span>
  - <span data-ttu-id="7ce95-175">Get-AzureRMDataLakeAnalyticsDataSource restituisce ora tutte le origini dati quando viene chiamato senza argomenti.</span><span class="sxs-lookup"><span data-stu-id="7ce95-175">Get-AzureRMDataLakeAnalyticsDataSource now returns all data sources when called with no arguments.</span></span>
  - <span data-ttu-id="7ce95-176">Questa modifica comporta anche la rimozione del parametro del tipo di origine dati dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ce95-176">This change also removes the data source type parameter from the cmdlet.</span></span>
  - <span data-ttu-id="7ce95-177">Questa modifica produce la restituzione di un nuovo oggetto per l'operazione di elenco con le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="7ce95-177">This change results in a new object being returned for the list operation with the following properties:</span></span>
    + <span data-ttu-id="7ce95-178">Type: tipo dell'origine dati</span><span class="sxs-lookup"><span data-stu-id="7ce95-178">Type, the type of data source</span></span>
    + <span data-ttu-id="7ce95-179">Name: nome dell'origine dati</span><span class="sxs-lookup"><span data-stu-id="7ce95-179">Name, the name of the data source</span></span>
    + <span data-ttu-id="7ce95-180">IsDefault: impostato su true se si tratta dell'origine dati predefinita per l'account</span><span class="sxs-lookup"><span data-stu-id="7ce95-180">IsDefault, set to true if this is the default data source for the account</span></span>
  - <span data-ttu-id="7ce95-181">Correzione di Get-AzureRMDataLakeAnalyticsJob per elencare determinati valori di offset di data e ora quando si filtra in base a submittedBefore e submittedAfter.</span><span class="sxs-lookup"><span data-stu-id="7ce95-181">Get-AzureRMDataLakeAnalyticsJob fixed for list for certain date time offset values when filtering on submittedBefore and submittedAfter.</span></span>
* <span data-ttu-id="7ce95-182">App Web</span><span class="sxs-lookup"><span data-stu-id="7ce95-182">Web Apps</span></span>
  - <span data-ttu-id="7ce95-183">Aggiunta del cmdlet Swap-AzureRmWebAppSlot per lo scambio normale e lo scambio con anteprima</span><span class="sxs-lookup"><span data-stu-id="7ce95-183">Add Swap-AzureRmWebAppSlot cmdlet for regular swap and swap with preview</span></span>
  - <span data-ttu-id="7ce95-184">Estensione del cmdlet Set-AzureRmWebAppSlot per supportare lo scambio automatico</span><span class="sxs-lookup"><span data-stu-id="7ce95-184">Extend Set-AzureRmWebAppSlot cmdlet to support auto swap</span></span>
* <span data-ttu-id="7ce95-185">Gestione API di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-185">Azure API Management</span></span>
  - <span data-ttu-id="7ce95-186">Correzione dei cmdlet di distribuzione di Gestione API di Azure per AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="7ce95-186">Fixed Azure Api Management Deployment cmdlets for AzureChinaCloud.</span></span>
  - <span data-ttu-id="7ce95-187">Rimozione del cmdlet Set-AzureRmApiManagementTenantGitAccess, perché l'accesso a Git è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="7ce95-187">Removed cmdlet Set-AzureRmApiManagementTenantGitAccess as Git Access is enabled by Default.</span></span>
* <span data-ttu-id="7ce95-188">Backup di Servizi di ripristino di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-188">Azure Recovery Services Backup</span></span>
  - <span data-ttu-id="7ce95-189">Aggiunta del supporto per il carico di lavoro SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-189">Added support for the Azure SQL workload</span></span>
  - <span data-ttu-id="7ce95-190">Aggiunta del supporto per il backup e il ripristino di VM di Azure crittografate</span><span class="sxs-lookup"><span data-stu-id="7ce95-190">Added support for backing up and restoring encrypted Azure VMs</span></span>
  - <span data-ttu-id="7ce95-191">Backup-AzureRmRecoveryServicesBackupItem: aggiunta della funzionalità per il tempo di conservazione facoltativa per punti di ripristino</span><span class="sxs-lookup"><span data-stu-id="7ce95-191">Backup-AzureRmRecoveryServicesBackupItem - Added optional retention time feature for recovery points</span></span>
  - <span data-ttu-id="7ce95-192">Minori correzioni di bug correlate ai filtri nei cmdlet Get-AzureRmRecoveryServicesBackupContainer e Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7ce95-192">Minor filter-related bug fixes in Get-AzureRmRecoveryServicesBackupContainer and Get-AzureRmRecoveryServicesBackupItem cmdlets</span></span>
* <span data-ttu-id="7ce95-193">Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="7ce95-193">Azure Automation</span></span>
  - <span data-ttu-id="7ce95-194">Aggiunta di Get-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="7ce95-194">Added Get-AzureRmAutomationHybridWorkerGroup</span></span>
