---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: ae4540a90508db73335a54408dfd6cdf3712a1e9
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/18/2019
ms.locfileid: "59364104"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduzione del nuovo modulo Az di Azure PowerShell

A partire da dicembre 2018, il modulo Az di Azure PowerShell si trova nella versione di disponibilità generale ed è ora il modulo PowerShell desiderato per l'interazione con Azure. Az offre comandi più brevi, maggiore stabilità e supporto multipiattaforma. Az offre anche parità delle funzionalità e un facile percorso di migrazione da AzureRM.

Az usa la libreria .NET Standard e viene pertanto eseguito in PowerShell 5 e PowerShell 6.
Dato che PowerShell 6 può essere eseguito in Linux, macOS e Windows, Azure PowerShell è ora disponibile per tutte le piattaforme.
L'uso di .NET Standard consente di unificare la base di codice di Azure PowerShell con un impatto minimo sugli utenti.

Dato che Az è un nuovo modulo, la versione è stata reimpostata su 1.0.0.

## <a name="upgrade-to-az"></a>Eseguire l'aggiornamento ad Az

È consigliabile che tutti gli utenti eseguano l'aggiornamento al nuovo modulo Az. A tale scopo, procedere come segue:

* __CONSIGLIATO__: [Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
* [Installare il modulo Az di Azure PowerShell](/powershell/azure/install-az-ps).
* Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per aggiungere gli alias per i cmdlet di AzureRM con `Enable-AzureRMAlias`. Abilitare gli alias __solo__ se non è installato AzureRM.

## <a name="migrate-existing-scripts-to-az"></a>Eseguire la migrazione degli script esistenti ad Az

Gli aggiornamenti importanti possono essere impegnativi. Il modulo Az, tuttavia, offre una modalità compatibilità che consente di usare gli script esistenti mentre si completano gli aggiornamenti alla nuova sintassi. Usare il cmdlet `Enable-AzureRmAlias` per abilitare la modalità compatibilità per AzureRM. Questo cmdlet definisce i nomi dei cmdlet di AzureRM come alias dei nuovi nomi dei cmdlet di Az.

I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare. Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`. Il precedente comando `New-AzureRMVm`, ad esempio, è diventato `New-AzVm`.

Per una descrizione completa del processo di migrazione, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Futuro supporto per AzureRM

Il modulo AzureRM esistente non riceverà più i nuovi cmdlet o le nuove funzionalità. AzureRM, tuttavia, continuerà a essere ufficialmente supportato e a ricevere correzioni di bug fino a dicembre 2020. Per restare al passo con i servizi e le funzionalità più recenti di Azure, passare al modulo Az.
