---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 05/28/2020
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: d99b40121deca0a4817c3a6364ad55020dadbda1
ms.sourcegitcommit: c19bf5a96a82a56e2b1fa9ab5e106690f850cedf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/27/2020
ms.locfileid: "87177493"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="06b19-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06b19-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="06b19-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="06b19-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="06b19-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="06b19-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="06b19-106">Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.</span><span class="sxs-lookup"><span data-stu-id="06b19-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="06b19-107">Disinstallare il modulo Az PowerShell dal pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="06b19-107">Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="06b19-108">Se il modulo Az PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06b19-108">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="06b19-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="06b19-109">Platform</span></span>         |                      <span data-ttu-id="06b19-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="06b19-110">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="06b19-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="06b19-111">Windows 10</span></span>               | <span data-ttu-id="06b19-112">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="06b19-112">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="06b19-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06b19-113">Windows 7</span></span> </br><span data-ttu-id="06b19-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06b19-114">Windows 8</span></span> | <span data-ttu-id="06b19-115">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="06b19-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="06b19-116">L'elenco dei programmi visualizzato nella schermata conterrà **Azure PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="06b19-116">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="06b19-117">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="06b19-117">This is the app to uninstall.</span></span> <span data-ttu-id="06b19-118">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="06b19-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="06b19-119">Disinstallare il modulo Az PowerShell da PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="06b19-119">Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="06b19-120">Per disinstallare i moduli Az, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="06b19-120">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="06b19-121">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="06b19-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="06b19-122">Per rimuovere completamente il modulo Az PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="06b19-122">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="06b19-123">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="06b19-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="06b19-124">Per verificare quali versioni del modulo Az PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="06b19-124">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

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

<span data-ttu-id="06b19-125">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="06b19-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="06b19-126">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="06b19-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="06b19-127">Per eseguire lo script in un ambito diverso da **Process** o **CurrentUser**, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="06b19-127">You need to have administrator access to run this script in a scope other than **Process** or **Current User**.</span></span>

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

<span data-ttu-id="06b19-128">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06b19-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="06b19-129">L'esempio seguente mostra come eseguire la funzione per rimuovere una versione precedente del modulo Az PowerShell e i relativi sottomoduli.</span><span class="sxs-lookup"><span data-stu-id="06b19-129">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="06b19-130">Durante l'esecuzione, lo script visualizzerà il **nome**, la **versione** e lo **stato** di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="06b19-130">As the script runs, it displays the **Name**, **Version**, and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="06b19-131">Per eseguire lo script in modo da vedere soltanto gli elementi che verranno eliminati senza rimuoverli, specificare il parametro `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="06b19-131">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="06b19-132">Se questo script non trova una corrispondenza con una dipendenza esatta con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza.</span><span class="sxs-lookup"><span data-stu-id="06b19-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="06b19-133">Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.</span><span class="sxs-lookup"><span data-stu-id="06b19-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="06b19-134">Eseguire l'esempio seguente per ogni versione del modulo Az PowerShell da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="06b19-134">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="06b19-135">Per praticità, lo script seguente disinstalla tutte le versioni di Az **ad eccezione** di quella più recente.</span><span class="sxs-lookup"><span data-stu-id="06b19-135">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="06b19-136">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="06b19-136">Uninstall the AzureRM module</span></span>

<span data-ttu-id="06b19-137">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, è possibile scegliere tra due opzioni.</span><span class="sxs-lookup"><span data-stu-id="06b19-137">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="06b19-138">Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="06b19-138">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="06b19-139">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="06b19-139">If you're not sure of your original installation method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="06b19-140">Disinstallare il modulo AzureRM PowerShell dal pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="06b19-140">Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="06b19-141">Se il modulo AzureRM PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06b19-141">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="06b19-142">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="06b19-142">Platform</span></span>         |                      <span data-ttu-id="06b19-143">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="06b19-143">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="06b19-144">Windows 10</span><span class="sxs-lookup"><span data-stu-id="06b19-144">Windows 10</span></span>               | <span data-ttu-id="06b19-145">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="06b19-145">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="06b19-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="06b19-146">Windows 7</span></span> </br><span data-ttu-id="06b19-147">Windows 8</span><span class="sxs-lookup"><span data-stu-id="06b19-147">Windows 8</span></span> | <span data-ttu-id="06b19-148">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="06b19-148">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="06b19-149">L'elenco di programmi visualizzato in questa schermata dovrebbe contenere **Azure PowerShell** o **Microsoft Azure PowerShell - Mese/anno**.</span><span class="sxs-lookup"><span data-stu-id="06b19-149">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="06b19-150">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="06b19-150">This is the app to uninstall.</span></span> <span data-ttu-id="06b19-151">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="06b19-151">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="06b19-152">Disinstallare il modulo AzureRM PowerShell da PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="06b19-152">Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="06b19-153">Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="06b19-153">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="06b19-154">L'esempio seguente rimuove _tutti_ i moduli AzureRM dal computer.</span><span class="sxs-lookup"><span data-stu-id="06b19-154">The following example removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="06b19-155">Richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="06b19-155">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
