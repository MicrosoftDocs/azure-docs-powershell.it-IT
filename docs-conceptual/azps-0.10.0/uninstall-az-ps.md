---
title: Disinstallare Azure PowerShell
description: Come eseguire una disinstallazione completa di Azure PowerShell
ms.date: 10/22/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 37f152fb43e23c361544db4a738d58911099da1f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "81445969"
---
# <a name="uninstall-the-azure-powershell-module"></a><span data-ttu-id="8db98-103">Disinstallare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8db98-103">Uninstall the Azure PowerShell module</span></span>

<span data-ttu-id="8db98-104">Questo articolo spiega come disinstallare una versione precedente di Azure PowerShell o come rimuoverla completamente dal sistema.</span><span class="sxs-lookup"><span data-stu-id="8db98-104">This article tells you how to uninstall an older version of Azure PowerShell, or completely remove it from your system.</span></span> <span data-ttu-id="8db98-105">Se si è deciso di disinstallare completamente Azure PowerShell, inviare commenti e suggerimenti tramite il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="8db98-105">If you've decided to completely uninstall the Azure PowerShell, give us some feedback through the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>
<span data-ttu-id="8db98-106">Se è stato rilevato un bug, [segnalare un problema di GitHub](https://github.com/azure/azure-powershell/issues) per consentirne la correzione.</span><span class="sxs-lookup"><span data-stu-id="8db98-106">If you encountered a bug, we'd appreciate it if you [file a GitHub issue](https://github.com/azure/azure-powershell/issues) so that it can be fixed.</span></span>

## <a name="uninstall-azure-powershell-from-msi"></a><span data-ttu-id="8db98-107">Disinstallare Azure PowerShell con il file MSI</span><span class="sxs-lookup"><span data-stu-id="8db98-107">Uninstall Azure PowerShell from MSI</span></span>

<span data-ttu-id="8db98-108">Se Azure PowerShell è stato installato con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8db98-108">If you installed Azure PowerShell using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="8db98-109">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="8db98-109">Platform</span></span> | <span data-ttu-id="8db98-110">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="8db98-110">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="8db98-111">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8db98-111">Windows 10</span></span> | <span data-ttu-id="8db98-112">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="8db98-112">Start > Settings > Apps</span></span> |
| <span data-ttu-id="8db98-113">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8db98-113">Windows 7</span></span> </br><span data-ttu-id="8db98-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8db98-114">Windows 8</span></span> | <span data-ttu-id="8db98-115">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="8db98-115">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="8db98-116">L'elenco dei programmi visualizzato nella schermata mostrerà __Azure PowerShell__.</span><span class="sxs-lookup"><span data-stu-id="8db98-116">Once on this screen you should see __Azure PowerShell__ in the program listing.</span></span> <span data-ttu-id="8db98-117">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="8db98-117">This is the app to uninstall.</span></span> <span data-ttu-id="8db98-118">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="8db98-118">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

## <a name="uninstall-azure-powershell-from-powershell-get"></a><span data-ttu-id="8db98-119">Disinstallare Azure PowerShell con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="8db98-119">Uninstall Azure PowerShell from PowerShell Get</span></span>

<span data-ttu-id="8db98-120">Per disinstallare i moduli Az, usare il cmdlet [Uninstall-Module](/powershell/module/powershellget/uninstall-module).</span><span class="sxs-lookup"><span data-stu-id="8db98-120">To uninstall the Az modules, use the [Uninstall-Module](/powershell/module/powershellget/uninstall-module) cmdlet.</span></span> <span data-ttu-id="8db98-121">Tuttavia `Uninstall-Module` disinstalla solo un modulo.</span><span class="sxs-lookup"><span data-stu-id="8db98-121">However, `Uninstall-Module` only uninstalls one module.</span></span> <span data-ttu-id="8db98-122">Per rimuovere completamente Azure PowerShell, è necessario disinstallare ogni modulo singolarmente.</span><span class="sxs-lookup"><span data-stu-id="8db98-122">To remove Azure PowerShell completely, you must uninstall each module individually.</span></span> <span data-ttu-id="8db98-123">Se si sono installate più versioni di Azure PowerShell, la disinstallazione può essere complessa.</span><span class="sxs-lookup"><span data-stu-id="8db98-123">Uninstallation can be complicated if you have more than one version of Azure PowerShell installed.</span></span>

<span data-ttu-id="8db98-124">Per verificare quali versioni di Azure PowerShell sono attualmente installate, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="8db98-124">To check which versions of Azure PowerShell you currently have installed, run the following command:</span></span>

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

<span data-ttu-id="8db98-125">Questo script esegue una query su PowerShell Gallery per ottenere un elenco dei moduli secondari dipendenti,</span><span class="sxs-lookup"><span data-stu-id="8db98-125">The following script queries the PowerShell Gallery to get a list of dependent submodules.</span></span> <span data-ttu-id="8db98-126">quindi disinstalla la versione corretta di ogni modulo secondario.</span><span class="sxs-lookup"><span data-stu-id="8db98-126">Then, the script uninstalls the correct version of each submodule.</span></span> <span data-ttu-id="8db98-127">Per eseguire lo script in un ambito diverso da `Process` o `CurrentUser`, è necessario l'accesso come amministratore.</span><span class="sxs-lookup"><span data-stu-id="8db98-127">You will need to have administrator access to run this script in a scope other than `Process` or `CurrentUser`.</span></span>

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

<span data-ttu-id="8db98-128">Per usare questa funzione, copiare e incollare il codice nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8db98-128">To use this function, copy and paste the code into your PowerShell session.</span></span> <span data-ttu-id="8db98-129">L'esempio seguente illustra come eseguire la funzione per rimuovere una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8db98-129">The following example shows how to run the function to remove an older version of Azure PowerShell.</span></span>

```powershell-interactive
Uninstall-AllModules -TargetModule Az -Version 0.7.0 -Force
```

<span data-ttu-id="8db98-130">Durante l'esecuzione, lo script visualizzerà il nome e la versione di ogni modulo secondario disinstallato.</span><span class="sxs-lookup"><span data-stu-id="8db98-130">As the script runs, it will display the name and version of each submodule that is being uninstalled.</span></span> <span data-ttu-id="8db98-131">Per eseguire lo script in modo da visualizzare soltanto gli elementi che verrebbero eliminati senza rimuoverli, usare l'opzione `-WhatIf`.</span><span class="sxs-lookup"><span data-stu-id="8db98-131">To run the script to only see what would be deleted, without removing it, use the `-WhatIf` option.</span></span>

```output
Creating list of dependencies...
Uninstalling Az.Profile version 0.7.0
Uninstalling Az.Aks version 0.7.0
Uninstalling Az.AnalysisServices version 0.7.0
...
```

> [!NOTE]
> <span data-ttu-id="8db98-132">Se questo script non consente di trovare una dipendenza con la stessa versione da disinstallare, non verrà disinstallata _alcuna_ versione di tale dipendenza.</span><span class="sxs-lookup"><span data-stu-id="8db98-132">If this script can't match an exact dependency with the same version to uninstall, it won't uninstall _any_ version of that dependecy.</span></span> <span data-ttu-id="8db98-133">Nel sistema potrebbero infatti esistere altre versioni del modulo di destinazione che si basano su queste dipendenze.</span><span class="sxs-lookup"><span data-stu-id="8db98-133">This is because there may be other versions of the target module on your system which rely on these dependencies.</span></span> <span data-ttu-id="8db98-134">In questo caso, vengono elencate le versioni disponibili della dipendenza.</span><span class="sxs-lookup"><span data-stu-id="8db98-134">In this case, the available versions of the dependency are listed.</span></span>
> <span data-ttu-id="8db98-135">È quindi possibile rimuovere manualmente le eventuali versioni precedenti con `Uninstall-Module`.</span><span class="sxs-lookup"><span data-stu-id="8db98-135">You can then remove any old versions manually with `Uninstall-Module`.</span></span>

<span data-ttu-id="8db98-136">Eseguire questo comando per ogni versione di Azure PowerShell che si vuole disinstallare.</span><span class="sxs-lookup"><span data-stu-id="8db98-136">Run this command for every version of Azure PowerShell that you want to uninstall.</span></span> <span data-ttu-id="8db98-137">Per praticità, lo script seguente disinstallerà tutte le versioni di Az __ad eccezione__ della più recente.</span><span class="sxs-lookup"><span data-stu-id="8db98-137">For convenience, the following script will uninstall all versions of Az __except__ for the latest.</span></span>

```powershell-interactive
$versions = (Get-InstalledModule Az -AllVersions | Select-Object Version)
$versions[0..($versions.Length-2)]  | foreach { Uninstall-AllModules -TargetModule Az -Version ($_.Version) -Force }
```

## <a name="uninstall-the-azurerm-module"></a><span data-ttu-id="8db98-138">Disinstallare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="8db98-138">Uninstall the AzureRM module</span></span>

<span data-ttu-id="8db98-139">Se nel sistema è installato il modulo Az e si vuole disinstallare AzureRM, esistono due opzioni che non richiedono l'esecuzione dello script `Uninstall-AllModules` indicato sopra.</span><span class="sxs-lookup"><span data-stu-id="8db98-139">If you have the Az module installed on your system and would like to uninstall AzureRM, there are two options that don't require running the `Uninstall-AllModules` script above.</span></span> <span data-ttu-id="8db98-140">Il metodo da seguire dipende dal modo in cui è stato installato il modulo AzureRM.</span><span class="sxs-lookup"><span data-stu-id="8db98-140">Which method you follow depends on how you installed the AzureRM module.</span></span>
<span data-ttu-id="8db98-141">Se non si è sicuri del metodo di installazione originale, seguire prima i passaggi per la disinstallazione di un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="8db98-141">If you're not sure of your original install method, follow the steps for uninstalling an MSI first.</span></span>

### <a name="uninstall-azure-powershell-msi"></a><span data-ttu-id="8db98-142">Disinstallare l'identità del servizio gestita di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8db98-142">Uninstall Azure PowerShell MSI</span></span>

<span data-ttu-id="8db98-143">Se i moduli AzureRM di Azure PowerShell sono stati installati con il pacchetto MSI, la disinstallazione deve essere eseguita tramite il sistema Windows anziché PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8db98-143">If you installed the Azure PowerShell AzureRM modules using the MSI package, you must uninstall through the Windows system rather than PowerShell.</span></span>

| <span data-ttu-id="8db98-144">Piattaforma</span><span class="sxs-lookup"><span data-stu-id="8db98-144">Platform</span></span> | <span data-ttu-id="8db98-145">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="8db98-145">Instructions</span></span> |
|----------|--------------|
| <span data-ttu-id="8db98-146">Windows 10</span><span class="sxs-lookup"><span data-stu-id="8db98-146">Windows 10</span></span> | <span data-ttu-id="8db98-147">Start > Impostazioni > App</span><span class="sxs-lookup"><span data-stu-id="8db98-147">Start > Settings > Apps</span></span> |
| <span data-ttu-id="8db98-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8db98-148">Windows 7</span></span> </br><span data-ttu-id="8db98-149">Windows 8</span><span class="sxs-lookup"><span data-stu-id="8db98-149">Windows 8</span></span> | <span data-ttu-id="8db98-150">Start > Pannello di controllo -> Programmi -> Disinstalla un programma</span><span class="sxs-lookup"><span data-stu-id="8db98-150">Start > Control Panel > Programs > Uninstall a program</span></span> |

<span data-ttu-id="8db98-151">In questa schermata dovrebbe essere visualizzata l'opzione __Azure PowerShell__ o __Microsoft Azure PowerShell - Mese/anno__ nell'elenco dei programmi.</span><span class="sxs-lookup"><span data-stu-id="8db98-151">Once on this screen you should see __Azure PowerShell__ or __Microsoft Azure PowerShell - Month Year__ in the program listing.</span></span> <span data-ttu-id="8db98-152">Si tratta dell'app da disinstallare.</span><span class="sxs-lookup"><span data-stu-id="8db98-152">This is the app to uninstall.</span></span> <span data-ttu-id="8db98-153">Se questo programma non è elencato, l'installazione è stata eseguita tramite PowerShellGet ed è necessario seguire la prossima serie di istruzioni.</span><span class="sxs-lookup"><span data-stu-id="8db98-153">If you don't see this program listed, then you installed through PowerShellGet, and should follow the next set of instructions.</span></span>

### <a name="uninstall-from-powershell"></a><span data-ttu-id="8db98-154">Eseguire la disinstallazione da PowerShell</span><span class="sxs-lookup"><span data-stu-id="8db98-154">Uninstall from PowerShell</span></span>

<span data-ttu-id="8db98-155">Se AzureRM è stato installato con PowerShellGet, è possibile rimuovere i moduli con il comando [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm), disponibile come parte del modulo `Az.Accounts`.</span><span class="sxs-lookup"><span data-stu-id="8db98-155">If you installed AzureRM with PowerShellGet, then you can remove the modules with the [Uninstall-AzureRM](/powershell/module/az.accounts/uninstall-azurerm) command, available as part of the `Az.Accounts` module.</span></span> <span data-ttu-id="8db98-156">Questa operazione rimuove _tutti_ i moduli AzureRM dal computer, ma richiede i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="8db98-156">This removes _all_ AzureRM modules from your machine, but requires administrator privileges.</span></span>

```powershell-interactive
Uninstall-AzureRm
```
<span data-ttu-id="8db98-157">o</span><span class="sxs-lookup"><span data-stu-id="8db98-157">or</span></span>
```powershell-interactive
Uninstall-Module AzureRm
```

<span data-ttu-id="8db98-158">Se non è possibile eseguire correttamente il comando `Uninstall-AzureRM`, usare lo [script`Uninstall-AllModules`](#uninstall-script) fornito in questo articolo con la chiamata seguente:</span><span class="sxs-lookup"><span data-stu-id="8db98-158">If you can't successfully run the `Uninstall-AzureRM` command, use the [`Uninstall-AllModules` script](#uninstall-script) provided in this article with the following invocation:</span></span>

```powershell-interactive
$versions = (Get-InstalledModule AzureRM -AllVersions | Select-Object Version)
$versions | foreach { Uninstall-AllModules -TargetModule AzureRM -Version ($_.Version) -Force }
```
<span data-ttu-id="8db98-159">o</span><span class="sxs-lookup"><span data-stu-id="8db98-159">or</span></span>
```powershell-interactive
foreach ($module in (Get-Module -ListAvailable AzureRM*).Name |Get-Unique) {
   write-host "Removing Module $module"
   Uninstall-module $module
}
```
