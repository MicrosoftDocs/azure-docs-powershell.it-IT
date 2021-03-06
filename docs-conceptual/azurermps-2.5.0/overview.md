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
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244314"
---
# <a name="azurerm-module-250"></a>Modulo AzureRM 2.5.0

## <a name="requirements"></a>Requisiti:
La versione minima supportata di Azure Stack è la 1904.

Nota: se si usa una versione precedente, installare la versione 1.2.11


## <a name="install"></a>Installazione
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

## <a name="release-notes"></a>Note sulla versione
* AzureRm.Resources
    * Nuovo modulo Resources che supporta l'API versione 2018-05-01 con profilo 2019-03-01-hybrid
    * Le operazioni PolicyDefinition(2016-12-01) e PolicyAssignment(2017-06-01-preview) usano ancora le versioni precedenti dell'API
* AzureRm.Compute
    * Nuovo modulo Compute che supporta l'API versione 2017-12-01.'


* Questa versione corrisponde al profilo di API specifico di Azure Stack 2019-03-01-hybrid
* Tutti i moduli acquisiscono la dipendenza "maggiore di" o uguale a" per il modulo AzureRm.Profile.
* È stata aggiornata la versione API supportata da ogni modulo. 
    * Calcolo - 2017-12-30
    * Rete - 2017-10-01
    * Archiviazione - 2016-01-01-01-01-01
    * Risorse - 2018-02-01
    * Key Vault - 2016-10-01
    * DNS - 2016-04-01
* La mappa completa delle versioni API per ogni tipo di risorsa è disponibile all'indirizzo https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json

## <a name="content"></a>Contenuto:
### <a name="azure-bridge"></a>Azure Bridge
Versione di anteprima del modulo amministratore AzureBridge di Azure Stack che consente di pubblicare immagini da Azure.

### <a name="backup"></a>Backup
Versione di anteprima del modulo amministratore di Backup che consente agli amministratori di:
- Configurare la posizione di archiviazione dei backup
- Eseguire backup
- Elencare e ripristinare i backup completati

### <a name="commerce"></a>Commercio
Versione di anteprima del modulo amministratore E-commerce di Azure Stack che consente di visualizzare l'aggregazione dell'utilizzo dei dati nel sistema Azure Stack.

### <a name="compute"></a>Calcolo
Versione di anteprima del modulo amministratore Calcolo di Azure Stack che fornisce le funzionalità per la gestione di quote di calcolo, immagini della piattaforma, dischi gestiti ed estensioni di macchine virtuali.

### <a name="fabric"></a>Infrastruttura
Versione di anteprima del modulo amministratore Infrastruttura di Azure Stack che consente agli amministratori di visualizzare e gestire i componenti dell'infrastruttura:
- Interruzione, avvio e arresto dei nodi di unità di scala
- Svuotamento e ripristino di nodi di unità di scala per attività correlate a FRU
- Ripristino dei nodi di unità di scala
- Riavvio del ruolo Infrastruttura
- Interruzione, avvio e arresto delle istanze del ruolo Infrastruttura
- Creare nuovi pool IP


### <a name="gallery"></a>Raccolta
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
