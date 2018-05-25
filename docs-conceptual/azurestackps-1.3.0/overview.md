# <a name="azure-stack-module-130"></a><span data-ttu-id="ed0b2-101">Modulo di Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="ed0b2-101">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ed0b2-102">Requirements:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-102">Requirements:</span></span>
<span data-ttu-id="ed0b2-103">La versione minima supportata di Azure Stack è 1804.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-103">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="ed0b2-104">Nota: se si usa una versione precedente, installare la versione 1.2.11</span><span class="sxs-lookup"><span data-stu-id="ed0b2-104">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="ed0b2-105">Problemi noti:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-105">Known issues:</span></span>

- <span data-ttu-id="ed0b2-106">Chiudi avviso richiede Azure Stack versione 1803</span><span class="sxs-lookup"><span data-stu-id="ed0b2-106">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="ed0b2-107">Alcuni cmdlet di Archiviazione richiedono Azure Stack versione 1804</span><span class="sxs-lookup"><span data-stu-id="ed0b2-107">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="ed0b2-108">New-AzsOffer non consente la creazione di un'offerta con stato pubblico.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ed0b2-109">Il cmdlet Set-AzsOffer deve essere chiamato successivamente per modificare lo stato.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ed0b2-110">Non è possibile rimuovere un pool IP senza una ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="ed0b2-111">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ed0b2-111">Breaking Changes</span></span>
<span data-ttu-id="ed0b2-112">Tutte le modifiche che causano un'interruzione durante la migrazione da 1.2.11 sono documentate qui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="ed0b2-112">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="ed0b2-113">Installa</span><span class="sxs-lookup"><span data-stu-id="ed0b2-113">Install</span></span>
```
# Remove previous Versions
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Uninstall-Module -Name AzureStack -Force 


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2017-03-09-profile -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.3.0
```
## <a name="content"></a><span data-ttu-id="ed0b2-114">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-114">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ed0b2-115">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ed0b2-115">Azure Bridge</span></span>
<span data-ttu-id="ed0b2-116">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-116">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ed0b2-117">Backup</span><span class="sxs-lookup"><span data-stu-id="ed0b2-117">Backup</span></span>
<span data-ttu-id="ed0b2-118">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-118">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ed0b2-119">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="ed0b2-119">Configure where backups are stored</span></span>
- <span data-ttu-id="ed0b2-120">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="ed0b2-120">Perform backups</span></span>
- <span data-ttu-id="ed0b2-121">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="ed0b2-121">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ed0b2-122">E-commerce</span><span class="sxs-lookup"><span data-stu-id="ed0b2-122">Commerce</span></span>
<span data-ttu-id="ed0b2-123">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-123">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ed0b2-124">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ed0b2-124">Compute</span></span>
<span data-ttu-id="ed0b2-125">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-125">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ed0b2-126">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ed0b2-126">Fabric</span></span>
<span data-ttu-id="ed0b2-127">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-127">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ed0b2-128">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="ed0b2-128">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ed0b2-129">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="ed0b2-129">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ed0b2-130">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="ed0b2-130">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ed0b2-131">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ed0b2-131">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ed0b2-132">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ed0b2-132">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ed0b2-133">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="ed0b2-133">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ed0b2-134">Gallery</span><span class="sxs-lookup"><span data-stu-id="ed0b2-134">Gallery</span></span>
<span data-ttu-id="ed0b2-135">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-135">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ed0b2-136">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ed0b2-136">Infrastructure Insights</span></span>
<span data-ttu-id="ed0b2-137">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-137">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ed0b2-138">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="ed0b2-138">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ed0b2-139">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="ed0b2-139">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ed0b2-140">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="ed0b2-140">KeyVault</span></span>
<span data-ttu-id="ed0b2-141">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-141">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ed0b2-142">Rete</span><span class="sxs-lookup"><span data-stu-id="ed0b2-142">Network</span></span>
<span data-ttu-id="ed0b2-143">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-143">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ed0b2-144">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="ed0b2-144">Management of network quotas</span></span>
- <span data-ttu-id="ed0b2-145">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="ed0b2-145">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ed0b2-146">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="ed0b2-146">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ed0b2-147">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-147">Storage</span></span>
<span data-ttu-id="ed0b2-148">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-148">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ed0b2-149">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-149">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ed0b2-150">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-150">Manage storage quotas</span></span>
- <span data-ttu-id="ed0b2-151">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="ed0b2-151">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ed0b2-152">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="ed0b2-152">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ed0b2-153">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="ed0b2-153">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ed0b2-154">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-154">View information about the individual storage components</span></span>
- <span data-ttu-id="ed0b2-155">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="ed0b2-155">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ed0b2-156">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-156">Subscription Admin</span></span>
<span data-ttu-id="ed0b2-157">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-157">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ed0b2-158">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-158">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ed0b2-159">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="ed0b2-159">Manage plans and offers</span></span>
- <span data-ttu-id="ed0b2-160">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="ed0b2-160">View usage and performance information</span></span>
- <span data-ttu-id="ed0b2-161">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="ed0b2-161">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ed0b2-162">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ed0b2-162">Subscription</span></span>
<span data-ttu-id="ed0b2-163">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-163">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ed0b2-164">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-164">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ed0b2-165">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="ed0b2-165">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ed0b2-166">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ed0b2-166">Update</span></span>
<span data-ttu-id="ed0b2-167">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ed0b2-167">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ed0b2-168">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="ed0b2-168">In this module administrators can:</span></span>
- <span data-ttu-id="ed0b2-169">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="ed0b2-169">List and install available updates</span></span>
- <span data-ttu-id="ed0b2-170">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ed0b2-170">Resume interrupted updates</span></span>
- <span data-ttu-id="ed0b2-171">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="ed0b2-171">View installed updates</span></span>
