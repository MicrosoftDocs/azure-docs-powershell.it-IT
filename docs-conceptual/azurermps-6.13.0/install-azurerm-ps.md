---
title: Installare Azure PowerShell in Windows con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: 5de386bde1b8be5a4455b85d4f5fcdf38e4fcea2
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "65535023"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="e4a12-103">Installare Azure PowerShell in Windows con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="e4a12-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="e4a12-104">Questo articolo illustra l'installazione dei moduli di Azure PowerShell per PowerShell 5.x per Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e4a12-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="e4a12-105">PowerShellGet con la gestione dei moduli rappresenta la modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="e4a12-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="e4a12-106">Il modello di distribuzione classica di Azure non è supportato da questa versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4a12-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="e4a12-107">Per il supporto delle distribuzioni classiche, seguire le istruzioni in [Installare il modulo Gestione dei servizi di Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="e4a12-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4a12-108">Il modulo AzureRM non è supportato per macOS o Linux.</span><span class="sxs-lookup"><span data-stu-id="e4a12-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="e4a12-109">Per usare i cmdlet di Azure PowerShell in queste piattaforme [installare il modulo Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="e4a12-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4a12-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e4a12-110">Requirements</span></span>

<span data-ttu-id="e4a12-111">A partire da Azure PowerShell versione 6.0, Azure PowerShell richiede PowerShell versione 5.0.</span><span class="sxs-lookup"><span data-stu-id="e4a12-111">Starting with Azure PowerShell version 6.0, Azure PowerShell requires PowerShell version 5.0.</span></span> <span data-ttu-id="e4a12-112">Per verificare la versione di PowerShell eseguita nel computer, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="e4a12-112">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="e4a12-113">Se è presente una versione obsoleta, vedere [Aggiornamento di Windows PowerShell esistente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="e4a12-113">If you have an outdated version, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4a12-114">Il modulo illustrato in questo documento, AzureRM, usa .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="e4a12-114">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="e4a12-115">Non è quindi compatibile con PowerShell 6.0, che usa .NET Core.</span><span class="sxs-lookup"><span data-stu-id="e4a12-115">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="e4a12-116">Se si usa PowerShell 6.0, seguire le [istruzioni di installazione per macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="e4a12-116">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e4a12-117">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4a12-117">Install the Azure PowerShell module</span></span>

<span data-ttu-id="e4a12-118">Sono necessari privilegi elevati per installare i moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="e4a12-118">You need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e4a12-119">Per installare Azure PowerShell, eseguire questo comando seguente in una sessione con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="e4a12-119">To install Azure PowerShell, run the following command in an elevated session:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -AllowClobber
```

> [!NOTE]
> <span data-ttu-id="e4a12-120">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="e4a12-120">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="e4a12-121">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e4a12-121">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e4a12-122">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="e4a12-122">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e4a12-123">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e4a12-123">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e4a12-124">Il modulo `AzureRM` è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4a12-124">The `AzureRM` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e4a12-125">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4a12-125">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e4a12-126">Accesso</span><span class="sxs-lookup"><span data-stu-id="e4a12-126">Sign in</span></span>

<span data-ttu-id="e4a12-127">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a12-127">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="e4a12-128">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="e4a12-128">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="e4a12-129">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="e4a12-129">Because of the way the module is structured, this can take a few seconds.</span></span>


<span data-ttu-id="e4a12-130">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="e4a12-130">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e4a12-131">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e4a12-131">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e4a12-132">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4a12-132">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e4a12-133">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="e4a12-133">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e4a12-134">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e4a12-134">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name AzureRM
```

<span data-ttu-id="e4a12-135">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e4a12-135">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e4a12-136">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e4a12-136">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e4a12-137">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e4a12-137">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e4a12-138">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e4a12-138">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name AzureRM -AllVersions | select Name,Version
```

<span data-ttu-id="e4a12-139">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e4a12-139">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="e4a12-140">Potrebbero essere necessarie più versioni se si usano risorse di Azure Stack locali, si esegue una versione meno recente di Windows oppure si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4a12-140">You might need more than one version if you work with on-premises Azure Stack resources, run an older version of Windows, or use the Azure classic deployment model.</span></span> <span data-ttu-id="e4a12-141">Per installare una versione precedente, specificare l'argomento `-RequiredVersion` durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e4a12-141">To install an older version, provide the `-RequiredVersion` argument when installing.</span></span>

```powershell-interactive
# Install version 2.3.0 of Azure PowerShell
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="e4a12-142">Quando si carica il modulo Azure PowerShell, viene caricata la versione più recente per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e4a12-142">When loading the Azure PowerShell module the latest version is loaded by default.</span></span> <span data-ttu-id="e4a12-143">Per caricare una versione diversa, specificare l'argomento `-RequiredVersion`.</span><span class="sxs-lookup"><span data-stu-id="e4a12-143">To load a different version, provide the `-RequiredVersion` argument.</span></span>

```powershell-interactive
# Load version 2.3.0 of Azure PowerShell
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

## <a name="provide-feedback"></a><span data-ttu-id="e4a12-144">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="e4a12-144">Provide feedback</span></span>

<span data-ttu-id="e4a12-145">Se si trova un bug quando si usa Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e4a12-145">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e4a12-146">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/azurerm.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="e4a12-146">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/azurerm.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e4a12-147">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="e4a12-147">Next Steps</span></span>

<span data-ttu-id="e4a12-148">Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e4a12-148">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
