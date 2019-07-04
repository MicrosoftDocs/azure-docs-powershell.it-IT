---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 06/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: cc0b6a4369116e92b8200ffbc0838d6ee2991263
ms.sourcegitcommit: febbbd3f75c8dd1a296281d265289f015b6cb537
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/12/2019
ms.locfileid: "67037685"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="5d02e-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d02e-103">Uninstall the Azure PowerShell module</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="5d02e-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="5d02e-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="5d02e-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="5d02e-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="5d02e-106">Se è stato rilevato un bug, [creare un problema di GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="5d02e-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi-or-web-platform-installer"></a><span data-ttu-id="5d02e-107">Disinstallare il pacchetto MSI o l'Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="5d02e-107">Uninstall MSI or Web Platform Installer</span></span>

<span data-ttu-id="5d02e-108">Se Azure PowerShell è stato installato con il pacchetto MSI o l'Installazione guidata piattaforma Web, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d02e-108">If you installed Azure PowerShell using the MSI package or the Web Platform Installer, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="5d02e-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="5d02e-109">Platform</span></span> | <span data-ttu-id="5d02e-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="5d02e-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="5d02e-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d02e-111">Windows 10</span></span> | <span data-ttu-id="5d02e-112">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="5d02e-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="5d02e-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5d02e-113">Windows 7</span></span> </br><span data-ttu-id="5d02e-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5d02e-114">Windows 8</span></span> | <span data-ttu-id="5d02e-115">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="5d02e-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="5d02e-116">L'elenco dei programmi visualizzato nella schermata mostrerà "Azure PowerShell". È possibile eseguire la disinstallazione da qui.</span><span class="sxs-lookup"><span data-stu-id="5d02e-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="5d02e-117">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="5d02e-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="5d02e-118">Se Azure PowerShell è stato installato con PowerShellGet, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="5d02e-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="5d02e-119">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="5d02e-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="5d02e-120">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="5d02e-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="5d02e-121">La disinstallazione può essere complicata se sono installate più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d02e-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="5d02e-122">È possibile usare lo script seguente per rimuovere completamente una singola versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d02e-122">You use the following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="5d02e-123">Lo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="5d02e-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="5d02e-124">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="5d02e-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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
    if ($_.PSObject.Properties.Name -contains 'requiredVersion') {
      $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.requiredVersion}
    }
    else { # Assume minimum version
      # Minimum version actually reports the installed dependency
      # which is used, not the actual "minimum dependency." Check to
      # see if the requested version was installed as a dependency earlier.
      $candidate = Get-InstalledModule $_.name -RequiredVersion $version -ErrorAction Ignore
      if ($candidate) {
        $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$version}
      }
      else {
        $availableModules = Get-InstalledModule $_.name -AllVersions
        Write-Warning ("Could not find uninstall candidate for {0}:{1} - module may require manual uninstall. Available versions are: {2}" -f $_.name,$version,($availableModules.Version -join ', '))
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

<span data-ttu-id="5d02e-125">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d02e-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="5d02e-126">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5d02e-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="5d02e-127">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="5d02e-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="5d02e-128">Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="5d02e-128">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

> [!NOTE]
> <span data-ttu-id="5d02e-129">Se questo script non consente di trovare una dipendenza con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza.</span><span class="sxs-lookup"><span data-stu-id="5d02e-129">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="5d02e-130">Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.</span><span class="sxs-lookup"><span data-stu-id="5d02e-130">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="5d02e-131">In questo caso, vengono elencate le versioni disponibili della dipendenza.</span><span class="sxs-lookup"><span data-stu-id="5d02e-131">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="5d02e-132">È quindi possibile rimuovere manualmente le eventuali versioni precedenti con `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="5d02e-132">You can then remove any old versions manually with `Uninstall-Module`.</span></span>


<span data-ttu-id="5d02e-133">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="5d02e-133">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="5d02e-134">Per praticità, lo script seguente disinstallerà tutte le versioni di AzureRM __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="5d02e-134">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
