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
ms.date: 5/1/2018
ms.openlocfilehash: 8515a267e80e5d1f7bb97557efa72b9e86b7b45d
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

---

## <a name="600---may-2018"></a>6.0.0 - maggio 2018

### <a name="general"></a>Generale
* Impostazione della dipendenza minima dei moduli su PowerShell 5.0

### <a name="azurestorage"></a>Azure.Storage
* Supporto come nodo contenitori BLOB di Archiviazione
    - New-AzureStorageBlobContainer
    - Remove-AzureStorageBlobContainer
    - Set-AzureStorageBlobContent
    - Get-AzureStorageBlobContent
* Correzione del problema per cui l'output degli errori di alcuni cmdlet di Archiviazione non contiene informazioni dettagliate sugli errori

### <a name="azurermapimanagement"></a>AzureRM.ApiManagement
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermautomation"></a>AzureRM.Automation
* Rimozione dell'alias 'Tags' deprecato dai cmdlet
    - 'Set-AzureRmAutomationRunbook'

### <a name="azurermbatch"></a>AzureRM.Batch
* Aggiornamento delle documentazione di New-AzureBatchPool per rimuovere un esempio deprecato

### <a name="azurermcdn"></a>AzureRM.Cdn
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermcompute"></a>AzureRM.Compute
* 'New-AzureRmVm' e 'New-AzureRmVmss' supportano l'output dettagliato dei parametri
* 'New-AzureRmVm' e 'New-AzureRmVmss' (set di parametri semplice) supportano l'assegnazione di identità definite dall'utente e/o dal sistema alle macchine virtuali.
* Funzionalità Redeploy e PerformMaintenance di VMSS
    -  Aggiunta dei nuovi parametri di opzione -Redeploy e -PerformMaintenance a 'Set-AzureRmVmss' e 'Set-AzureRmVmssVM'
* Aggiunta del parametro di opzione DisableVMAgent al cmdlet 'Set-AzureRmVMOperatingSystem'
* 'New-AzureRmVm' e 'New-AzureRmVmss' (set di parametri semplice) supportano un'immagine 'Win10'.
* Aggiunta del cmdlet 'Repair-AzureRmVmssServiceFabricUpdateDomain'.
* Introduzione di numerose modifiche di rilievo
    - Per altri dettagli, vedere la guida alla migrazione
* Con 'Set-AzureRmVmDiskEncryptionExtension' i parametri di AAD diventano facoltativi

### <a name="azurermdatafactories"></a>AzureRM.DataFactories
* Rimozione dell'alias 'Tags' deprecato dai cmdlet
    - New-AzureRmDataFactory

### <a name="azurermdatafactoryv2"></a>AzureRM.DataFactoryV2
* Aggiornamento di ADF .Net SDK alla versione 0.7.0-preview contenente le modifiche seguenti:
    - Aggiunta dei parametri di esecuzione e della proprietà di gestione connessione nell'attività ExecuteSSISPackage
    - Aggiornamento di PostgreSql, servizio collegato di MySql, per l'uso della stringa di connessione completa invece di server, database, schema, nome utente e password
    - Rimozione dello schema dal servizio collegato DB2
    - Rimozione della proprietà dello schema dal servizio collegato Teradata
    - Aggiunta di LinkedService, Dataset, CopySource per Responsys

### <a name="azurermdatalakeanalytics"></a>AzureRM.DataLakeAnalytics
* Rimozione dell'alias 'Tags' deprecato dai cmdlet
    - 'New-AzureRmDataLakeAnalyticsAccount'
    - 'Set-AzureRmDataLakeAnalyticsAccount'

### <a name="azurermdatalakestore"></a>AzureRM.DataLakeStore
* Aggiunta della nuova funzionalità di modifica ACL ricorsiva a Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl
* Aggiunta del nuovo cmdlet per il recupero del riepilogo del contenuto in una directory
* Aggiunta del nuovo cmdlet per il recupero del dump AVL e dell'utilizzo del disco
* Correzione del tipo restituito di Set-AzureRmDataLakeStoreItemAcl bool in IEnumerable<DataLakeStoreItemAce>
* Correzione del tipo restituito di Set-AzureRmDataLakeStoreItemAclEntry bool in IEnumerable<DataLakeStoreItemAce>
* Modifiche di rilievo in Export-AzureRmDataLakeStoreItem, Import-AzureRmDataLakeStoreItem, Remove-AzureRmDataLakeStoreItem

### <a name="azurermdns"></a>AzureRM.Dns
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermeventhub"></a>AzureRM.EventHub
* Aggiornamento della Guida per i cmdlet con esempi mancanti

### <a name="azurerminsights"></a>AzureRM.Insights
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermiothub"></a>AzureRM.IotHub
* Abilitazione dei tag e dello SKU Basic nell'hub IoT

### <a name="azurermkeyvault"></a>AzureRM.KeyVault
* Modifiche di rilievo per supportare scenari di piping
* Aggiunta di nuovi cmdlet: Backup/Restore-AzureKeyVaultManagedStorageAccount, Backup/Restore-AzureKeyVaultCertificate, Undo-AzureKeyVaultManagedStorageSasDefinitionRemoval e Undo-AzureKeyVaultManagedStorageAccountRemoval

### <a name="azurermmachinelearning"></a>AzureRM.MachineLearning
* Rimozione dell'alias 'Tags' deprecato dai cmdlet
    - Update-AzureRmMlCommitmentPlan

### <a name="azurermmedia"></a>AzureRM.Media
* Rimozione dell'alias 'Tags' deprecato dai cmdlet
    - 'Set-AzureRmMediaService'

### <a name="azurermnetwork"></a>AzureRM.Network
* Aggiunta del supporto per la risorsa del piano di protezione DDoS
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermnotificationhubs"></a>AzureRM.NotificationHubs
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermoperationalinsights"></a>AzureRM.OperationalInsights
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermprofile"></a>AzureRM.Profile
* Abilitazione del salvataggio automatico del contesto per impostazione predefinita
* Aggiunta delle proprietà USGovernmentOperationalInsightsEndpoint e USGovernmentOperationalInsightsEndpointResourceId all'ambiente Azure per US Gov.

### <a name="azurermrecoveryservicessiterecovery"></a>AzureRM.RecoveryServices.SiteRecovery
* Correzione dell'intestazione di autenticazione in scenari SiteRecovery

### <a name="azurermrediscache"></a>AzureRM.RedisCache
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermresources"></a>AzureRM.Resources
* Rimozione del parametro obsoleto -AtScopeAndBelow dalla chiamata Get-AzureRmRoledefinition
* Inclusione delle assegnazioni a utenti/gruppi/entità servizio eliminati nel risultato di Get-AzureRmRoleAssignment
* Aggiunta dei completer di tabulazione per Scope e ResourceType
* Aggiunta di un cmdlet pratico per la creazione di entità servizio
* Unione della funzionalità di Get- e Find- in Get-AzureRmResource
* Aggiunta di cmdlet AD:
  - Remove-AzureRmADGroupMember
  - Get-AzureRmADGroup
  - New-AzureRmADGroup
  - Remove-AzureRmADGroup
  - Remove-AzureRmADUser
  - Update-AzureRmADApplication
  - Update-AzureRmADServicePrincipal
  - Update-AzureRmADUser

### <a name="azurermservicefabric"></a>AzureRM.ServiceFabric
* Aggiornamento dello SKU di versione predefinito dell'immagine Linux
  - Aggiornamento dello SKU UbuntuServer1604 predefinito di NewAzureServiceFabricCluster.cs

### <a name="azurermstorage"></a>AzureRM.Storage
* Introduzione di numerose modifiche di rilievo
    - Per altre informazioni, vedere la guida alla migrazione

### <a name="azurermwebsites"></a>AzureRM.Websites
* Aggiornamento alla versione più recente dell'SDK di Siti Web
* Aggiunta delle proprietà -AssignIdentity e -Httpsonly per Set-AzureRmWebApp e Set-AzureRmWebAppSlot
* Aggiunta di due nuovi cmdlet: Get-AzureRmWebAppSnapshots e Restore-AzureRmWebAppSnapshot
