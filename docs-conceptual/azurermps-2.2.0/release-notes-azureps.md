---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: ca25f3c66f8e8f4c64fc04275da2bd28e32d2f6c
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854614"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

## <a name="version-220"></a>Versione 2.2.0
* Calcolo
  - Aggiunta del supporto per l'esecuzione di query sullo stato di crittografia dall'estensione AzureDiskEncryptionForLinux
* DataFactory
  - Aggiunta di un nuovo cmdlet per elencare le finestre attività
    + Get-AzureRmDataFactoryActivityWindow
* DataLake
  - Modifica del parametro `Host` in `DatabaseHost` e aggiunta dell'alias a `Host`
    + New-AzureRmDataLakeAnalyticsCatalogSecret
    + Set-AzureRmDataLakeAnalyticsCatalogSecret
  - Aggiunta del supporto per la rimozione di ACL e ACL predefiniti
  - Aggiunta del supporto per ottenere e impostare autorizzazioni senza nome per file e cartelle
* Insieme di credenziali delle chiavi
  - Aggiunta del supporto per certificati
    + Add-AzureKeyVaultCertificate
    + Add-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificate
    + Get-AzureKeyVaultCertificateContact
    + Get-AzureKeyVaultCertificateIssuer
    + Get-AzureKeyVaultCertificateOperation
    + Get-AzureKeyVaultCertificatePolicy
    + Import-AzureKeyVaultCertificate
    + New-AzureKeyVaultCertificateAdministratorDetails
    + New-AzureKeyVaultCertificateOrganizationDetails
    + New-AzureKeyVaultCertificatePolicy
    + Remove-AzureKeyVaultCertificate
    + Remove-AzureKeyVaultCertificateContact
    + Remove-AzureKeyVaultCertificateIssuer
    + Remove-AzureKeyVaultCertificateOperation
    + Set-AzureKeyVaultCertificateAttribute
    + Set-AzureKeyVaultCertificateIssuer
    + Set-AzureKeyVaultCertificatePolicy
    + Stop-AzureKeyVaultCertificateOperation
* Rete

  - Aggiunta di un nuovo parametro opzionale per l'interfaccia di rete per abilitare/disabilitare la rete accelerata +New-AzureRmNetworkInterface -EnableAcceleratedNetworking
  - Abilitazione di cmdlet di PowerShell per la funzionalità del gateway attiva-attiva
    + Add-AzureRmVirtualNetworkGatewayIpConfig
    + Remove-AzureRmVirtualNetworkGatewayIpConfig
  - Aggiunta di un nuovo cmdlet
    + Test-AzureRmPrivateIpAddressAvailability
* Risorse
  - Supporto delle zone nei cmdlet di provider e risorse
    + Get-AzureRmProvider
    + New-AzureRmResource
    + Set-AzureRmResource
* Sql
  - Aggiunta di nuovi cmdlet per la gestione dei criteri di rilevamento delle minacce di SQL di Azure a livello di server
    + Get-AzureRmSqlServerThreatDetectionPolicy
    + Remove-AzureRmSqlServerThreatDetectionPolicy
    + Set-AzureRmSqlServerThreatDetectionPolicy
  - Aggiunta di nuovi cmdlet per supportare l'abilitazione/disabilitazione di GeoBackupPolicy per Azure SQL Data Warehouse
    + Get-AzureRmSqlDatabaseGeoBackupPolicy
    + Set-AzureRmSqlDatabaseGeoBackupPolicy
  - Aggiunta di nuovi cmdlet per Advisor SQL di Azure e API per azioni consigliate
    + Get-AzureRmSqlDatabaseAdvisor
    + Get-AzureRmSqlElasticPoolAdvisor
    + Get-AzureRmSqlServerAdvisor
    + Get-AzureRmSqlDatabaseRecommendedActions
    + Get-AzureRmSqlElasticPoolRecommendedActions
    + Get-AzureRmSqlServerRecommendedActions
    + Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus
    + Set-AzureRmSqlElasticPoolAdvisorAutoExecuteStatus
    + Set-AzureRmSqlServerAdvisorAutoExecuteStatus
    + Set-AzureRmSqlDatabaseRecommendedActionState
    + Set-AzureRmSqlElasticPoolRecommendedActionState
    + Set-AzureRmSqlServerRecommendedActionState
