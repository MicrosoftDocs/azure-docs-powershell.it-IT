---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: d99265c7f156622d876d700106e2b06dd729e8b8
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365734"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="1763e-103">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1763e-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="1763e-104">Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1763e-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="1763e-105">Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="1763e-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="1763e-106">Per il modulo Az non sono attualmente supportati altri metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="1763e-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1763e-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1763e-107">Requirements</span></span>

<span data-ttu-id="1763e-108">Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell Core 6.x e versioni successive in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="1763e-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="1763e-109">Se non si è sicuri di avere PowerShell o se si usa macOS o Linux, [installare la versione più recente di PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="1763e-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="1763e-110">Per controllare la versione di PowerShell, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="1763e-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="1763e-111">Per eseguire Azure PowerShell in PowerShell 5.1 in Windows:</span><span class="sxs-lookup"><span data-stu-id="1763e-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="1763e-112">Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="1763e-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="1763e-113">Se si usa Windows 10, PowerShell 5.1 è già installato.</span><span class="sxs-lookup"><span data-stu-id="1763e-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="1763e-114">Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="1763e-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="1763e-115">Quando si usa PowerShell Core, non sono previsti requisiti aggiuntivi per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1763e-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="1763e-116">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1763e-116">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1763e-117">I moduli AzureRM e Az possono essere installati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="1763e-117">You can have both the AzureRM and Az modules installed at the same time.</span></span> <span data-ttu-id="1763e-118">Se sono installati entrambi i moduli, __non abilitare gli alias__.</span><span class="sxs-lookup"><span data-stu-id="1763e-118">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="1763e-119">L'abilitazione degli alias causerà conflitti tra i cmdlet di AzureRM e gli alias dei comandi di Az e potrebbe determinare comportamenti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="1763e-119">Enabling aliases will cause conflicts between AzureRM cmdlets and Az command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="1763e-120">È consigliabile disinstallare AzureRM prima di installare il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="1763e-120">It's recommended that before installing the Az module, you uninstall AzureRM.</span></span> <span data-ttu-id="1763e-121">È sempre possibile disinstallare AzureRM o abilitare gli alias in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="1763e-121">You can always uninstall AzureRM or enable aliases at any time.</span></span> <span data-ttu-id="1763e-122">Per altre informazioni sugli alias dei comandi di AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-122">To learn about the AzureRM command aliases, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
> <span data-ttu-id="1763e-123">Per istruzioni sulla disinstallazione, vedere [Disinstallare il modulo AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="1763e-123">For uninstall instructions, see [Uninstall the AzureRM module](uninstall-az-ps.md#uninstall-the-azurerm-module).</span></span> 

<span data-ttu-id="1763e-124">Per installare i moduli in un ambito globale, sono necessari privilegi elevati per l'installazione di moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="1763e-124">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="1763e-125">Per installare Azure PowerShell, eseguire questo comando in una sessione con privilegi elevati ("Esegui come amministratore" in Windows o con diritti di utente con privilegi avanzati in macOS o Linux):</span><span class="sxs-lookup"><span data-stu-id="1763e-125">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="1763e-126">Se non si ha accesso a privilegi di amministratore, è possibile eseguire l'installazione per l'utente corrente aggiungendo l'argomento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="1763e-126">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="1763e-127">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="1763e-127">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="1763e-128">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="1763e-128">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="1763e-129">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1763e-129">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="1763e-130">Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1763e-130">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1763e-131">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1763e-131">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="1763e-132">Accesso</span><span class="sxs-lookup"><span data-stu-id="1763e-132">Sign in</span></span>

<span data-ttu-id="1763e-133">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="1763e-133">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="1763e-134">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="1763e-134">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="1763e-135">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="1763e-135">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="1763e-136">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="1763e-136">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="1763e-137">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-137">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="1763e-138">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1763e-138">Update the Azure PowerShell module</span></span>

<span data-ttu-id="1763e-139">In considerazione della modalità di creazione del pacchetto del modulo Az, il comando [Update-Module](/powershell/module/powershellget/update-module) non consente di aggiornare correttamente l'installazione.</span><span class="sxs-lookup"><span data-stu-id="1763e-139">Because of how the Az module is package, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="1763e-140">AZ è tecnicamente un metamodulo e comprende tutti i moduli secondari contenenti i cmdlet per interagire con i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="1763e-140">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="1763e-141">Per aggiornare il modulo Azure PowerShell, è quindi necessario __reinstallarlo__, anziché semplicemente __aggiornarlo__.</span><span class="sxs-lookup"><span data-stu-id="1763e-141">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="1763e-142">L'operazione è analoga all'installazione, ma può essere necessario aggiungere l'argomento `-Force`:</span><span class="sxs-lookup"><span data-stu-id="1763e-142">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="1763e-143">Anche se questa operazione può comportare la sovrascrittura di moduli installati, è comunque possibile che nel sistema siano ancora presenti versioni meno recenti.</span><span class="sxs-lookup"><span data-stu-id="1763e-143">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="1763e-144">Per informazioni su come rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-144">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="1763e-145">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1763e-145">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="1763e-146">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1763e-146">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="1763e-147">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="1763e-147">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="1763e-148">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-148">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="1763e-149">È possibile installare o caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="1763e-149">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="1763e-150">Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="1763e-150">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="1763e-151">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="1763e-151">Provide feedback</span></span>

<span data-ttu-id="1763e-152">Se si trova un bug in Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="1763e-152">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="1763e-153">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="1763e-153">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1763e-154">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="1763e-154">Next Steps</span></span>

<span data-ttu-id="1763e-155">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-155">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="1763e-156">Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1763e-156">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
