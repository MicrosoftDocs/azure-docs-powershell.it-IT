---
title: Installare e configurare Azure PowerShell | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 7b099fead7cb985fc8f7e6fed55b8c1107caa0d9
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "75720379"
---
# <a name="install-azure-powershell-on-windows-with-powershellget"></a><span data-ttu-id="76213-103">Installare Azure PowerShell in Windows con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="76213-103">Install Azure PowerShell on Windows with PowerShellGet</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="76213-104">Questo articolo illustra l'installazione dei moduli di Azure PowerShell per PowerShell 5.x per Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="76213-104">This article explains the steps to install the Azure PowerShell modules for PowerShell 5.x for Windows using PowerShellGet.</span></span> <span data-ttu-id="76213-105">PowerShellGet con la gestione dei moduli rappresenta la modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="76213-105">PowerShellGet and module management is the preferred way to install Azure PowerShell but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="76213-106">Il modello di distribuzione classica di Azure non è supportato da questa versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76213-106">The Azure classic deployment model is not supported by this version of Azure PowerShell.</span></span> <span data-ttu-id="76213-107">Per il supporto delle distribuzioni classiche, seguire le istruzioni in [Installare il modulo Gestione dei servizi di Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps).</span><span class="sxs-lookup"><span data-stu-id="76213-107">For support for classic deployments, follow the instructions in [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="76213-108">Il modulo AzureRM non è supportato per macOS o Linux.</span><span class="sxs-lookup"><span data-stu-id="76213-108">The AzureRM module is not supported for macOS or Linux.</span></span> <span data-ttu-id="76213-109">Per usare i cmdlet di Azure PowerShell in queste piattaforme [installare il modulo Az](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="76213-109">To use Azure PowerShell cmdlets on these platforms, [Install the Az module](/powershell/azure/install-az-ps).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="76213-110">Passaggio 1: installare PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="76213-110">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="76213-111">L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="76213-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="76213-112">Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="76213-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="76213-113">Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="76213-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>


```powershell-interactive
Get-InstalledModule -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="76213-114">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="76213-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="76213-115">È necessario PowerShellGet versione 1.1.2.0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="76213-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="76213-116">Per aggiornare PowerShellGet, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="76213-116">To update PowerShellGet, use the following command:</span></span>

```powershell-interactive
Install-Module PowerShellGet -Force
```

<span data-ttu-id="76213-117">Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="76213-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="76213-118">L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script.</span><span class="sxs-lookup"><span data-stu-id="76213-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="76213-119">Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="76213-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>
>
> [!IMPORTANT]
> <span data-ttu-id="76213-120">Il modulo illustrato in questo documento, AzureRM, usa .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="76213-120">The module described in this document, AzureRM, uses .NET Framework.</span></span> <span data-ttu-id="76213-121">Non è quindi compatibile con PowerShell 6.0, che usa .NET Core.</span><span class="sxs-lookup"><span data-stu-id="76213-121">This makes it incompatible with PowerShell 6.0, which uses .NET Core.</span></span> <span data-ttu-id="76213-122">Se si usa PowerShell 6.0, seguire le [istruzioni di installazione per macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="76213-122">If you are using PowerShell 6.0, follow the [installation instructions for macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="76213-123">Passaggio 2: Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76213-123">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="76213-124">L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="76213-124">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="76213-125">Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="76213-125">Run the following command from an elevated PowerShell session:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="76213-126">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="76213-126">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="76213-127">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="76213-127">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="76213-128">Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="76213-128">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="76213-129">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="76213-129">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="76213-130">Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="76213-130">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="76213-131">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="76213-131">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="76213-132">Se è installata una versione precedente di Azure PowerShell è probabile che venga visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="76213-132">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="76213-133">Per risolvere questo problema, vedere la sezione [Eseguire l'aggiornamento a una nuova versione di Azure PowerShell](#update-azps) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="76213-133">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="76213-134">Passaggio 3: caricare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="76213-134">Step 3: Load the AzureRM module</span></span>

<span data-ttu-id="76213-135">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76213-135">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="76213-136">Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="76213-136">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="76213-137">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="76213-137">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell-interactive
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="76213-138">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="76213-138">Next Steps</span></span>

<span data-ttu-id="76213-139">Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="76213-139">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="76213-140">Guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76213-140">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="76213-141">Segnalazione di problemi e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="76213-141">Reporting issues and feedback</span></span>

<span data-ttu-id="76213-142">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-powershell/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="76213-142">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="76213-143">Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="76213-143">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="76213-144">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="76213-144">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="76213-145">Come ottenere PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="76213-145">How to get PowerShellGet</span></span>

|<span data-ttu-id="76213-146">Versione sistema operativo</span><span class="sxs-lookup"><span data-stu-id="76213-146">OS Version</span></span>|<span data-ttu-id="76213-147">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="76213-147">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="76213-148">Il sistema operativo è Windows 10 o Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="76213-148">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="76213-149">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="76213-149">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="76213-150">Si vuole eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="76213-150">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="76213-151">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="76213-151">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|
|<span data-ttu-id="76213-152">È in esecuzione una versione di Windows con PowerShell 3 o 4</span><span class="sxs-lookup"><span data-stu-id="76213-152">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="76213-153">Ottenere i moduli PackageManagement</span><span class="sxs-lookup"><span data-stu-id="76213-153">Get the PackageManagement modules</span></span>](https://go.microsoft.com/fwlink/?LinkID=746217)|

### <a name="div-idhelpmechoosechecking-the-version-of-azure-powershell"></a><div id="helpmechoose"/><span data-ttu-id="76213-154">Controllo della versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76213-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="76213-155">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate.</span><span class="sxs-lookup"><span data-stu-id="76213-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="76213-156">Per determinare la versione di Azure PowerShell installata, eseguire `Get-InstalledModule AzureRM` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="76213-156">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule AzureRM` from your command line.</span></span>

```powershell-interactive
Get-InstalledModule AzureRM -AllVersions | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="76213-157">Supporto per i metodi di distribuzione classica</span><span class="sxs-lookup"><span data-stu-id="76213-157">Support for classic deployment methods</span></span>

<span data-ttu-id="76213-158">In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76213-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="76213-159">Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="76213-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="76213-160">I moduli Azure e AzureRM condividono dipendenze comuni.</span><span class="sxs-lookup"><span data-stu-id="76213-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="76213-161">Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="76213-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="div-idupdate-azpsupdating-to-a-new-version-of-azure-powershell"></a><div id="update-azps"/><span data-ttu-id="76213-162">Aggiornamento a una nuova versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="76213-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="76213-163">Se è installata una versione precedente di Azure PowerShell che include il modulo Gestione dei servizi, è probabile che venga visualizzato l'errore seguente:</span><span class="sxs-lookup"><span data-stu-id="76213-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="76213-164">Come indicato nel messaggio di errore, è necessario usare il parametro -AllowClobber per installare il modulo.</span><span class="sxs-lookup"><span data-stu-id="76213-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="76213-165">Usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="76213-165">Use the following command:</span></span>

```powershell-interactive
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="76213-166">Per altre informazioni, vedere l'argomento relativo alla guida per [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="76213-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="76213-167">Installazione di versioni del modulo affiancate</span><span class="sxs-lookup"><span data-stu-id="76213-167">Installing module versions side by side</span></span>

<span data-ttu-id="76213-168">Il metodo di installazione PowerShellGet è l'unico che supporta l'installazione di più versioni.</span><span class="sxs-lookup"><span data-stu-id="76213-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="76213-169">Ad esempio, è possibile che molti script siano stati scritti con una versione precedente di Azure PowerShell che non si è in grado di aggiornare per mancanza di tempo o risorse.</span><span class="sxs-lookup"><span data-stu-id="76213-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="76213-170">I comandi seguenti mostrano come installare più versioni di Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="76213-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell-interactive
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 2.3.0
```

<span data-ttu-id="76213-171">Solo una versione del modulo può essere caricata in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="76213-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="76213-172">È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica dei cmdlet di AzureRM:</span><span class="sxs-lookup"><span data-stu-id="76213-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell-interactive
Import-Module -Name AzureRM -RequiredVersion 2.3.0
```

> [!NOTE]
> <span data-ttu-id="76213-173">La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati.</span><span class="sxs-lookup"><span data-stu-id="76213-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="76213-174">Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="76213-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="76213-175">Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76213-175">This results in the cmdlets prompting you to sign in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="76213-176">Altri metodi di installazione</span><span class="sxs-lookup"><span data-stu-id="76213-176">Other installation methods</span></span>

<span data-ttu-id="76213-177">Per informazioni sull'installazione con l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Other installation methods](other-install.md) (Altri metodi di installazione)</span><span class="sxs-lookup"><span data-stu-id="76213-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
