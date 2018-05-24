---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c821153db7fb2c337e936abbd8ebb8c848069415
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

## <a name="version-170"></a>Versione 1.7.0

* **Modifica comportamentale per i parametri -Force, -Confirm e $ConfirmPreference per tutti i cmdlet. Questa implementazione è in fase di modifica per allinearla alle linee guida di PowerShell. Per la maggior parte dei cmdlet, questo significa rimuovere il parametro Force e per ignorare la richiesta ShouldProcess, gli utenti dovranno includere il parametro‘-Confirm:$false’ negli script di PowerShell.** Queste modifiche permettono di risolvere i problemi seguenti:
  - Implementazione corretta della funzionalità -WhatIf, per permettere a un utente di determinare gli effetti di un cmdlet o uno script senza apportare alcuna modifica effettiva
  - Controllo sulle richieste tramite $ConfirmPreference a livello di sessione, in modo che l'utente riceva le richieste in base all'impatto di una potenziale modifica (come indicato nell'impostazione ConfirmImpact nel cmdlet)
  - Controllo specifico dei cmdlet sulle richieste di conferma tramite il parametro -Confirm
  - Uso coerente di ShouldContinue e del parametro -Force nei cmdlet, solo per le azioni che richiedono la generazione di richieste all'utente a causa della natura speciale delle modifiche, ad esempio riguardo all'eliminazione di file nascosti
  - Coerenza con altri cmdlet di PowerShell, in modo che la conoscenza degli script di PowerShell acquisita da altri cmdlet possa essere immediatamente applicata ai cmdlet di Azure PowerShell.

**Si noti che per *ignorare automaticamente tutte le richieste in tutti i casi*, i cmdlet di Azure PowerShell richiedono ora all'utente di fornire due parametri:**
```powershell
My-CmdletWithConfirmation –Confirm:$false -Force
```
* Calcolo di Azure
  - Set-AzureRmVMADDomainExtension
  - Get-AzureRmVMADDomainExtension
  - Parametro -Redeploy per Restart-AzureVM
  - Parametro -Validate per Move-AzureService, Move-AzureStorageAccount e Move-AzureVirtualNetwork
  - I parametri per nome e versione per i cmdlet di estensione sono facoltativi come nelle versioni precedenti.
  - New-AzureVM può ottenere un tipo di licenza dall'oggetto VM.
* Archiviazione di Azure
  - Modifica del parametro Tags in Tag e aggiunta dell'alias di parametro Tags
    + New-AzureRmStorageAccount
    + Set-AzureRmStorageAccount
* Azure Network
  - Aggiunta di un nuovo cmdlet per il peering di rete virtuale
* Cache Redis di Azure
  - Aggiunta di un nuovo cmdlet per Reset-AzureRmRedisCache
  - Aggiunta di un nuovo cmdlet per Export-AzureRmRedisCache
  - Aggiunta di un nuovo cmdlet per Import-AzureRmRedisCache
  - Modifica del cmdlet New-AzureRmRedisCache per includere una modifica del parametro per vNet
* Backup/ripristino del database SQL di Azure
  - Cmdlet per la funzionalità di backup con conservazione a lungo termine
  - Get-AzureRmSqlServerBackupLongTermRetentionVault
  - Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Set-AzureRmSqlServerBackupLongTermRetentionVault
  - Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy
  - Restore-AzureRmSqlDatabase supporta ora il ripristino temporizzato di un database eliminato
  - Restore-AzureRmSqlDatabase supporta ora il ripristino da un backup con conservazione a lungo termine
* Azure LogicApp
  - Aggiunta di cmdlet per gli account di integrazione di LogicApp.
  - Get-AzureRmIntegrationAccountAgreement
  - Get-AzureRmIntegrationAccountCallbackUrl
  - Get-AzureRmIntegrationAccountCertificate
  - Get-AzureRmIntegrationAccount
  - Get-AzureRmIntegrationAccountMap
  - Get-AzureRmIntegrationAccountPartner
  - Get-AzureRmIntegrationAccountSchema
  - New-AzureRmIntegrationAccountAgreement
  - New-AzureRmIntegrationAccountCertificate
  - New-AzureRmIntegrationAccount
  - New-AzureRmIntegrationAccountMap
  - New-AzureRmIntegrationAccountPartner
  - New-AzureRmIntegrationAccountSchema
  - Remove-AzureRmIntegrationAccountAgreement
  - Remove-AzureRmIntegrationAccountCertificate
  - Remove-AzureRmIntegrationAccount
  - Remove-AzureRmIntegrationAccountMap
  - Remove-AzureRmIntegrationAccountPartner
  - Remove-AzureRmIntegrationAccountSchema
  - Set-AzureRmIntegrationAccountAgreement
  - Set-AzureRmIntegrationAccountCertificate
  - Set-AzureRmIntegrationAccount
  - Set-AzureRmIntegrationAccountMap
  - Set-AzureRmIntegrationAccountPartner
  - Set-AzureRmIntegrationAccountSchema
* Archivio Azure Data Lake
  - Drastico miglioramento delle prestazioni di caricamento e download di file e cartelle.
  - Sono incluse una piccola modifica ai nomi di parametro per il download e l'aggiunta di due nuovi parametri per il caricamento:
    + NumThreads -> PerFileThreadCount, usato per indicare il numero di thread da usare in un singolo file
    + ConcurrentFileCount, usato per indicare il numero di file da caricare/scaricare in parallelo per il caricamento/download di cartelle.
  - Vengono ora designati i valori di threading predefiniti per offrire una migliore velocità effettiva complessiva per la maggior parte delle dimensioni di file. Se le prestazioni sono insufficienti, i valori indicati sopra possono essere modificati per soddisfare i requisiti.
* Azure Data Lake Analytics.
  - Get-AzureRMDataLakeAnalyticsDataSource restituisce ora tutte le origini dati quando viene chiamato senza argomenti.
  - Questa modifica comporta anche la rimozione del parametro del tipo di origine dati dal cmdlet.
  - Questa modifica produce la restituzione di un nuovo oggetto per l'operazione di elenco con le proprietà seguenti:
    + Type: tipo dell'origine dati
    + Name: nome dell'origine dati
    + IsDefault: impostato su true se si tratta dell'origine dati predefinita per l'account
  - Correzione di Get-AzureRMDataLakeAnalyticsJob per elencare determinati valori di offset di data e ora quando si filtra in base a submittedBefore e submittedAfter.
* App Web
  - Aggiunta del cmdlet Swap-AzureRmWebAppSlot per lo scambio normale e lo scambio con anteprima
  - Estensione del cmdlet Set-AzureRmWebAppSlot per supportare lo scambio automatico
* Gestione API di Azure
  - Correzione dei cmdlet di distribuzione di Gestione API di Azure per AzureChinaCloud.
  - Rimozione del cmdlet Set-AzureRmApiManagementTenantGitAccess, perché l'accesso a Git è abilitato per impostazione predefinita.
* Backup di Servizi di ripristino di Azure
  - Aggiunta del supporto per il carico di lavoro SQL di Azure
  - Aggiunta del supporto per il backup e il ripristino di VM di Azure crittografate
  - Backup-AzureRmRecoveryServicesBackupItem: aggiunta della funzionalità per il tempo di conservazione facoltativa per punti di ripristino
  - Minori correzioni di bug correlate ai filtri nei cmdlet Get-AzureRmRecoveryServicesBackupContainer e Get-AzureRmRecoveryServicesBackupItem
* Automazione di Azure
  - Aggiunta di Get-AzureRmAutomationHybridWorkerGroup
