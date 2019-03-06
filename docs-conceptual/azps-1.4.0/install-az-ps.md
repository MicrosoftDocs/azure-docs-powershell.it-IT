---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837572"
---
# <a name="install-the-azure-powershell-module"></a>Installare il modulo Azure PowerShell

Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet. Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux. Per il modulo Az non sono attualmente supportati altri metodi di installazione.

## <a name="requirements"></a>Requisiti

Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell 6 in qualsiasi piattaforma.
Per controllare la versione di PowerShell, eseguire il comando:

```powershell-interactive
$PSVersionTable.PSVersion
```

Se si ha una versione obsoleta o è necessario installare PowerShell, vedere [Installazione di varie versioni di PowerShell](/powershell/scripting/setup/installing-powershell). In tale pagina sono disponibili collegamenti a informazioni sull'installazione per la piattaforma in uso.

Se si usa PowerShell 5 in Windows, è necessario che sia installato anche .NET Framework 4.7.2. Per istruzioni su come aggiornare o installare una nuova versione di .NET Framework, vedere la [Guida all'installazione di .NET Framework](/dotnet/framework/install).

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

È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module). Questo comando __non__ disinstalla le versioni precedenti.

```powershell-interactive
Update-Module -Name Az
```

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
