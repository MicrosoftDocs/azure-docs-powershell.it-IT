---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 06/20/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 92af0fdd8db451e2f0f092d66a3e296ad8d6a09e
ms.sourcegitcommit: 8b882d1c27d9e323447ff85f56d11bbf5e244d7f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2018
ms.locfileid: "39110348"
---
# <a name="uninstall-the-azure-powershell-module"></a>Disinstallare il modulo Azure PowerShell

Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema. Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).
Se è stato rilevato un bug, [creare un problema di GitHub](https://github.com/azure/azure-powershell/issues).

## <a name="uninstall-msi"></a>Disinstallare il pacchetto MSI

Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.

| Piattaforma | Istruzioni |
|----------|--------------|
| Windows 10 | Start > Impostazioni > App |
| Windows 7 </br>Windows 8 | Start > Pannello di controllo > Programmi > Disinstalla un programma |

L'elenco dei programmi visualizzato nella schermata mostrerà "Azure PowerShell". È possibile eseguire la disinstallazione da qui.

## <a name="uninstall-from-powershell"></a>Eseguire la disinstallazione da PowerShell

Se Azure PowerShell è stato installato con PowerShellGet, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Tuttavia `Uninstall-Module` disinstalla solo un modulo. Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente. La disinstallazione può essere complicata se sono installate più versioni di Azure PowerShell.

Lo script può essere usato per rimuovere completamente una singola versione di Azure PowerShell. Lo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti, quindi disinstalla la versione corretta di ogni modulo secondario.

```powershell
function Uninstall-AllModules {
  param(
    [Parameter(Mandatory=$true)]
    [string]$TargetModule,

    [Parameter(Mandatory=$true)]
    [string]$Version,

    [switch]$Force
  )

  $AllModules = @()

  'Creating list of dependencies...'
  $target = Find-Module $TargetModule -RequiredVersion $version
  $target.Dependencies | ForEach-Object {
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredversion}
  }
  $AllModules += New-Object -TypeName psobject -Property @{name=$TargetModule; version=$Version}

  foreach ($module in $AllModules) {
    Write-Host ('Uninstalling {0} version {1}' -f $module.name,$module.version)
    try {
      Uninstall-Module -Name $module.name -RequiredVersion $module.version -Force:$Force -ErrorAction Stop
    } catch {
      Write-Host ("`t" + $_.Exception.Message)
    }
  }
}
```

Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell. L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.
