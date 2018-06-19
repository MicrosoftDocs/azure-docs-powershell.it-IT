---
title: Installare Azure PowerShell con PowerShellGet
description: Come installare Azure PowerShell con PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/31/2018
ms.openlocfilehash: 9b7046157e32a5c8473210e9840f9ae1b2f45902
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323102"
---
# <a name="install-azure-powershell-with-powershellget"></a><span data-ttu-id="06525-103">Installare Azure PowerShell con PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="06525-103">Install Azure PowerShell with PowerShellGet</span></span>

<span data-ttu-id="06525-104">Questo articolo illustra l'installazione dei moduli di Azure PowerShell in ambiente Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="06525-104">This article explains the steps to install the Azure PowerShell modules in a Windows environment using PowerShellGet.</span></span>  <span data-ttu-id="06525-105">Si tratta della modalità di installazione ideale di Azure PowerShell, ma se si preferisce usare Installazione guidata piattaforma Web o il pacchetto MSI, vedere [Altri metodi di installazione ](other-install.md).</span><span class="sxs-lookup"><span data-stu-id="06525-105">This is the preferred way to install Azure PowerShell, but if you would rather install with the Web Platform Installer or MSI package, see [Other installation methods](other-install.md).</span></span>

<span data-ttu-id="06525-106">Se si intende usa Azure PowerShell in ambiente macOS o Linux, vedere l'articolo seguente: [Installare e configurare Azure PowerShell in macOS e Linux](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="06525-106">If you want to use Azure PowerShell on macOS or Linux, see the following article: [Install and configure Azure PowerShell on macOS and Linux](install-azurermps-maclinux.md).</span></span>

## <a name="system-requirements"></a><span data-ttu-id="06525-107">Requisiti di sistema</span><span class="sxs-lookup"><span data-stu-id="06525-107">System requirements</span></span>

<span data-ttu-id="06525-108">La versione 6.1.0 di Azure PowerShell richiede la versione 5.0 (o superiore) di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06525-108">Azure PowerShell version 6.1.0 requires version 5.0 (or higher) of PowerShell.</span></span> <span data-ttu-id="06525-109">Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [Aggiornamento di Windows PowerShell esistente](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="06525-109">For information on upgrading to PowerShell 5.0, see [Upgrading existing Windows PowerShell](/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

<span data-ttu-id="06525-110">PowerShellGet è automaticamente incluso come componente di PowerShell 5.0.</span><span class="sxs-lookup"><span data-stu-id="06525-110">PowerShellGet is automatically included as part of PowerShell 5.0.</span></span>

## <a name="install-or-update-the-azure-powershell-module"></a><span data-ttu-id="06525-111">Installare o aggiornare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06525-111">Install or update the Azure PowerShell module</span></span>

<span data-ttu-id="06525-112">L'installazione di Azure PowerShell da PowerShell Gallery richiede privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="06525-112">Installing Azure PowerShell from the PowerShell Gallery requires elevated privileges.</span></span> <span data-ttu-id="06525-113">Eseguire il comando seguente da una sessione di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="06525-113">Run the following command from an elevated PowerShell session:</span></span>

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

> [!IMPORTANT]
> <span data-ttu-id="06525-114">Questo comando aggiorna qualsiasi installazione esistente di Azure PowerShell nel sistema.</span><span class="sxs-lookup"><span data-stu-id="06525-114">This command will update any existing installation of Azure PowerShell on your system.</span></span> <span data-ttu-id="06525-115">Se è necessario installare più versioni, vedere la risposta alla domanda frequente [È possibile installare più versioni di Azure PowerShell?](#multiple-versions)</span><span class="sxs-lookup"><span data-stu-id="06525-115">If you need to have more than one version installed, see the FAQ answer for [Can I install multiple versions of Azure PowerShell?](#multiple-versions)</span></span>

<span data-ttu-id="06525-116">Per impostazione predefinita, PowerShell Gallery non è configurata come archivio attendibile per PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="06525-116">By default, the PowerShell gallery is not configured as a trusted repository for PowerShellGet.</span></span> <span data-ttu-id="06525-117">La prima volta che si usa PSGallery verrà visualizzato il messaggio seguente:</span><span class="sxs-lookup"><span data-stu-id="06525-117">The first time you use the PSGallery you see the following prompt:</span></span>

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

<span data-ttu-id="06525-118">Rispondere "Sì" o "Yes to All" (Sì a tutti) per continuare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="06525-118">Answer 'Yes' or 'Yes to All' to continue with the installation.</span></span>

> [!NOTE]
> <span data-ttu-id="06525-119">Se si dispone di una versione precedente alla versione 2.8.5.201 di NuGet, viene richiesto di scaricare e installare la versione più recente di NuGet.</span><span class="sxs-lookup"><span data-stu-id="06525-119">If you have a version older than 2.8.5.201 of NuGet, you are prompted to download and install the latest version of NuGet.</span></span>

<span data-ttu-id="06525-120">Il modulo AzureRM è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="06525-120">The AzureRM module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="06525-121">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure PowerShell non installato precedentemente viene scaricato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="06525-121">When you install the AzureRM module, any Azure PowerShell module not previously installed is downloaded from the PowerShell Gallery.</span></span>

## <a name="load-the-azure-powershell-module"></a><span data-ttu-id="06525-122">Caricare il modulo Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06525-122">Load the Azure PowerShell module</span></span>

<span data-ttu-id="06525-123">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06525-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="06525-124">Eseguire questa operazione in una normale sessione di PowerShell, senza privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="06525-124">You should do this in a normal (non-elevated) PowerShell session.</span></span> <span data-ttu-id="06525-125">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="06525-125">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module -Name AzureRM
```

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="06525-126">Segnalazione di problemi e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="06525-126">Reporting issues and feedback</span></span>

<span data-ttu-id="06525-127">Se si verificano bug con lo strumento, [registrare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="06525-127">If you encounter any bugs with the tool, please [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="06525-128">Per inserire commenti e suggerimenti dalla riga di comando, usare il cmdlet `Send-Feedback`.</span><span class="sxs-lookup"><span data-stu-id="06525-128">To provide feedback from the command line, use the `Send-Feedback` cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="06525-129">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="06525-129">Next Steps</span></span>

<span data-ttu-id="06525-130">Per altre informazioni sull'uso di Azure PowerShell, vedere gli articoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="06525-130">For more information about using Azure PowerShell, see the following articles:</span></span>

* [<span data-ttu-id="06525-131">Guida introduttiva ad Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06525-131">Get started with Azure PowerShell</span></span>](get-started-azureps.md)

## <a name="frequently-asked-questions"></a><span data-ttu-id="06525-132">Domande frequenti</span><span class="sxs-lookup"><span data-stu-id="06525-132">Frequently asked questions</span></span>

### <a id="helpmechoose"></a><span data-ttu-id="06525-133">Come si verifica la versione di Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="06525-133">How do I check the version of Azure PowerShell?</span></span>

<span data-ttu-id="06525-134">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono supportate.</span><span class="sxs-lookup"><span data-stu-id="06525-134">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are supported.</span></span> <span data-ttu-id="06525-135">Per determinare la versione di Azure PowerShell installata, eseguire `Get-Module AzureRM` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="06525-135">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="can-i-use-azure-powershell-for-azure-classic-deployments"></a><span data-ttu-id="06525-136">È possibile usare Azure PowerShell per le distribuzioni classiche di Azure?</span><span class="sxs-lookup"><span data-stu-id="06525-136">Can I use Azure PowerShell for Azure Classic deployments?</span></span>

<span data-ttu-id="06525-137">In presenza di distribuzioni che usano il modello di distribuzione classico, è possibile installare la versione di Gestione dei servizi di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06525-137">If you have deployments that use the classic deployment model you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="06525-138">Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="06525-138">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span> <span data-ttu-id="06525-139">I moduli Azure e AzureRM condividono dipendenze comuni.</span><span class="sxs-lookup"><span data-stu-id="06525-139">The Azure and AzureRM modules share common dependencies.</span></span> <span data-ttu-id="06525-140">Se si usano sia moduli di Azure che quelli di AzureRM, è necessario installare la stessa versione di ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="06525-140">If you use both the Azure and AzureRM modules, you should install the same version of each package.</span></span>

### <a name="a-namemultiple-versionscan-i-install-multiple-versions-of-azure-powershell"></a><span data-ttu-id="06525-141"><a name="multiple-versions"/>È possibile installare più versioni di Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="06525-141"><a name="multiple-versions"/>Can I install multiple versions of Azure PowerShell?</span></span>

<span data-ttu-id="06525-142">PowerShellGet è l'unico metodo di installazione che supporta più versioni.</span><span class="sxs-lookup"><span data-stu-id="06525-142">PowerShellGet the only method of installation that supports multiple versions.</span></span> <span data-ttu-id="06525-143">Per installare più versioni, è possibile aggiungere il parametro `-RequiredVersion` al cmdlet `Install-Module`.</span><span class="sxs-lookup"><span data-stu-id="06525-143">To install multiple versions, you can add the `-RequiredVersion` parameter to the `Install-Module` cmdlet.</span></span> <span data-ttu-id="06525-144">Per installare ad esempio le versioni 6.1.0 e 1.2.9:</span><span class="sxs-lookup"><span data-stu-id="06525-144">For example, to install both versions 6.1.0 and 1.2.9:</span></span>

```powershell
Install-Module -Name AzureRM -RequiredVersion 6.1.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

<span data-ttu-id="06525-145">Solo una versione del modulo può essere caricata in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06525-145">Only one version of the module can be loaded in a PowerShell session.</span></span> <span data-ttu-id="06525-146">È necessario aprire una nuova finestra di PowerShell e usare `Import-Module` per importare una versione specifica del modulo Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06525-146">You must open a new PowerShell window and use `Import-Module` to import a specific version of the Azure PowerShell module.</span></span>

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> <span data-ttu-id="06525-147">La versione 2.1.0 e la versione 1.2.6 sono le prime versioni del modulo progettate per l'installazione e l'uso affiancati.</span><span class="sxs-lookup"><span data-stu-id="06525-147">Version 2.1.0 and version 1.2.6 are the first module versions designed to be installed and used side by side.</span></span> <span data-ttu-id="06525-148">Durante il caricamento di una versione precedente di Azure PowerShell, vengono caricate versioni incompatibili del modulo **AzureRM.Profile**.</span><span class="sxs-lookup"><span data-stu-id="06525-148">When loading an earlier version of the Azure PowerShell, incompatible versions of the **AzureRM.Profile** module are loaded.</span></span> <span data-ttu-id="06525-149">Di conseguenza, i cmdlet richiedono di effettuare l'accesso ogni volta che si esegue un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06525-149">This results in the cmdlets prompting you to log in whenever you execute a cmdlet.</span></span>
