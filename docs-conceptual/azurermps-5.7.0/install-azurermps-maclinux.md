---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2018
ms.locfileid: "51210959"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installare Azure PowerShell in macOS o Linux

Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6. Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core. Per usare queste piattaforme è disponibile un'apposita versione .NET di Azure PowerShell.

> [!NOTE]
> Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.
> Il supporto per questi prodotti è limitato. Se si verificano problemi o si trovano bug, registrare un problema in GitHub.
>
> * [Problemi per PowerShell Core v6](https://github.com/PowerShell/PowerShell/issues)
> * [Problemi per Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installare PowerShell Core

Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.
Per istruzioni dettagliate, vedere gli articoli seguenti.

* [Installare PowerShell Core in macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installare PowerShell Core in Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a>Installare Azure PowerShell per .NET Core

PowerShell Core viene fornito con il modulo PowerShellGet già installato. L'installazione dei moduli in PowerShell richiede privilegi elevati, quindi è necessario avviare la sessione come utente con privilegi avanzati:

```bash
sudo pwsh
```

Per installare Azure PowerShell, eseguire questo comando:

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> Il modulo `AzureRM` descritto in altri articoli non è progettato per .NET Core e non funziona con PowerShell Core. `AzureRM` e `AzureRM.NetCore` usano gli stessi nomi cmdlet, quindi l'unica differenza è il nome del modulo di rollup e la versione .NET per la quale sono progettati.

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM.Netcore` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure. L'importazione di un modulo __non__ richiede privilegi elevati.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`. Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="available-cmdlets"></a>Cmdlet disponibili

I moduli di Azure PowerShell per .NET Core sono ancora in fase di sviluppo. Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli. Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:

* Gestione account
  * Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory
  * Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext
* Environment
  * Recupero di ambienti predefiniti di Microsoft Azure diversi
  * Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack
* Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.
  * Macchina virtuale
  * Servizio app (siti Web)
  * Database SQL
  * Archiviazione
  * Rete

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).
