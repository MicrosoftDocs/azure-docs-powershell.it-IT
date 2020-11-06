---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490585"
---
# Modulo AzureRM. Insights
## Descrizione
In questo argomento vengono visualizzati gli argomenti della Guida relativi ai cmdlet Azure Insights.

## Cmdlet AzureRM. Insights
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Crea un'impostazione di scalabilità verticale.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Aggiunge o sostituisce una regola di avviso del log.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Crea un nuovo profilo del log attività. Questo profilo viene usato per archiviare il log delle attività in un account di archiviazione di Azure o in un flusso di lavoro in un hub di eventi di Azure nello stesso abbonamento. 

- Solo **account di archiviazione standard (account di** archiviazione Premium non supportato) è supportato. Potrebbe essere di tipo ARM o Classic. Se è stato eseguito l'accesso a un account di archiviazione, il costo di archiviazione del log attività viene addebitato alle normali tariffe di archiviazione standard. Per esportare il log delle attività può essere usato un solo profilo di log per abbonamento in modo consequenziale solo un account di archiviazione per abbonamento. 

- **Hub eventi** : per esportare il log delle attività può essere usato solo un profilo di log per ogni sottoscrizione in modo consequenziale solo un hub eventi per ogni abbonamento. Se il log attività viene trasmesso a un hub eventi, verrà applicato il prezzo standard dell'hub eventi. 

Nel registro attività gli eventi possono essere relativi a un'area geografica o "globale". Global significa essenzialmente che questi eventi sono agnostici della regione e sono indipendenti dall'area geografica, infatti la maggior parte degli eventi rientra in questa categoria. Se il profilo del log attività è impostato dal portale, aggiunge implicitamente "globale" insieme a qualsiasi altra area selezionata nell'interfaccia utente. Quando si usa il cmdlet, la posizione "globale" deve essere menzionata in modo esplicito, oltre a qualsiasi altra area geografica. 

**Nota** : se **non si imposta "globale" nelle posizioni, la maggior parte del log delle attività non viene esportata.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Aggiunge o aggiorna una regola di avviso basata su metriche.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Aggiunge o aggiorna una regola di avviso di WebTest.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Disabilita un avviso del log attività e ne imposta i contrassegni.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Abilita un avviso del log attività e ne imposta i contrassegni.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Ottiene i gruppi di azioni.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Ottiene una o più risorse di avviso del log attività.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Ottiene la cronologia degli avvisi.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Ottiene le regole di avviso.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Ottiene la cronologia di scalabilità verticale.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Ottiene le impostazioni di scalabilità orizzontale.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Ottiene le categorie registrate e i grani temporali.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Ottiene un log di eventi.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Ottiene un profilo di log.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Ottiene i valori metrici di una risorsa.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Ottiene le definizioni metriche.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Ottiene le metriche di utilizzo per una risorsa.

### [New-AzureRmActionGroup](New-AzureRmActionGroup.md)
Crea un oggetto di riferimento ActionGroup in memoria.

### [New-AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Crea un nuovo destinatario del gruppo di azioni.

### [New-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Crea un nuovo oggetto condizione di avviso del log attività in memoria.

### [New-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Crea un'azione di posta elettronica per una regola di avviso.

### [New-AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Crea una regola di avviso webhook.

### [New-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Crea una notifica tramite posta elettronica di scala.

### [New-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Crea un profilo di scalabilità verticale.

### [New-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Crea una regola di scalabilità verticale.

### [New-AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Crea un webhook di scalabilità verticale.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Rimuove un gruppo di azioni.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Rimuove un avviso del log attività.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Rimuove una regola di avviso.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Rimuove un'impostazione di scala.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Rimuove un profilo di log.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Crea un nuovo o aggiorna un gruppo di azioni esistente.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Crea un nuovo o imposta un avviso del log attività esistente.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Imposta le impostazioni dei registri e delle metriche per la risorsa.

