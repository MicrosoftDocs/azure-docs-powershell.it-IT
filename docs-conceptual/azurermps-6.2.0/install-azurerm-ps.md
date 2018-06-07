---
title: Installare e configurare Azure PowerShell | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 9f737201f13c07565b95a20227c75794b624e99c
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821973"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="a88c0-103">Installare e configurare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a88c0-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="a88c0-104">Questo articolo illustra i passaggi per installare i moduli di Azure PowerShell in ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="a88c0-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="a88c0-105">Se si intende usa Azure PowerShell in ambiente macOS o Linux, vedere l'articolo seguente: [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="a88c0-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="a88c0-106">Requisiti di sistema</span><span class="sxs-lookup"><span data-stu-id="a88c0-106">System requirements</span></span>

<span data-ttu-id="a88c0-107">Con Azure PowerShell versione 6.0.0 è richiesta la versione 5.0 (o successiva) di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a88c0-107">Azure PowerShell version 6.0.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="a88c0-108">Per eseguire un qualsiasi cmdlet, con le versioni precedenti di Azure PowerShell era richiesta _almeno_ la versione 3.0 di PowerShell. Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [questa tabella](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="a88c0-108">Previous versions of Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.For information on upgrading to PowerShell 5.0, please see [this table](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="a88c0-109">Passaggio 1: installare PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="a88c0-109">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="a88c0-110">L'installazione di Azure PowerShell da PowerShell Gallery è il metodo preferito di installazione.</span><span class="sxs-lookup"><span data-stu-id="a88c0-110">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

<span data-ttu-id="a88c0-111">L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a88c0-111">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="a88c0-112">Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="a88c0-112">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="a88c0-113">Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="a88c0-113">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="a88c0-114">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-114">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="a88c0-115">È necessario PowerShellGet versione 1.1.2.0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="a88c0-115">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="a88c0-116">Per aggiornare PowerShellGet, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-116">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="a88c0-117">Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="a88c0-117">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="a88c0-118">L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script.</span><span class="sxs-lookup"><span data-stu-id="a88c0-118">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="a88c0-119">Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="a88c0-119">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="a88c0-120">Passaggio 2: Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a88c0-120">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="a88c0-121">L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="a88c0-121">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="a88c0-122">Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="a88c0-122">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="a88c0-123">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="a88c0-123">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="a88c0-124">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-124">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="a88c0-125">Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a88c0-125">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="a88c0-126">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="a88c0-126">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="a88c0-127">Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a88c0-127">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="a88c0-128">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="a88c0-128">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="a88c0-129">Se è installata una versione precedente di Azure PowerShell è probabile che venga visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="a88c0-129">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="a88c0-130">Per risolvere questo problema, vedere la sezione [Eseguire l'aggiornamento a una nuova versione di Azure PowerShell](#update-azps) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="a88c0-130">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="a88c0-131">Passaggio 3: caricare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="a88c0-131">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="a88c0-132">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a88c0-132">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="a88c0-133">Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="a88c0-133">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="a88c0-134">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="a88c0-134">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="a88c0-135">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="a88c0-135">Next Steps</span></span>

<span data-ttu-id="a88c0-136">Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="a88c0-136">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="a88c0-137">Guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a88c0-137">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="a88c0-138">Segnalazione di problemi e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="a88c0-138">Reporting issues and feedback</span></span>

<span data-ttu-id="a88c0-139">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-powershell/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="a88c0-139">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="a88c0-140">Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="a88c0-140">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="a88c0-141">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="a88c0-141">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="a88c0-142">Come ottenere PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="a88c0-142">How to get PowerShellGet</span></span>

|<span data-ttu-id="a88c0-143">Scenario</span><span class="sxs-lookup"><span data-stu-id="a88c0-143">Scenario</span></span>|<span data-ttu-id="a88c0-144">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="a88c0-144">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="a88c0-145">Windows 10</span><span class="sxs-lookup"><span data-stu-id="a88c0-145">Windows 10</span></span><br/><span data-ttu-id="a88c0-146">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a88c0-146">Windows Server 2016</span></span>|<span data-ttu-id="a88c0-147">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a88c0-147">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="a88c0-148">Si vuole eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="a88c0-148">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="a88c0-149">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="a88c0-149">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="a88c0-150">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="a88c0-151">È in esecuzione una versione di Windows con PowerShell 3 o 4</span><span class="sxs-lookup"><span data-stu-id="a88c0-151">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="a88c0-152"><il>[Ottenere i moduli PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="a88c0-152"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="a88c0-153">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-153">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="a88c0-154">Controllo della versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a88c0-154">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="a88c0-155">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate.</span><span class="sxs-lookup"><span data-stu-id="a88c0-155">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="a88c0-156">Per determinare la versione di Azure PowerShell installata, eseguire `Get-Module AzureRM` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="a88c0-156">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="a88c0-157">Supporto per i metodi di distribuzione classica</span><span class="sxs-lookup"><span data-stu-id="a88c0-157">Support for classic deployment methods</span></span>

<span data-ttu-id="a88c0-158">In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a88c0-158">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="a88c0-159">Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="a88c0-159">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="a88c0-160">I moduli Azure e AzureRM condividono dipendenze comuni.</span><span class="sxs-lookup"><span data-stu-id="a88c0-160">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="a88c0-161">Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="a88c0-161">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="a88c0-162">Eseguire l'aggiornamento a una nuova versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="a88c0-162">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="a88c0-163">Se è installata una versione precedente di Azure PowerShell che include il modulo Gestione dei servizi, è probabile che venga visualizzato l'errore seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-163">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

<span data-ttu-id="a88c0-164">Come indicato nel messaggio di errore, è necessario usare il parametro -AllowClobber per installare il modulo.</span><span class="sxs-lookup"><span data-stu-id="a88c0-164">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="a88c0-165">Usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="a88c0-165">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="a88c0-166">Per altre informazioni, vedere l'argomento relativo alla guida per [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="a88c0-166">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="a88c0-167">Installazione di versioni del modulo affiancate</span><span class="sxs-lookup"><span data-stu-id="a88c0-167">Installing module versions side by side</span></span>

<span data-ttu-id="a88c0-168">Il metodo di installazione PowerShellGet è l'unico che supporta l'installazione di più versioni.</span><span class="sxs-lookup"><span data-stu-id="a88c0-168">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="a88c0-169">Ad esempio, è possibile che molti script siano stati scritti con una versione precedente di Azure PowerShell che non si è in grado di aggiornare per mancanza di tempo o risorse.</span><span class="sxs-lookup"><span data-stu-id="a88c0-169">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="a88c0-170">I comandi seguenti mostrano come installare più versioni di Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="a88c0-170">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="a88c0-171">Solo una versione del modulo può essere caricata in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a88c0-171">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="a88c0-172">È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica dei cmdlet di AzureRM:</span><span class="sxs-lookup"><span data-stu-id="a88c0-172">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="a88c0-173">La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati.</span><span class="sxs-lookup"><span data-stu-id="a88c0-173">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="a88c0-174">Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="a88c0-174">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="a88c0-175">Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a88c0-175">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="a88c0-176">Altri metodi di installazione</span><span class="sxs-lookup"><span data-stu-id="a88c0-176">Other installation methods</span></span>

<span data-ttu-id="a88c0-177">Per informazioni sull'installazione con l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Other installation methods](other-install.md) (Altri metodi di installazione)</span><span class="sxs-lookup"><span data-stu-id="a88c0-177">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
