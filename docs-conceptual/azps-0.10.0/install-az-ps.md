---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/26/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 00cb5542e8d805f6e5e79e2177270fcbb93af808
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241900"
---
# <a name="install-azure-powershell"></a><span data-ttu-id="98c88-103">Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="98c88-103">Install Azure PowerShell</span></span>

<span data-ttu-id="98c88-104">Questo articolo illustra come installare i moduli di Azure PowerShell con [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span><span class="sxs-lookup"><span data-stu-id="98c88-104">This article explains how to install the Azure PowerShell modules using [PowerShellGet](/powershell/scripting/gallery/installing-psget).</span></span> <span data-ttu-id="98c88-105">Queste istruzioni sono applicabili alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="98c88-105">These instructions work on Windows, macOS, and Linux platforms.</span></span>

<span data-ttu-id="98c88-106">Azure PowerShell è anche disponibile in Azure [Cloud Shell](/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="98c88-106">Azure PowerShell is also available in Azure [Cloud Shell](/azure/cloud-shell/overview).</span></span>

## <a name="requirements"></a><span data-ttu-id="98c88-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="98c88-107">Requirements</span></span>

<span data-ttu-id="98c88-108">Azure PowerShell è compatibile con PowerShell 5.1 o versione successiva in Windows oppure con PowerShell Core 6.x e versioni successive in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="98c88-108">Azure PowerShell works with PowerShell 5.1 or higher on Windows, or PowerShell Core 6.x and later on all platforms.</span></span> <span data-ttu-id="98c88-109">È necessario installare la [versione più recente di PowerShell](/powershell/scripting/install/installing-powershell) disponibile per il sistema operativo in uso.</span><span class="sxs-lookup"><span data-stu-id="98c88-109">You should install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell) available for your operating system.</span></span> <span data-ttu-id="98c88-110">Azure PowerShell non prevede requisiti aggiuntivi quando viene eseguito in PowerShell 6.2.4 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="98c88-110">Azure PowerShell has no additional requirements when run on PowerShell 6.2.4 and later.</span></span>

<span data-ttu-id="98c88-111">Per controllare la versione di PowerShell, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="98c88-111">To check your PowerShell version, run the command:</span></span>

```azurepowershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="98c88-112">Per usare Azure PowerShell in PowerShell 5.1 in Windows:</span><span class="sxs-lookup"><span data-stu-id="98c88-112">To use Azure PowerShell in PowerShell 5.1 on Windows:</span></span>

1. <span data-ttu-id="98c88-113">Eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="98c88-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span></span>
   <span data-ttu-id="98c88-114">Se si usa Windows 10 versione 1607 o successiva, PowerShell 5.1 è già installato.</span><span class="sxs-lookup"><span data-stu-id="98c88-114">If you're on Windows 10 version 1607 or higher, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="98c88-115">Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="98c88-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>
3. <span data-ttu-id="98c88-116">Assicurarsi di avere la versione più recente di PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="98c88-116">Make sure you have the latest version of PowerShellGet.</span></span> <span data-ttu-id="98c88-117">Eseguire `Install-Module -Name PowerShellGet -Force`.</span><span class="sxs-lookup"><span data-stu-id="98c88-117">Run `Install-Module -Name PowerShellGet -Force`.</span></span>

## <a name="install-the-azure-powershell-module"></a><span data-ttu-id="98c88-118">Installare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="98c88-118">Install the Azure PowerShell module</span></span>

> [!WARNING]
> <span data-ttu-id="98c88-119">L'installazione simultanea dei moduli AzureRM e Az per PowerShell 5.1 per Windows non è supportata.</span><span class="sxs-lookup"><span data-stu-id="98c88-119">We do not support having both the AzureRM and Az modules installed for PowerShell 5.1 on Windows at the same time.</span></span> <span data-ttu-id="98c88-120">Se è necessario mantenere AzureRM nel sistema, installare il modulo Az per PowerShell 6.2.4.x o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="98c88-120">If you need to keep AzureRM available on your system, install the Az module for PowerShell 6.2.4 or later.</span></span>

<span data-ttu-id="98c88-121">Il metodo di installazione preferito prevede l'uso dei cmdlet PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="98c88-121">Using the PowerShellGet cmdlets is the preferred installation method.</span></span> <span data-ttu-id="98c88-122">Installare il modulo Az solo per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="98c88-122">Install the Az module for the current user only.</span></span> <span data-ttu-id="98c88-123">Questo è l'ambito di installazione consigliato.</span><span class="sxs-lookup"><span data-stu-id="98c88-123">This is the recommended installation scope.</span></span> <span data-ttu-id="98c88-124">Questo metodo è applicabile anche alle piattaforme Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="98c88-124">This method works the same on Windows, macOS, and Linux platforms.</span></span> <span data-ttu-id="98c88-125">Eseguire il comando seguente da una sessione di PowerShell:</span><span class="sxs-lookup"><span data-stu-id="98c88-125">Run the following command from a PowerShell session:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope CurrentUser
}
```

<span data-ttu-id="98c88-126">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="98c88-126">By default, the PowerShell gallery isn't configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="98c88-127">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="98c88-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="98c88-128">Rispondere `Yes` o `Yes to All` per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="98c88-128">Answer `Yes` or `Yes to All` to continue with the installation.</span></span>

<span data-ttu-id="98c88-129">Per installare il modulo per tutti gli utenti di un sistema, sono necessari privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="98c88-129">Installing the module for all users on a system requires elevated privileges.</span></span> <span data-ttu-id="98c88-130">Per avviare la sessione di PowerShell, usare **Esegui come amministratore** in Windows oppure il comando `sudo` in macOS o Linux:</span><span class="sxs-lookup"><span data-stu-id="98c88-130">Start the PowerShell session using **Run as administrator** in Windows or use the `sudo` command on macOS or Linux:</span></span>

```powershell-interactive
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Scope AllUsers
}
```

<span data-ttu-id="98c88-131">Il modulo Az è un modulo di rollup per i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="98c88-131">The Az module is a rollup module for the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="98c88-132">Con la sua installazione vengono scaricati tutti i moduli Az PowerShell disponibili a livello generale e vengono messi a disposizione i relativi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c88-132">Installing it downloads all of the generally available Az PowerShell modules, and makes their cmdlets available for use.</span></span>

## <a name="install-offline"></a><span data-ttu-id="98c88-133">Eseguire l'installazione offline</span><span class="sxs-lookup"><span data-stu-id="98c88-133">Install offline</span></span>

<span data-ttu-id="98c88-134">In alcuni ambienti non è possibile connettersi a PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="98c88-134">In some environments, it's not possible to connect to the PowerShell Gallery.</span></span> <span data-ttu-id="98c88-135">In questi casi è comunque possibile eseguire l'installazione offline usando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="98c88-135">In those situations, you can still install offline using one of these methods:</span></span>

* <span data-ttu-id="98c88-136">Scaricare i moduli in un altro percorso di rete e usare tale percorso come origine dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="98c88-136">Download the modules to another location in your network and use that as an installation source.</span></span>
  <span data-ttu-id="98c88-137">Questo metodo consente di memorizzare i moduli di PowerShell nella cache di un singolo server o di una condivisione file da distribuire con PowerShellGet in qualsiasi sistema disconnesso.</span><span class="sxs-lookup"><span data-stu-id="98c88-137">This method allows you to cache PowerShell modules on a single server or file share to be deployed with PowerShellGet to any disconnected systems.</span></span> <span data-ttu-id="98c88-138">Per informazioni su come configurare un repository locale ed eseguire l'installazione in sistemi disconnessi, vedere [Uso dei repository PowerShellGet locali](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span><span class="sxs-lookup"><span data-stu-id="98c88-138">Learn how to set up a local repository and install on disconnected systems with [Working with local PowerShellGet repositories](/powershell/scripting/gallery/how-to/working-with-local-psrepositories).</span></span>
* <span data-ttu-id="98c88-139">[Scaricare il file MSI di Azure PowerShell](install-az-ps-msi.md) in un computer connesso alla rete e quindi copiare il programma di installazione nei sistemi senza accesso a PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="98c88-139">[Download the Azure PowerShell MSI](install-az-ps-msi.md) to a machine connected to the network, and then copy the installer to systems without access to PowerShell Gallery.</span></span> <span data-ttu-id="98c88-140">Tenere presente che il programma di installazione MSI funziona solo per PowerShell 5.1 in Windows.</span><span class="sxs-lookup"><span data-stu-id="98c88-140">Keep in mind that the MSI installer only works for PowerShell 5.1 on Windows.</span></span>
* <span data-ttu-id="98c88-141">Salvare il modulo con [Save-Module](/powershell/module/PowershellGet/Save-Module) in una condivisione file oppure salvarlo in un'altra origine e copiarlo manualmente in altri computer:</span><span class="sxs-lookup"><span data-stu-id="98c88-141">Save the module with [Save-Module](/powershell/module/PowershellGet/Save-Module) to a file share, or save it to another source and manually copy it to other machines:</span></span>

  ```powershell-interactive
  Save-Module -Name Az -Path '\\server\share\PowerShell\modules' -Force
  ```

## <a name="troubleshooting"></a><span data-ttu-id="98c88-142">Risoluzione dei problemi</span><span class="sxs-lookup"><span data-stu-id="98c88-142">Troubleshooting</span></span>

<span data-ttu-id="98c88-143">Ecco alcuni problemi comuni che possono verificarsi durante l'installazione del modulo Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="98c88-143">Here are some common problems seen when installing the Azure PowerShell module.</span></span> <span data-ttu-id="98c88-144">Se si verifica un problema non elencato in questo articolo, [segnalarlo in GitHub](https://github.com/azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="98c88-144">If you experience a problem not listed here, [file an issue on GitHub](https://github.com/azure/azure-powershell/issues).</span></span>

### <a name="proxy-blocks-connection"></a><span data-ttu-id="98c88-145">Il proxy blocca la connessione</span><span class="sxs-lookup"><span data-stu-id="98c88-145">Proxy blocks connection</span></span>

<span data-ttu-id="98c88-146">Se `Install-Module` restituisce errori che indicano che PowerShell Gallery non è raggiungibile, è possibile che si sia protetti da un proxy.</span><span class="sxs-lookup"><span data-stu-id="98c88-146">If you get errors from `Install-Module` that indicate the PowerShell Gallery is unreachable, you may be behind a proxy.</span></span> <span data-ttu-id="98c88-147">I requisiti per configurare un proxy a livello di sistema variano a seconda del sistema operativo e dell'ambiente di rete.</span><span class="sxs-lookup"><span data-stu-id="98c88-147">Different operating systems and network environment have different requirements for configuring a system-wide proxy.</span></span> <span data-ttu-id="98c88-148">Per conoscere le impostazioni del proxy e sapere come configurarlo per l'ambiente corrente, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="98c88-148">Contact your system administrator for your proxy settings and how to configure them for your environment.</span></span>

<span data-ttu-id="98c88-149">PowerShell stesso potrebbe non essere configurato per l'uso automatico di questo proxy.</span><span class="sxs-lookup"><span data-stu-id="98c88-149">PowerShell itself may not be configured to use this proxy automatically.</span></span> <span data-ttu-id="98c88-150">Con PowerShell 5.1 e versioni successive usare i comandi seguenti per configurare la sessione di PowerShell per l'uso di un proxy:</span><span class="sxs-lookup"><span data-stu-id="98c88-150">With PowerShell 5.1 and later, configure the PowerShell session to use a proxy using the following commands:</span></span>

```powershell
$webClient = New-Object System.Net.WebClient
$webClient.Proxy.Credentials = [System.Net.CredentialCache]::DefaultNetworkCredentials
```

<span data-ttu-id="98c88-151">Se le credenziali del sistema operativo sono configurate correttamente, questa configurazione consentirà di reindirizzare le richieste di PowerShell tramite il proxy.</span><span class="sxs-lookup"><span data-stu-id="98c88-151">If your operating system credentials are configured correctly, this configuration routes PowerShell requests through the proxy.</span></span> <span data-ttu-id="98c88-152">Per rendere persistente questa impostazione tra una sessione e l'altra, aggiungere i comandi al proprio [profilo PowerShell](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="98c88-152">To have this setting persist between sessions, add the commands to your [PowerShell profile](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>

<span data-ttu-id="98c88-153">Per installare il pacchetto, il proxy deve consentire le connessioni HTTPS all'indirizzo seguente:</span><span class="sxs-lookup"><span data-stu-id="98c88-153">To install the package, your proxy needs to allow HTTPS connections to the following address:</span></span>

* `https://www.powershellgallery.com`

## <a name="sign-in"></a><span data-ttu-id="98c88-154">Accesso</span><span class="sxs-lookup"><span data-stu-id="98c88-154">Sign in</span></span>

<span data-ttu-id="98c88-155">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="98c88-155">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with a browser sign in token
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="98c88-156">Se il caricamento automatico dei moduli è stato disabilitato, importare manualmente il modulo con `Import-Module -Name Az`.</span><span class="sxs-lookup"><span data-stu-id="98c88-156">If you've disabled module autoloading, manually import the module with `Import-Module -Name Az`.</span></span>
> <span data-ttu-id="98c88-157">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="98c88-157">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="98c88-158">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="98c88-158">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="98c88-159">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-159">To learn how to persist your Azure sign in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="update-the-azure-powershell-module"></a><span data-ttu-id="98c88-160">Aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="98c88-160">Update the Azure PowerShell module</span></span>

<span data-ttu-id="98c88-161">Per aggiornare qualsiasi modulo di PowerShell, è necessario usare lo stesso metodo adottato per installare il modulo.</span><span class="sxs-lookup"><span data-stu-id="98c88-161">To update any PowerShell module, you should use the same method used to install the module.</span></span> <span data-ttu-id="98c88-162">Se, ad esempio, in origine è stato usato `Install-Module`, è necessario usare [Update-Module](/powershell/module/powershellget/update-module) per scaricare l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="98c88-162">For example, if you originally used `Install-Module`, then you should use [Update-Module](/powershell/module/powershellget/update-module) to get the latest version.</span></span> <span data-ttu-id="98c88-163">Se in origine è stato usato il pacchetto MSI, è necessario scaricare e installare la nuova versione del pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="98c88-163">If you originally used the MSI package then you should download and install the new MSI package.</span></span>

<span data-ttu-id="98c88-164">I cmdlet PowerShellGet non possono aggiornare moduli installati da un pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="98c88-164">The PowerShellGet cmdlets cannot update modules that were installed from an MSI package.</span></span> <span data-ttu-id="98c88-165">I pacchetti MSI non consentono di aggiornare moduli installati con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="98c88-165">MSI packages do not update modules that were installed using PowerShellGet.</span></span> <span data-ttu-id="98c88-166">Se si verificano problemi durante l'aggiornamento con PowershellGet, è necessario procedere alla**reinstallazione** invece che al semplice **aggiornamento**.</span><span class="sxs-lookup"><span data-stu-id="98c88-166">If you have any issues updating using PowershellGet, then you should **reinstall**, rather than **update**.</span></span> <span data-ttu-id="98c88-167">La reinstallazione è un'operazione analoga all'installazione, ma richiede l'aggiunta del parametro `-Force`:</span><span class="sxs-lookup"><span data-stu-id="98c88-167">Reinstalling is done the same way as installing, but you need to add the `-Force` parameter:</span></span>

```powershell
if (Get-Module -Name AzureRM -ListAvailable) {
    Write-Warning -Message ('Az module not installed. Having both the AzureRM and ' +
      'Az modules installed at the same time is not supported.')
} else {
    Install-Module -Name Az -AllowClobber -Force
}
```

<span data-ttu-id="98c88-168">Diversamente dalle installazioni basate su MSI, l'installazione o l'aggiornamento con PowerShellGet non comporta la rimozione delle versioni precedenti che possono esistere nel sistema.</span><span class="sxs-lookup"><span data-stu-id="98c88-168">Unlike MSI-based installations, installing or updating using PowerShellGet does not remove older versions that may exist on your system.</span></span> <span data-ttu-id="98c88-169">Per rimuovere le versioni precedenti di Azure PowerShell dal sistema, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-169">To remove old versions of Azure PowerShell from your system, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span> <span data-ttu-id="98c88-170">Per altre informazioni sulle installazioni basate su MSI, vedere [Installare Azure PowerShell con un file MSI](install-az-ps-msi.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-170">For more information about MSI-based installations, see [Install Azure PowerShell with an MSI](install-az-ps-msi.md).</span></span>

## <a name="use-multiple-versions-of-azure-powershell"></a><span data-ttu-id="98c88-171">Usare più versioni di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="98c88-171">Use multiple versions of Azure PowerShell</span></span>

<span data-ttu-id="98c88-172">È possibile installare più versioni di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="98c88-172">It's possible to install more than one version of Azure PowerShell.</span></span> <span data-ttu-id="98c88-173">Per controllare se sono installate più versioni di Azure PowerShell, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="98c88-173">To check if you have multiple versions of Azure PowerShell installed, use the following command:</span></span>

```powershell-interactive
Get-InstalledModule -Name Az -AllVersions | Select-Object -Property Name, Version
```

<span data-ttu-id="98c88-174">Per rimuovere una versione di Azure PowerShell, vedere [Disinstallare il modulo Azure PowerShell](uninstall-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-174">To remove a version of Azure PowerShell, see [Uninstall the Azure PowerShell module](uninstall-az-ps.md).</span></span>

<span data-ttu-id="98c88-175">Se sono installate più versioni del modulo, il modulo viene caricato automaticamente e `Import-Module` carica per impostazione predefinita l'ultima versione.</span><span class="sxs-lookup"><span data-stu-id="98c88-175">If you have more than one version of the module installed, module autoload and `Import-Module` load the latest version by default.</span></span>

<span data-ttu-id="98c88-176">È possibile installare o caricare una versione specifica del modulo `Az` usando il parametro `-RequiredVersion`:</span><span class="sxs-lookup"><span data-stu-id="98c88-176">You can install or load a specific version of the `Az` module by using the `-RequiredVersion` parameter:</span></span>

```powershell-interactive
# Install Az version 3.6.1
Install-Module -Name Az -RequiredVersion 3.6.1
# Load Az version 3.6.1
Import-Module -Name Az -RequiredVersion 3.6.1
```

## <a name="provide-feedback"></a><span data-ttu-id="98c88-177">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="98c88-177">Provide feedback</span></span>

<span data-ttu-id="98c88-178">Se si trova un bug in Azure PowerShell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="98c88-178">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="98c88-179">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="98c88-179">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="98c88-180">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="98c88-180">Next Steps</span></span>

<span data-ttu-id="98c88-181">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-181">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="98c88-182">Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="98c88-182">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
