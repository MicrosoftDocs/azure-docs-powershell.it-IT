---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 269119333b2197a15ed7bb50e3e5d90588456174
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2019
ms.locfileid: "59363712"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="8b42b-103">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b42b-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="8b42b-104">Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="8b42b-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="8b42b-105">Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="8b42b-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="8b42b-106">Per il modulo Az non sono attualmente supportati altri metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="8b42b-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b42b-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8b42b-107">Requirements</span></span>

<span data-ttu-id="8b42b-108">Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell 6 in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="8b42b-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell 6 on any platform.</span></span>
<span data-ttu-id="8b42b-109">Per controllare la versione di PowerShell, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="8b42b-109">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="8b42b-110">Se si ha una versione obsoleta o è necessario installare PowerShell, vedere [Installazione di varie versioni di PowerShell](/powershell/scripting/setup/installing-powershell).</span><span class="sxs-lookup"><span data-stu-id="8b42b-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](/powershell/scripting/setup/installing-powershell).</span></span> <span data-ttu-id="8b42b-111">In tale pagina sono disponibili collegamenti a informazioni sull'installazione per la piattaforma in uso.</span><span class="sxs-lookup"><span data-stu-id="8b42b-111">Install information for your platform is linked from that page.</span></span>

<span data-ttu-id="8b42b-112">Se si usa PowerShell 5 in Windows, è necessario che sia installato anche .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="8b42b-112">If you are using PowerShell 5 on Windows, you also need .NET Framework 4.7.2 installed.</span></span> <span data-ttu-id="8b42b-113">Per istruzioni su come aggiornare o installare una nuova versione di .NET Framework, vedere la [Guida all'installazione di .NET Framework](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="8b42b-113">For instructions on updating or installing a new version of .NET Framework, see the [.NET Framework installation guide](/dotnet/framework/install).</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="8b42b-114">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b42b-114">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="8b42b-115">I moduli AzureRM e Az possono essere installati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="8b42b-115">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="8b42b-116">Se sono installati entrambi i moduli, __non abilitare gli alias__.</span><span class="sxs-lookup"><span data-stu-id="8b42b-116">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="8b42b-117">L'abilitazione degli alias causerà conflitti tra i cmdlet di AzureRM e gli alias dei comandi di Az e potrebbe determinare comportamenti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="8b42b-117">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="8b42b-118">È consigliabile disinstallare AzureRM prima di installare il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="8b42b-118">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="8b42b-119">È sempre possibile disinstallare AzureRM o abilitare gli alias in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="8b42b-119">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="8b42b-120">Per altre informazioni sugli alias dei comandi di AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-120">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="8b42b-121">Per istruzioni sulla disinstallazione, vedere [Disinstallare il modulo AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="8b42b-121">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="8b42b-122">Per installare i moduli in un ambito globale, sono necessari privilegi elevati per l'installazione di moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="8b42b-122">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="8b42b-123">Per installare Azure PowerShell, eseguire questo comando in una sessione con privilegi elevati ("Esegui come amministratore" in Windows o con diritti di utente con privilegi avanzati in macOS o Linux):</span><span class="sxs-lookup"><span data-stu-id="8b42b-123">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="8b42b-124">Se non si ha accesso a privilegi di amministratore, è possibile eseguire l'installazione per l'utente corrente aggiungendo l'argomento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="8b42b-124">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="8b42b-125">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="8b42b-125">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="8b42b-126">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="8b42b-126">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="8b42b-127">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="8b42b-127">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="8b42b-128">Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b42b-128">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8b42b-129">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b42b-129">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="8b42b-130">Accesso</span><span class="sxs-lookup"><span data-stu-id="8b42b-130">Sign in</span></span>

<span data-ttu-id="8b42b-131">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="8b42b-131">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="8b42b-132">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="8b42b-132">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="8b42b-133">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="8b42b-133">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="8b42b-134">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="8b42b-134">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="8b42b-135">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-135">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="8b42b-136">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b42b-136">Update the Azure PowerShell module</span></span>

<span data-ttu-id="8b42b-137">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="8b42b-137">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="8b42b-138">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="8b42b-138">This command does __not__ uninstall older versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="8b42b-139">Per informazioni su come rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-139">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="8b42b-140">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b42b-140">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="8b42b-141">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8b42b-141">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="8b42b-142">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="8b42b-142">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="8b42b-143">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-143">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="8b42b-144">È possibile installare o caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="8b42b-144">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="8b42b-145">Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="8b42b-145">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="8b42b-146">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="8b42b-146">Provide feedback</span></span>

<span data-ttu-id="8b42b-147">Se si trova un bug in Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="8b42b-147">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="8b42b-148">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="8b42b-148">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="8b42b-149">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="8b42b-149">Next Steps</span></span>

<span data-ttu-id="8b42b-150">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-150">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="8b42b-151">Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="8b42b-151">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
