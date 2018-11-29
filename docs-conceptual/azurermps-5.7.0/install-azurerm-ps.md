---
title: Installare Azure PowerShell in Windows con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.openlocfilehash: 5f7f65aa25d86feb77a85fc28d122118216542cc
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2018
ms.locfileid: "52588044"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="ff8ab-103">Installare Azure PowerShell in Windows con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="ff8ab-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

<span data-ttu-id="ff8ab-104">Questo articolo illustra l'installazione dei moduli di Azure PowerShell in ambiente Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span> <span data-ttu-id="ff8ab-105">PowerShellGet con la gestione dei moduli rappresenta la modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="ff8ab-106">Per istruzioni su come installare Azure PowerShell in altre piattaforme, vedere [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-106">For instructions to install Azure PowerShell on other platforms, see [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="ff8ab-107">Il modello di distribuzione classica di Azure non è supportato da questa versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-107">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="ff8ab-108">Per il supporto delle distribuzioni classiche, seguire le istruzioni in [Installare il modulo Gestione dei servizi di Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-108">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8ab-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ff8ab-109">Requirements</span></span>

<span data-ttu-id="ff8ab-110">Per installare Azure PowerShell è necessario PowerShellGet versione 1.1.2.0 o superiore.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-110">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="ff8ab-111">Per verificare se è disponibile nel sistema, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-111">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="ff8ab-112">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-112">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="ff8ab-113">Se è necessario aggiornare l'installazione di PowerShellGet, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-113">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="ff8ab-114">Se PowerShellGet non è installato, vedere le istruzioni nella tabella seguente per il proprio sistema.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-114">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="ff8ab-115">Scenario</span><span class="sxs-lookup"><span data-stu-id="ff8ab-115">Scenario</span></span>|<span data-ttu-id="ff8ab-116">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="ff8ab-116">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="ff8ab-117">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ff8ab-117">Windows 10</span></span><br/><span data-ttu-id="ff8ab-118">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ff8ab-118">Windows Server 2016</span></span>|<span data-ttu-id="ff8ab-119">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="ff8ab-119">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="ff8ab-120">Eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="ff8ab-120">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="ff8ab-121">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="ff8ab-121">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="ff8ab-122">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-122">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="ff8ab-123">Windows con PowerShell 3 o PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="ff8ab-123">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="ff8ab-124"><il>[Ottenere i moduli PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="ff8ab-124"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="ff8ab-125">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-125">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="ff8ab-126">L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-126">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="ff8ab-127">Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-127">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="ff8ab-128">Il modulo illustrato in questo documento, AzureRM, usa .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-128">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="ff8ab-129">Non è quindi compatibile con PowerShell 6.0, che usa .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-129">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="ff8ab-130">Se si usa PowerShell 6.0, seguire le [istruzioni di installazione per macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-130">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="ff8ab-131">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff8ab-131">Install the Azure PowerShell module</span></span>

<span data-ttu-id="ff8ab-132">Sono necessari privilegi elevati per installare i moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-132">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="ff8ab-133">Per installare Azure PowerShell, eseguire questo comando seguente in una sessione con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-133">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="ff8ab-134">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-134">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="ff8ab-135">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-135">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="ff8ab-136">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="ff8ab-136">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="ff8ab-137">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-137">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="ff8ab-138">Il modulo `AzureRM` è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-138">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ff8ab-139">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-139">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="ff8ab-140">Accesso</span><span class="sxs-lookup"><span data-stu-id="ff8ab-140">Sign in</span></span>

<span data-ttu-id="ff8ab-141">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-141">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="ff8ab-142">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-142">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="ff8ab-143">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-143">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="ff8ab-144">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-144">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="ff8ab-145">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff8ab-145">Update the Azure PowerShell module</span></span>

<span data-ttu-id="ff8ab-146">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-146">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="ff8ab-147">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-147">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="ff8ab-148">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-148">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="ff8ab-149">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ff8ab-149">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="ff8ab-150">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-150">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="ff8ab-151">Potrebbero essere necessarie più versioni se si usano risorse di Azure Stack locali, si esegue una versione precedente di Windows che non può essere aggiornata a PowerShell 5.0 oppure si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-151">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="ff8ab-152">Per installare una versione precedente, specificare l'argomento `-RequiredVersion` durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-152">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="ff8ab-153">Quando si carica il modulo Azure PowerShell, viene caricata la versione più recente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-153">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="ff8ab-154">Per caricare una versione diversa, specificare l'argomento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-154">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="ff8ab-155">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="ff8ab-155">Provide feedback</span></span>

<span data-ttu-id="ff8ab-156">Se si trova un bug quando si usa Azure Powershell, [registrare un problema su GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-156">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="ff8ab-157">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="ff8ab-157">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ff8ab-158">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="ff8ab-158">Next Steps</span></span>

<span data-ttu-id="ff8ab-159">Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.</span><span class="sxs-lookup"><span data-stu-id="ff8ab-159">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
