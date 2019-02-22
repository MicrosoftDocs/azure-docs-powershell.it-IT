---
title: Panoramica di PowerShell per Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per Azure Stack con istruzioni per l'installazione e la configurazione.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: cd415e862bfaa2b767cce108689ebaf34ef74305
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144751"
---
# <a name="azurerm-module-230"></a><span data-ttu-id="67a93-103">Modulo AzureRM 2.3.0</span><span class="sxs-lookup"><span data-stu-id="67a93-103">AzureRM Module 2.3.0</span></span>

## <a name="requirements"></a><span data-ttu-id="67a93-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="67a93-104">Requirements:</span></span>
<span data-ttu-id="67a93-105">La versione minima supportata di Azure Stack è 1808.</span><span class="sxs-lookup"><span data-stu-id="67a93-105">Minimum supported Azure Stack version is 1808.</span></span>

<span data-ttu-id="67a93-106">Note: Se si usa una versione precedente, installare la versione 1.2.11</span><span class="sxs-lookup"><span data-stu-id="67a93-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="67a93-107">Installa</span><span class="sxs-lookup"><span data-stu-id="67a93-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="67a93-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="67a93-108">Release Notes</span></span>
* <span data-ttu-id="67a93-109">La versione 2.3.0 contiene un elenco di modifiche di rilievo.</span><span class="sxs-lookup"><span data-stu-id="67a93-109">The release 2.3.0 comes with a list of breaking changes.</span></span> <span data-ttu-id="67a93-110">Per eseguire l'aggiornamento dalla versione 1.2.11, è stata creata una Guida alla migrazione disponibile all'indirizzo https://aka.ms/azspowershellmigration</span><span class="sxs-lookup"><span data-stu-id="67a93-110">To upgrade from the 1.2.11 version, we have created a migration guide at https://aka.ms/azspowershellmigration</span></span>
* <span data-ttu-id="67a93-111">Questa versione corrisponde al profilo di API specifico di Azure Stack 2018-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="67a93-111">This release corresponds to the azurestack specific api profile 2018-03-01-hybrid</span></span>
* <span data-ttu-id="67a93-112">Tutti i moduli acquisiscono la dipendenza "maggiore di" o uguale a" per il modulo AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="67a93-112">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="67a93-113">È stata aggiornata la versione API supportata da ogni modulo.</span><span class="sxs-lookup"><span data-stu-id="67a93-113">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="67a93-114">Calcolo - 2017-03-30</span><span class="sxs-lookup"><span data-stu-id="67a93-114">Compute - 2017-03-30</span></span>
    * <span data-ttu-id="67a93-115">Rete - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="67a93-115">Network - 2017-10-01</span></span>
    * <span data-ttu-id="67a93-116">Archiviazione - 2016-01-01-01-01-01</span><span class="sxs-lookup"><span data-stu-id="67a93-116">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="67a93-117">Risorse - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="67a93-117">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="67a93-118">Key Vault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="67a93-118">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="67a93-119">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="67a93-119">Dns - 2016-04-01</span></span>
* <span data-ttu-id="67a93-120">La mappa completa delle versioni API per ogni tipo di risorsa è disponibile all'indirizzo https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="67a93-120">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="67a93-121">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="67a93-121">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="67a93-122">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="67a93-122">Azure Bridge</span></span>
<span data-ttu-id="67a93-123">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="67a93-123">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="67a93-124">Backup</span><span class="sxs-lookup"><span data-stu-id="67a93-124">Backup</span></span>
<span data-ttu-id="67a93-125">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="67a93-125">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="67a93-126">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="67a93-126">Configure where backups are stored</span></span>
- <span data-ttu-id="67a93-127">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="67a93-127">Perform backups</span></span>
- <span data-ttu-id="67a93-128">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="67a93-128">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="67a93-129">E-commerce</span><span class="sxs-lookup"><span data-stu-id="67a93-129">Commerce</span></span>
<span data-ttu-id="67a93-130">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="67a93-130">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="67a93-131">Calcolo</span><span class="sxs-lookup"><span data-stu-id="67a93-131">Compute</span></span>
<span data-ttu-id="67a93-132">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma, dischi gestiti ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="67a93-132">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="67a93-133">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="67a93-133">Fabric</span></span>
<span data-ttu-id="67a93-134">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="67a93-134">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="67a93-135">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="67a93-135">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="67a93-136">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="67a93-136">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="67a93-137">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="67a93-137">Repair of scale unit nodes</span></span>
- <span data-ttu-id="67a93-138">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="67a93-138">Restart of Infrastructure role</span></span>
- <span data-ttu-id="67a93-139">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="67a93-139">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="67a93-140">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="67a93-140">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="67a93-141">Gallery</span><span class="sxs-lookup"><span data-stu-id="67a93-141">Gallery</span></span>
<span data-ttu-id="67a93-142">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="67a93-142">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="67a93-143">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="67a93-143">Infrastructure Insights</span></span>
<span data-ttu-id="67a93-144">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="67a93-144">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="67a93-145">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="67a93-145">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="67a93-146">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="67a93-146">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="67a93-147">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="67a93-147">KeyVault</span></span>
<span data-ttu-id="67a93-148">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="67a93-148">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="67a93-149">Rete</span><span class="sxs-lookup"><span data-stu-id="67a93-149">Network</span></span>
<span data-ttu-id="67a93-150">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="67a93-150">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="67a93-151">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="67a93-151">Management of network quotas</span></span>
- <span data-ttu-id="67a93-152">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="67a93-152">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="67a93-153">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="67a93-153">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="67a93-154">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="67a93-154">Storage</span></span>
<span data-ttu-id="67a93-155">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="67a93-155">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="67a93-156">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="67a93-156">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="67a93-157">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="67a93-157">Manage storage quotas</span></span>
- <span data-ttu-id="67a93-158">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="67a93-158">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="67a93-159">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="67a93-159">Restore deleted storage accounts</span></span>
- <span data-ttu-id="67a93-160">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="67a93-160">Migrate containers from one share to another</span></span>
- <span data-ttu-id="67a93-161">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="67a93-161">View information about the individual storage components</span></span>
- <span data-ttu-id="67a93-162">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="67a93-162">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="67a93-163">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="67a93-163">Subscription Admin</span></span>
<span data-ttu-id="67a93-164">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="67a93-164">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="67a93-165">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="67a93-165">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="67a93-166">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="67a93-166">Manage plans and offers</span></span>
- <span data-ttu-id="67a93-167">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="67a93-167">View usage and performance information</span></span>
- <span data-ttu-id="67a93-168">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="67a93-168">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="67a93-169">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="67a93-169">Subscription</span></span>
<span data-ttu-id="67a93-170">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="67a93-170">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="67a93-171">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="67a93-171">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="67a93-172">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="67a93-172">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="67a93-173">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="67a93-173">Update</span></span>
<span data-ttu-id="67a93-174">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="67a93-174">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="67a93-175">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="67a93-175">In this module administrators can:</span></span>
- <span data-ttu-id="67a93-176">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="67a93-176">List and install available updates</span></span>
- <span data-ttu-id="67a93-177">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="67a93-177">Resume interrupted updates</span></span>
- <span data-ttu-id="67a93-178">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="67a93-178">View installed updates</span></span>
