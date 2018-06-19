---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323255"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installare Azure PowerShell in macOS o Linux

Per le piattaforme non Windows, è possibile eseguire Azure PowerShell con PowerShell Core v6. Invece della versione standard di Azure PowerShell basata su .NET Framework per Windows, questo prodotto è pensato per .NET Core e può essere eseguito in qualsiasi piattaforma che supporti il runtime .Net Core.

> [!NOTE]
> Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.
> Il supporto per questi prodotti è limitato. Se si verificano problemi o si trovano bug, registrare un problema in GitHub.
>
> * [Problemi per PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemi per Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a>Installare PowerShell Core v6

L'installazione di PowerShell Core v6 in Linux o macOS varia a seconda della distribuzione Linux e della versione del sistema operativo.
Per istruzioni dettagliate, vedere gli articoli seguenti.

- [Installare PowerShell Core in macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [Installare PowerShell Core in Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installare Azure PowerShell per .NET Core

PowerShell Core v6 viene fornito con il modulo PowerShellGet già installato. Ciò semplifica l'installazione di qualsiasi modulo pubblicato in PowerShell Gallery. Per installare Azure PowerShell, aprire una nuova sessione di PowerShell ed eseguire il comando seguente:

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a>Caricare il modulo AzureRM.Netcore

Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell. I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

Al termine dell'importazione, è possibile testare il modulo appena installato eseguendo un tentativo di accesso ad Azure con il comando seguente:

```powershell
Connect-AzureRmAccount
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
