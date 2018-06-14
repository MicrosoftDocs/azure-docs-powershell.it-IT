---
title: Installare e configurare Azure PowerShell | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: 8819a0ba2dfb6bc3f88e80581257180aa1558ba4
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853815"
---
# <a name="install-and-configure-azure-powershell"></a><span data-ttu-id="f9f2f-103">Installare e configurare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9f2f-103">Install and configure Azure PowerShell</span></span>

<span data-ttu-id="f9f2f-104">Questo articolo illustra i passaggi per installare i moduli di Azure PowerShell in ambiente Windows.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment.</span></span>
<span data-ttu-id="f9f2f-105">Se si intende usa Azure PowerShell in ambiente macOS o Linux, vedere l'articolo seguente: [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="f9f2f-105">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

<span data-ttu-id="f9f2f-106">L'installazione di Azure PowerShell da PowerShell Gallery è il metodo preferito di installazione.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-106">Installing Azure PowerShell from the PowerShell Gallery is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="f9f2f-107">Passaggio 1: installare PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="f9f2f-107">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="f9f2f-108">L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-108">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="f9f2f-109">Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-109">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="f9f2f-110">Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-110">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

<span data-ttu-id="f9f2f-111">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-111">You should see something similar to the following output:</span></span>

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="f9f2f-112">È necessario PowerShellGet versione 1.1.2.0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-112">You need PowerShellGet version 1.1.2.0 or higher.</span></span> <span data-ttu-id="f9f2f-113">Per aggiornare PowerShellGet, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-113">To update PowerShellGet, use the following command:</span></span>

```powershell
Install-Module PowerShellGet -Force
```

<span data-ttu-id="f9f2f-114">Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-114">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget) section of this article.</span></span>

> [!NOTE]
> <span data-ttu-id="f9f2f-115">L'uso di PowerShellGet richiede criteri di esecuzione che consentono di eseguire script.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-115">Using PowerShellGet requires an Execution Policy that allows you to run scripts.</span></span> <span data-ttu-id="f9f2f-116">Per altre informazioni sui criteri di esecuzione di PowerShell, vedere [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies) (Informazioni sui criteri di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="f9f2f-116">For more information about PowerShell's Execution Policy, see [About Execution Policies](/powershell/module/microsoft.powershell.core/about/about_execution_policies).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="f9f2f-117">Passaggio 2: Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9f2f-117">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="f9f2f-118">L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-118">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="f9f2f-119">Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-119">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="f9f2f-120">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-120">By default, the PowerShell gallery is not configured as a Trusted repository for PowerShellGet.</span></span> <span data-ttu-id="f9f2f-121">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-121">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

<span data-ttu-id="f9f2f-122">Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-122">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="f9f2f-123">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-123">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="f9f2f-124">Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-124">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="f9f2f-125">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-125">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded and from the PowerShell Gallery.</span></span>

<span data-ttu-id="f9f2f-126">Se è installata una versione precedente di Azure PowerShell è probabile che venga visualizzato un errore.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-126">If you have a previous version of Azure PowerShell installed you may receive an error.</span></span> <span data-ttu-id="f9f2f-127">Per risolvere questo problema, vedere la sezione [Eseguire l'aggiornamento a una nuova versione di Azure PowerShell](#update-azps) di questo articolo.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-127">To resolve this issue, see the [Updating to a new version of Azure PowerShell](#update-azps) section of this article.</span></span>

## <a name="step-3-load-the-azurerm-module"></a><span data-ttu-id="f9f2f-128">Passaggio 3: caricare il modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="f9f2f-128">Step 3: Load the AzureRM module</span></span>
<span data-ttu-id="f9f2f-129">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-129">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="f9f2f-130">Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-130">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="f9f2f-131">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-131">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a><span data-ttu-id="f9f2f-132">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="f9f2f-132">Next Steps</span></span>

<span data-ttu-id="f9f2f-133">Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-133">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="f9f2f-134">Guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9f2f-134">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="f9f2f-135">Segnalazione di problemi e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="f9f2f-135">Reporting issues and feedback</span></span>

<span data-ttu-id="f9f2f-136">Se si rilevano bug con lo strumento, segnalare un problema nella sezione [Issues](https://github.com/Azure/azure-powershell/issues) (Problemi) del repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-136">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-powershell/issues) section of our GitHub repo.</span></span> <span data-ttu-id="f9f2f-137">Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-137">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="f9f2f-138">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="f9f2f-138">Frequently asked questions</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="f9f2f-139">Come ottenere PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="f9f2f-139">How to get PowerShellGet</span></span>

|<span data-ttu-id="f9f2f-140">Scenario</span><span class="sxs-lookup"><span data-stu-id="f9f2f-140">Scenario</span></span>|<span data-ttu-id="f9f2f-141">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="f9f2f-141">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="f9f2f-142">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f9f2f-142">Windows 10</span></span><br/><span data-ttu-id="f9f2f-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f9f2f-143">Windows Server 2016</span></span>|<span data-ttu-id="f9f2f-144">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f9f2f-144">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="f9f2f-145">Si vuole eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="f9f2f-145">I want to upgrade to PowerShell 5</span></span>|<ol><li>[<span data-ttu-id="f9f2f-146">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="f9f2f-146">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)</li><li><span data-ttu-id="f9f2f-147">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-147">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|
|<span data-ttu-id="f9f2f-148">È in esecuzione una versione di Windows con PowerShell 3 o 4</span><span class="sxs-lookup"><span data-stu-id="f9f2f-148">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|<ol><span data-ttu-id="f9f2f-149"><il>[Ottenere i moduli PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span><span class="sxs-lookup"><span data-stu-id="f9f2f-149"><il>[Get the PackageManagement modules](http://go.microsoft.com/fwlink/?LinkID=746217)</il></span></span><li><span data-ttu-id="f9f2f-150">Eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-150">Run the following command:</span></span><br/>```Install-Module PowerShellGet -Force```</li></ol>|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="f9f2f-151">Controllo della versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9f2f-151">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="f9f2f-152">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-152">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="f9f2f-153">Per determinare la versione di Azure PowerShell installata, eseguire `Get-Module AzureRM` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-153">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a><span data-ttu-id="f9f2f-154">Supporto per i metodi di distribuzione classica</span><span class="sxs-lookup"><span data-stu-id="f9f2f-154">Support for classic deployment methods</span></span>

<span data-ttu-id="f9f2f-155">In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-155">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="f9f2f-156">Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="f9f2f-156">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="f9f2f-157">I moduli Azure e AzureRM condividono dipendenze comuni.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-157">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="f9f2f-158">Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-158">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a id="update-azps"></a><span data-ttu-id="f9f2f-159">Eseguire l'aggiornamento a una nuova versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f9f2f-159">Updating to a new version of Azure PowerShell</span></span>

<span data-ttu-id="f9f2f-160">Se è installata una versione precedente di Azure PowerShell che include il modulo Gestione dei servizi, è probabile che venga visualizzato l'errore seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-160">If you have a previous version of Azure PowerShell installed that includes the Service Management module, you may receive the following error:</span></span>

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

<span data-ttu-id="f9f2f-161">Come indicato nel messaggio di errore, è necessario usare il parametro -AllowClobber per installare il modulo.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-161">As the error message states, you need to use the -AllowClobber parameter to install the module.</span></span> <span data-ttu-id="f9f2f-162">Usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-162">Use the following command:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

<span data-ttu-id="f9f2f-163">Per altre informazioni, vedere l'argomento relativo alla guida per [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span><span class="sxs-lookup"><span data-stu-id="f9f2f-163">For more information, see the help topic for [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).</span></span>

### <a name="installing-module-versions-side-by-side"></a><span data-ttu-id="f9f2f-164">Installazione di versioni del modulo affiancate</span><span class="sxs-lookup"><span data-stu-id="f9f2f-164">Installing module versions side by side</span></span>

<span data-ttu-id="f9f2f-165">Il metodo di installazione PowerShellGet è l'unico che supporta l'installazione di più versioni.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-165">The PowerShellGet method of installation is the only method that supports the installation of multiple versions.</span></span> <span data-ttu-id="f9f2f-166">Ad esempio, è possibile che molti script siano stati scritti con una versione precedente di Azure PowerShell che non si è in grado di aggiornare per mancanza di tempo o risorse.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-166">For example, you may have scripts written using a previous version of Azure PowerShell that you don't have the time or resources to updated.</span></span> <span data-ttu-id="f9f2f-167">I comandi seguenti mostrano come installare più versioni di Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-167">The following commands illustrate how to install multiple versions of Azure PowerShell:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="f9f2f-168">Solo una versione del modulo può essere caricata in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-168">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="f9f2f-169">È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica dei cmdlet di AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f9f2f-169">You must open a new PowerShell window and use `Import-Module` to import a specific version of the AzureRM cmdlets:</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="f9f2f-170">La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-170">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="f9f2f-171">Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-171">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="f9f2f-172">Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9f2f-172">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>

### <a name="other-installation-methods"></a><span data-ttu-id="f9f2f-173">Altri metodi di installazione</span><span class="sxs-lookup"><span data-stu-id="f9f2f-173">Other installation methods</span></span>

<span data-ttu-id="f9f2f-174">Per informazioni sull'installazione con l'Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Other installation methods](other-install.md) (Altri metodi di installazione)</span><span class="sxs-lookup"><span data-stu-id="f9f2f-174">For information about installing using the Web Platform Installer or the MSI Package, see [Other installation methods](other-install.md)</span></span>
