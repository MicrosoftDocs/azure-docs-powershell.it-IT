---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 09/15/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 7f831bdf6d6144640e036d72900958847283acf1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753584"
---
# <a name="how-to-uninstall-azure-powershell-modules"></a><span data-ttu-id="367dc-103">Come disinstallare i moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="367dc-103">How to uninstall Azure PowerShell modules</span></span>

<span data-ttu-id="367dc-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="367dc-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="367dc-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="367dc-105">If you've decided to completely uninstall Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span> <span data-ttu-id="367dc-106">Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.</span><span class="sxs-lookup"><span data-stu-id="367dc-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="367dc-107">Disinstallare il modulo Az</span><span class="sxs-lookup"><span data-stu-id="367dc-107">Uninstall the Az module</span></span>

<span data-ttu-id="367dc-108">Se nel sistema è installato il modulo Az ed è necessario disinstallarlo, sono disponibili due opzioni.</span><span class="sxs-lookup"><span data-stu-id="367dc-108">If you have the Az module installed on your system and would like to uninstall it, there are two options.</span></span> <span data-ttu-id="367dc-109">Il metodo da seguire dipende dal modo in cui è stato installato il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="367dc-109">Which method you follow depends on how you installed the Az module.</span></span> <span data-ttu-id="367dc-110">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="367dc-110">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-az-powershell-module-from-msi"></a><span data-ttu-id="367dc-111">Opzione 1: Disinstallare il modulo Az PowerShell dal pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="367dc-111">Option 1: Uninstall the Az PowerShell module from MSI</span></span>

<span data-ttu-id="367dc-112">Se il modulo Az PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="367dc-112">If you installed Az PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="367dc-113">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="367dc-113">Platform</span></span>         |                      <span data-ttu-id="367dc-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="367dc-114">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="367dc-115">Windows 10</span><span class="sxs-lookup"><span data-stu-id="367dc-115">Windows 10</span></span>               | <span data-ttu-id="367dc-116">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="367dc-116">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="367dc-117">Windows 7</span><span class="sxs-lookup"><span data-stu-id="367dc-117">Windows 7</span></span> </br><span data-ttu-id="367dc-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="367dc-118">Windows 8</span></span> | <span data-ttu-id="367dc-119">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="367dc-119">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="367dc-120">L'elenco dei programmi visualizzato nella schermata conterrà **Azure PowerShell** .</span><span class="sxs-lookup"><span data-stu-id="367dc-120">Once on this screen, you should see **Azure PowerShell** in the program listing.</span></span> <span data-ttu-id="367dc-121">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="367dc-121">This is the app to uninstall.</span></span> <span data-ttu-id="367dc-122">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="367dc-122">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-az-powershell-module-from-powershellget"></a><span data-ttu-id="367dc-123">Opzione 2: Disinstallare il modulo Az PowerShell da PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="367dc-123">Option 2: Uninstall the Az PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="367dc-124">Per disinstallare i moduli Az, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="367dc-124">To uninstall the Az modules, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="367dc-125">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="367dc-125">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="367dc-126">Per rimuovere completamente il modulo Az PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="367dc-126">To remove the Az PowerShell module completely, you must uninstall each module individually.</span></span> <span data-ttu-id="367dc-127">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="367dc-127">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="367dc-128">Per verificare quali versioni del modulo Az PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="367dc-128">To check which versions of the Az PowerShell module you've installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
3.8.0               Az                             PSGallery            Microsoft Azure PowerShell
4.1.0               Az                             PSGallery            Microsoft Azure PowerShell
```

<span data-ttu-id="367dc-129">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="367dc-129">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="367dc-130">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="367dc-130">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="367dc-131">Per eseguire lo script in un ambito diverso da **Process** o **CurrentUser** , è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="367dc-131">You need to have administrator access to run this script in a scope other than **Process** or **Current User** .</span></span>

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

<span data-ttu-id="367dc-132">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="367dc-132">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="367dc-133">L'esempio seguente mostra come eseguire la funzione per rimuovere una versione precedente del modulo Az PowerShell e i relativi sottomoduli.</span><span class="sxs-lookup"><span data-stu-id="367dc-133">The following example shows how to run the function to remove an older version of the Az PowerShell module and its submodules.</span></span>

```powershell-interactive
Uninstall-AzModule -Name Az -Version 1.8.0
```

<span data-ttu-id="367dc-134">Durante l'esecuzione, lo script visualizzerà il **nome** , la **versione** e lo **stato** di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="367dc-134">As the script runs, it displays the **Name** , **Version** , and **State** of each submodule that is being uninstalled.</span></span> <span data-ttu-id="367dc-135">Per eseguire lo script in modo da vedere soltanto gli elementi che verranno eliminati senza rimuoverli, specificare il parametro `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="367dc-135">To run the script to only see what would be deleted, without removing it, specify the `-WhatIf` parameter.</span></span>

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
> <span data-ttu-id="367dc-136">Se questo script non trova una corrispondenza con una dipendenza esatta con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza.</span><span class="sxs-lookup"><span data-stu-id="367dc-136">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependency.</span></span> <span data-ttu-id="367dc-137">Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.</span><span class="sxs-lookup"><span data-stu-id="367dc-137">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span>

<span data-ttu-id="367dc-138">Eseguire l'esempio seguente per ogni versione del modulo Az PowerShell da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="367dc-138">Run the following example for every version of the Az PowerShell module that you want to uninstall.</span></span>
<span data-ttu-id="367dc-139">Per praticità, lo script seguente disinstalla tutte le versioni di Az **ad eccezione** di quella più recente.</span><span class="sxs-lookup"><span data-stu-id="367dc-139">For convenience, the following script uninstalls all versions of Az **except** for the latest.</span></span>

```powershell-interactive
$Modules = Get-InstalledModule -Name Az -AllVersions |
    Sort-Object -Property Version -Descending |
        Select-Object -Skip 1
$Modules | ForEach-Object {Uninstall-AzModule -Name $_.Name -Version $_.Version}
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="367dc-140">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="367dc-140">Uninstall the AzureRM module</span></span>

<span data-ttu-id="367dc-141">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, è possibile scegliere tra due opzioni.</span><span class="sxs-lookup"><span data-stu-id="367dc-141">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options.</span></span> <span data-ttu-id="367dc-142">Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="367dc-142">Which method you follow depends on how you installed the AzureRM module.</span></span> <span data-ttu-id="367dc-143">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="367dc-143">If you're not sure of your original installation method, follow the MSI steps for uninstalling first.</span></span>

### <a name="option-1-uninstall-the-azurerm-powershell-module-from-msi"></a><span data-ttu-id="367dc-144">Opzione 1: Disinstallare il modulo AzureRM PowerShell dal pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="367dc-144">Option 1: Uninstall the AzureRM PowerShell module from MSI</span></span>

<span data-ttu-id="367dc-145">Se il modulo AzureRM PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="367dc-145">If you installed the AzureRM PowerShell module using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

|         <span data-ttu-id="367dc-146">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="367dc-146">Platform</span></span>         |                      <span data-ttu-id="367dc-147">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="367dc-147">Instructions</span></span>                      |
| ------------------------ | ------------------------------------------------------ |
| <span data-ttu-id="367dc-148">Windows 10</span><span class="sxs-lookup"><span data-stu-id="367dc-148">Windows 10</span></span>               | <span data-ttu-id="367dc-149">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="367dc-149">Start > Settings > Apps</span></span>                                |
| <span data-ttu-id="367dc-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="367dc-150">Windows 7</span></span> </br><span data-ttu-id="367dc-151">Windows 8</span><span class="sxs-lookup"><span data-stu-id="367dc-151">Windows 8</span></span> | <span data-ttu-id="367dc-152">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="367dc-152">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="367dc-153">L'elenco di programmi visualizzato in questa schermata dovrebbe contenere **Azure PowerShell** o **Microsoft Azure PowerShell - Mese/anno** .</span><span class="sxs-lookup"><span data-stu-id="367dc-153">Once on this screen, you should see **Azure PowerShell** or **Microsoft Azure PowerShell - Month Year** in the program listing.</span></span> <span data-ttu-id="367dc-154">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="367dc-154">This is the app to uninstall.</span></span> <span data-ttu-id="367dc-155">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="367dc-155">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="option-2-uninstall-the-azurerm-powershell-module-from-powershellget"></a><span data-ttu-id="367dc-156">Opzione 2: Disinstallare il modulo AzureRM PowerShell da PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="367dc-156">Option 2: Uninstall the AzureRM PowerShell module from PowerShellGet</span></span>

<span data-ttu-id="367dc-157">Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il cmdlet [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="367dc-157">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) cmdlet, available as part of the `Az.Accounts` module.</span></span>

<span data-ttu-id="367dc-158">Per usare il modulo `Az.Accounts`, è necessario che sia installato il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="367dc-158">In order to use the `Az.Accounts` module, you will need to have the Az module installed.</span></span>  <span data-ttu-id="367dc-159">La presenza contemporanea dei moduli AzureRM e Az installati non è supportata, ma è possibile usare il modulo Az per disinstallare immediatamente il nodulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="367dc-159">Having both the AzureRM and the Az modules installed at the same time is not supported however the Az module can be used to immediately uninstall the AzureRM module.</span></span>  <span data-ttu-id="367dc-160">È possibile installare il modulo Az e ignorare l'avviso sul modulo AzureRM con il comando seguente, se il modulo Az non è già installato:</span><span class="sxs-lookup"><span data-stu-id="367dc-160">You can install the Az module and bypass the AzureRM module warning with the following command if you do not have the Az module installed already:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="367dc-161">Una volta installato il modulo Az, il comando seguente rimuove _tutti_  i moduli AzureRM dal computer.</span><span class="sxs-lookup"><span data-stu-id="367dc-161">Once the Az module is installed, the following command removes _all_ AzureRM modules from your machine.</span></span> <span data-ttu-id="367dc-162">Richiede privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="367dc-162">It requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
