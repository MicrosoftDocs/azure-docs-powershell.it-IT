---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: fcec2c713d1967a5a70df9b13aa30d9ff4625e9d
ms.sourcegitcommit: 447276d46ffeeb37f0c07a570536665e36c5ddb8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/14/2019
ms.locfileid: "57882361"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="aef1b-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aef1b-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="aef1b-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="aef1b-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="aef1b-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="aef1b-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="aef1b-106">Se si rileva un bug, [creare un problema GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="aef1b-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-the-az-module"></a><span data-ttu-id="aef1b-107">Disinstallare il modulo Az</span><span class="sxs-lookup"><span data-stu-id="aef1b-107">Uninstall the Az module</span></span>

<span data-ttu-id="aef1b-108">Per disinstallare i moduli Az, usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="aef1b-108">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="aef1b-109">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="aef1b-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="aef1b-110">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="aef1b-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="aef1b-111">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="aef1b-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="aef1b-112">Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="aef1b-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions
```

```output
Version             Name                           Repository           Description
-------             ----                           ----------           -----------
0.7.0               Az                             PSGallery            Azure Resource Manager Module
1.0.0               Az                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="aef1b-113">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="aef1b-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="aef1b-114">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="aef1b-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="aef1b-115">Per eseguire lo script in un ambito diverso da `Process` o `CurrentUser`, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="aef1b-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="aef1b-116">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aef1b-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="aef1b-117">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aef1b-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="aef1b-118">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="aef1b-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="aef1b-119">Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="aef1b-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

<span data-ttu-id="aef1b-120">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="aef1b-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="aef1b-121">Per praticità, lo script seguente disinstallerà tutte le versioni di Az __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="aef1b-121">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="aef1b-122">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="aef1b-122">Uninstall the AzureRM module</span></span>

<span data-ttu-id="aef1b-123">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, sono disponibili due opzioni semplici che non richiedono l'esecuzione dello script `Uninstall-AllModules` precedente.</span><span class="sxs-lookup"><span data-stu-id="aef1b-123">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two simple options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="aef1b-124">Il metodo da seguire dipende dal modo in cui è stato installato AzureRM.</span><span class="sxs-lookup"><span data-stu-id="aef1b-124">Which method you follow depends on how you installed AzureRM.</span></span>
<span data-ttu-id="aef1b-125">Se non si è sicuri, verificare prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="aef1b-125">If you're not sure, check the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="aef1b-126">Disinstallare l'identità del servizio gestita di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="aef1b-126">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="aef1b-127">Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="aef1b-127">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="aef1b-128">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="aef1b-128">Platform</span></span> | <span data-ttu-id="aef1b-129">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="aef1b-129">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="aef1b-130">Windows 10</span><span class="sxs-lookup"><span data-stu-id="aef1b-130">Windows 10</span></span> | <span data-ttu-id="aef1b-131">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="aef1b-131">Start > Settings > Apps</span></span> |
| <span data-ttu-id="aef1b-132">Windows 7</span><span class="sxs-lookup"><span data-stu-id="aef1b-132">Windows 7</span></span> </br><span data-ttu-id="aef1b-133">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aef1b-133">Windows 8</span></span> | <span data-ttu-id="aef1b-134">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="aef1b-134">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="aef1b-135">L'elenco dei programmi visualizzato nella schermata mostrerà __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="aef1b-135">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="aef1b-136">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="aef1b-136">This is the app to uninstall.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="aef1b-137">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="aef1b-137">Uninstall from PowerShell</span></span>

<span data-ttu-id="aef1b-138">Se AzureRM è stato installato da PowerShellGet, sarà possibile rimuovere i moduli con il nuovo comando `Uninstall-AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="aef1b-138">If you installed AzureRM from PowerShellGet, then you can remove the modules with the new `Uninstall-AzureRM` command.</span></span> <span data-ttu-id="aef1b-139">Questa operazione rimuove _tutti_ i moduli AzureRM dal computer, ma richiede i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="aef1b-139">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```

<span data-ttu-id="aef1b-140">Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo script `Uninstall-AllModules` fornito in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="aef1b-140">If you can't successfully run the `Uninstall-AzureRM` command, use the `Uninstall-AllModules` script provided in this article instead.</span></span>
