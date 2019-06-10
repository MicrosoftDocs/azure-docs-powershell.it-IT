---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: eaabd8014368f7ea8f4c9504e58d920dad8a6518
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365445"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="cbb96-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbb96-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="cbb96-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="cbb96-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="cbb96-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="cbb96-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="cbb96-106">Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.</span><span class="sxs-lookup"><span data-stu-id="cbb96-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="cbb96-107">Disinstallare il modulo Az</span><span class="sxs-lookup"><span data-stu-id="cbb96-107">Uninstall the Az module</span></span>

<span data-ttu-id="cbb96-108">Per disinstallare i moduli Az, usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="cbb96-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="cbb96-109">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="cbb96-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="cbb96-110">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="cbb96-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="cbb96-111">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="cbb96-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="cbb96-112">Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="cbb96-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<a name="uninstall-script"/>

<span data-ttu-id="cbb96-113">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="cbb96-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="cbb96-114">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="cbb96-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="cbb96-115">Per eseguire lo script in un ambito diverso da `Process` o `CurrentUser`, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="cbb96-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="cbb96-116">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbb96-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="cbb96-117">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbb96-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="cbb96-118">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="cbb96-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="cbb96-119">Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="cbb96-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="cbb96-120">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="cbb96-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="cbb96-121">Per praticità, lo script seguente disinstallerà tutte le versioni di Az __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="cbb96-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="cbb96-122">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="cbb96-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="cbb96-123">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, esistono due opzioni che non richiedono l'esecuzione dello script `Uninstall-AllModules` indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="cbb96-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="cbb96-124">Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="cbb96-124">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="cbb96-125">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="cbb96-125">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="cbb96-126">Disinstallare l'identità del servizio gestita di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbb96-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="cbb96-127">Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbb96-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="cbb96-128">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="cbb96-128">Platform</span></span> | <span data-ttu-id="cbb96-129">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="cbb96-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="cbb96-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="cbb96-130">Windows 10</span></span> | <span data-ttu-id="cbb96-131">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="cbb96-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="cbb96-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cbb96-132">Windows 7</span></span> </br><span data-ttu-id="cbb96-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="cbb96-133">Windows 8</span></span> | <span data-ttu-id="cbb96-134">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="cbb96-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="cbb96-135">L'elenco dei programmi visualizzato nella schermata mostrerà __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="cbb96-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="cbb96-136">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="cbb96-136">This is the app to uninstall.</span></span> <span data-ttu-id="cbb96-137">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="cbb96-137">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="cbb96-138">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="cbb96-138">Uninstall from PowerShell</span></span>

<span data-ttu-id="cbb96-139">Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il comando [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="cbb96-139">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="cbb96-140">Questa operazione rimuove _tutti_ i moduli AzureRM dal computer, ma richiede i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="cbb96-140">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="cbb96-141">Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo [script`Uninstall-AllModules`](#uninstall-script) fornito in questo articolo con la chiamata seguente:</span><span class="sxs-lookup"><span data-stu-id="cbb96-141">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```