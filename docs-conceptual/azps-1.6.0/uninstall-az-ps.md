---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 6a34ac1821c3cec359d0d64664d3f1689621b304
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475569"
---
# <a name="uninstall-the-azure-powershell-module"></a>Disinstallare il modulo Azure PowerShell

Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema. Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).
Se si rileva un bug, [creare un problema GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-the-az-module"></a>Disinstallare il modulo Az

Per disinstallare i moduli Az, usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Tuttavia `Uninstall-Module` disinstalla solo un modulo. Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente. Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.

Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti, quindi disinstalla la versione corretta di ogni modulo secondario. Per eseguire lo script in un ambito diverso da `Process` o `CurrentUser`, è necessario l'accesso come amministratore.

```powershell-interactive
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force,

    [switch]$WhatIf
  )
  
  $AllModules = @()
  
  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    if ($_.requiredVersion) {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall" -f $_.name,$version)
      }
    }
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}...' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop -WhatIf:$WhatIf
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell. L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato. Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare. Per praticità, lo script seguente disinstallerà tutte le versioni di Az __ad eccezione__ della più recente.

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a>Disinstallare il modulo AzureRM

Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, esistono due opzioni che non richiedono l'esecuzione dello script `Uninstall-AllModules` indicato sopra. Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.
Se non si è sicuri, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.

### <a name="uninstall-azure-powershell-msi"></a>Disinstallare l'identità del servizio gestita di Azure PowerShell

Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.

| Piattaforma | Istruzioni |
|----------|--------------|
| Windows 10 | Start > Impostazioni > App |
| Windows 7 </br>Windows 8 | Start > Pannello di controllo > Programmi > Disinstalla un programma |

L'elenco dei programmi visualizzato nella schermata mostrerà __Azure PowerShell__. Si tratta dell'app da disinstallare. Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.

### <a name="uninstall-from-powershell"></a>Eseguire la disinstallazione da PowerShell

Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il comando [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`. Questa operazione rimuove _tutti_ i moduli AzureRM dal computer, ma richiede i privilegi di amministratore.

```powershell-interactive
Uninstall-AzureRm
```

Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo script `Uninstall-AllModules` fornito in questo articolo.