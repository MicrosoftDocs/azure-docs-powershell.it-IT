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
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="b1e53-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1e53-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="b1e53-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="b1e53-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="b1e53-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare feedback tramite il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="b1e53-105">If you've decided to completely uninstall the Azure PowerShell, please give us some feedback through the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>
<span data-ttu-id="b1e53-106">Se è stato rilevato un bug, [creare un problema di GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="b1e53-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues).</span></span>

## <a name="uninstall-msi"></a><span data-ttu-id="b1e53-107">Disinstallare il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="b1e53-107">Uninstall MSI</span></span>

<span data-ttu-id="b1e53-108">Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1e53-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="b1e53-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="b1e53-109">Platform</span></span> | <span data-ttu-id="b1e53-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="b1e53-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="b1e53-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b1e53-111">Windows 10</span></span> | <span data-ttu-id="b1e53-112">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="b1e53-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="b1e53-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1e53-113">Windows 7</span></span> </br><span data-ttu-id="b1e53-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b1e53-114">Windows 8</span></span> | <span data-ttu-id="b1e53-115">Start > Pannello di controllo > Programmi > Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="b1e53-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="b1e53-116">L'elenco dei programmi visualizzato nella schermata mostrerà "Azure PowerShell". È possibile eseguire la disinstallazione da qui.</span><span class="sxs-lookup"><span data-stu-id="b1e53-116">Once on this screen you should see "Azure PowerShell" in the program listing, and can uninstall from there.</span></span>

## <a name="uninstall-from-powershell"></a><span data-ttu-id="b1e53-117">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="b1e53-117">Uninstall from PowerShell</span></span>

<span data-ttu-id="b1e53-118">Se Azure PowerShell è stato installato con PowerShellGet, è possibile usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="b1e53-118">If you installed Azure PowerShell using PowerShellGet, you can use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="b1e53-119">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="b1e53-119">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="b1e53-120">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="b1e53-120">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="b1e53-121">La disinstallazione può essere complicata se sono installate più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1e53-121">Uninstallation can be complicated if you have multiple versions of Azure PowerShell installed.</span></span>

<span data-ttu-id="b1e53-122">Lo script può essere usato per rimuovere completamente una singola versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1e53-122">The following script can be used to completely remove a single version of Azure PowerShell.</span></span> <span data-ttu-id="b1e53-123">Lo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="b1e53-123">The script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="b1e53-124">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="b1e53-124">Then, the script uninstalls the correct version of each submodule.</span></span>

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

<span data-ttu-id="b1e53-125">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1e53-125">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="b1e53-126">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b1e53-126">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell
Uninstall-AllModules -TargetModule AzureRM -Version 4.4.1 -Force
```

<span data-ttu-id="b1e53-127">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="b1e53-127">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span>

```output
Creating list of dependencies...
Uninstalling AzureRM.Profile version 3.4.1
Uninstalling Azure.Storage version 3.4.1
Uninstalling AzureRM.AnalysisServices version 0.4.7
Uninstalling Azure.AnalysisServices version 0.4.7
...
```

<span data-ttu-id="b1e53-128">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="b1e53-128">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span>
