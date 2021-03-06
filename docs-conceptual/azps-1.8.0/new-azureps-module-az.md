---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 02/12/2021
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: f6ffd66d20943541c3591d41db7c72861f44204c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415462"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduzione del nuovo modulo Az di Azure PowerShell

A partire da dicembre 2018, il modulo Az di Azure PowerShell è in disponibilità generale ed è ora il modulo di PowerShell previsto per l'interazione con Azure. Az offre comandi più brevi, maggiore stabilità e supporto multipiattaforma. Az ha anche parità delle funzionalità con AzureRM, assicurando un percorso di migrazione semplice.

Con il modulo Az, Azure PowerShell è ora compatibile con PowerShell 5.1 in Windows e PowerShell Core 6.x e versioni successive in tutte le piattaforme supportate, tra cui Windows, macOS e Linux.

Dato che Az è un nuovo modulo, la versione è stata reimpostata su 1.0.0.

## <a name="why-a-new-module"></a>Perché è stato creato un nuovo modulo?

Gli aggiornamenti principali possono risultare poco pratici, di conseguenza è importante informare gli utenti in merito ai motivi per cui si è deciso di introdurre un nuovo set di moduli, con nuovi cmdlet, per l'interazione con Azure da PowerShell.

La modifica principale e più importante è che in seguito all'introduzione di [PowerShell](/powershell/scripting/overview) basato sulla libreria .NET Standard, PowerShell è diventato un prodotto multipiattaforma.
Dal momento che è intenzione di Microsoft includere il supporto per Azure in tutte le piattaforme, era necessario aggiornare i moduli di Azure PowerShell in modo che potessero usare .NET Standard e fossero compatibili con PowerShell Core. Invece di usare il modulo AzureRM esistente e introdurre modifiche complesse per aggiungere questo supporto, è stato creato il modulo Az.

La creazione di un nuovo modulo ha inoltre offerto ai nostri sviluppatori l'opportunità di uniformare la progettazione e la denominazione di cmdlet e moduli. Ora i nomi di tutti i moduli iniziano con il prefisso `Az.` e i cmdlet usano tutti il formato _verbo_-`Az`_sostantivo_. In precedenza, i nomi dei cmdlet non solo erano più lunghi, ma risultavano incoerenti.

È stato inoltre ridotto il numero di moduli: alcuni moduli usati con gli stessi servizi sono stati raggruppati e ora i cmdlet del piano di gestione e del piano dati sono tutti contenuti in singoli moduli per i relativi servizi. Questo approccio semplifica le operazioni eseguite dagli utenti che gestiscono manualmente dipendenze e importazioni.

Apportando queste importanti modifiche che hanno richiesto la creazione di un nuovo modulo di Azure PowerShell, il team si è impegnato a rendere ancor più semplice usare Azure con i cmdlet di PowerShell e su un numero di piattaforme maggiore rispetto alle versioni precedenti.

## <a name="upgrade-to-az"></a>Eseguire l'aggiornamento ad Az

Per restare al passo con le funzionalità più recenti di Azure in PowerShell, è opportuno eseguire al più presto la migrazione al modulo Az. Se non si è pronti a installare il modulo Az in sostituzione di AzureRM, sono disponibili alcune opzioni per provare Az:

* Usare un ambiente `PowerShell` con [Azure Cloud Shell](/azure/cloud-shell/overview). Azure Cloud Shell è un ambiente di shell basato su browser che è disponibile quando si installa il modulo Az e si abilita gli alias per la compatibilità con `Enable-AzureRM`.
* Mantenere installato il modulo AzureRM con PowerShell 5.1 per Windows, ma installare il modulo Az per PowerShell Core 6.x o versioni successive. PowerShell 5.1 per Windows e PowerShell Core usano raccolte di moduli separate. Seguire le istruzioni per [installare PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) e quindi [installare il modulo Az](install-az-ps.md) da un terminale di PowerShell Core.

Per eseguire l'aggiornamento da un'installazione esistente di AzureRM:

1. [Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
2. [Installare il modulo Az di Azure PowerShell](install-az-ps.md).
3. **FACOLTATIVO**: Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per aggiungere gli alias per i cmdlet di AzureRM con [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias). Per maggiori dettagli, vedere la sezione successiva oppure [avviare la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-to-az"></a>Eseguire la migrazione degli script esistenti ad Az

I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare. Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`. Il precedente comando `New-AzureRMVm`, ad esempio, è diventato `New-AzVm`.
La migrazione, tuttavia, non implica solo acquisire familiarità con i nuovi nomi dei cmdlet: sono presenti altre importanti modifiche, tra cui moduli e parametri rinominati.

Per facilitare il processo di migrazione da AzureRM ad Az, sono disponibili numerose risorse:

* [Introduzione alla migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md)
* [Elenco completo delle modifiche di rilievo apportate durante la migrazione da AzureRM ad Az 1.0.0](migrate-az-1.0.0.md)
* Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

Il modulo Az offre una modalità compatibilità che consente di usare gli script esistenti mentre esegue l'aggiornamento alla nuova sintassi. Il cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) abilita una modalità compatibilità tramite alias, per consentire agli utenti di usare script esistenti con modifiche minime mentre si predispone una migrazione completa ad Az.

> [!IMPORTANT]
> Anche se sono stati creati alias per i nomi dei cmdlet, possono esistere comunque parametri nuovi o rinominati oppure valori restituiti modificati per i cmdlet di Az. Tenere presente che l'abilitazione degli alias non implica l'esecuzione automatica della migrazione. Per individuare le parti degli script che potrebbero richiedere aggiornamenti, vedere l'[elenco completo delle modifiche di rilievo](migrate-az-1.0.0.md).

## <a name="support-for-azurerm"></a>Supporto per AzureRM

Poiché i moduli AZ PowerShell ora hanno tutte le funzionalità dei moduli di AzureRM PowerShell e altro ancora, i moduli AzureRM PowerShell verranno ritirati il 29 febbraio 2024.

Per evitare interruzioni del servizio, [aggiornare gli script](https://aka.ms/azpsmigrate) che usano i moduli di PowerShell AzureRM per usare i moduli AZ PowerShell del 29 febbraio 2024. Per aggiornare automaticamente gli script, seguire la [Guida introduttiva](/powershell/azure/quickstart-migrate-azurerm-to-az-automatically).
