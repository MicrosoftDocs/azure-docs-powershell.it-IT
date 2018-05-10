---
title: Installare e configurare Azure PowerShell in macOS e Linux | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso in macOS e Linux.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 64a86dfd4af7f3f0a91501e9a096ff190f7100cb
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a>Installare e configurare Azure PowerShell in macOS e Linux

È ora possibile installare PowerShell Core v6 e Azure PowerShell in piattaforme non Windows.
Il processo di installazione di Azure PowerShell in macOS e Linux non è molto diverso da quello per Windows, ma è prima necessario installare PowerShell Core v6.

> [!NOTE]

> Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.
> Il supporto per questi prodotti è limitato. Se si verificano problemi o si trovano bug, registrare i problemi in GitHub.
>
> * [Problemi per PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemi per Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a>Passaggio 1: Installare PowerShell Core v6

Il processo di installazione di PowerShell Core v6 varia a seconda del sistema operativo di destinazione.
Nonostante sia possibile installare PowerShell Core v6 in Windows, questo articolo è incentrato su macOS e Linux. Se si intende usare Azure PowerShell in Windows, vedere l'articolo dedicato all'[installazione](./install-azurerm-ps.md) per Windows.

L'installazione di **PowerShell Core v6** in Linux o macOS varia a seconda della distribuzione Linux e della versione del sistema operativo.
Per istruzioni dettagliate, vedere l'articolo seguente:

- [Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux) (Installazione di PowerShell Core in macOS e Linux)

## <a name="step-2-install-azure-powershell-for-net-core"></a>Passaggio 2: installare Azure PowerShell per .NET Core

PowerShell Core v6 viene fornito con il modulo PowerShellGet già installato. Ciò semplifica l'installazione di qualsiasi modulo pubblicato in PowerShell Gallery. Per installare Azure PowerShell, aprire una nuova sessione di PowerShell ed eseguire il comando seguente:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a>Passaggio 3: caricare il modulo AzureRM.Netcore

Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell. I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Al termine dell'importazione, è possibile testare il modulo appena installato eseguendo un tentativo di accesso ad Azure con il comando seguente:

```powershell
Login-AzureRMAccount
```

Il comando riportato sopra richiede di passare a `https://aka.ms/devicelogin` e immettere il codice fornito.

## <a name="available-cmdlets"></a>Cmdlet disponibili

I moduli di Azure PowerShell per .NET Standard sono ancora in fase di sviluppo. Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli. Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:

* Gestione account
  - Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory
  - Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext
* Environment
  - Recupero di ambienti predefiniti di Microsoft Azure diversi
  - Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack
* Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.
  - Macchina virtuale
  - Servizio app (siti Web)
  - Database SQL
  - Archiviazione
  - Rete

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).
