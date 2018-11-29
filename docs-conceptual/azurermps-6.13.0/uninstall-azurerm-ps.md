---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 09/11/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: bf1f81b4929ec066eeb888da4ba1303430f026b4
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586582"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="d381c-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d381c-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="d381c-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="d381c-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="d381c-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="d381c-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="d381c-106">Se si rileva un bug, [creare un problema GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="d381c-106">If you encounter a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="d381c-107">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="d381c-107">Uninstall from PowerShell</span></span>

<span data-ttu-id="d381c-108">Se Azure PowerShell è stato installato con PowerShellGet, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="d381c-108">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="d381c-109">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="d381c-109">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="d381c-110">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="d381c-110">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="d381c-111">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="d381c-111">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="d381c-112">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="d381c-112">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="d381c-113">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="d381c-113">Then, the script uninstalls the correct version of each submodule.</span></span>

```powershell-interactive
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
    $AllModules += New-Object -TypeName psobject -Property @{name=$_.name; version=$_.minimumVersion}
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

<span data-ttu-id="d381c-114">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d381c-114">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="d381c-115">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d381c-115">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="d381c-116">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="d381c-116">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="d381c-117">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="d381c-117">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="d381c-118">Per praticità, lo script seguente disinstallerà tutte le versioni di AzureRM __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="d381c-118">For convenience, the following script will uninstall all versions of AzureRM __except__ for the latest.</span></span>

```powershell-interactive
$versions = (get-installedmodule AzureRM -AllVersions | Select-Object Version)
$versions[1..($versions.Length-1)]  | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```

## <a name="uninstall-msi"></a><span data-ttu-id="d381c-119">Disinstallare il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="d381c-119">Uninstall MSI</span></span>

<span data-ttu-id="d381c-120">Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d381c-120">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="d381c-121">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="d381c-121">Platform</span></span> | <span data-ttu-id="d381c-122">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="d381c-122">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="d381c-123">Windows 10</span><span class="sxs-lookup"><span data-stu-id="d381c-123">Windows 10</span></span> | <span data-ttu-id="d381c-124">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="d381c-124">Start > Settings > Apps</span></span> |
| <span data-ttu-id="d381c-125">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d381c-125">Windows 7</span></span> </br><span data-ttu-id="d381c-126">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d381c-126">Windows 8</span></span> | <span data-ttu-id="d381c-127">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="d381c-127">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="d381c-128">L'elenco dei programmi visualizzato nella schermata mostrerà "Azure PowerShell". È possibile eseguire la disinstallazione da qui.</span><span class="sxs-lookup"><span data-stu-id="d381c-128">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>
