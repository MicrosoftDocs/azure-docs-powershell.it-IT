---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 47611281f67d68c9fc2686e0c6156b060a225158
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273821"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="ee42d-103">Installare Azure PowerShell in macOS o Linux</span><span class="sxs-lookup"><span data-stu-id="ee42d-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="ee42d-104">Per le piattaforme non Windows, è possibile eseguire Azure PowerShell in PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="ee42d-104">For non-Windows platforms, it's possible to run Azure PowerShell in PowerShell Core v6.</span></span> <span data-ttu-id="ee42d-105">Questa versione di PowerShell è progettata per l'uso in qualsiasi piattaforma con supporto .NET Core.</span><span class="sxs-lookup"><span data-stu-id="ee42d-105">This version of PowerShell is built for use on any platform that supports .NET Core.</span></span> <span data-ttu-id="ee42d-106">Per usare queste piattaforme è disponibile un'apposita versione .NET di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ee42d-106">To work with these platforms, there's a special .NET Core version of Azure PowerShell available.</span></span>

> [!NOTE]
> <span data-ttu-id="ee42d-107">Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.</span><span class="sxs-lookup"><span data-stu-id="ee42d-107">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="ee42d-108">Il supporto per questi prodotti è limitato.</span><span class="sxs-lookup"><span data-stu-id="ee42d-108">Support for these products is limited.</span></span> <span data-ttu-id="ee42d-109">Se si verificano problemi o si trovano bug, registrare un problema in GitHub.</span><span class="sxs-lookup"><span data-stu-id="ee42d-109">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="ee42d-110">Problemi per PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="ee42d-110">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="ee42d-111">Problemi per Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee42d-111">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core"></a><span data-ttu-id="ee42d-112">Installare PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="ee42d-112">Install PowerShell Core</span></span>

<span data-ttu-id="ee42d-113">Le istruzioni di installazione di PowerShell Core sono diverse per macOS e la maggior parte delle distribuzioni Linux.</span><span class="sxs-lookup"><span data-stu-id="ee42d-113">The installation instructions for PowerShell Core are different for macOS and most Linux distributions.</span></span>
<span data-ttu-id="ee42d-114">Per istruzioni dettagliate, vedere gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="ee42d-114">Detailed instructions can be found in the following articles:</span></span>

* [<span data-ttu-id="ee42d-115">Installare PowerShell Core in macOS</span><span class="sxs-lookup"><span data-stu-id="ee42d-115">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
* [<span data-ttu-id="ee42d-116">Installare PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="ee42d-116">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="ee42d-117">Installare Azure PowerShell per .NET Core</span><span class="sxs-lookup"><span data-stu-id="ee42d-117">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="ee42d-118">PowerShell Core viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="ee42d-118">PowerShell Core comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="ee42d-119">L'installazione dei moduli in PowerShell richiede privilegi elevati, quindi è necessario avviare la sessione come utente con privilegi avanzati:</span><span class="sxs-lookup"><span data-stu-id="ee42d-119">Installation of modules in PowerShell requires elevated privileges, so you'll need to start your session as superuser:</span></span>

```bash
sudo pwsh
```

<span data-ttu-id="ee42d-120">Per installare Azure PowerShell, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="ee42d-120">To install Azure PowerShell, run the following command:</span></span>

```powershell-interactive
Install-Module AzureRM.NetCore
```

> [!IMPORTANT]
> <span data-ttu-id="ee42d-121">Il modulo `AzureRM` descritto in altri articoli non è progettato per .NET Core e non funziona con PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="ee42d-121">The `AzureRM` module detailed in other articles is not built for .NET Core and will not work with PowerShell Core.</span></span> <span data-ttu-id="ee42d-122">`AzureRM` e `AzureRM.NetCore` usano gli stessi nomi cmdlet, quindi l'unica differenza è il nome del modulo di rollup e la versione .NET per la quale sono progettati.</span><span class="sxs-lookup"><span data-stu-id="ee42d-122">Both `AzureRM` and `AzureRM.NetCore` use the same cmdlet names, so the only difference is the name of the rollup module and which .NET version they are built against.</span></span>

<span data-ttu-id="ee42d-123">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="ee42d-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="ee42d-124">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="ee42d-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="ee42d-125">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="ee42d-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

## <a name="sign-in"></a><span data-ttu-id="ee42d-126">Accesso</span><span class="sxs-lookup"><span data-stu-id="ee42d-126">Sign in</span></span>

<span data-ttu-id="ee42d-127">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM.Netcore` nella sessione di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee42d-127">To start working with Azure PowerShell, you need to load `AzureRM.Netcore` into your PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span> <span data-ttu-id="ee42d-128">L'importazione di un modulo __non__ richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="ee42d-128">Importing a module does __not__ require elevated privileges.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM.Netcore
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="ee42d-129">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="ee42d-129">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="ee42d-130">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="ee42d-130">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="ee42d-131">In macOS e Linux usare il proprio profilo tramite la variabile di ambiente `$Profile`.</span><span class="sxs-lookup"><span data-stu-id="ee42d-131">On macOS and Linux, you should work with your profile through the `$Profile` environment variable.</span></span> <span data-ttu-id="ee42d-132">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="ee42d-132">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="ee42d-133">Cmdlet disponibili</span><span class="sxs-lookup"><span data-stu-id="ee42d-133">Available cmdlets</span></span>

<span data-ttu-id="ee42d-134">I moduli di Azure PowerShell per .NET Core sono ancora in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="ee42d-134">The Azure PowerShell modules for .NET Core are still in development.</span></span> <span data-ttu-id="ee42d-135">Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli.</span><span class="sxs-lookup"><span data-stu-id="ee42d-135">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="ee42d-136">Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="ee42d-136">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="ee42d-137">Gestione account</span><span class="sxs-lookup"><span data-stu-id="ee42d-137">Account management</span></span>
  * <span data-ttu-id="ee42d-138">Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="ee42d-138">Sign in with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  * <span data-ttu-id="ee42d-139">Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="ee42d-139">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="ee42d-140">Environment</span><span class="sxs-lookup"><span data-stu-id="ee42d-140">Environment</span></span>
  * <span data-ttu-id="ee42d-141">Recupero di ambienti predefiniti di Microsoft Azure diversi</span><span class="sxs-lookup"><span data-stu-id="ee42d-141">Get the different out-of-box Microsoft Azure environments</span></span>
  * <span data-ttu-id="ee42d-142">Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack</span><span class="sxs-lookup"><span data-stu-id="ee42d-142">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="ee42d-143">Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="ee42d-143">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  * <span data-ttu-id="ee42d-144">Macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="ee42d-144">Virtual Machine</span></span>
  * <span data-ttu-id="ee42d-145">Servizio app (siti Web)</span><span class="sxs-lookup"><span data-stu-id="ee42d-145">App Service (Websites)</span></span>
  * <span data-ttu-id="ee42d-146">Database SQL</span><span class="sxs-lookup"><span data-stu-id="ee42d-146">SQL Database</span></span>
  * <span data-ttu-id="ee42d-147">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="ee42d-147">Storage</span></span>
  * <span data-ttu-id="ee42d-148">Rete</span><span class="sxs-lookup"><span data-stu-id="ee42d-148">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="ee42d-149">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="ee42d-149">Next Steps</span></span>

<span data-ttu-id="ee42d-150">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="ee42d-150">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
