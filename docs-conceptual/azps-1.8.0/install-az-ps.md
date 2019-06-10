---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365734"
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

> [!IMPORTANT]
>
> I moduli AzureRM e Az possono essere installati contemporaneamente. Se sono installati entrambi i moduli, __non abilitare gli alias__.
> L'abilitazione degli alias causerà conflitti tra i cmdlet di AzureRM e gli alias dei comandi di Az e potrebbe determinare comportamenti imprevisti.
> È consigliabile disinstallare AzureRM prima di installare il modulo Az. È sempre possibile disinstallare AzureRM o abilitare gli alias in qualsiasi momento. Per altre informazioni sugli alias dei comandi di AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).
> Per istruzioni sulla disinstallazione, vedere [Disinstallare il modulo AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module). 

Per installare i moduli in un ambito globale, sono necessari privilegi elevati per l'installazione di moduli da PowerShell Gallery. Per installare Azure PowerShell, eseguire questo comando in una sessione con privilegi elevati ("Esegui come amministratore" in Windows o con diritti di utente con privilegi avanzati in macOS o Linux):

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

Se non si ha accesso a privilegi di amministratore, è possibile eseguire l'installazione per l'utente corrente aggiungendo l'argomento `-Scope`.

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
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

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`. L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aggiornare il modulo Azure PowerShell

In considerazione della modalità di creazione del pacchetto del modulo Az, il comando [Update-Module](/powershell/module/powershellget/update-module) non consente di aggiornare correttamente l'installazione. AZ è tecnicamente un metamodulo e comprende tutti i moduli secondari contenenti i cmdlet per interagire con i servizi di Azure. Per aggiornare il modulo Azure PowerShell, è quindi necessario __reinstallarlo__, anziché semplicemente __aggiornarlo__. L'operazione è analoga all'installazione, ma può essere necessario aggiungere l'argomento `-Force`:

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
