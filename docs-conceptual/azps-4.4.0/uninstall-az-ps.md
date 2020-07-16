---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 4b40a3aebab84176a48bcdb0ef818cfa05dea269
ms.sourcegitcommit: 23e5b2b0751777ef0a5ca74e40c7772653e339a3
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/14/2020
ms.locfileid: "86382163"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="c94e2-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c94e2-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="c94e2-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c94e2-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="c94e2-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="c94e2-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="c94e2-106">Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.</span><span class="sxs-lookup"><span data-stu-id="c94e2-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="c94e2-107">Disinstallare Azure PowerShell con il file MSI</span><span class="sxs-lookup"><span data-stu-id="c94e2-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="c94e2-108">Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c94e2-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="c94e2-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="c94e2-109">Platform</span></span>         |                      <span data-ttu-id="c94e2-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c94e2-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="c94e2-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c94e2-111">Windows 10</span></span>               | <span data-ttu-id="c94e2-112">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="c94e2-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="c94e2-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c94e2-113">Windows 7</span></span> </br><span data-ttu-id="c94e2-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c94e2-114">Windows 8</span></span> | <span data-ttu-id="c94e2-115">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="c94e2-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c94e2-116">L'elenco dei programmi visualizzato nella schermata conterrà **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="c94e2-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="c94e2-117">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="c94e2-117">This is the app to uninstall.</span></span> <span data-ttu-id="c94e2-118">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="c94e2-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershellget"></a><span data-ttu-id="c94e2-119">Disinstallare Azure PowerShell con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="c94e2-119">Uninstall Azure PowerShell from PowerShellGet</span></span>

<span data-ttu-id="c94e2-120">Per disinstallare i moduli Az, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="c94e2-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="c94e2-121">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="c94e2-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="c94e2-122">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="c94e2-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="c94e2-123">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="c94e2-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="c94e2-124">Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="c94e2-124">To check which versions of Azure PowerShell you've installed, run the following command:</span></span>

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

<span data-ttu-id="c94e2-125">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="c94e2-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="c94e2-126">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="c94e2-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="c94e2-127">Per eseguire lo script in un ambito diverso da **Process** o **CurrentUser**, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="c94e2-127">You need to have administrator access to run this script in a scope other than **Process** or **CurrentUser**.</span></span>

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

<span data-ttu-id="c94e2-128">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c94e2-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="c94e2-129">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c94e2-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="c94e2-130">Durante l'esecuzione, lo script visualizzerà il **nome**, la **versione** e lo **stato** di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="c94e2-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="c94e2-131">Per eseguire lo script in modo da vedere soltanto gli elementi che verranno eliminati senza rimuoverli, specificare il parametro `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="c94e2-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="c94e2-132">Se questo script non trova una corrispondenza con una dipendenza esatta con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza.</span><span class="sxs-lookup"><span data-stu-id="c94e2-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="c94e2-133">Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.</span><span class="sxs-lookup"><span data-stu-id="c94e2-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="c94e2-134">Eseguire l'esempio seguente per ogni versione di Azure PowerShell da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="c94e2-134">Run the following example for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="c94e2-135">Per praticità, lo script seguente disinstalla tutte le versioni di Az **ad eccezione** di quella più recente.</span><span class="sxs-lookup"><span data-stu-id="c94e2-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions | 
    Sort-Object -Property Version -Descending | 
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="c94e2-136">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="c94e2-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="c94e2-137">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, esistono due opzioni che non richiedono l'esecuzione dello script `Uninstall-AzModule` indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="c94e2-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AzModule` script above.</span></span> <span data-ttu-id="c94e2-138">Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="c94e2-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="c94e2-139">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="c94e2-139">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="c94e2-140">Disinstallare l'identità del servizio gestita di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c94e2-140">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="c94e2-141">Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c94e2-141">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="c94e2-142">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="c94e2-142">Platform</span></span>         |                      <span data-ttu-id="c94e2-143">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c94e2-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="c94e2-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c94e2-144">Windows 10</span></span>               | <span data-ttu-id="c94e2-145">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="c94e2-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="c94e2-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c94e2-146">Windows 7</span></span> </br><span data-ttu-id="c94e2-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c94e2-147">Windows 8</span></span> | <span data-ttu-id="c94e2-148">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="c94e2-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c94e2-149">L'elenco di programmi visualizzato in questa schermata dovrebbe contenere **Azure PowerShell** o **Microsoft Azure PowerShell - Mese/anno**.</span><span class="sxs-lookup"><span data-stu-id="c94e2-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="c94e2-150">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="c94e2-150">This is the app to uninstall.</span></span> <span data-ttu-id="c94e2-151">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="c94e2-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="c94e2-152">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="c94e2-152">Uninstall from PowerShell</span></span>

<span data-ttu-id="c94e2-153">Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="c94e2-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="c94e2-154">L'esempio seguente rimuove _tutti_ i moduli AzureRM dal computer, ma richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="c94e2-154">The following example removes _all_ AzureRM modules from your machine but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="c94e2-155">Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo [script`Uninstall-AzModule`](#uninstall-script) fornito in questo articolo con la chiamata seguente:</span><span class="sxs-lookup"><span data-stu-id="c94e2-155">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AzModule` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name AzureRM -AllVersions
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```
