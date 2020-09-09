---
title: Installare Azure PowerShell in Windows con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/15/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c287afa2fb34938cac7304028071afd7deedb263
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243787"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="624df-103">Installare Azure PowerShell in Windows con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="624df-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

<span data-ttu-id="624df-104">Questo articolo illustra l'installazione dei moduli di Azure PowerShell per PowerShell 5.x per Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="624df-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="624df-105">PowerShellGet con la gestione dei moduli rappresenta la modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="624df-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="624df-106">Il modello di distribuzione classica di Azure non è supportato da questa versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624df-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="624df-107">Per il supporto delle distribuzioni classiche, seguire le istruzioni in [Installare il modulo Gestione dei servizi di Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="624df-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="624df-108">Il modulo AzureRM non è supportato per macOS o Linux.</span><span class="sxs-lookup"><span data-stu-id="624df-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="624df-109">Per usare i cmdlet di Azure PowerShell in queste piattaforme [installare il modulo Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="624df-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="624df-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="624df-110">Requirements</span></span>

<span data-ttu-id="624df-111">Per installare Azure PowerShell è necessario PowerShellGet versione 1.1.2.0 o superiore.</span><span class="sxs-lookup"><span data-stu-id="624df-111">To install Azure PowerShell, you need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="624df-112">Per verificare se è disponibile nel sistema, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="624df-112">To check if it is available on your system, run the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name PowerShellGet -AllVersions | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="624df-113">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="624df-113">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="624df-114">Se è necessario aggiornare l'installazione di PowerShellGet, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="624df-114">If you need to update your installation of PowerShellGet, run the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="624df-115">Se PowerShellGet non è installato, vedere le istruzioni nella tabella seguente per il proprio sistema.</span><span class="sxs-lookup"><span data-stu-id="624df-115">If you don't have PowerShellGet installed, follow the instructions in the table below for your system.</span></span>

|<span data-ttu-id="624df-116">Scenario</span><span class="sxs-lookup"><span data-stu-id="624df-116">Scenario</span></span>|<span data-ttu-id="624df-117">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="624df-117">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="624df-118">Windows 10</span><span class="sxs-lookup"><span data-stu-id="624df-118">Windows 10</span></span><br/><span data-ttu-id="624df-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="624df-119">Windows Server 2016</span></span>|<span data-ttu-id="624df-120">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="624df-120">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="624df-121">Eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="624df-121">Upgrade to PowerShell 5</span></span>| <ol><li>[<span data-ttu-id="624df-122">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="624df-122">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)</li><li><span data-ttu-id="624df-123">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="624df-123">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="624df-124">Windows con PowerShell 3 o PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="624df-124">Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="624df-125"><il>[Ottenere i moduli PackageManagement](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="624df-125"><il>[Get the PackageManagement modules](https://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="624df-126">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="624df-126">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

> [!NOTE]
> <span data-ttu-id="624df-127">L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script.</span><span class="sxs-lookup"><span data-stu-id="624df-127">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="624df-128">Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="624df-128">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="624df-129">Il modulo illustrato in questo documento, AzureRM, usa .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="624df-129">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="624df-130">Non è quindi compatibile con PowerShell 6.0, che usa .NET Core.</span><span class="sxs-lookup"><span data-stu-id="624df-130">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="624df-131">Se si usa PowerShell 6.0, seguire le [istruzioni di installazione per macOS e Linux](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="624df-131">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](/powershell/azure/install-az-ps).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="624df-132">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="624df-132">Install the Azure PowerShell module</span></span>

<span data-ttu-id="624df-133">Sono necessari privilegi elevati per installare i moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="624df-133">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="624df-134">Per installare Azure PowerShell, eseguire questo comando seguente in una sessione con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="624df-134">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM
```

> [!NOTE]
> <span data-ttu-id="624df-135">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="624df-135">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="624df-136">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="624df-136">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="624df-137">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="624df-137">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="624df-138">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="624df-138">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="624df-139">Il modulo `AzureRM` è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624df-139">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="624df-140">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="624df-140">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="624df-141">Accesso</span><span class="sxs-lookup"><span data-stu-id="624df-141">Sign in</span></span>

<span data-ttu-id="624df-142">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="624df-142">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="624df-143">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="624df-143">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="624df-144">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="624df-144">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="624df-145">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="624df-145">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="624df-146">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="624df-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="624df-147">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="624df-147">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="624df-148">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="624df-148">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="624df-149">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="624df-149">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="624df-150">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="624df-150">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="624df-151">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="624df-151">It's possible to install multiple versions of Azure PowerShell.</span></span> <span data-ttu-id="624df-152">Potrebbero essere necessarie più versioni se si usano risorse di Azure Stack locali, si esegue una versione precedente di Windows che non può essere aggiornata a PowerShell 5.0 oppure si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="624df-152">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows that you can't update to PowerShell 5.0, or use the Azure classic deployment model.</span></span> <span data-ttu-id="624df-153">Per installare una versione precedente, specificare l'argomento `-RequiredVersion` durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="624df-153">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="624df-154">Quando si carica il modulo Azure PowerShell, viene caricata la versione più recente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="624df-154">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="624df-155">Per caricare una versione diversa, specificare l'argomento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="624df-155">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="624df-156">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="624df-156">Provide feedback</span></span>

<span data-ttu-id="624df-157">Se si trova un bug quando si usa Azure Powershell, [registrare un problema su GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="624df-157">If you find a bug when using Azure Powershell, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="624df-158">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="624df-158">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="624df-159">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="624df-159">Next Steps</span></span>

<span data-ttu-id="624df-160">Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.</span><span class="sxs-lookup"><span data-stu-id="624df-160">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
