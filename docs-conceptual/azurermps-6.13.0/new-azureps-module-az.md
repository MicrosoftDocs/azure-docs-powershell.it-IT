---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2018
ms.locfileid: "52828111"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a>Introduzione del nuovo modulo Az di Azure PowerShell

A partire da novembre 2018, il modulo `Az` di Azure PowerShell è disponibile in anteprima pubblica completa.
Az offre comandi più brevi e maggiore stabilità e supporta Windows, macOS e Linux. Az offre anche parità delle funzionalità e un facile percorso di migrazione da AzureRM.

Az usa la libreria .NET Standard e viene pertanto eseguito in PowerShell 5.x e PowerShell 6.x.
Dato che PowerShell 6.x può essere eseguito in Linux, macOS e Windows, Az è disponibile per tutte le piattaforme.
L'uso di .NET Standard consente di unificare la base di codice di Azure PowerShell con un impatto minimo sugli utenti.

Dato che Az è un nuovo modulo, la versione è stata reimpostata. La prima versione stabile sarà la 1.0, ma il modulo offre parità delle funzionalità rispetto ad AzureRM da novembre 2018.

## <a name="upgrade-to-az"></a>Eseguire l'aggiornamento ad Az

È consigliabile che gli utenti eseguano l'aggiornamento al nuovo modulo `Az`. A tale scopo, procedere come segue:

* [Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-azurerm-ps).
* [Installare il modulo Az di Azure PowerShell](/powershell/azure/install-az-ps).
* Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per AzureRM con `Enable-AzureRMAlias`.

## <a name="migrate-existing-scripts-to-az"></a>Eseguire la migrazione degli script esistenti ad Az

Gli aggiornamenti importanti possono essere impegnativi. Il modulo `Az`, tuttavia, offre una modalità compatibilità che consente di usare gli script esistenti mentre si completano gli aggiornamenti alla nuova sintassi. Usare il cmdlet `Enable-AzureRmAlias` per abilitare la modalità compatibilità per `AzureRM`. Questo cmdlet definisce i nomi dei cmdlet di `AzureRM` come alias dei nuovi nomi dei cmdlet di `Az`.

I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare. Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`. Il precedente comando `New-AzureRmVm`, ad esempio, è diventato `New-AzVm`.

Per una descrizione completa del processo di migrazione, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

## <a name="the-future-of-support-for-azurerm"></a>Futuro supporto per AzureRM

Dopo il rilascio della versione 1.0 di `Az` nel mese di dicembre 2018, non verranno più resi disponibili nuovi cmdlet o funzionalità per il modulo `AzureRM` esistente. `AzureRM`, tuttavia, continuerà a essere ufficialmente supportato e a ricevere correzioni di bug. Per restare al passo con i servizi e le funzionalità più recenti di Azure, è consigliabile passare al modulo `Az`.