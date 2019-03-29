---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 28122ca953d62b405f19effbbc680f2dc6202cca
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475377"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Eseguire la migrazione da AzureRM ad Az di Azure PowerShell

Il modulo Az offre parità delle funzionalità rispetto ad AzureRM, ma usa nomi di cmdlet più brevi e coerenti.
Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo. Per facilitare la transizione, Az offre strumenti che consentono di eseguire gli script esistenti con AzureRM. Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al nuovo modulo.

Per visualizzare l'elenco completo delle modifiche che causano un'interruzione tra AzureRM e Az, vedere [Guida alla migrazione per Az 1.0.0](migrate-az-1.0.0.md)

## <a name="check-for-installed-versions-of-azurerm"></a>Controllo delle versioni installate di AzureRM

Il modulo Az può essere installato insieme al modulo AzureRM, ma questo non è consigliato. Prima di eseguire i passaggi di migrazione, verificare quali versioni di AzureRM sono installate nel sistema. In questo modo è possibile assicurarsi che gli script siano già in esecuzione nella versione più recente e sapere se è possibile abilitare gli alias dei comandi senza disinstallare AzureRM.

Per controllare quale versione di AzureRM è stata installata, eseguire il comando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM

È il passaggio più importante. Eseguire gli script esistenti e verificarne il funzionamento con l'_ultima_ versione di AzureRM (__6.13.1__). Se gli script non funzionano, vedere la [guida alla migrazione per AzureRM](/powershell/azure/azurerm/migration-guide.6.0.0).

## <a name="install-the-azure-powershell-az-module"></a>Installare il modulo Az di Azure PowerShell

Il primo passaggio consiste nell'installare il modulo Az nella piattaforma. Quando si installa Az, è consigliabile disinstallare AzureRM. I passaggi riportati di seguito illustreranno come continuare a eseguire gli script esistenti e abilitare la compatibilità per i nomi dei cmdlet precedenti.

Per installare il modulo Az di Azure PowerShell, seguire questa procedura:

* __CONSIGLIATO__: [Disinstallare il modulo AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
  Assicurarsi di rimuovere _tutte_ le versioni installate di AzureRM, non solo quella più recente.
* [Installare il modulo Az](install-az-ps.md).

## <a name="a-namealiasesenable-azurerm-compatibility-aliases"></a><a name="aliases"/>Abilitare gli alias per la compatibilità di AzureRM 

> [!IMPORTANT]
>
> Abilitare la modalità di compatibilità solo se sono state disinstallate _tutte_ le versioni di AzureRM. L'abilitazione della modalità di compatibilità con i cmdlet di AzureRM ancora disponibili può causare comportamenti imprevisti. Ignorare questo passaggio se si è scelto di mantenere AzureRM installato, ma tenere presente che qualsiasi cmdlet di AzureRM userà i moduli precedenti e non chiamerà i cmdlet di Az.

Dopo la verifica del funzionamento degli script con l'ultima versione di AzureRM e la disinstallazione di AzureRM, il passaggio successivo consiste nell'abilitare la modalità compatibilità per il modulo Az. La compatibilità viene abilitata con questo comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Gli alias offrono la possibilità di usare i nomi dei cmdlet precedenti con il modulo Az installato. Gli alias vengono scritti nel profilo utente per l'ambito selezionato. Se non esistono profili utente, ne viene creato uno.

> [!WARNING]
>
> È possibile usare un valore di `-Scope` diverso per il comando, ma non è consigliabile. Dato che gli alias vengono scritti nel profilo utente per l'ambito selezionato, abilitarli per un ambito il più limitato possibile. L'abilitazione degli alias a livello di sistema potrebbe anche causare problemi per altri utenti nel cui ambito locale è installato AzureRM.

Dopo aver abilitato la modalità alias, eseguire di nuovo gli script per verificare che continuino a funzionare come previsto. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modificare i nomi dei cmdlet e le importazioni del modulo

In generale, i nomi del modulo e i cmdlet sono stati modificati sostituendo `AzureRM` e `Azure` con `Az`.
Il modulo `AzureRM.Compute`, ad esempio, è stato rinominato `Az.Compute`. `New-AzureRMVM` è diventato `New-AzVM` e `Get-AzureStorageBlob` è ora `Get-AzStorageBlob`.

È opportuno essere a conoscenza delle eccezioni a tale modifica dei nomi. Alcuni moduli sono stati rinominati o uniti in moduli esistenti senza che questo influenzi il suffisso dei relativi cmdlet, a parte la modifica di `AzureRM` o `Azure` in `Az`. Diversamente il suffisso del cmdlet completo è stato modificato per riflettere il nuovo nome del modulo.

| Modulo AzureRM | Modulo Az | Modifica del suffisso del cmdlet |
|----------------|-----------|------------------------|
| AzureRM.Profile | Az.Accounts | Sì |
| AzureRM.Insights | Az.Monitor | Sì |
| AzureRM.DataFactories | Az.DataFactory | Sì |
| AzureRM.DataFactoryV2 | Az.DataFactory | Sì |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices | No  |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices | No  |
| AzureRM.Tags | Az.Resources | No  |
| AzureRM.MachineLearningCompute | Az.MachineLearning | No  |
| AzureRM.UsageAggregates | Az.Billing | No  |
| AzureRM.Consumption | Az.Billing | No  |

## <a name="summary"></a>Summary

Seguendo questi passaggi è possibile aggiornare tutti gli script esistenti in modo da usare il nuovo modulo. In caso di domande o problemi con questi passaggi che hanno reso difficile la migrazione, lasciare un commento su questo articolo per consentire un miglioramento delle istruzioni.
