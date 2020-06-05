---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: cef87acc9f2a0d296bef74f526afd2e067e8146b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/02/2020
ms.locfileid: "84294743"
---
# <a name="uninstall-the-azure-powershell-module"></a>Disinstallare il modulo Azure PowerShell

Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema. Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback). Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.

## <a name="uninstall-azure-powershell-from-msi"></a>Disinstallare Azure PowerShell con il file MSI

Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.

|         Piattaforma         |                      Istruzioni                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Impostazioni > App                                |
| Windows 7 </br>Windows 8 | Start > Pannello di controllo -> Programmi -> Disinstalla un programma |

L'elenco dei programmi visualizzato nella schermata conterrà **Azure PowerShell**. Si tratta dell'app da disinstallare. Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.

## <a name="uninstall-azure-powershell-from-powershellget"></a>Disinstallare Azure PowerShell con PowerShellGet

Per disinstallare i moduli Az, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module). Tuttavia `Uninstall-Module` disinstalla solo un modulo. Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente. Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.

Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<a name="uninstall-script"/>

Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti, quindi disinstalla la versione corretta di ogni modulo secondario. Per eseguire lo script in un ambito diverso da **Process** o **CurrentUser**, è necessario l'accesso come amministratore.

```powershell-interactive
function Uninstall-AzModule {
  [CmdletBinding(SupportsShouldProcess)]
  param(
    [ValidateNotNullOrEmpty()]
    [ValidateSet('Az','AzureRM','Azure')]
    [string]$Name = 'Az',

    [Parameter(Mandatory)]
    [string]$Version,

    [switch]$AllowPrerelease
  )

  $Params = @{}

  if ($PSBoundParameters.AllowPrerelease) {
    $Params.AllowPrerelease = $true
  }

  $IsAdmin = ([Security.Principal.WindowsPrincipal] [Security.Principal.WindowsIdentity]::GetCurrent()).IsInRole([Security.Principal.WindowsBuiltInRole] 'Administrator')

  if (-not(Get-InstalledModule -Name $Name -RequiredVersion $Version -ErrorAction SilentlyContinue -OutVariable RootModule @Params)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version not found."

  } elseif (($RootModule.InstalledLocation -notlike "*$env:USERPROFILE*") -and ($IsAdmin -eq $false)) {

    Write-Warning -Message "Uninstall aborted. $Name version $Version exists in a system path. PowerShell must be run elevated as an admin to remove it."

  } elseif ((Get-Process -Name powershell, pwsh -OutVariable Sessions -ErrorAction SilentlyContinue).Count -gt 1) {

    Write-Warning -Message "Uninstall aborted. Please close all other PowerShell sessions before continuing. There are currently $($Sessions.Count) PowerShell sessions running."

  } else {
    Write-Verbose -Message 'Creating list of dependencies...'
    $target = Find-Module -Name $Name -RequiredVersion $Version @Params

    $AllModules = @([pscustomobject]@{
      Name = $Name
      Version = $Version
    })

    $AllModules += foreach ($dependency in $target.Dependencies) {
      switch ($dependency.keys) {
        {$_ -contains 'RequiredVersion'} {$UninstallVersion = $dependency.RequiredVersion; break}
        {$_ -contains 'MinimumVersion'} {$UninstallVersion = $dependency.MinimumVersion; break}
      }

      [pscustomobject]@{
        Name = $dependency.Name
        Version = $UninstallVersion
      }
    }

    [int]$i = 100 / $AllModules.Count

    foreach ($module in $AllModules) {
      Write-Progress -Activity 'Uninstallation in Progress' -Status "$i% Complete:" -PercentComplete $i
      $i++

      if (Get-InstalledModule -Name $module.Name -RequiredVersion $module.Version -ErrorAction SilentlyContinue @Params) {
        Write-Verbose -Message "Uninstalling $($module.Name) version $($module.Version)"

        Remove-Module -FullyQualifiedName @{ModuleName=$module.Name;ModuleVersion=$module.Version} -ErrorAction SilentlyContinue

        try {
          if ($PSCmdlet.ShouldProcess("$($module.Name) version $($module.Version)")) {
            Uninstall-Module -Name $module.Name -RequiredVersion $module.Version -Force -ErrorAction Stop @Params
          }
          $State = 'Uninstalled'
        } Catch {
          $State = 'Manual uninstall required'
          Write-Verbose -Message "$($module.Name) version: $($module.Version) may require manual uninstallation."
        }

      } else {
        $State = 'Not found'
        Write-Verbose -Message "$($module.Name) version: $($module.Version) not found."
      }

      if (-not $PSBoundParameters.WhatIf) {
        [pscustomobject]@{
          ModuleName = $module.Name
          Version = $module.Version
          State = $State
        }
      }

    }
  }
}
```

Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell. L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

Durante l'esecuzione, lo script visualizzerà il **nome**, la **versione** e lo **stato** di ogni modulo secondario disinstallato. Per eseguire lo script in modo da vedere soltanto gli elementi che verranno eliminati senza rimuoverli, specificare il parametro `-WhatIf`.

```output
ModuleName              Version  State
----------              -------  -----
Az.Accounts             1.5.1    Not found
Az.Aks                  1.0.1    Uninstalled
Az.AnalysisServices     1.1.0    Uninstalled
Az.ApiManagement        1.0.0    Uninstalled
Az.ApplicationInsights  1.0.0    Uninstalled
...
```

> [!IMPORTANT]
> Se questo script non trova una corrispondenza con una dipendenza esatta con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza. Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.

Eseguire l'esempio seguente per ogni versione di Azure PowerShell da disinstallare. Per praticità, lo script seguente disinstalla tutte le versioni di Az **ad eccezione** di quella più recente.

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a>Disinstallare il modulo AzureRM

Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, esistono due opzioni che non richiedono l'esecuzione dello script `Uninstall-AzModule` indicato sopra. Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM. Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.

### <a name="uninstall-azure-powershell-msi"></a>Disinstallare l'identità del servizio gestita di Azure PowerShell

Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.

|         Piattaforma         |                      Istruzioni                      |
| ------------------------ | ------------------------------------------------------ |
| Windows 10               | Start > Impostazioni > App                                |
| Windows 7 </br>Windows 8 | Start > Pannello di controllo -> Programmi -> Disinstalla un programma |

L'elenco di programmi visualizzato in questa schermata dovrebbe contenere **Azure PowerShell** o **Microsoft Azure PowerShell - Mese/anno**. Si tratta dell'app da disinstallare. Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.

### <a name="uninstall-from-powershell"></a>Eseguire la disinstallazione da PowerShell

Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`. L'esempio seguente rimuove _tutti_ i moduli AzureRM dal computer, ma richiede privilegi di amministratore.

```powershell-interactive
Uninstall-AzureRm
```

Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo [script`Uninstall-AzModule`](#uninstall-script) fornito in questo articolo con la chiamata seguente:

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
