---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: f014d62e898da195a38052db6b7e37a2cd96dfdd
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560117"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="9fdb5-103">Installare Azure PowerShell in macOS o Linux</span><span class="sxs-lookup"><span data-stu-id="9fdb5-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="9fdb5-104">Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="9fdb5-105">Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="9fdb5-106">Per usare queste piattaforme è disponibile una versione .NET Standard di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-106">To work with these platforms, there's a .NET Standard version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="9fdb5-107">Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="9fdb5-108">Il supporto per questi prodotti è limitato.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-108">Support for these products is limited.</span></span> <span data-ttu-id="9fdb5-109">Se si verificano problemi o si trovano bug, registrare un problema in GitHub.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="9fdb5-110">Problemi per PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="9fdb5-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="9fdb5-111">Problemi per Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9fdb5-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="9fdb5-112">Installare PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="9fdb5-112">Install PowerShell Core</span></span>

<span data-ttu-id="9fdb5-113">Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="9fdb5-114">Per istruzioni dettagliate, vedere gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="9fdb5-115">Installare PowerShell Core in macOS</span><span class="sxs-lookup"><span data-stu-id="9fdb5-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="9fdb5-116">Installare PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="9fdb5-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="9fdb5-117">Installare Azure PowerShell per .NET Core</span><span class="sxs-lookup"><span data-stu-id="9fdb5-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9fdb5-118">PowerShell Core viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9fdb5-119">L'installazione dei moduli in PowerShell richiede privilegi elevati, quindi è necessario avviare la sessione come utente con privilegi avanzati:</span><span class="sxs-lookup"><span data-stu-id="9fdb5-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="9fdb5-120">Per installare Azure PowerShell, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="9fdb5-120">To install Azure PowerShell, run the following command:</span></span>

```powershell
Install-Module Az
```

> [!IMPORTANT]
> <span data-ttu-id="9fdb5-121">Il modulo `AzureRM` descritto in altri articoli non è progettato per .NET Core e non funziona con PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="9fdb5-122">I moduli `Az` contengono gli alias dei comandi per tutti i cmdlet `AzureRM`, quindi è applicabile tutta la documentazione relativa a `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-122">The `Az` modules contain command aliases for all `AzureRM` cmdlets, so all of the documentation for `AzureRM` applies.</span></span>

<span data-ttu-id="9fdb5-123">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9fdb5-124">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="9fdb5-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9fdb5-125">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="9fdb5-126">Accesso</span><span class="sxs-lookup"><span data-stu-id="9fdb5-126">Sign in</span></span>

<span data-ttu-id="9fdb5-127">Per iniziare a usare Azure PowerShell è necessario caricare `Az` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-127">To start working with Azure PowerShell, you need to load `Az` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="9fdb5-128">L'importazione di un modulo __non__ richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module Az
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="9fdb5-129">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9fdb5-130">L'importazione automatica del modulo `Az` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="9fdb5-130">Automatically importing the `Az` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="9fdb5-131">In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="9fdb5-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="9fdb5-132">Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9fdb5-132">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="9fdb5-133">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="9fdb5-133">Next Steps</span></span>

<span data-ttu-id="9fdb5-134">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9fdb5-134">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
