---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: 66d755384e532d434811f3e6122dcba97d5c48b5
ms.sourcegitcommit: a321ef9d134c684fa24ababcbd898f86b00d9364
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "77477849"
---
# <a name="install-the-azure-powershell-module"></a>Installare il modulo Azure PowerShell

Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet. Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux. Per il modulo Az non sono attualmente supportati altri metodi di installazione.

## <a name="requirements"></a>Requisiti

Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell Core 6.x e versioni successive in qualsiasi piattaforma. Se non si è sicuri di avere PowerShell o se si usa macOS o Linux, [installare la versione più recente di PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).

Per controllare la versione di PowerShell, eseguire il comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Per eseguire Azure PowerShell in PowerShell 5.1 in Windows:

1. Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell). Se si usa Windows 10, PowerShell 5.1 è già installato.
2. Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).

Quando si usa PowerShell Core, non sono previsti requisiti aggiuntivi per Azure PowerShell.

## <a name="install-the-azure-powershell-module"></a>Installare il modulo Azure PowerShell

> [!WARNING]
> __Non è possibile__ installare contemporaneamente i moduli AzureRM e Az per PowerShell 5.1 per Windows. Se è necessario mantenere AzureRM nel sistema, installare il modulo Az per PowerShell Core 6.x o versioni successive. A questo scopo, [installare PowerShell Core 6.x or versioni successive](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows) e quindi seguire queste istruzioni in un terminale di PowerShell Core.

Il metodo consigliato consiste nell'eseguire l'installazione solo per l'utente attivo:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

Se si vuole eseguire l'installazione per tutti gli utenti di un sistema, sono necessari privilegi di amministratore. Da una sessione di PowerShell con privilegi elevati eseguita come amministratore oppure con il comando `sudo` in MacOS o Linux:

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell. Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.

## <a name="install-offline"></a>Eseguire l'installazione offline

In alcuni ambienti non è possibile connettersi a PowerShell Gallery. In questi casi è comunque possibile eseguire l'installazione offline usando uno dei metodi seguenti:

* Scaricare i moduli in un altro percorso e usarli come origine dell'installazione in rete. Questo processo può essere complicato, ma consente di memorizzare i moduli di PowerShell nella cache di un singolo server o condivisione file da distribuire con PowerShellGet in qualsiasi sistema disconnesso. Per informazioni su come configurare un repository locale ed eseguire l'installazione in sistemi disconnessi, vedere [Uso dei repository PowerShellGet locali](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Scaricare il file MSI di Azure PowerShell](install-az-ps-msi.md) in un computer connesso alla rete e quindi copiare il programma di installazione nei sistemi senza accesso a PowerShell Gallery. Tenere presente che il programma di installazione MSI funziona solo per PowerShell 5.1 in Windows.
* Salvare il modulo con [Save-Module](/powershell/module/PowershellGet/Save-Module) in una condivisione file oppure salvarlo in un'altra origine e copiarlo manualmente in altri computer:
  
  ```powershell-interactive
  Save-Module -Name Az -Path '\\someshare\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Risoluzione dei problemi

Ecco alcuni problemi comuni che possono verificarsi durante l'installazione del modulo Azure PowerShell. Se si verifica un problema non elencato in questo articolo, [segnalarlo in GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Il proxy blocca la connessione

Se `Install-Module` restituisce errori che indicano che PowerShell Gallery non è raggiungibile, è possibile che si sia protetti da un proxy. I requisiti per configurare un proxy a livello di sistema variano a seconda del sistema operativo e non vengono illustrati in dettaglio in questo articolo. Per conoscere le impostazioni del proxy e sapere come configurarlo per il sistema operativo corrente, contattare l'amministratore di sistema.

PowerShell stesso potrebbe non essere configurato per l'uso automatico di questo proxy. Con PowerShell 5.1 e versioni successive configurare il proxy per l'uso di una sessione di PowerShell con il comando seguente:

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Se le credenziali del sistema operativo sono configurate correttamente, le richieste di PowerShell verranno instradate tramite il proxy.
Per rendere persistente questa impostazione tra una sessione e l'altra, aggiungere il comando a un [profilo PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Per installare il pacchetto, il proxy deve consentire le connessioni HTTPS all'indirizzo seguente:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Se il caricamento automatico dei moduli è stato disabilitato, importare manualmente il modulo con `Import-Module Az`. L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aggiornare il modulo Azure PowerShell

Se in origine è stato usato Install-Module, è necessario usare [Update-Module](/powershell/module/powershellget/update-module) per ottenere l'ultima versione. Se in origine è stato usato il pacchetto MSI, è necessario scaricare e installare la nuova versione di MSI per eseguire l'aggiornamento. Se si verificano problemi durante l'aggiornamento usando il pacchetto di PowershellGet, è necessario procedere alla__reinstallazione__ invece che al semplice __aggiornamento__. L'operazione è analoga all'installazione, ma può essere necessario aggiungere l'argomento `-Force`:

```powershell
Install-Module -Name Az -AllowClobber -Force
```

Anche se questa operazione può comportare la sovrascrittura di moduli installati, è comunque possibile che nel sistema siano ancora presenti versioni meno recenti.
Per informazioni su come rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usare più versioni di Azure PowerShell

È possibile installare più versioni di Azure PowerShell. Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).

È possibile installare o caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion`:

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.

## <a name="provide-feedback"></a>Fornire commenti e suggerimenti

Se si trova un bug in Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).
Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).
Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).
