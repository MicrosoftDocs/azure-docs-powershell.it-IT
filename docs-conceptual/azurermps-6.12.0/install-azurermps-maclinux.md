---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51576420"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installare Azure PowerShell in macOS o Linux

Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6. Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core. Per usare queste piattaforme è disponibile una versione .NET Standard di Azure PowerShell.

> [!NOTE]
> Attualmente, Azure PowerShell per .NET Standard è ancora in versione beta.
> Se si verificano problemi o si trovano bug, registrare un problema in GitHub.
>
> * [Problemi per Azure PowerShell](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a>Installare PowerShell Core

Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.
Per istruzioni dettagliate, vedere gli articoli seguenti.

* [Installare PowerShell Core in macOS](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [Installare PowerShell Core in Linux](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a>Installare Azure PowerShell per .NET Standard

> [!IMPORTANT]
> Il modulo `AzureRM` descritto nei dettagli in altri articoli non funziona con PowerShell Core.
> È necessario installare il modulo `Az` per ottenere la funzionalità di Azure PowerShell in PowerShell Core.

PowerShell Core viene fornito con il modulo PowerShellGet già installato. Avviare PowerShell con il comando:

```bash
pwsh
```

Per installare Azure PowerShell, eseguire questo comando:

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> Se si verifica un errore nelle autorizzazioni quando si prova a installare il modulo, potrebbe essere necessario eseguire PowerShell in modalità utente con privilegi avanzati per installare i moduli.
>
> ```bash
> sudo pwsh
> ```

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

## <a name="enable-aliases"></a>Abilitare gli alias

Per la compatibilità con il modulo `AzureRM` esistente, il nuovo modulo `Az` può creare alias compatibili con le versioni precedenti per i cmdlet `AzureRM`. Prima di usare il modulo per la prima volta, configurare questi alias con il comando seguente:

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

Gli alias vengono configurati solo per l'utente corrente. Vedere la Guida dei cmdlet per altri valori che possono essere forniti a `-Scope` per configurare gli alias.

> [!NOTE]
> Se si verifica un errore in un percorso, assicurarsi che esista nel sistema locale. Per l'ambito `CurrentUser`, questo errore può essere risolto eseguendo questo comando in `bash`:
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell è necessario caricare `Az` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure. L'importazione di un modulo __non__ richiede privilegi elevati.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `Az` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`. Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).
