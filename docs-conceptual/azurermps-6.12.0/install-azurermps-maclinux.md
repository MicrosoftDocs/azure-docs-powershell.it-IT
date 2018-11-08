---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/05/2018
ms.openlocfilehash: f60ea1c608be4b1c8319d53303713ba039276abc
ms.sourcegitcommit: 06f9206e025afa7207d4657c8f57c94ddb74817a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2018
ms.locfileid: "51212892"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="a42ff-103">Installare Azure PowerShell in macOS o Linux</span><span class="sxs-lookup"><span data-stu-id="a42ff-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="a42ff-104">Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="a42ff-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="a42ff-105">Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core.</span><span class="sxs-lookup"><span data-stu-id="a42ff-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="a42ff-106">Per usare queste piattaforme è disponibile una versione .NET Standard di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a42ff-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="a42ff-107">Attualmente, Azure PowerShell per .NET Standard è ancora in versione beta.</span><span class="sxs-lookup"><span data-stu-id="a42ff-107">At this time, Azure PowerShell for .NET Standard is still in beta.</span></span>
> <span data-ttu-id="a42ff-108">Se si verificano problemi o si trovano bug, registrare un problema in GitHub.</span><span class="sxs-lookup"><span data-stu-id="a42ff-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="a42ff-109">Problemi per Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a42ff-109">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="a42ff-110">Installare PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="a42ff-110">Install PowerShell Core</span></span>

<span data-ttu-id="a42ff-111">Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.</span><span class="sxs-lookup"><span data-stu-id="a42ff-111">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="a42ff-112">Per istruzioni dettagliate, vedere gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="a42ff-112">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="a42ff-113">Installare PowerShell Core in macOS</span><span class="sxs-lookup"><span data-stu-id="a42ff-113">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="a42ff-114">Installare PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="a42ff-114">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-standard"></a><span data-ttu-id="a42ff-115">Installare Azure PowerShell per .NET Standard</span><span class="sxs-lookup"><span data-stu-id="a42ff-115">Install Azure PowerShell for .NET Standard</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a42ff-116">Il modulo `AzureRM` descritto nei dettagli in altri articoli non funziona con PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a42ff-116">The `AzureRM` module detailed in other articles does not work with PowerShell Core.</span></span>
> <span data-ttu-id="a42ff-117">È necessario installare il modulo `Az` per ottenere la funzionalità di Azure PowerShell in PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a42ff-117">You must install the `Az` module to get Azure PowerShell functionality in PowerShell Core.</span></span>

<span data-ttu-id="a42ff-118">PowerShell Core viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="a42ff-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="a42ff-119">Avviare PowerShell con il comando:</span><span class="sxs-lookup"><span data-stu-id="a42ff-119">Start PowerShell with the command:</span></span>

```bash
pwsh
```

<span data-ttu-id="a42ff-120">Per installare Azure PowerShell, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="a42ff-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module Az
```

> [!NOTE]
> <span data-ttu-id="a42ff-121">Se si verifica un errore nelle autorizzazioni quando si prova a installare il modulo, potrebbe essere necessario eseguire PowerShell in modalità utente con privilegi avanzati per installare i moduli.</span><span class="sxs-lookup"><span data-stu-id="a42ff-121">If you encounter a permissions error when attempting to install the module, you may need to run PowerShell in superuser mode to install modules.</span></span>
>
> ```bash
> sudo pwsh
> ```

<span data-ttu-id="a42ff-122">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a42ff-122">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a42ff-123">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="a42ff-123">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="a42ff-124">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a42ff-124">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="enable-aliases"></a><span data-ttu-id="a42ff-125">Abilitare gli alias</span><span class="sxs-lookup"><span data-stu-id="a42ff-125">Enable aliases</span></span>

<span data-ttu-id="a42ff-126">Per la compatibilità con il modulo `AzureRM` esistente, il nuovo modulo `Az` può creare alias compatibili con le versioni precedenti per i cmdlet `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="a42ff-126">For compatibility with the existing `AzureRM` module, the new `Az` module has the ability to create backwards compatible aliases for the `AzureRM` cmdlets.</span></span> <span data-ttu-id="a42ff-127">Prima di usare il modulo per la prima volta, configurare questi alias con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="a42ff-127">Before using the module for the first time, set up these aliases with the following command:</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Enable AzureRM aliases for the user
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="a42ff-128">Gli alias vengono configurati solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="a42ff-128">This sets up aliases for the current user only.</span></span> <span data-ttu-id="a42ff-129">Vedere la Guida dei cmdlet per altri valori che possono essere forniti a `-Scope` per configurare gli alias.</span><span class="sxs-lookup"><span data-stu-id="a42ff-129">Check the cmdlet help for other values that can be provided to `-Scope` to set up the aliases.</span></span>

> [!NOTE]
> <span data-ttu-id="a42ff-130">Se si verifica un errore in un percorso, assicurarsi che esista nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="a42ff-130">If you encounter an error about a path location, make sure that it exists on your local system.</span></span> <span data-ttu-id="a42ff-131">Per l'ambito `CurrentUser`, questo errore può essere risolto eseguendo questo comando in `bash`:</span><span class="sxs-lookup"><span data-stu-id="a42ff-131">For the `CurrentUser` scope, this error can be resolved by running the following command in `bash`:</span></span>
>
> ```bash
> mkdir -p $HOME/.config/powershell
> ```

## <a name="sign-in"></a><span data-ttu-id="a42ff-132">Accesso</span><span class="sxs-lookup"><span data-stu-id="a42ff-132">Sign in</span></span>

<span data-ttu-id="a42ff-133">Per iniziare a usare Azure PowerShell è necessario caricare `Az` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="a42ff-133">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="a42ff-134">L'importazione di un modulo __non__ richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="a42ff-134">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="a42ff-135">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="a42ff-135">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="a42ff-136">L'importazione automatica del modulo `Az` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="a42ff-136">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="a42ff-137">In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="a42ff-137">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="a42ff-138">Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="a42ff-138">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a42ff-139">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="a42ff-139">Next Steps</span></span>

<span data-ttu-id="a42ff-140">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="a42ff-140">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
