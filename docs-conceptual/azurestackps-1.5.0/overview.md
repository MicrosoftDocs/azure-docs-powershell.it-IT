---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: afa83a6258e57e961576b328e67fad634704dddf
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51580562"
---
# <a name="azure-stack-module-150"></a><span data-ttu-id="96089-103">Modulo di Azure Stack 1.5.0</span><span class="sxs-lookup"><span data-stu-id="96089-103">Azure Stack Module 1.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="96089-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="96089-104">Requirements:</span></span>
<span data-ttu-id="96089-105">La versione minima supportata di Azure Stack è 1808.</span><span class="sxs-lookup"><span data-stu-id="96089-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="96089-106">Nota: se si usa una versione precedente, installare la versione 1.4.0</span><span class="sxs-lookup"><span data-stu-id="96089-106">Note: If you are using an earlier version install version 1.4.0</span></span>

## <a name="known-issues"></a><span data-ttu-id="96089-107">Problemi noti:</span><span class="sxs-lookup"><span data-stu-id="96089-107">Known issues:</span></span>

- <span data-ttu-id="96089-108">New-AzsOffer non consente la creazione di un'offerta con stato pubblico.</span><span class="sxs-lookup"><span data-stu-id="96089-108">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="96089-109">Il cmdlet Set-AzsOffer deve essere chiamato successivamente per modificare lo stato.</span><span class="sxs-lookup"><span data-stu-id="96089-109">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="96089-110">Non è possibile rimuovere un pool IP senza una ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="96089-110">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="install"></a><span data-ttu-id="96089-111">Installa</span><span class="sxs-lookup"><span data-stu-id="96089-111">Install</span></span>
```
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force
Uninstall-Module AzureRM.AzureStackStorage -Force
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.5.0
```

## <a name="release-notes"></a><span data-ttu-id="96089-112">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="96089-112">Release Notes</span></span>
* <span data-ttu-id="96089-113">Tutti i moduli di amministrazione di Azure Stack sono stati aggiornati per la dipendenza "maggiore di" o "uguale a" nel modulo AzureRm.Profile</span><span class="sxs-lookup"><span data-stu-id="96089-113">All the Azure Stack Admin modules are updated for greater than or equal to dependency on the AzureRm.Profile module</span></span>
* <span data-ttu-id="96089-114">Supporto per la gestione di nomi di risorse annidati in tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="96089-114">Support for handling nested resource names in all the modules</span></span>
* <span data-ttu-id="96089-115">Correzione di bug in tutti i moduli in cui si esegue l'override di ErrorActionPreference affinché sia Stop</span><span class="sxs-lookup"><span data-stu-id="96089-115">Bug fix in all the modules where ErrorActionPreference is being overridden to be Stop</span></span>
* <span data-ttu-id="96089-116">Modulo Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="96089-116">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="96089-117">Aggiunta di nuove proprietà delle quote per il supporto del disco gestito</span><span class="sxs-lookup"><span data-stu-id="96089-117">New quota properties added for the support of manged disk</span></span>
    * <span data-ttu-id="96089-118">Aggiunta di cmdlet per la migrazione dei dischi</span><span class="sxs-lookup"><span data-stu-id="96089-118">Addition of disk migration related cmdlets</span></span>
    * <span data-ttu-id="96089-119">Proprietà aggiuntive negli oggetti di estensione delle immagini della piattaforma e delle VM</span><span class="sxs-lookup"><span data-stu-id="96089-119">Additional properties in the Platform Image and VM extesnion objects</span></span>
* <span data-ttu-id="96089-120">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="96089-120">Azs.Fabric.Admin</span></span> 
    * <span data-ttu-id="96089-121">Nuovo cmdlet per l'aggiunta di nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="96089-121">New cmdlet for adding scale unit node</span></span>
* <span data-ttu-id="96089-122">Azs.Backup.Admin</span><span class="sxs-lookup"><span data-stu-id="96089-122">Azs.Backup.Admin</span></span>
    * <span data-ttu-id="96089-123">Set-AzsBackupShare è ora un alias per il cmdlet Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="96089-123">Set-AzsBackupShare is an alias now to the cmdlet Set-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="96089-124">Get-AzsBackupLocation è ora un alias per il cmdlet Get-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="96089-124">Get-AzsBackupLocation is an alias now to the cmdlet Get-AzsBackupConfiguration</span></span>
    * <span data-ttu-id="96089-125">Set-AzsBackupConfiguration: il parametro BackupShare è ora un alias per il parametro path</span><span class="sxs-lookup"><span data-stu-id="96089-125">Set-AzsBackupConfiguration, the parameter BackupShare is an alias now for the parameter path</span></span>
* <span data-ttu-id="96089-126">Azs.Subscriptions</span><span class="sxs-lookup"><span data-stu-id="96089-126">Azs.Subscriptions</span></span>
    * <span data-ttu-id="96089-127">Get-AzsDelegatedProviderOffer: il parametro OfferName è ora un alias per Offer</span><span class="sxs-lookup"><span data-stu-id="96089-127">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>
* <span data-ttu-id="96089-128">Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="96089-128">Azs.Subscriptions.Admin</span></span>
    * <span data-ttu-id="96089-129">Get-AzsDelegatedProviderOffer: il parametro OfferName è ora un alias per Offer</span><span class="sxs-lookup"><span data-stu-id="96089-129">Get-AzsDelegatedProviderOffer, the parameter OfferName is now an alias for Offer</span></span>

## <a name="content"></a><span data-ttu-id="96089-130">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="96089-130">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="96089-131">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="96089-131">Azure Bridge</span></span>
<span data-ttu-id="96089-132">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="96089-132">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="96089-133">Backup</span><span class="sxs-lookup"><span data-stu-id="96089-133">Backup</span></span>
<span data-ttu-id="96089-134">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="96089-134">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="96089-135">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="96089-135">Configure where backups are stored</span></span>
- <span data-ttu-id="96089-136">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="96089-136">Perform backups</span></span>
- <span data-ttu-id="96089-137">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="96089-137">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="96089-138">E-commerce</span><span class="sxs-lookup"><span data-stu-id="96089-138">Commerce</span></span>
<span data-ttu-id="96089-139">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="96089-139">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="96089-140">Calcolo</span><span class="sxs-lookup"><span data-stu-id="96089-140">Compute</span></span>
<span data-ttu-id="96089-141">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma, dischi gestiti ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="96089-141">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="96089-142">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="96089-142">Fabric</span></span>
<span data-ttu-id="96089-143">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="96089-143">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="96089-144">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="96089-144">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="96089-145">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="96089-145">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="96089-146">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="96089-146">Repair of scale unit nodes</span></span>
- <span data-ttu-id="96089-147">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="96089-147">Restart of Infrastructure role</span></span>
- <span data-ttu-id="96089-148">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="96089-148">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="96089-149">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="96089-149">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="96089-150">Gallery</span><span class="sxs-lookup"><span data-stu-id="96089-150">Gallery</span></span>
<span data-ttu-id="96089-151">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="96089-151">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="96089-152">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="96089-152">Infrastructure Insights</span></span>
<span data-ttu-id="96089-153">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="96089-153">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="96089-154">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="96089-154">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="96089-155">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="96089-155">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="96089-156">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="96089-156">KeyVault</span></span>
<span data-ttu-id="96089-157">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="96089-157">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="96089-158">Rete</span><span class="sxs-lookup"><span data-stu-id="96089-158">Network</span></span>
<span data-ttu-id="96089-159">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="96089-159">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="96089-160">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="96089-160">Management of network quotas</span></span>
- <span data-ttu-id="96089-161">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="96089-161">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="96089-162">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="96089-162">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="96089-163">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="96089-163">Storage</span></span>
<span data-ttu-id="96089-164">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="96089-164">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="96089-165">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="96089-165">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="96089-166">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="96089-166">Manage storage quotas</span></span>
- <span data-ttu-id="96089-167">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="96089-167">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="96089-168">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="96089-168">Restore deleted storage accounts</span></span>
- <span data-ttu-id="96089-169">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="96089-169">Migrate containers from one share to another</span></span>
- <span data-ttu-id="96089-170">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="96089-170">View information about the individual storage components</span></span>
- <span data-ttu-id="96089-171">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="96089-171">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="96089-172">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="96089-172">Subscription Admin</span></span>
<span data-ttu-id="96089-173">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="96089-173">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="96089-174">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="96089-174">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="96089-175">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="96089-175">Manage plans and offers</span></span>
- <span data-ttu-id="96089-176">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="96089-176">View usage and performance information</span></span>
- <span data-ttu-id="96089-177">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="96089-177">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="96089-178">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="96089-178">Subscription</span></span>
<span data-ttu-id="96089-179">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="96089-179">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="96089-180">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="96089-180">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="96089-181">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="96089-181">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="96089-182">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="96089-182">Update</span></span>
<span data-ttu-id="96089-183">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="96089-183">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="96089-184">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="96089-184">In this module administrators can:</span></span>
- <span data-ttu-id="96089-185">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="96089-185">List and install available updates</span></span>
- <span data-ttu-id="96089-186">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="96089-186">Resume interrupted updates</span></span>
- <span data-ttu-id="96089-187">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="96089-187">View installed updates</span></span>
