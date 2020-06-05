---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/22/2019
ms.openlocfilehash: b62fdd051b59708cc2afb6d4cec925aa73af55d9
ms.sourcegitcommit: 9f5c7d231b069ad501729bf015a829f3fe89bc6a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/28/2020
ms.locfileid: "84121354"
---
# <a name="install-azure-powershell"></a>Installare Azure PowerShell

Questo articolo illustra come installare i moduli di Azure PowerShell con [PowerShellGet](/powershell/scripting/gallery/installing-psget). Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.

Azure PowerShell è anche disponibile in Azure [Cloud Shell](/azure/cloud-shell/overview).

## <a name="requirements"></a>Requisiti

> [!NOTE]
> PowerShell 7.x e versioni successive è la versione consigliata di PowerShell per l'uso con Azure PowerShell in tutte le piattaforme.

Azure PowerShell funziona con PowerShell 6.2.4 e versioni successive in tutte le piattaforme. È supportato anche con PowerShell 5.1 in Windows. Installare la [versione più recente di PowerShell](/powershell/scripting/install/installing-powershell) disponibile per il sistema operativo in uso. Azure PowerShell non prevede requisiti aggiuntivi quando viene eseguito in PowerShell 6.2.4 e versioni successive.

Per controllare la versione di PowerShell, eseguire il comando:

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

Per usare Azure PowerShell in PowerShell 5.1 in Windows:

1. Eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).
   Se si usa Windows 10 versione 1607 o successiva, PowerShell 5.1 è già installato.
2. Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).
3. Assicurarsi di avere la versione più recente di PowerShellGet. Eseguire `Install-Module -Name PowerShellGet -Force`.

## <a name="install-the-azure-powershell-module"></a>Installare il modulo Azure PowerShell

> [!WARNING]
> L'installazione simultanea dei moduli AzureRM e Az per PowerShell 5.1 per Windows non è supportata. Se è necessario mantenere AzureRM nel sistema, installare il modulo Az per PowerShell Core 6.x o versioni successive.

Il metodo di installazione preferito prevede l'uso dei cmdlet PowerShellGet. Installare il modulo Az solo per l'utente corrente. Questo è l'ambito di installazione consigliato. Questo metodo è applicabile anche alle piattaforme Windows, macOS e Linux. Eseguire il comando seguente da una sessione di PowerShell:

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

Per installare il modulo per tutti gli utenti di un sistema, sono necessari privilegi elevati. Per avviare la sessione di PowerShell, usare **Esegui come amministratore** in Windows oppure il comando `sudo` in macOS o Linux:

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell. Con la sua installazione vengono scaricati tutti i moduli Az PowerShell disponibili a livello generale e vengono messi a disposizione i relativi cmdlet.

## <a name="install-offline"></a>Eseguire l'installazione offline

In alcuni ambienti non è possibile connettersi a PowerShell Gallery. In questi casi è comunque possibile eseguire l'installazione offline usando uno dei metodi seguenti:

* Scaricare i moduli in un altro percorso di rete e usare tale percorso come origine dell'installazione.
  Questo metodo consente di memorizzare i moduli di PowerShell nella cache di un singolo server o di una condivisione file da distribuire con PowerShellGet in qualsiasi sistema disconnesso. Per informazioni su come configurare un repository locale ed eseguire l'installazione in sistemi disconnessi, vedere [Uso dei repository PowerShellGet locali](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).
* [Scaricare il file MSI di Azure PowerShell](install-az-ps-msi.md) in un computer connesso alla rete e quindi copiare il programma di installazione nei sistemi senza accesso a PowerShell Gallery. Tenere presente che il programma di installazione MSI funziona solo per PowerShell 5.1 in Windows.
* Salvare il modulo con [Save-Module](/powershell/module/PowershellGet/Save-Module) in una condivisione file oppure salvarlo in un'altra origine e copiarlo manualmente in altri computer:

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a>Risoluzione dei problemi

Ecco alcuni problemi comuni che possono verificarsi durante l'installazione del modulo Azure PowerShell. Se si verifica un problema non elencato in questo articolo, [segnalarlo in GitHub](https://github.com/azure/azure-powershell/issues).

### <a name="proxy-blocks-connection"></a>Il proxy blocca la connessione

Se `Install-Module` restituisce errori che indicano che PowerShell Gallery non è raggiungibile, è possibile che si sia protetti da un proxy. I requisiti per configurare un proxy a livello di sistema variano a seconda del sistema operativo e dell'ambiente di rete. Per conoscere le impostazioni del proxy e sapere come configurarlo per l'ambiente corrente, contattare l'amministratore di sistema.

PowerShell stesso potrebbe non essere configurato per l'uso automatico di questo proxy. Con PowerShell 5.1 e versioni successive usare i comandi seguenti per configurare la sessione di PowerShell per l'uso di un proxy:

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

Se le credenziali del sistema operativo sono configurate correttamente, questa configurazione consentirà di reindirizzare le richieste di PowerShell tramite il proxy. Per rendere persistente questa impostazione tra una sessione e l'altra, aggiungere i comandi al proprio [profilo PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).

Per installare il pacchetto, il proxy deve consentire le connessioni HTTPS all'indirizzo seguente:

* `https://www.powershellgallery.com`

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> Se il caricamento automatico dei moduli è stato disabilitato, importare manualmente il modulo con `Import-Module -Name Az`.
> L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aggiornare il modulo Azure PowerShell

Per aggiornare qualsiasi modulo di PowerShell, è necessario usare lo stesso metodo adottato per installare il modulo. Se, ad esempio, in origine è stato usato `Install-Module`, è necessario usare [Update-Module](/powershell/module/powershellget/update-module) per scaricare l'ultima versione. Se in origine è stato usato il pacchetto MSI, è necessario scaricare e installare la nuova versione del pacchetto MSI.

I cmdlet PowerShellGet non possono aggiornare moduli installati da un pacchetto MSI. I pacchetti MSI non consentono di aggiornare moduli installati con PowerShellGet. Se si verificano problemi durante l'aggiornamento con PowershellGet, è necessario procedere alla**reinstallazione** invece che al semplice **aggiornamento**. La reinstallazione è un'operazione analoga all'installazione, ma richiede l'aggiunta del parametro `-Force`:

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

Diversamente dalle installazioni basate su MSI, l'installazione o l'aggiornamento con PowerShellGet non comporta la rimozione delle versioni precedenti che possono esistere nel sistema. Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md). Per altre informazioni sulle installazioni basate su MSI, vedere [Installare Azure PowerShell con un file MSI](install-az-ps-msi.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usare più versioni di Azure PowerShell

È possibile installare più versioni di Azure PowerShell. Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).

Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.

È possibile installare o caricare una versione specifica del modulo `Az` usando il parametro `-RequiredVersion`:

```powershell-interactive
# Install Az version 2.8.0
Install-Module -Name Az -RequiredVersion 2.8.0
# Load Az version 2.8.0
Import-Module -Name Az -RequiredVersion 2.8.0
```

## <a name="provide-feedback"></a>Fornire commenti e suggerimenti

Se si trova un bug in Azure PowerShell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues). Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).

## <a name="next-steps"></a>Passaggi successivi

Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md). Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).
