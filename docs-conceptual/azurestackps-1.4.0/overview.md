# <a name="azure-stack-module-140"></a><span data-ttu-id="d90ef-101">Modulo di Azure Stack 1.4.0</span><span class="sxs-lookup"><span data-stu-id="d90ef-101">Azure Stack Module 1.4.0</span></span>

## <a name="requirements"></a><span data-ttu-id="d90ef-102">Requirements:</span><span class="sxs-lookup"><span data-stu-id="d90ef-102">Requirements:</span></span>
<span data-ttu-id="d90ef-103">La versione minima supportata di Azure Stack è 1804.</span><span class="sxs-lookup"><span data-stu-id="d90ef-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="d90ef-104">Nota: se si usa una versione precedente, installare la versione 1.2.11</span><span class="sxs-lookup"><span data-stu-id="d90ef-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="d90ef-105">Problemi noti:</span><span class="sxs-lookup"><span data-stu-id="d90ef-105">Known issues:</span></span>

- <span data-ttu-id="d90ef-106">Chiudi avviso richiede Azure Stack versione 1803</span><span class="sxs-lookup"><span data-stu-id="d90ef-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="d90ef-107">New-AzsOffer non consente la creazione di un'offerta con stato pubblico.</span><span class="sxs-lookup"><span data-stu-id="d90ef-107">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="d90ef-108">Il cmdlet Set-AzsOffer deve essere chiamato successivamente per modificare lo stato.</span><span class="sxs-lookup"><span data-stu-id="d90ef-108">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="d90ef-109">Non è possibile rimuovere un pool IP senza una ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="d90ef-109">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="d90ef-110">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="d90ef-110">Breaking Changes</span></span>
<span data-ttu-id="d90ef-111">Non sono presenti modifiche di rilievo rispetto alla versione 1.3.0.</span><span class="sxs-lookup"><span data-stu-id="d90ef-111">There are no breaking changes from the version 1.3.0.</span></span> <span data-ttu-id="d90ef-112">Tutte le modifiche che causano un'interruzione durante la migrazione da 1.2.11 sono documentate qui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="d90ef-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="d90ef-113">Installa</span><span class="sxs-lookup"><span data-stu-id="d90ef-113">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.4.0
```
## <a name="release-notes"></a><span data-ttu-id="d90ef-114">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="d90ef-114">Release Notes</span></span>
    * <span data-ttu-id="d90ef-115">AzureStack versione 1.4.0 non ha modifiche di rilievo rispetto alla versione 1.3.0 precedente</span><span class="sxs-lookup"><span data-stu-id="d90ef-115">Azurestack 1.4.0 version has no breaking changes from the previous release 1.3.0</span></span>
    * <span data-ttu-id="d90ef-116">Azs.AzureBridge.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-116">Azs.AzureBridge.Admin</span></span>
        - <span data-ttu-id="d90ef-117">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-117">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-118">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-118">Azs.Backup.Admin</span></span>
        - <span data-ttu-id="d90ef-119">Aggiunta di nuovi parametri BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays nel cmdlet Set-AzsBackupShare</span><span class="sxs-lookup"><span data-stu-id="d90ef-119">Added new parameters BackupFrequencyInHours, IsBackupSchedulerEnabled, BackupRetentionPeriodInDays in cmdlet Set-AzsBackupShare</span></span>
        - <span data-ttu-id="d90ef-120">Aggiunta di un cmdlet New-EncyptionKeyBase64 per agevolare la creazione di una chiave di crittografia</span><span class="sxs-lookup"><span data-stu-id="d90ef-120">Added a cmdlet New-EncyptionKeyBase64 to facilitate creating encryption key</span></span>
        - <span data-ttu-id="d90ef-121">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-121">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-122">Azs.Commerce.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-122">Azs.Commerce.Admin</span></span>
        - <span data-ttu-id="d90ef-123">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-123">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-124">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-124">Azs.Fabric.Admin</span></span>
        - <span data-ttu-id="d90ef-125">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-125">Fix for the bug that returned only a single page in paginated results</span></span>
        - <span data-ttu-id="d90ef-126">Aggiunta di un cmdlet Add-AzsScaleUnitNode per consentire all'amministratore di aggiungere nuovi nodi di unità di scala allo stamp azurestack</span><span class="sxs-lookup"><span data-stu-id="d90ef-126">Added a cmdlet Add-AzsScaleUnitNode to enable admin to add new scale unit nodes to the azurestack stamp</span></span>
        - <span data-ttu-id="d90ef-127">Aggiunta di cmdlet e New-AzsScaleUnitNodeObject per agevolare la creazione di oggetti dei parametri di unità di scala</span><span class="sxs-lookup"><span data-stu-id="d90ef-127">Added cmdlet and New-AzsScaleUnitNodeObject to facilitate the creation scale unit parameter objects</span></span>
    * <span data-ttu-id="d90ef-128">Azs.Gallery.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-128">Azs.Gallery.Admin</span></span>
        - <span data-ttu-id="d90ef-129">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-129">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-130">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-130">Azs.InfrastructureInsights.Admin</span></span>
        - <span data-ttu-id="d90ef-131">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-131">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-132">Azs.Network.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-132">Azs.Network.Admin</span></span>
        - <span data-ttu-id="d90ef-133">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-133">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-134">Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-134">Azs.Update.Admin</span></span>
        - <span data-ttu-id="d90ef-135">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-135">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-136">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="d90ef-136">Azs.Subscriptions</span></span>
        - <span data-ttu-id="d90ef-137">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-137">Fix for the bug that returned only a single page in paginated results</span></span>
    * <span data-ttu-id="d90ef-138">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="d90ef-138">Azs.Subscriptions.Admin</span></span>
        - <span data-ttu-id="d90ef-139">Aggiunta di un cmdlet Move-AzsSubscription per trasferire le sottoscrizioni tra offerte di provider delegati</span><span class="sxs-lookup"><span data-stu-id="d90ef-139">Added a cmdlet Move-AzsSubscription to move subscriptions between delegated provider offers</span></span>
        - <span data-ttu-id="d90ef-140">Aggiunta di un cmdlet Test-AzsMoveSubscription per convalidare che le sottoscrizioni utente possano essere trasferite tra offerte di provider delegati</span><span class="sxs-lookup"><span data-stu-id="d90ef-140">Added a cmdlet Test-AzsMoveSubscription to validate that user subscriptions can be moved between delegated provider offers</span></span>
        - <span data-ttu-id="d90ef-141">Correzione del bug che restituiva una sola pagina nei risultati impaginati</span><span class="sxs-lookup"><span data-stu-id="d90ef-141">Fix for the bug that returned only a single page in paginated results'</span></span>

## <a name="content"></a><span data-ttu-id="d90ef-142">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="d90ef-142">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="d90ef-143">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="d90ef-143">Azure Bridge</span></span>
<span data-ttu-id="d90ef-144">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="d90ef-144">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="d90ef-145">Backup</span><span class="sxs-lookup"><span data-stu-id="d90ef-145">Backup</span></span>
<span data-ttu-id="d90ef-146">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="d90ef-146">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="d90ef-147">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="d90ef-147">Configure where backups are stored</span></span>
- <span data-ttu-id="d90ef-148">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="d90ef-148">Perform backups</span></span>
- <span data-ttu-id="d90ef-149">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="d90ef-149">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="d90ef-150">E-commerce</span><span class="sxs-lookup"><span data-stu-id="d90ef-150">Commerce</span></span>
<span data-ttu-id="d90ef-151">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d90ef-151">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="d90ef-152">Calcolo</span><span class="sxs-lookup"><span data-stu-id="d90ef-152">Compute</span></span>
<span data-ttu-id="d90ef-153">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="d90ef-153">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="d90ef-154">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d90ef-154">Fabric</span></span>
<span data-ttu-id="d90ef-155">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="d90ef-155">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="d90ef-156">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="d90ef-156">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="d90ef-157">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="d90ef-157">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="d90ef-158">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="d90ef-158">Repair of scale unit nodes</span></span>
- <span data-ttu-id="d90ef-159">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d90ef-159">Restart of Infrastructure role</span></span>
- <span data-ttu-id="d90ef-160">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d90ef-160">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="d90ef-161">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="d90ef-161">Create new IP Pools</span></span>

### <a name="gallery"></a><span data-ttu-id="d90ef-162">Gallery</span><span class="sxs-lookup"><span data-stu-id="d90ef-162">Gallery</span></span>
<span data-ttu-id="d90ef-163">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="d90ef-163">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="d90ef-164">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="d90ef-164">Infrastructure Insights</span></span>
<span data-ttu-id="d90ef-165">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="d90ef-165">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="d90ef-166">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="d90ef-166">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="d90ef-167">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="d90ef-167">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="d90ef-168">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="d90ef-168">KeyVault</span></span>
<span data-ttu-id="d90ef-169">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="d90ef-169">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="d90ef-170">Rete</span><span class="sxs-lookup"><span data-stu-id="d90ef-170">Network</span></span>
<span data-ttu-id="d90ef-171">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="d90ef-171">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="d90ef-172">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="d90ef-172">Management of network quotas</span></span>
- <span data-ttu-id="d90ef-173">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="d90ef-173">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="d90ef-174">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="d90ef-174">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="d90ef-175">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="d90ef-175">Storage</span></span>
<span data-ttu-id="d90ef-176">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d90ef-176">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="d90ef-177">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="d90ef-177">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="d90ef-178">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d90ef-178">Manage storage quotas</span></span>
- <span data-ttu-id="d90ef-179">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="d90ef-179">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="d90ef-180">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="d90ef-180">Restore deleted storage accounts</span></span>
- <span data-ttu-id="d90ef-181">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="d90ef-181">Migrate containers from one share to another</span></span>
- <span data-ttu-id="d90ef-182">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d90ef-182">View information about the individual storage components</span></span>
- <span data-ttu-id="d90ef-183">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="d90ef-183">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="d90ef-184">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d90ef-184">Subscription Admin</span></span>
<span data-ttu-id="d90ef-185">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d90ef-185">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="d90ef-186">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="d90ef-186">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="d90ef-187">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="d90ef-187">Manage plans and offers</span></span>
- <span data-ttu-id="d90ef-188">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="d90ef-188">View usage and performance information</span></span>
- <span data-ttu-id="d90ef-189">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="d90ef-189">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="d90ef-190">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="d90ef-190">Subscription</span></span>
<span data-ttu-id="d90ef-191">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d90ef-191">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="d90ef-192">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="d90ef-192">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="d90ef-193">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="d90ef-193">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="d90ef-194">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="d90ef-194">Update</span></span>
<span data-ttu-id="d90ef-195">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="d90ef-195">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="d90ef-196">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="d90ef-196">In this module administrators can:</span></span>
- <span data-ttu-id="d90ef-197">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="d90ef-197">List and install available updates</span></span>
- <span data-ttu-id="d90ef-198">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="d90ef-198">Resume interrupted updates</span></span>
- <span data-ttu-id="d90ef-199">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="d90ef-199">View installed updates</span></span>
