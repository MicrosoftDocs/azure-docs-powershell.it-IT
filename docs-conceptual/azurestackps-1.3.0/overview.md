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
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2018
ms.locfileid: "51211979"
---
# <a name="azure-stack-module-130"></a>Modulo di Azure Stack 1.3.0

## <a name="requirements"></a>Requirements:
La versione minima supportata di Azure Stack è 1804.

Nota: se si usa una versione precedente, installare la versione 1.2.11

## <a name="known-issues"></a>Problemi noti:

- Chiudi avviso richiede Azure Stack versione 1803
- Alcuni cmdlet di Archiviazione richiedono Azure Stack versione 1804
- New-AzsOffer non consente la creazione di un'offerta con stato pubblico. Il cmdlet Set-AzsOffer deve essere chiamato successivamente per modificare lo stato.
- Non è possibile rimuovere un pool IP senza una ridistribuzione

## <a name="breaking-changes"></a>Modifiche di rilievo
Tutte le modifiche che causano un'interruzione durante la migrazione da 1.2.11 sono documentate qui https://aka.ms/azspowershellmigration

## <a name="install"></a>Installa
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
## <a name="content"></a>Contenuto:
### <a name="azure-bridge"></a>Azure Bridge
Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.

### <a name="backup"></a>Backup
Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:
- Configurare la posizione di archiviazione dei backup
- Eseguire backup
- Elencare e ripristinare i backup completati

### <a name="commerce"></a>E-commerce
Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.

### <a name="compute"></a>Calcolo
Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma ed estensioni di macchine virtuali.

### <a name="fabric"></a>Infrastruttura
Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:
- Interruzione, avvio e arresto dei nodi di unità di scala
- Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU
- Ripristino dei nodi di unità di scala
- Riavvio del ruolo Infrastruttura
- Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura
- Creare nuovi pool IP


### <a name="gallery"></a>Gallery
Versione di anteprima del modulo amministratore Raccolta di Azure Stack che fornisce le funzionalità per la gestione degli elementi della raccolta in Azure Stack Marketplace.

### <a name="infrastructure-insights"></a>Informazioni dettagliate sull'infrastruttura
Versione di anteprima del modulo amministratore Informazioni dettagliate sull'infrastruttura che consente agli amministratori di:
- Visualizzare l'integrità delle rispettive risorse timbro di Azure Stack
- Visualizzare e gestire gli avvisi

### <a name="keyvault"></a>Insieme di credenziali delle chiavi
Versione di anteprima del modulo amministratore Insieme di credenziali delle chiavi di Azure Stack che consente agli amministratori di visualizzare le quote dell'insieme di credenziali delle chiavi.

### <a name="network"></a>Rete
Versione di anteprima del modulo amministratore Rete che consente di:
- Gestione di quote di rete
- Visualizzare le risorse di rete allocate, come indirizzi IP pubblici, reti virtuali e servizi di bilanciamento del carico
- Fornisce un cmdlet che mostra una panoramica dell'amministratore

### <a name="storage"></a>Archiviazione
Versione di anteprima del modulo amministratore Archiviazione di Azure Stack.  Questa versione include le funzionalità per:
- Gestire le quote di archiviazione
- Eseguire operazioni di Garbage Collection delle risorse di archiviazione eliminate
- Ripristinare gli account di archiviazione eliminati
- Eseguire la migrazione di contenitori da una condivisione a un'altra
- Visualizzare informazioni sui singoli componenti di archiviazione
- Visualizzare informazioni sull'utilizzo e sulle prestazioni

### <a name="subscription-admin"></a>Amministratore della sottoscrizione
Versione di anteprima del modulo Amministratore della sottoscrizione di Azure Stack.  Questo modulo consente agli amministratori di:
- Gestire i piani e le offerte
- Visualizzare informazioni sull'utilizzo e sulle prestazioni
- Gestire il controllo degli accessi in base al ruolo

### <a name="subscription"></a>Sottoscrizione
Versione di anteprima del modulo Sottoscrizione di Azure Stack.  Questo modulo consente agli utenti di:
- Creare, eliminare e aggiornare le sottoscrizioni

### <a name="update"></a>Aggiornamento
Versione di anteprima del modulo amministratore Aggiornamento di Azure Stack.  In questo modulo gli amministratori possono:
- Elencare e installare gli aggiornamenti disponibili
- Riprendere gli aggiornamenti interrotti
- Visualizzare gli aggiornamenti installati
