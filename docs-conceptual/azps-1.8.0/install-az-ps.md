---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 8e63e3efb2671eef435498063010d5704c793060
ms.sourcegitcommit: a261efc84dedfd829c0613cf62f8fcf3aa62adb8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/06/2019
ms.locfileid: "68807514"
---
# <a name="install-the-azure-powershell-module"></a><span data-ttu-id="189f5-103">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="189f5-103">Install the Azure PowerShell module</span></span>

<span data-ttu-id="189f5-104">Questo articolo illustra come installare i moduli di Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="189f5-104">This article tells you how to install the Azure PowerShell modules using PowerShellGet.</span></span> <span data-ttu-id="189f5-105">Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="189f5-105">These instructions work on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="189f5-106">Per il modulo Az non sono attualmente supportati altri metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="189f5-106">For the Az module, currently no other installation methods are supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="189f5-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="189f5-107">Requirements</span></span>

<span data-ttu-id="189f5-108">Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell Core 6.x e versioni successive in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="189f5-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="189f5-109">Se non si è sicuri di avere PowerShell o se si usa macOS o Linux, [installare la versione più recente di PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span><span class="sxs-lookup"><span data-stu-id="189f5-109">If you aren't sure if you have PowerShell, or are on macOS or Linux, [install the latest version of PowerShell Core](/powershell/scripting/install/installing-powershell#powershell-core).</span></span>

<span data-ttu-id="189f5-110">Per controllare la versione di PowerShell, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="189f5-110">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="189f5-111">Per eseguire Azure PowerShell in PowerShell 5.1 in Windows:</span><span class="sxs-lookup"><span data-stu-id="189f5-111">To run Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="189f5-112">Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="189f5-112">Update to [Windows PowerShell 5.1](/powershell/scripting/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="189f5-113">Se si usa Windows 10, PowerShell 5.1 è già installato.</span><span class="sxs-lookup"><span data-stu-id="189f5-113">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="189f5-114">Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="189f5-114">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

<span data-ttu-id="189f5-115">Quando si usa PowerShell Core, non sono previsti requisiti aggiuntivi per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189f5-115">There are no additional requirements for Azure PowerShell when using PowerShell Core.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="189f5-116">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="189f5-116">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="189f5-117">__Non è possibile__ installare contemporaneamente i moduli AzureRM e Az per PowerShell 5.1 per Windows.</span><span class="sxs-lookup"><span data-stu-id="189f5-117">You __can't__ have both the AzureRM and Az modules installed for PowerShell 5.1 for Windows at the same time.</span></span> <span data-ttu-id="189f5-118">Se è necessario mantenere AzureRM nel sistema, installare il modulo Az per PowerShell Core 6.x o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="189f5-118">If you need to keep AzureRM available on your system, install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="189f5-119">A questo scopo, [installare PowerShell Core 6.x or versioni successive](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) e quindi seguire queste istruzioni in un terminale di PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="189f5-119">To do this, [install PowerShell Core 6.x or later](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows) and then follow these instructions in a PowerShell Core terminal.</span></span>

<span data-ttu-id="189f5-120">Il metodo consigliato consiste nell'eseguire l'installazione solo per l'utente attivo:</span><span class="sxs-lookup"><span data-stu-id="189f5-120">The recommended install method is to only install for the active user:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope CurrentUser
```

<span data-ttu-id="189f5-121">Se si vuole eseguire l'installazione per tutti gli utenti di un sistema, sono necessari privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="189f5-121">If you want to install for all users on a system, this requires administrator privileges.</span></span> <span data-ttu-id="189f5-122">Da una sessione di PowerShell con privilegi elevati eseguita come amministratore oppure con il comando `sudo` in MacOS o Linux:</span><span class="sxs-lookup"><span data-stu-id="189f5-122">From an elevated PowerShell session either run as administrator or with the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
Install-Module -Name Az -AllowClobber -Scope AllUsers
```

<span data-ttu-id="189f5-123">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="189f5-123">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="189f5-124">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="189f5-124">The first time you use the PSGallery you see the following prompt:</span></span>

```output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="189f5-125">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="189f5-125">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="189f5-126">Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189f5-126">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="189f5-127">Con la sua installazione vengono scaricati tutti i moduli di Azure Resource Manager disponibili e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="189f5-127">Installing it downloads all of the available Azure Resource Manager modules, and makes their cmdlets available for use.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="189f5-128">risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="189f5-128">Troubleshooting</span></span>

<span data-ttu-id="189f5-129">Ecco alcuni problemi comuni che possono verificarsi durante l'installazione del modulo Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189f5-129">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="189f5-130">Se si verifica un problema non elencato in questo articolo, [segnalarlo in GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="189f5-130">If you experience a problem not listed here, please [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="189f5-131">Il proxy blocca la connessione</span><span class="sxs-lookup"><span data-stu-id="189f5-131">Proxy blocks connection</span></span>

<span data-ttu-id="189f5-132">Se `Install-Module` restituisce errori che indicano che PowerShell Gallery non è raggiungibile, è possibile che si sia protetti da un proxy.</span><span class="sxs-lookup"><span data-stu-id="189f5-132">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="189f5-133">I requisiti per configurare un proxy a livello di sistema variano a seconda del sistema operativo e non vengono illustrati in dettaglio in questo articolo.</span><span class="sxs-lookup"><span data-stu-id="189f5-133">Different operating systems will have different requirements for configuring a system-wide proxy, which are not covered in detail here.</span></span> <span data-ttu-id="189f5-134">Per conoscere le impostazioni del proxy e sapere come configurarlo per il sistema operativo corrente, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="189f5-134">Contact your system administrator for your proxy settings and how to configure them for your OS.</span></span>

<span data-ttu-id="189f5-135">PowerShell stesso potrebbe non essere configurato per l'uso automatico di questo proxy.</span><span class="sxs-lookup"><span data-stu-id="189f5-135">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="189f5-136">Con PowerShell 5.1 e versioni successive configurare il proxy per l'uso di una sessione di PowerShell con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="189f5-136">With PowerShell 5.1 and later, configure the proxy to use for a PowerShell session with the following command:</span></span>

```powershell
(New-Object System.Net.WebClient).Proxy.Credentials = `
  [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="189f5-137">Se le credenziali del sistema operativo sono configurate correttamente, le richieste di PowerShell verranno instradate tramite il proxy.</span><span class="sxs-lookup"><span data-stu-id="189f5-137">If your operating system credentials are configured correctly, this will route PowerShell requests through the proxy.</span></span>
<span data-ttu-id="189f5-138">Per rendere persistente questa impostazione tra una sessione e l'altra, aggiungere il comando a un [profilo PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="189f5-138">In order to have this setting persist between sessions, add the command to a [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="189f5-139">Per installare il pacchetto, il proxy deve consentire le connessioni HTTPS all'indirizzo seguente:</span><span class="sxs-lookup"><span data-stu-id="189f5-139">In order to install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="189f5-140">Accesso</span><span class="sxs-lookup"><span data-stu-id="189f5-140">Sign in</span></span>

<span data-ttu-id="189f5-141">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="189f5-141">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
>
> <span data-ttu-id="189f5-142">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="189f5-142">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="189f5-143">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="189f5-143">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="189f5-144">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="189f5-144">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="189f5-145">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="189f5-145">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="189f5-146">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="189f5-146">Update the Azure PowerShell module</span></span>

<span data-ttu-id="189f5-147">In considerazione della modalità di creazione del pacchetto del modulo Az, il comando [Update-Module](/powershell/module/powershellget/update-module) non consente di aggiornare correttamente l'installazione.</span><span class="sxs-lookup"><span data-stu-id="189f5-147">Because of how the Az module is packaged, the [Update-Module](/powershell/module/powershellget/update-module) command won't update your installation correctly.</span></span> <span data-ttu-id="189f5-148">AZ è tecnicamente un metamodulo e comprende tutti i moduli secondari contenenti i cmdlet per interagire con i servizi di Azure.</span><span class="sxs-lookup"><span data-stu-id="189f5-148">Az is technically a meta-module, encompassing all of the submodules that contain cmdlets to interact with Azure services.</span></span> <span data-ttu-id="189f5-149">Per aggiornare il modulo Azure PowerShell, è quindi necessario __reinstallarlo__, anziché semplicemente __aggiornarlo__.</span><span class="sxs-lookup"><span data-stu-id="189f5-149">That means that to update the Azure PowerShell module, you will need to __reinstall__, rather than just __update__.</span></span> <span data-ttu-id="189f5-150">L'operazione è analoga all'installazione, ma può essere necessario aggiungere l'argomento `-Force`:</span><span class="sxs-lookup"><span data-stu-id="189f5-150">This is done in the same way as installing, but you may need to add the `-Force` argument:</span></span>

```powershell
Install-Module -Name Az -AllowClobber -Force
```

<span data-ttu-id="189f5-151">Anche se questa operazione può comportare la sovrascrittura di moduli installati, è comunque possibile che nel sistema siano ancora presenti versioni meno recenti.</span><span class="sxs-lookup"><span data-stu-id="189f5-151">Although this can overwrite installed modules, you may still have older versions left on your system.</span></span>
<span data-ttu-id="189f5-152">Per informazioni su come rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="189f5-152">To learn how to remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="189f5-153">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="189f5-153">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="189f5-154">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="189f5-154">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="189f5-155">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="189f5-155">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | select Name,Version
```

<span data-ttu-id="189f5-156">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="189f5-156">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="189f5-157">È possibile installare o caricare una versione specifica del modulo `Az` usando l'argomento `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="189f5-157">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` argument:</span></span>

```powershell-interactive
# Install Az version 0.7.0
Install-Module -Name Az -RequiredVersion 0.7.0 
# Load Az version 0.7.0
Import-Module -Name Az -RequiredVersion 0.7.0
```

<span data-ttu-id="189f5-158">Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="189f5-158">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="189f5-159">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="189f5-159">Provide feedback</span></span>

<span data-ttu-id="189f5-160">Se si trova un bug in Azure Powershell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="189f5-160">If you find a bug in Azure Powershell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span>
<span data-ttu-id="189f5-161">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="189f5-161">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="189f5-162">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="189f5-162">Next Steps</span></span>

<span data-ttu-id="189f5-163">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="189f5-163">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span>
<span data-ttu-id="189f5-164">Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="189f5-164">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
