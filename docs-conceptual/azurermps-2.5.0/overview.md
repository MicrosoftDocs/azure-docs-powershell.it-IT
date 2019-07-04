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
ms.openlocfilehash: 55f19ac5e6767df1312e0b531184e8621b60a011
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038194"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="6b5a0-103">Modulo AzureRM 2.5.0</span><span class="sxs-lookup"><span data-stu-id="6b5a0-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="6b5a0-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-104">Requirements:</span></span>
<span data-ttu-id="6b5a0-105">La versione minima supportata di Azure Stack è la 1904.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="6b5a0-106">Note: Se si usa una versione precedente, installare la versione 1.2.11</span><span class="sxs-lookup"><span data-stu-id="6b5a0-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="6b5a0-107">Installa</span><span class="sxs-lookup"><span data-stu-id="6b5a0-107">Install</span></span>
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

## <a name="release-notes"></a><span data-ttu-id="6b5a0-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-108">Release Notes</span></span>
* <span data-ttu-id="6b5a0-109">AzureRm.Resources</span><span class="sxs-lookup"><span data-stu-id="6b5a0-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="6b5a0-110">Nuovo modulo Resources che supporta l'API versione 2018-05-01 con profilo 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="6b5a0-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="6b5a0-111">Le operazioni PolicyDefinition(2016-12-01) e PolicyAssignment(2017-06-01-preview) usano ancora le versioni precedenti dell'API</span><span class="sxs-lookup"><span data-stu-id="6b5a0-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="6b5a0-112">AzureRm.Compute</span><span class="sxs-lookup"><span data-stu-id="6b5a0-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="6b5a0-113">Nuovo modulo Compute che supporta l'API versione 2017-12-01.'</span><span class="sxs-lookup"><span data-stu-id="6b5a0-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="6b5a0-114">Questa versione corrisponde al profilo di API specifico di Azure Stack 2019-03-01-hybrid</span><span class="sxs-lookup"><span data-stu-id="6b5a0-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="6b5a0-115">Tutti i moduli acquisiscono la dipendenza "maggiore di" o uguale a" per il modulo AzureRm.Profile.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="6b5a0-116">È stata aggiornata la versione API supportata da ogni modulo.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="6b5a0-117">Calcolo - 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="6b5a0-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="6b5a0-118">Rete - 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="6b5a0-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="6b5a0-119">Archiviazione - 2016-01-01-01-01-01</span><span class="sxs-lookup"><span data-stu-id="6b5a0-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="6b5a0-120">Risorse - 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="6b5a0-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="6b5a0-121">Key Vault - 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="6b5a0-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="6b5a0-122">DNS - 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="6b5a0-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="6b5a0-123">La mappa completa delle versioni API per ogni tipo di risorsa è disponibile all'indirizzo https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span><span class="sxs-lookup"><span data-stu-id="6b5a0-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="6b5a0-124">Contenuto:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="6b5a0-125">Azure Bridge</span><span class="sxs-lookup"><span data-stu-id="6b5a0-125">Azure Bridge</span></span>
<span data-ttu-id="6b5a0-126">Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="6b5a0-127">Backup</span><span class="sxs-lookup"><span data-stu-id="6b5a0-127">Backup</span></span>
<span data-ttu-id="6b5a0-128">Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="6b5a0-129">Configurare la posizione di archiviazione dei backup</span><span class="sxs-lookup"><span data-stu-id="6b5a0-129">Configure where backups are stored</span></span>
- <span data-ttu-id="6b5a0-130">Eseguire backup</span><span class="sxs-lookup"><span data-stu-id="6b5a0-130">Perform backups</span></span>
- <span data-ttu-id="6b5a0-131">Elencare e ripristinare i backup completati</span><span class="sxs-lookup"><span data-stu-id="6b5a0-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="6b5a0-132">E-commerce</span><span class="sxs-lookup"><span data-stu-id="6b5a0-132">Commerce</span></span>
<span data-ttu-id="6b5a0-133">Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="6b5a0-134">Calcolo</span><span class="sxs-lookup"><span data-stu-id="6b5a0-134">Compute</span></span>
<span data-ttu-id="6b5a0-135">Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma, dischi gestiti ed estensioni di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="6b5a0-136">Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="6b5a0-136">Fabric</span></span>
<span data-ttu-id="6b5a0-137">Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="6b5a0-138">Interruzione, avvio e arresto dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="6b5a0-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="6b5a0-139">Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU</span><span class="sxs-lookup"><span data-stu-id="6b5a0-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="6b5a0-140">Ripristino dei nodi di unità di scala</span><span class="sxs-lookup"><span data-stu-id="6b5a0-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="6b5a0-141">Riavvio del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="6b5a0-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="6b5a0-142">Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura</span><span class="sxs-lookup"><span data-stu-id="6b5a0-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="6b5a0-143">Creare nuovi pool IP</span><span class="sxs-lookup"><span data-stu-id="6b5a0-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="6b5a0-144">Gallery</span><span class="sxs-lookup"><span data-stu-id="6b5a0-144">Gallery</span></span>
<span data-ttu-id="6b5a0-145">Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="6b5a0-146">Informazioni dettagliate sull'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="6b5a0-146">Infrastructure Insights</span></span>
<span data-ttu-id="6b5a0-147">Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="6b5a0-148">Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="6b5a0-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="6b5a0-149">Visualizzare e gestire gli avvisi</span><span class="sxs-lookup"><span data-stu-id="6b5a0-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="6b5a0-150">Insieme di credenziali delle chiavi</span><span class="sxs-lookup"><span data-stu-id="6b5a0-150">KeyVault</span></span>
<span data-ttu-id="6b5a0-151">Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="6b5a0-152">Rete</span><span class="sxs-lookup"><span data-stu-id="6b5a0-152">Network</span></span>
<span data-ttu-id="6b5a0-153">Versione di anteprima del modulo amministratore Rete che consente di:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="6b5a0-154">Gestione di quote di rete</span><span class="sxs-lookup"><span data-stu-id="6b5a0-154">Management of network quotas</span></span>
- <span data-ttu-id="6b5a0-155">Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="6b5a0-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="6b5a0-156">Fornisce un cmdlet che mostra una panoramica dell'amministratore</span><span class="sxs-lookup"><span data-stu-id="6b5a0-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="6b5a0-157">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-157">Storage</span></span>
<span data-ttu-id="6b5a0-158">Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="6b5a0-159">Questa versione include le funzionalità per:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="6b5a0-160">Gestire le quote di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-160">Manage storage quotas</span></span>
- <span data-ttu-id="6b5a0-161">Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate</span><span class="sxs-lookup"><span data-stu-id="6b5a0-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="6b5a0-162">Ripristinare gli account di archiviazione eliminati</span><span class="sxs-lookup"><span data-stu-id="6b5a0-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="6b5a0-163">Eseguire la migrazione di contenitori da una condivisione a un'altra</span><span class="sxs-lookup"><span data-stu-id="6b5a0-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="6b5a0-164">Visualizzare informazioni sui singoli componenti di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-164">View information about the individual storage components</span></span>
- <span data-ttu-id="6b5a0-165">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="6b5a0-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="6b5a0-166">Amministratore della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-166">Subscription Admin</span></span>
<span data-ttu-id="6b5a0-167">Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="6b5a0-168">Questo modulo consente agli amministratori di:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="6b5a0-169">Gestire i piani e le offerte</span><span class="sxs-lookup"><span data-stu-id="6b5a0-169">Manage plans and offers</span></span>
- <span data-ttu-id="6b5a0-170">Visualizzare informazioni sull'utilizzo e sulle prestazioni</span><span class="sxs-lookup"><span data-stu-id="6b5a0-170">View usage and performance information</span></span>
- <span data-ttu-id="6b5a0-171">Gestire il controllo degli accessi in base al ruolo</span><span class="sxs-lookup"><span data-stu-id="6b5a0-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="6b5a0-172">Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="6b5a0-172">Subscription</span></span>
<span data-ttu-id="6b5a0-173">Versione di anteprima del modulo Sottoscrizione di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="6b5a0-174">Questo modulo consente agli utenti di:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="6b5a0-175">Creare, eliminare e aggiornare le sottoscrizioni</span><span class="sxs-lookup"><span data-stu-id="6b5a0-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="6b5a0-176">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="6b5a0-176">Update</span></span>
<span data-ttu-id="6b5a0-177">Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="6b5a0-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="6b5a0-178">In questo modulo gli amministratori possono:</span><span class="sxs-lookup"><span data-stu-id="6b5a0-178">In this module administrators can:</span></span>
- <span data-ttu-id="6b5a0-179">Elencare e installare gli aggiornamenti disponibili</span><span class="sxs-lookup"><span data-stu-id="6b5a0-179">List and install available updates</span></span>
- <span data-ttu-id="6b5a0-180">Riprendere gli aggiornamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="6b5a0-180">Resume interrupted updates</span></span>
- <span data-ttu-id="6b5a0-181">Visualizzare gli aggiornamenti installati</span><span class="sxs-lookup"><span data-stu-id="6b5a0-181">View installed updates</span></span>
