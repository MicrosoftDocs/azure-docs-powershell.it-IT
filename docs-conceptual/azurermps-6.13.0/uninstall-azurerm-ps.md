---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 11/30/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: a35814f4411dd9cab75fa36bd13ff087cdec8f9b
ms.sourcegitcommit: 93f93b90ef88c2659be95f3acaba514fe9639169
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2018
ms.locfileid: "52826698"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="c4cf9-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4cf9-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="c4cf9-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="c4cf9-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="c4cf9-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="c4cf9-106">Se si rileva un bug, [creare un problema GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="c4cf9-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="c4cf9-107">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="c4cf9-107">Uninstall from PowerShell</span></span>

<span data-ttu-id="c4cf9-108">Se Azure PowerShell è stato installato con PowerShellGet, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="c4cf9-108">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="c4cf9-109">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="c4cf9-110">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="c4cf9-111">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="c4cf9-112">Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="c4cf9-112">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions
```

```output
Version              Name                                Repository           Description
-------              ----                                ----------           -----------
6.11.0               AzureRM                             PSGallery            Azure Resource Manager Module
6.13.1               AzureRM                             PSGallery            Azure Resource Manager Module
```

<span data-ttu-id="c4cf9-113">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="c4cf9-113">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="c4cf9-114">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-114">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="c4cf9-115">Per eseguire lo script in un ambito diverso da `Process` o `CurrentUser`, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-115">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="c4cf9-116">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-116">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="c4cf9-117">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-117">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="c4cf9-118">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-118">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="c4cf9-119">Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-119">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="c4cf9-120">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-120">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="c4cf9-121">Per praticità, lo script seguente disinstallerà tutte le versioni di AzureRM __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-121">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a><span data-ttu-id="c4cf9-122">Disinstallare il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="c4cf9-122">Uninstall MSI</span></span>

<span data-ttu-id="c4cf9-123">Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-123">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="c4cf9-124">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="c4cf9-124">Platform</span></span> | <span data-ttu-id="c4cf9-125">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c4cf9-125">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="c4cf9-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="c4cf9-126">Windows 10</span></span> | <span data-ttu-id="c4cf9-127">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="c4cf9-127">Start > Settings > Apps</span></span> |
| <span data-ttu-id="c4cf9-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c4cf9-128">Windows 7</span></span> </br><span data-ttu-id="c4cf9-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c4cf9-129">Windows 8</span></span> | <span data-ttu-id="c4cf9-130">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="c4cf9-130">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="c4cf9-131">L'elenco dei programmi visualizzato nella schermata mostrerà "Azure PowerShell". È possibile eseguire la disinstallazione da qui.</span><span class="sxs-lookup"><span data-stu-id="c4cf9-131">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>
