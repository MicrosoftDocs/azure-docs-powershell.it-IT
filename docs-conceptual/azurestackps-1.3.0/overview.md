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
ms.openlocfilehash: fb892daeafb1365ea62324392ac806cf9f3d39cf
ms.sourcegitcommit: f6f5e256143aa6c097de3e57e930d8badea49f30
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/18/2018
ms.locfileid: "49399944"
---
# <a name="azure-stack-module-130"></a><span data-ttu-id="ff241-103">Modulo di Azure Stack 1.3.0</span><span class="sxs-lookup"><span data-stu-id="ff241-103">Azure Stack Module 1.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="ff241-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="ff241-104">Requirements:</span></span>
<span data-ttu-id="ff241-105">La versione minima supportata di Azure Stack è 1804.</span><span class="sxs-lookup"><span data-stu-id="ff241-105">Minimum supported Azure Stack version is 1804.</span></span>

<span data-ttu-id="ff241-106">Nota: se si usa una versione precedente, installare la versione 1.2.11</span><span class="sxs-lookup"><span data-stu-id="ff241-106">Note: If you are using an earlier version install version 1.2.11</span></span>

## <a name="known-issues"></a><span data-ttu-id="ff241-107">Problemi noti:</span><span class="sxs-lookup"><span data-stu-id="ff241-107">Known issues:</span></span>

- <span data-ttu-id="ff241-108">Chiudi avviso richiede Azure Stack versione 1803</span><span class="sxs-lookup"><span data-stu-id="ff241-108">Close Alert requires Azure Stack version 1803</span></span>
- <span data-ttu-id="ff241-109">Alcuni cmdlet di Archiviazione richiedono Azure Stack versione 1804</span><span class="sxs-lookup"><span data-stu-id="ff241-109">Some Storage cmdlets do require Azure Stack version 1804</span></span>
- <span data-ttu-id="ff241-110">New-AzsOffer non consente la creazione di un'offerta con stato pubblico.</span><span class="sxs-lookup"><span data-stu-id="ff241-110">New-AzsOffer does not allow to create an offer with state public.</span></span> <span data-ttu-id="ff241-111">Il cmdlet Set-AzsOffer deve essere chiamato successivamente per modificare lo stato.</span><span class="sxs-lookup"><span data-stu-id="ff241-111">The Set-AzsOffer cmdlet needs to be called afterwards to change the state.</span></span>
- <span data-ttu-id="ff241-112">Non è possibile rimuovere un pool IP senza una ridistribuzione</span><span class="sxs-lookup"><span data-stu-id="ff241-112">An IP Pool cannot be removed without a redeployment</span></span>

## <a name="breaking-changes"></a><span data-ttu-id="ff241-113">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="ff241-113">Breaking Changes</span></span>
<span data-ttu-id="ff241-114">Tutte le modifiche che causano un'interruzione durante la migrazione da 1.2.11 sono documentate qui https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="ff241-114">All breaking changes migrating from 1.2.11 are documented here https://aka.ms/azspowershellmigration</span></span>

## <a name="install"></a><span data-ttu-id="ff241-115">Installa</span><span class="sxs-lookup"><span data-stu-id="ff241-115">Install</span></span>
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
## <a name="content"></a><span data-ttu-id="ff241-116">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="ff241-116">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="ff241-117">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="ff241-117">Azure Bridge</span></span>
<span data-ttu-id="ff241-118">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="ff241-118">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="ff241-119">Backup</span><span class="sxs-lookup"><span data-stu-id="ff241-119">Backup</span></span>
<span data-ttu-id="ff241-120">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ff241-120">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="ff241-121">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="ff241-121">Configure where backups are stored</span></span>
- <span data-ttu-id="ff241-122">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="ff241-122">Perform backups</span></span>
- <span data-ttu-id="ff241-123">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="ff241-123">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="ff241-124">E-commerce</span><span class="sxs-lookup"><span data-stu-id="ff241-124">Commerce</span></span>
<span data-ttu-id="ff241-125">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ff241-125">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="ff241-126">Calcolo</span><span class="sxs-lookup"><span data-stu-id="ff241-126">Compute</span></span>
<span data-ttu-id="ff241-127">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="ff241-127">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="ff241-128">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ff241-128">Fabric</span></span>
<span data-ttu-id="ff241-129">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="ff241-129">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="ff241-130">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="ff241-130">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="ff241-131">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="ff241-131">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="ff241-132">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="ff241-132">Repair of scale unit nodes</span></span>
- <span data-ttu-id="ff241-133">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ff241-133">Restart of Infrastructure role</span></span>
- <span data-ttu-id="ff241-134">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ff241-134">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="ff241-135">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="ff241-135">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="ff241-136">Gallery</span><span class="sxs-lookup"><span data-stu-id="ff241-136">Gallery</span></span>
<span data-ttu-id="ff241-137">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ff241-137">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="ff241-138">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="ff241-138">Infrastructure Insights</span></span>
<span data-ttu-id="ff241-139">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ff241-139">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="ff241-140">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="ff241-140">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="ff241-141">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="ff241-141">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="ff241-142">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="ff241-142">KeyVault</span></span>
<span data-ttu-id="ff241-143">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="ff241-143">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="ff241-144">Rete</span><span class="sxs-lookup"><span data-stu-id="ff241-144">Network</span></span>
<span data-ttu-id="ff241-145">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="ff241-145">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="ff241-146">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="ff241-146">Management of network quotas</span></span>
- <span data-ttu-id="ff241-147">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="ff241-147">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="ff241-148">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="ff241-148">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="ff241-149">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff241-149">Storage</span></span>
<span data-ttu-id="ff241-150">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ff241-150">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="ff241-151">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="ff241-151">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="ff241-152">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff241-152">Manage storage quotas</span></span>
- <span data-ttu-id="ff241-153">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="ff241-153">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="ff241-154">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="ff241-154">Restore deleted storage accounts</span></span>
- <span data-ttu-id="ff241-155">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="ff241-155">Migrate containers from one share to another</span></span>
- <span data-ttu-id="ff241-156">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="ff241-156">View information about the individual storage components</span></span>
- <span data-ttu-id="ff241-157">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="ff241-157">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="ff241-158">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ff241-158">Subscription Admin</span></span>
<span data-ttu-id="ff241-159">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ff241-159">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="ff241-160">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="ff241-160">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="ff241-161">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="ff241-161">Manage plans and offers</span></span>
- <span data-ttu-id="ff241-162">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="ff241-162">View usage and performance information</span></span>
- <span data-ttu-id="ff241-163">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="ff241-163">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="ff241-164">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="ff241-164">Subscription</span></span>
<span data-ttu-id="ff241-165">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ff241-165">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="ff241-166">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="ff241-166">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="ff241-167">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="ff241-167">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="ff241-168">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="ff241-168">Update</span></span>
<span data-ttu-id="ff241-169">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="ff241-169">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="ff241-170">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="ff241-170">In this module administrators can:</span></span>
- <span data-ttu-id="ff241-171">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="ff241-171">List and install available updates</span></span>
- <span data-ttu-id="ff241-172">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="ff241-172">Resume interrupted updates</span></span>
- <span data-ttu-id="ff241-173">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="ff241-173">View installed updates</span></span>
