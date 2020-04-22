---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/10/2019
ms.openlocfilehash: 02b39653ebb4aa0f74d2340a7be7b35e08d5e44d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740100"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Eseguire la migrazione di Azure PowerShell da AzureRM ad Az

Il modulo Az offre parità delle funzionalità rispetto ad AzureRM, ma usa nomi di cmdlet più brevi e coerenti.
Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo. Per facilitare la transizione, Az offre strumenti che consentono di eseguire gli script esistenti con AzureRM. Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al nuovo modulo.

Per visualizzare l'elenco completo delle modifiche di rilievo tra AzureRM e Az, vedere [Modifiche di rilievo della migrazione da AzureRM ad Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM

Prima di eseguire i passaggi di migrazione, verificare quali versioni di AzureRM sono installate nel sistema. In questo modo è possibile assicurarsi che gli script siano già in esecuzione nella versione più recente e sapere quali versioni di AzureRM devono essere disinstallate.

Per controllare quale versione di AzureRM è stata installata, eseguire il comando:

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

La versione __più recente__ disponibile di AzureRM è la __6.13.1__. Se questa versione non è installata, per poter usare gli script esistenti con il modulo Az, può essere necessario apportare ulteriori modifiche oltre a quelle descritte in questo articolo e nell'[elenco di modifiche di rilievo](migrate-az-1.0.0.md).

Se gli script non funzionano con AzureRM 6.13.1, aggiornarli in base alle indicazioni della [guida alla migrazione di AzureRM dalla versione 5.x alla versione 6.x](/powershell/azure/azurerm/migration-guide.6.0.0).
Se si usa una versione precedente del modulo AzureRM, sono disponibili guide alla migrazione per ogni versione principale.

## <a name="uninstall-azurerm"></a>Disinstallare AzureRM

Il modulo Az non è necessariamente compatibile con tutte le installazioni esistenti di AzureRM in PowerShell 5.1 per Windows. Prima di installare il modulo Az, [disinstallare AzureRM](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).

> [!IMPORTANT]
>
> Se non si è ancora pronti a rimuovere il modulo AzureRM dal sistema, è possibile disinstallare il modulo Az per [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) 6.x o versione successiva. PowerShell Core e PowerShell 5.1 per Windows usano librerie di moduli diverse, di conseguenza non si verificheranno conflitti. È comunque possibile [abilitare gli alias](#enable-azurerm-compatibility-aliases) in PowerShell Core.

## <a name="install-the-azure-powershell-az-module"></a>Installare il modulo Az di Azure PowerShell

Il primo passaggio consiste nell'installare il modulo Az nella piattaforma. Quando si installa Az, è consigliabile disinstallare AzureRM. I passaggi riportati di seguito illustreranno come continuare a eseguire gli script esistenti e abilitare la compatibilità per i nomi dei cmdlet precedenti.

Per installare il modulo Az di Azure PowerShell, seguire le istruzioni in [Installare il modulo Az](install-az-ps.md).

> [!NOTE]
> A questo punto è opportuno eseguire il cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) incluso nel modulo Az, per essere sicuri che tutte le versioni di AzureRM siano state disinstallate e non causino conflitti.

## <a name="enable-azurerm-compatibility-aliases"></a>Abilitare gli alias per la compatibilità di AzureRM

Dopo la verifica del funzionamento degli script con l'ultima versione di AzureRM e la disinstallazione di AzureRM, il passaggio successivo consiste nell'abilitare la modalità compatibilità per il modulo Az. La compatibilità viene abilitata con questo comando:

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

Gli alias offrono la possibilità di usare i nomi dei cmdlet precedenti con il modulo Az installato. Gli alias vengono scritti nel profilo per l'ambito selezionato. Se non esistono profili, ne viene creato uno.
Quando si usa un argomento `-Scope` con valore più ampio di `CurrentUser`, sono necessarie le autorizzazioni appropriate per creare o aggiornare il file di profilo corrispondente.

> [!IMPORTANT]
> Gli alias vengono creati __solo__ per i nomi di cmdlet e non per i nomi di modulo. Se si usano `#Requires`, `Import-Module`, elenchi di dipendenze in un file `.psd1` o nomi di cmdlet completi, assicurarsi di eseguire la migrazione in questo momento seguendo il processo descritto nell'[elenco delle modifiche di rilievo](migrate-az-1.0.0.md) relativo ai nomi di modulo.

> [!WARNING]
>
> È possibile usare un valore di `-Scope` diverso per il comando, ma non è consigliabile. Dato che gli alias vengono scritti nel profilo utente per l'ambito selezionato, abilitarli per un ambito il più limitato possibile. L'abilitazione degli alias a livello di sistema può causare problemi per altri utenti nel cui ambito locale è installato AzureRM.

Dopo aver abilitato la modalità alias, eseguire di nuovo gli script per verificare che continuino a funzionare come previsto.
Alcuni nomi di parametro sono stati modificati, aggiunti o resi obbligatori dal modulo Az. Anche i tipi di output dei cmdlet possono essere cambiati. Queste modifiche sono descritte in dettaglio nell'[elenco delle modifiche di rilievo](migrate-az-1.0.0.md).

## <a name="update-cmdlets-modules-and-parameters"></a>Aggiornare cmdlet, moduli e parametri

Se si usano script aggiornati e in esecuzione con alias, è possibile dedicare del tempo ad aggiornarli in modo da usare i nuovi cmdlet e sfruttare altre modifiche, come le nuove funzionalità. Per la maggior parte degli script è sufficiente aggiornare solo i nomi dei cmdlet, [seguendo lo schema di denominazione dei nuovi cmdlet in Az](migrate-az-1.0.0.md#cmdlet-noun-prefix-changes). Per garantire il funzionamento degli script, potrebbe essere necessario apportare altre modifiche a seconda del motivo per cui vengono usati e delle funzionalità di Azure PowerShell che sfruttano.

I [cmdlet di archiviazione BLOB](migrate-az-1.0.0.md#azstorage-previously-azurestorage-and-azurermstorage), ad esempio, sono stati completamente rielaborati e ora usano un nuovo modello asincrono, di conseguenza l'aggiornamento degli script in cui vengono usati richiederà più tempo rispetto all'aggiornamento degli script in cui le uniche modifiche di rilievo riguardavano i nomi dei cmdlet.

Anche se fino a questo punto sono state apportate solo modifiche semplici e di lieve entità agli script o se gli script funzionano senza ulteriori modifiche in seguito all'abilitazione degli alias, vedere l'[elenco completo delle modifiche di rilievo in Az 1.0.0](migrate-az-1.0.0.md) per assicurarsi di non fare affidamento sul comportamento trasparente degli alias che potrebbero scomparire dopo aver modificato i nomi dei cmdlet e aver disabilitato gli alias.

## <a name="disable-aliases"></a>Disabilitare gli alias

È consigliabile disabilitare gli alias dopo aver completato la migrazione, quando non è più necessario fare affidamento sul comportamento degli alias. Per eseguire questa operazione, usare il cmdlet [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).

> [!IMPORTANT]
> Quando si esegue questo cmdlet, __assicurarsi__ di chiamarlo per ogni argomento `-Scope` per cui è stato chiamato `Enable-AzureRmAlias`; in caso contrario, nel sistema potrebbero essere ancora presenti script che fanno affidamento sul comportamento degli alias.
