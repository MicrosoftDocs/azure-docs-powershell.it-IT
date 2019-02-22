---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 936bb24eecb4077080e172bf0d29fe57ec652187
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153689"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="9384d-103">Installare Azure PowerShell in macOS o Linux</span><span class="sxs-lookup"><span data-stu-id="9384d-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="9384d-104">Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="9384d-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="9384d-105">Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core.</span><span class="sxs-lookup"><span data-stu-id="9384d-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="9384d-106">Per usare queste piattaforme è disponibile un'apposita versione .NET di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9384d-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

## <a name="install-powershell-core"></a><span data-ttu-id="9384d-107">Installare PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="9384d-107">Install PowerShell Core</span></span>

<span data-ttu-id="9384d-108">Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.</span><span class="sxs-lookup"><span data-stu-id="9384d-108">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="9384d-109">Per istruzioni dettagliate, vedere gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="9384d-109">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="9384d-110">Installare PowerShell Core in macOS</span><span class="sxs-lookup"><span data-stu-id="9384d-110">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="9384d-111">Installare PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="9384d-111">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="9384d-112">Installare Azure PowerShell per .NET Core</span><span class="sxs-lookup"><span data-stu-id="9384d-112">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9384d-113">PowerShell Core viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="9384d-113">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9384d-114">L'installazione dei moduli in PowerShell richiede privilegi elevati, quindi è necessario avviare la sessione come utente con privilegi avanzati:</span><span class="sxs-lookup"><span data-stu-id="9384d-114">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="9384d-115">Per installare Azure PowerShell, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="9384d-115">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="9384d-116">Il modulo `AzureRM` descritto in altri articoli non è progettato per .NET Core e non funziona con PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="9384d-116">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="9384d-117">`AzureRM` e `AzureRM.NetCore` usano gli stessi nomi cmdlet, quindi l'unica differenza è il nome del modulo di rollup e la versione .NET per la quale sono progettati.</span><span class="sxs-lookup"><span data-stu-id="9384d-117">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="9384d-118">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="9384d-118">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="9384d-119">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="9384d-119">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="9384d-120">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="9384d-120">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="9384d-121">Accesso</span><span class="sxs-lookup"><span data-stu-id="9384d-121">Sign in</span></span>

<span data-ttu-id="9384d-122">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM.Netcore` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="9384d-122">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="9384d-123">L'importazione di un modulo __non__ richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="9384d-123">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="9384d-124">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="9384d-124">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="9384d-125">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="9384d-125">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="9384d-126">In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="9384d-126">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="9384d-127">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="9384d-127">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="9384d-128">Cmdlet disponibili</span><span class="sxs-lookup"><span data-stu-id="9384d-128">Available cmdlets</span></span>

<span data-ttu-id="9384d-129">I moduli di Azure PowerShell per .NET Core sono ancora in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="9384d-129">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="9384d-130">Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli.</span><span class="sxs-lookup"><span data-stu-id="9384d-130">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="9384d-131">Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="9384d-131">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="9384d-132">Gestione account</span><span class="sxs-lookup"><span data-stu-id="9384d-132">Account management</span></span>
  * <span data-ttu-id="9384d-133">Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9384d-133">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="9384d-134">Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9384d-134">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="9384d-135">Environment</span><span class="sxs-lookup"><span data-stu-id="9384d-135">Environment</span></span>
  * <span data-ttu-id="9384d-136">Recupero di ambienti predefiniti di Microsoft Azure diversi</span><span class="sxs-lookup"><span data-stu-id="9384d-136">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="9384d-137">Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack</span><span class="sxs-lookup"><span data-stu-id="9384d-137">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="9384d-138">Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="9384d-138">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="9384d-139">Macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9384d-139">Virtual Machine</span></span>
  * <span data-ttu-id="9384d-140">Servizio app (siti Web)</span><span class="sxs-lookup"><span data-stu-id="9384d-140">App Service (Websites)</span></span>
  * <span data-ttu-id="9384d-141">Database SQL</span><span class="sxs-lookup"><span data-stu-id="9384d-141">SQL Database</span></span>
  * <span data-ttu-id="9384d-142">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="9384d-142">Storage</span></span>
  * <span data-ttu-id="9384d-143">Rete</span><span class="sxs-lookup"><span data-stu-id="9384d-143">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="9384d-144">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="9384d-144">Next Steps</span></span>

<span data-ttu-id="9384d-145">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9384d-145">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
