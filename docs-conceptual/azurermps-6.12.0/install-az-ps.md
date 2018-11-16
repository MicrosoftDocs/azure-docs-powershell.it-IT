---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: c4af07816aaa6713d67e3349a45880f8cc22c80a
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574499"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="55d6a-103">Installare Azure PowerShell con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="55d6a-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="55d6a-104">Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="55d6a-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="55d6a-105">Per la versione di anteprima di Az non sono supportati altri metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="55d6a-105">For the preview release of Az, no other install methods are supported.</span></span> 

## <a name="requirements"></a><span data-ttu-id="55d6a-106">Requisiti</span><span class="sxs-lookup"><span data-stu-id="55d6a-106">Requirements</span></span>

<span data-ttu-id="55d6a-107">Azure PowerShell è compatibile con PowerShell 5.x in Windows o con PowerShell 6.x in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="55d6a-107">Azure PowerShell works with either PowerShell 5.x on Windows, or PowerShell 6.x on any platform.</span></span> <span data-ttu-id="55d6a-108">Per verificare la versione di PowerShell eseguita nel computer, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="55d6a-108">To check the version of PowerShell running on your machine, run the following command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="55d6a-109">Se si ha una versione obsoleta o è necessario installare PowerShell, vedere [Installazione di varie versioni di PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span><span class="sxs-lookup"><span data-stu-id="55d6a-109">If you have an outdated version or need to install PowerShell, see [Installing various versions of PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/setup/installing-powershell?view=powershell-6).</span></span> <span data-ttu-id="55d6a-110">In tale pagina sono disponibili collegamenti a informazioni sull'installazione per la piattaforma in uso.</span><span class="sxs-lookup"><span data-stu-id="55d6a-110">Install information for your platform is linked from that page.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="55d6a-111">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55d6a-111">Install the Azure PowerShell module</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="55d6a-112">I moduli `AzureRM` e `Az` non dovrebbero essere installati contemporaneamente in un sistema.</span><span class="sxs-lookup"><span data-stu-id="55d6a-112">You shouldn't have both the `AzureRM` and `Az` modules installed on a system at the same time.</span></span> <span data-ttu-id="55d6a-113">Per installare il modulo `Az`, è necessario disinstallare `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="55d6a-113">In order to install the `Az` module, `AzureRM` must be uninstalled.</span></span> <span data-ttu-id="55d6a-114">Per istruzioni sulla procedura da seguire, vedere l'articolo su come [disinstallare il modulo AzureRM di Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="55d6a-114">For instructions on how to do that, see [Uninstall the Azure PowerShell module (AzureRM)](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="55d6a-115">Per installare i moduli in un ambito globale, sono necessari privilegi elevati per l'installazione di moduli da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="55d6a-115">To install modules at a global scope, you need elevated privileges to install modules from the PowerShell Gallery.</span></span> <span data-ttu-id="55d6a-116">Per installare Azure PowerShell, eseguire questo comando in una sessione con privilegi elevati ("Esegui come amministratore" in Windows o con diritti di utente con privilegi avanzati in macOS o Linux):</span><span class="sxs-lookup"><span data-stu-id="55d6a-116">To install Azure PowerShell, run the following command in an elevated session ("Run as Administrator" on Windows, or with superuser privileges on macOS or Linux):</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber
```

<span data-ttu-id="55d6a-117">Se non si ha accesso a privilegi di amministratore, è possibile eseguire l'installazione per l'utente corrente aggiungendo l'argomento `-Scope`.</span><span class="sxs-lookup"><span data-stu-id="55d6a-117">If you don't have access to administrator privileges, you can install for the current user by adding the `-Scope` argument.</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="55d6a-118">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="55d6a-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="55d6a-119">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="55d6a-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="55d6a-120">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="55d6a-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="55d6a-121">Il modulo `Az` è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="55d6a-121">The `Az` module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="55d6a-122">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55d6a-122">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="sign-in"></a><span data-ttu-id="55d6a-123">Accesso</span><span class="sxs-lookup"><span data-stu-id="55d6a-123">Sign in</span></span>

<span data-ttu-id="55d6a-124">Per iniziare a usare Azure PowerShell è necessario caricare `Az` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="55d6a-124">To start working with Azure PowerShell, you need to load `Az` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

<span data-ttu-id="55d6a-125">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="55d6a-125">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="55d6a-126">L'importazione automatica del modulo `Az` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="55d6a-126">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="55d6a-127">Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="55d6a-127">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="55d6a-128">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55d6a-128">Update the Azure PowerShell module</span></span>

<span data-ttu-id="55d6a-129">È possibile aggiornare l'installazione di Azure PowerShell eseguendo [Update-Module](/powershell/module/powershellget/update-module).</span><span class="sxs-lookup"><span data-stu-id="55d6a-129">You can update your Azure PowerShell installation by running [Update-Module](/powershell/module/powershellget/update-module).</span></span> <span data-ttu-id="55d6a-130">Questo comando __non__ disinstalla le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="55d6a-130">This command does __not__ uninstall earlier versions.</span></span>

```powershell-interactive
Update-Module -Name Az
```

<span data-ttu-id="55d6a-131">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="55d6a-131">If you want to remove older versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="55d6a-132">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="55d6a-132">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="55d6a-133">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="55d6a-133">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="55d6a-134">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="55d6a-134">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-Module -Name Az -List | select Name,Version
```

<span data-ttu-id="55d6a-135">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="55d6a-135">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-azurerm-ps.md).</span></span>

<span data-ttu-id="55d6a-136">È possibile caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion` con `Install-Module` o `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="55d6a-136">You can load a specific version of the `Az` module by using the `-RequiredVersion` argument with `Install-Module` or `Import-Module`:</span></span>

```powershell-interactive
Install-Module -Name Az -RequiredVersion 0.4.0
Import-Module -Name Az -RequiredVersion 0.4.0
```

<span data-ttu-id="55d6a-137">Se sono installate più versioni del modulo, con l'importazione viene caricata per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="55d6a-137">If you have more than one version of the module installed, the latest version is loaded by default when importing.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="55d6a-138">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="55d6a-138">Provide feedback</span></span>

<span data-ttu-id="55d6a-139">Se si trova un bug quando si usa Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="55d6a-139">If you find a bug when using Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="55d6a-140">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.profile/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="55d6a-140">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.profile/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="55d6a-141">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="55d6a-141">Next Steps</span></span>

<span data-ttu-id="55d6a-142">Per iniziare a usare Azure PowerShell, vedere [Guida introduttiva ad Azure PowerShell](get-started-azureps.md) per altre informazioni sul modulo e sulle sue funzionalità.</span><span class="sxs-lookup"><span data-stu-id="55d6a-142">To get started using Azure PowerShell, see [Get Started with Azure PowerShell](get-started-azureps.md) to learn more about the module and its features.</span></span>