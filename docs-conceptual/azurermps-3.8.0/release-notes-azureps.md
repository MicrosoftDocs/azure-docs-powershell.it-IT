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
ms.openlocfilehash: b777a5fe036cda58a930ac0f5aaef3b9a7c2b420
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853441"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

## <a name="version-380"></a>Versione 3.8.0
* Calcolo
  - Correzione di un bug nei cmdlet Get-*, per permettere il recupero di più pagine di dati (oltre 120 elementi)
* DataLakeAnalytics
  - Correzione della Guida per alcuni comandi in modo da includere il testo e gli esempi appropriati.
* DataLakeStore
  - Aggiunta del supporto per le parti iniziale e finale al cmdlet `Get-AzureRMDataLakeStoreItemContent`. In questo modo, è possibile restituire le prime e ultime N nuove righe delimitate da riga da visualizzare.
* HDInsight
  - Aggiunta del supporto per il tipo di cluster RServer
    + È possibile specificare le dimensioni delle VM Edgenode per un cluster RServer in New-AzureRmHDInsightCluster o New-AzureRmHDInsightClusterConfig
    + RServer è ora un'opzione di configurazione in Add-AzureRmHDInsightConfigValues. Permette l'impostazione del flag RStudio per indicare che è necessario eseguire l'installazione di R Studio.
* LogicApp
  - I cmdlet Set-AzureRmIntegrationAccountSchema e Set-AzureRmIntegrationAccountMap sono stati corretti per quanto riguarda il problema relativo a contentLink (impostazione simultanea di content e contentLink, che produce un errore di aggiornamento).
* Rete
  - Aggiunta del supporto per nuove funzionalità del firewall applicazione Web ai gateway applicazione
    + Aggiunta di New-AzureRmApplicationGatewayFirewallDisabledRuleGroupConfig
    + Aggiunta di Get-AzureRmApplicationGatewayAvailableWafRuleSets (alias: List-AzureRmApplicationGatewayAvailableWafRuleSets)
    + Aggiornamento di New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: aggiunta dei parametri -RuleSetType -RuleSetVersion e -DisabledRuleGroups
    + Aggiornamento di Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration: aggiunta dei parametri -RuleSetType -RuleSetVersion e -DisabledRuleGroups
  - Aggiunta del supporto per criteri IPSec a connessioni del gateway di rete virtuale
  - Aggiunta di New-AzureRmIpsecPolicy
  - Aggiornamento di New-AzureRmVirtualNetworkGatewayConnection: aggiunta dei parametri -IpsecPolicies e -UsePolicyBasedTrafficSelectors
* Profilo
  - *Obsoleto*: Save-AzureRmProfile è stato rinominato in Save-AzureRmContext. È disponibile un alias per il nome precedente del cmdlet, che verrà rimosso nella prossima versione.
  - *Obsoleto*: Select-AzureRmProfile è stato rinominato in Import-AzureRmContext. È disponibile un alias per il nome precedente del cmdlet, che verrà rimosso nella prossima versione.
  - I tipi di output PSAzureContext e PSAzureProfile dei cmdlet dei profili verranno modificati nella prossima versione.
  - Il cmdlet Save-AzureRmContext non includerà OutputType nella prossima versione.
  - Correzione di un bug nel codice comune dei cmdlet per usare l'algoritmo conforme a FIPS per hash di dati: https://github.com/Azure/azure-powershell/issues/3651
* Sql
  - Correzione di bug nei cmdlet del gruppo di failover di Azure
  - Correzione per il polling di operazioni
  - Correzione del valore GracePeriodWithDataLossHour quando si imposta FailoverPolicy su Manual
* TrafficManager
  - Supporto per il metodo di routing del traffico Geographic
    + Nuovo valore "Geographic" per il parametro TrafficRoutingMethod di New-AzureRmTrafficManagerProfile
    + Nuovo parametro "GeoMapping" per New-AzureRmTrafficManagerEndpoint e Add-AzureRmTrafficManagerEndpointConfig
    + Correzione dell'invio tramite pipe per Get-AzureRmTrafficManagerProfile quando restituisce una raccolta di profili
* ServiceManagement
  - Restart-AzureVM: aggiunta del parametro InitiateMaintenance per l'esecuzione di attività di manutenzione durante il riavvio della VM.
  - Get-AzureVM: aggiunta del campo per lo stato di manutenzione.
  - Aggiunta di nuovi cmdlet per supportare l'aggiornamento dell'insieme di credenziali di Servizi di ripristino
    + Test-AzureRecoveryServicesVaultUpgrade
    + Invoke-AzureRecoveryServicesVaultUpgrade
