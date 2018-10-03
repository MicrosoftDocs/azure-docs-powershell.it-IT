---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560117"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a>Installare Azure PowerShell in macOS o Linux

Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6. Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core. Per usare queste piattaforme è disponibile una versione .NET Standard di Azure PowerShell.

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

```powershell
Install-Module Az
```

> [!IMPORTANT]
> Il modulo `AzureRM` descritto in altri articoli non è progettato per .NET Core e non funziona con PowerShell Core. I moduli `Az` contengono gli alias dei comandi per tutti i cmdlet `AzureRM`, quindi è applicabile tutta la documentazione relativa a `AzureRM`.

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell è necessario caricare `Az` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure. L'importazione di un modulo __non__ richiede privilegi elevati.

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `Az` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`. Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).
