---
title: Installare il modulo 'Az' di Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet in Windows, macOS e Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/26/2018
ms.openlocfilehash: 3d52b18750341f220dc8e10d6bf89796457c5a10
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/13/2018
ms.locfileid: "53216998"
---
# <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="e5769-103">Installare il modulo 'Az' di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5769-103">Install the Azure PowerShell 'Az' module</span></span>

<span data-ttu-id="e5769-104">Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e5769-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="e5769-105">Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="e5769-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="e5769-106">Per la versione di anteprima di Az non sono supportati altri metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="e5769-106">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="e5769-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e5769-107">Requirements</span></span>

<span data-ttu-id="e5769-108">Azure PowerShell è compatibile con PowerShell 5.x in Windows o con PowerShell 6.x in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="e5769-108">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="e5769-109">Per verificare la versione di PowerShell eseguita nel computer, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="e5769-109">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="e5769-110">Se si ha una versione obsoleta o è necessario installare PowerShell, vedere [Installazione di varie versioni di PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="e5769-110">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="e5769-111">In tale pagina sono disponibili collegamenti a informazioni sull'installazione per la piattaforma in uso.</span><span class="sxs-lookup"><span data-stu-id="e5769-111">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="e5769-112">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5769-112">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="e5769-113">I moduli `AzureRM` e `Az` possono essere installati contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="e5769-113">You can have both the `AzureRM` and `Az` modules installed at the same time.</span></span> <span data-ttu-id="e5769-114">Se sono installati entrambi i moduli, __non abilitare gli alias__.</span><span class="sxs-lookup"><span data-stu-id="e5769-114">If you have both modules installed, __don't enable aliases__.</span></span>
> <span data-ttu-id="e5769-115">L'abilitazione degli alias causerà conflitti tra i cmdlet di `AzureRM` e gli alias dei comandi di `Az` e potrebbe determinare comportamenti imprevisti.</span><span class="sxs-lookup"><span data-stu-id="e5769-115">Enabling aliases will cause conflicts between `AzureRM` cmdlets and `Az` command aliases, and could cause unexpected behavior.</span></span>
> <span data-ttu-id="e5769-116">È consigliabile disinstallare `AzureRM` prima di installare il modulo `Az`.</span><span class="sxs-lookup"><span data-stu-id="e5769-116">It's recommended that before installing the `Az` module, you uninstall `AzureRM`.</span></span> <span data-ttu-id="e5769-117">È sempre possibile disinstallare `AzureRM` o abilitare gli alias in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e5769-117">You can always uninstall `AzureRM` or enable aliases at any time.</span></span> <span data-ttu-id="e5769-118">Per istruzioni per la disinstallazione, vedere l'articolo su come [disinstallare il modulo AzureRM di Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e5769-118">For uninstall instructions, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span> 

<span data-ttu-id="e5769-119">Per installare i moduli in un ambito globale, sono necessari privilegi elevati per l'installazione di moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="e5769-119">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="e5769-120">Per installare Azure PowerShell, eseguire questo comando in una sessione con privilegi elevati ("Esegui come amministratore" in Windows o con diritti di utente con privilegi avanzati in macOS o Linux):</span><span class="sxs-lookup"><span data-stu-id="e5769-120">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="e5769-121">Se non si ha accesso a privilegi di amministratore, è possibile eseguire l'installazione per l'utente corrente aggiungendo l'argomento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="e5769-121">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="e5769-122">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e5769-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="e5769-123">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="e5769-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="e5769-124">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="e5769-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="e5769-125">Il modulo `Az` è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5769-125">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="e5769-126">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5769-126">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="e5769-127">Accesso</span><span class="sxs-lookup"><span data-stu-id="e5769-127">Sign in</span></span>

<span data-ttu-id="e5769-128">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e5769-128">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="e5769-129">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="e5769-129">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="e5769-130">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="e5769-130">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="e5769-131">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="e5769-131">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="e5769-132">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e5769-132">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="e5769-133">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5769-133">Update the Azure PowerShell module</span></span>

<span data-ttu-id="e5769-134">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="e5769-134">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="e5769-135">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="e5769-135">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="e5769-136">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e5769-136">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="e5769-137">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e5769-137">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="e5769-138">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e5769-138">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="e5769-139">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="e5769-139">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="e5769-140">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="e5769-140">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="e5769-141">È possibile caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion` con `Install-Module` e `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="e5769-141">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` and `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="e5769-142">Se sono installate più versioni del modulo, viene caricata per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="e5769-142">If you have more than one version of the module installed, the latest version is loaded by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="e5769-143">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="e5769-143">Provide feedback</span></span>

<span data-ttu-id="e5769-144">Se si trova un bug quando si usa Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="e5769-144">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="e5769-145">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="e5769-145">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e5769-146">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="e5769-146">Next Steps</span></span>

<span data-ttu-id="e5769-147">Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.</span><span class="sxs-lookup"><span data-stu-id="e5769-147">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>
