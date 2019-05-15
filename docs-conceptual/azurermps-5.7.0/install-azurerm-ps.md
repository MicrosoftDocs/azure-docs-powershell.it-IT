---
title: Installare Azure PowerShell in Windows con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: afa858975a38fe0e35c9e27667fbd1ac4c3300e9
ms.sourcegitcommit: b37b8bb6f8e39ecea5b50ceec48601eed313add7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/09/2019
ms.locfileid: "65511568"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a>Installare Azure PowerShell in Windows con PowerShellGet

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Questo articolo illustra l'installazione dei moduli di Azure PowerShell per PowerShell 5.x per Windows con PowerShellGet. PowerShellGet con la gestione dei moduli rappresenta la modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).

Il modello di distribuzione classica di Azure non è supportato da questa versione di Azure PowerShell. Per il supporto delle distribuzioni classiche, seguire le istruzioni in [Installare il modulo Gestione dei servizi di Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).

> [!IMPORTANT]
> Il modulo AzureRM non è supportato per macOS o Linux. Per usare i cmdlet di Azure PowerShell in queste piattaforme [installare il modulo Az](/powershell/azure/install-az-ps).

## <a name="requirements"></a>Requisiti

Per installare Azure PowerShell è necessario PowerShellGet versione 1.1.2.0 o superiore. Per verificare se è disponibile nel sistema, eseguire questo comando:

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

Verrà visualizzata una schermata simile all'output seguente:

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Se è necessario aggiornare l'installazione di PowerShellGet, eseguire questo comando:

```powershell-interactive
Install-Module PowerShellGet -Force
```

Se PowerShellGet non è installato, vedere le istruzioni nella tabella seguente per il proprio sistema.

|Scenario|Istruzioni di installazione|
|---|---|
|Windows 10<br/>Windows Server 2016|Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo|
|Eseguire l'aggiornamento a PowerShell 5| <ol><li>[Installare la versione più recente di WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li>Eseguire il comando seguente:<br/>```Install-Module PowerShellGet -Force```</li></ol>|
|Windows con PowerShell 3 o PowerShell 4|<ol><il>[Ottenere i moduli PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il><li>Eseguire il comando seguente:<br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script. Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).
>
> [!IMPORTANT]
> Il modulo illustrato in questo documento, AzureRM, usa .NET Framework. Non è quindi compatibile con PowerShell 6.0, che usa .NET Core. Se si usa PowerShell 6.0, seguire le [istruzioni di installazione per macOS e Linux](install-azurermps-maclinux.md).

## <a name="install-the-azure-powershell-module"></a>Installare il modulo Azure PowerShell

Sono necessari privilegi elevati per installare i moduli da PowerShell Gallery. Per installare Azure PowerShell, eseguire questo comando seguente in una sessione con privilegi elevati:

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.

Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet. La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

Rispondere `Yes` o `Yes to All` per continuare l'installazione.

Il modulo `AzureRM` è un modulo di rollup per i cmdlet di Azure PowerShell. Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.

## <a name="sign-in"></a>Accesso

Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata. L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).
Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).

## <a name="update-the-azure-powershell-module"></a>Aggiornare il modulo Azure PowerShell

È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module). Questo comando __non__ disinstalla le versioni precedenti.

```powershell-interactive
Update-Module -Name AzureRM
```

Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).

## <a name="use-multiple-versions-of-azure-powershell"></a>Usare più versioni di Azure PowerShell

È possibile installare più versioni di Azure PowerShell. Potrebbero essere necessarie più versioni se si usano risorse di Azure Stack locali, si esegue una versione precedente di Windows che non può essere aggiornata a PowerShell 5.0 oppure si usa il modello di distribuzione classica di Azure. Per installare una versione precedente, specificare l'argomento `-RequiredVersion` durante l'installazione.

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

Quando si carica il modulo Azure PowerShell, viene caricata la versione più recente per impostazione predefinita. Per caricare una versione diversa, specificare l'argomento `-RequiredVersion`.

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a>Fornire commenti e suggerimenti

Se si trova un bug quando si usa Azure Powershell, [registrare un problema su GitHub](https://github.com/Azure/azure-powershell/issues).
Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).

## <a name="next-steps"></a>Passaggi successivi

Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.
