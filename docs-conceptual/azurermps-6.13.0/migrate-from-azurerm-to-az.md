---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 720387ec1b23f10ddf2b153cf0705b2b6d1b7b82
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216195"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a>Eseguire la migrazione da AzureRM ad Az di Azure PowerShell

Il modulo Az offre parità delle funzionalità rispetto ad AzureRM, ma usa nomi di cmdlet più brevi e coerenti.
Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo. Per facilitare la transizione, Az offre strumenti che consentono di eseguire gli script esistenti con AzureRM. Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al nuovo modulo.

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a>Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM

È il passaggio più importante. Eseguire gli script esistenti e verificarne il funzionamento con l'_ultima_ versione di AzureRM (__6.13.0__). Se gli script non funzionano, vedere la [guida alla migrazione per AzureRM](migration-guide.6.0.0.md).

## <a name="install-the-azure-powershell-az-module"></a>Installare il modulo Az di Azure PowerShell

Il primo passaggio consiste nell'installare il modulo Az nella piattaforma. Per installare Az, è necessario disinstallare AzureRM.
I passaggi riportati di seguito illustreranno come continuare a eseguire gli script esistenti e abilitare la compatibilità per i nomi dei cmdlet precedenti.

Per installare il modulo Az di Azure PowerShell, seguire questa procedura:

* [Disinstallare il modulo AzureRM](uninstall-azurerm-ps.md). Assicurarsi di rimuovere _tutte_ le versioni installate di AzureRM, non solo quella più recente.
* [Installare il modulo Az](install-az-ps.md).

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><a name="aliases"/>Abilitare la modalità alias per AzureRM

Dopo la verifica del funzionamento degli script con l'ultima versione di AzureRM e la disinstallazione di AzureRM, è necessario abilitare la modalità compatibilità per il modulo Az. La compatibilità viene abilitata con questo comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Gli alias offrono la possibilità di usare i nomi dei cmdlet precedenti con il modulo `Az` installato. Gli alias vengono scritti nel profilo utente per l'ambito selezionato. Se non esistono profili utente, ne viene creato uno.

> [!WARNING]
>
> È possibile usare un valore di `-Scope` diverso per il comando, ma non è consigliabile. Dato che gli alias vengono scritti nel profilo utente per l'ambito selezionato, abilitarli per un ambito il più limitato possibile. L'abilitazione degli alias a livello di sistema potrebbe anche causare problemi per altri utenti nel cui ambito locale è installato `AzureRM`.

Dopo aver abilitato la modalità alias, eseguire di nuovo gli script per verificare che continuino a funzionare come previsto. 

## <a name="change-module-imports-and-cmdlet-names"></a>Modificare i nomi dei cmdlet e le importazioni del modulo

In generale, i nomi del modulo e i cmdlet sono stati modificati sostituendo `AzureRM` e `Azure` con `Az`.
Il modulo `AzureRM.Compute`, ad esempio, è stato rinominato `Az.Compute`. `New-AzureRmVM` è diventato `New-AzVM` e `Get-AzureStorageBlob` è ora `Get-AzStorageBlob`.

Prima di eseguire qualsiasi ridenominazione è opportuno essere a conoscenza delle eccezioni a tale modifica dei nomi:

| Modulo AzureRM | Modulo Az |
|----------------|-----------|
| AzureRM.DataFactories | Az.DataFactory |
| AzureRM.DataFactoryV2 | Az.DataFactory |
| AzureRM.RecoveryServices.Backup | Az.RecoveryServices |
| AzureRM.RecoveryServices.SiteRecovery | Az.RecoveryServices |

## <a name="summary"></a>Summary

Seguendo questi passaggi è possibile aggiornare tutti gli script esistenti in modo da usare il nuovo modulo. In caso di domande o problemi con questi passaggi che hanno reso difficile la migrazione, lasciare un commento su questo articolo per consentire un miglioramento delle istruzioni.
