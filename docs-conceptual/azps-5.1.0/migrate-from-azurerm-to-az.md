---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sulle procedure e sugli strumenti disponibili per la migrazione degli script di Azure PowerShell da AzureRM al nuovo modulo Az di PowerShell.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 12/1/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: bc37d0b73db0e6df226788795730730c077fcefa
ms.sourcegitcommit: cd243c8f6dc02dbd6234e764b065643dfd31dd8b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/02/2020
ms.locfileid: "96502590"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Eseguire la migrazione di Azure PowerShell da AzureRM ad Az

Tutte le versioni del modulo AzureRM PowerShell sono obsolete. Il [modulo Az PowerShell](install-az-ps.md) è ora il modulo di PowerShell consigliato per l'interazione con Azure.

## <a name="why-a-new-module"></a>Perché è stato creato un nuovo modulo?

La modifica principale e anche la più importante è che, essendo [PowerShell](/powershell/scripting/overview) basato sulla libreria .NET Standard, è un prodotto multipiattaforma sin dall'introduzione.

Come per il linguaggio PowerShell, Microsoft si impegna a includere il supporto di Azure in tutte le piattaforme. Questo impegno ha evidenziato l'esigenza di aggiornare i moduli di Azure PowerShell in modo che usino .NET Standard e siano compatibili con PowerShell Core. Invece di introdurre modifiche complesse nel modulo AzureRM esistente, per aggiungere questo supporto è stato creato il modulo Az.

La creazione di un nuovo modulo ha inoltre consentito ai nostri tecnici di uniformare la progettazione e la denominazione di cmdlet e moduli. Ora i nomi di tutti i moduli iniziano con il prefisso `Az.` e i cmdlet usano tutti la convenzione di denominazione `Verb-AzNoun`. In precedenza, i nomi dei cmdlet erano più lunghi e incoerenti.

È stato inoltre ridotto il numero di moduli: alcuni moduli usati con gli stessi servizi sono stati raggruppati e ora i cmdlet del piano di gestione e del piano dati per lo stesso servizio sono contenuti in un singolo modulo. Questo consolidamento semplifica di molto il lavoro di chi gestisce manualmente le dipendenze e le importazioni.

Apportando queste importanti modifiche, il team si è impegnato a rendere ancora più semplice l'uso di Azure con i cmdlet di PowerShell e con un numero di piattaforme maggiore rispetto alle versioni precedenti.

## <a name="upgrading-to-az-powershell"></a>Aggiornamento ad Az di PowerShell

Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con Az. Per semplificare la transizione, è stato sviluppato il [toolkit di migrazione da AzureRM ad Az](https://github.com/Azure/azure-powershell-migration). Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al modulo Az PowerShell. Per altre informazioni sui motivi per cui il modulo Az PowerShell è stato creato, vedere [Introduzione del nuovo modulo Az di Azure PowerShell](new-azureps-module-az.md).

I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare. Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`. Ad esempio, il vecchio cmdlet `New-AzureRMVm` è diventato `New-AzVm`.
La migrazione, tuttavia, non implica solo di acquisire familiarità con i nuovi nomi dei cmdlet: sono presenti altre importanti modifiche, tra cui moduli e parametri rinominati.

Per visualizzare l'elenco completo delle modifiche di rilievo tra AzureRM e Az, vedere [Modifiche di rilievo della migrazione da AzureRM ad Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM

Prima di eseguire i passaggi di migrazione, verificare quali versioni di AzureRM sono installate nel sistema.
In questo modo è possibile assicurarsi che gli script siano già in esecuzione nella versione più recente, oltre a identificare le versioni di AzureRM da disinstallare.

Per controllare quale versione di AzureRM è stata installata, eseguire questo esempio:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

La versione **più recente** disponibile di AzureRM è la **6.13.1**. Se questa versione non è installata, per poter usare gli script esistenti con il modulo Az, può essere necessario apportare altre modifiche che esulano dall'ambito di questo articolo e dell'[elenco di modifiche di rilievo](migrate-az-1.0.0.md).

Se gli script non funzionano con AzureRM 6.13.1, aggiornarli in base alle indicazioni della [guida alla migrazione di AzureRM dalla versione 5.x alla versione 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Se si usa una versione precedente del modulo AzureRM, sono disponibili guide alla migrazione per ogni versione principale.

## <a name="option-1-recommended-automatically-migrate-your-powershell-scripts"></a>Opzione 1 (scelta consigliata): Eseguire automaticamente la migrazione degli script di PowerShell

Questa opzione consigliata riduce al minimo gli interventi richiesti per la migrazione degli script di AzureRM ad Az.

### <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installare il toolkit di migrazione da AzureRM ad Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

### <a name="convert-your-scripts-automatically"></a>Convertire gli script automaticamente

Grazie al toolkit di migrazione da AzureRM ad Az, è possibile generare un piano per determinare quali modifiche verranno eseguite sugli script prima di apportare modifiche agli script e prima di installare il modulo Az PowerShell.

L'avvio rapido [Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) illustra in modo dettagliato l'intero processo di aggiornamento automatico degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.

## <a name="option-2-use-compatibility-mode-with-enable-azurermalias"></a>Opzione 2: Usare la modalità di compatibilità con Enable-AzureRmAlias

Il modulo Az offre una modalità compatibilità che consente di usare gli script esistenti mentre esegue l'aggiornamento alla nuova sintassi. Il cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) abilita una modalità di compatibilità tramite alias. Questa modalità consente di usare gli script esistenti con modifiche minime mentre si procede alla migrazione completa ad Az. Per impostazione predefinita, `Enable-AzureRmAlias` abilita solo gli alias di compatibilità per la sessione corrente di PowerShell. Usare il parametro `Scope` per salvare in modo permanente gli alias di compatibilità nelle sessioni di PowerShell. Per altre informazioni, vedere la [documentazione di riferimento di Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).

> [!IMPORTANT]
> Anche se sono stati creati alias per i nomi dei cmdlet, possono esistere comunque parametri nuovi o rinominati oppure valori restituiti modificati per i cmdlet di Az. Tenere presente che l'abilitazione degli alias non implica l'esecuzione automatica della migrazione. Per individuare le parti degli script che potrebbero richiedere aggiornamenti, vedere l'[elenco completo delle modifiche di rilievo](migrate-az-1.0.0.md).

## <a name="option-3-migrate-your-scripts-in-visual-studio-code-with-the-azure-powershell-extension"></a>Opzione 3: Eseguire la migrazione degli script in Visual Studio Code con l'estensione di Azure PowerShell

### <a name="install-the-azure-powershell-extension-for-visual-studio-code"></a>Installare l'estensione di Azure PowerShell per Visual Studio Code

Installare l'[estensione di Azure PowerShell per VSCode](https://marketplace.visualstudio.com/items?itemName=azps-tools.azps-tools)

### <a name="convert-your-scripts-manually"></a>Convertire gli script manualmente

1. Caricare lo script di AzureRM in VSCode
2. Avviare la migrazione aprendo il riquadro comandi `Ctrl+Shift+P`, quindi selezionare `Migrate Azure PowerShell script`
3. Selezionare la versione di origine `AzureRM`
4. Seguire le procedure consigliate per ogni comando o parametro sottolineato.

## <a name="next-steps"></a>Passaggi successivi

[Disinstallare AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
[Installare Azure PowerShell](install-az-ps.md)
