---
title: Altre modalità di installazione e configurazione di Azure PowerShell | Microsoft Docs
description: Come installare Azure PowerShell usando il pacchetto MSI o l'Installazione guidata piattaforma Web.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/06/2017
ms.openlocfilehash: cb4ced3b72b69546594d75e7eb7db822b549a664
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34821446"
---
# <a name="other-installation-methods"></a><span data-ttu-id="a5197-103">Altri metodi di installazione</span><span class="sxs-lookup"><span data-stu-id="a5197-103">Other installation methods</span></span>

<span data-ttu-id="a5197-104">Per Azure PowerShell sono disponibili più metodi di installazione.</span><span class="sxs-lookup"><span data-stu-id="a5197-104">Azure PowerShell has multiple installation methods.</span></span> <span data-ttu-id="a5197-105">L'uso di PowerShellGet con PowerShell Gallery è il metodo preferito.</span><span class="sxs-lookup"><span data-stu-id="a5197-105">Using PowerShellGet with the PowerShell Gallery is the preferred method.</span></span> <span data-ttu-id="a5197-106">Azure PowerShell può essere installato in Windows usando l'Installazione guidata piattaforma Web (WebPI) o il file MSI disponibile su GitHub.</span><span class="sxs-lookup"><span data-stu-id="a5197-106">Azure PowerShell can be installed on Windows using the Web Platform Installer (WebPI) or by using the MSI file available from GitHub.</span></span> <span data-ttu-id="a5197-107">Azure PowerShell può anche essere installato in un contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="a5197-107">Azure PowerShell can also be installed in a Docker container.</span></span>

## <a name="install-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="a5197-108">Eseguire l'installazione in Windows con l'Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="a5197-108">Install on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="a5197-109">L'installazione della versione più recente di Azure PowerShell dall'Installazione guidata piattaforma Web è uguale a quella per le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a5197-109">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="a5197-110">Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](http://aka.ms/webpi-azps) e avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a5197-110">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="a5197-111">Se sono stati installati precedentemente moduli Azure da PowerShell Gallery, il programma di installazione li rimuoverà automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a5197-111">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="a5197-112">Ciò semplifica l'ambiente, garantendo l'installazione di una sola versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5197-112">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="a5197-113">Tuttavia, esistono scenari in cui sono necessarie più versioni installate nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="a5197-113">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="a5197-114">I moduli di PowerShell Gallery consentono di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="a5197-114">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="a5197-115">Al contrario, il programma di Installazione guidata piattaforma Web installerà i moduli di Azure in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="a5197-115">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="a5197-116">Se si verifica un errore durante l'installazione, è possibile rimuovere manualmente le cartelle di Azure\* nella cartella `$env:ProgramFiles\WindowsPowerShell\Modules` e ripetere l'installazione.</span><span class="sxs-lookup"><span data-stu-id="a5197-116">If an error occurs during install, you can manually remove the Azure\* folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="a5197-117">Al termine dell'installazione, l'impostazione `$env:PSModulePath` includerà le directory contenenti i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5197-117">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="a5197-118">È possibile usare il comando seguente per verificare che Azure PowerShell sia installato correttamente.</span><span class="sxs-lookup"><span data-stu-id="a5197-118">The following command can be used to verify that the Azure PowerShell is installed properly.</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="a5197-119">Durante l'uso dell'Installazione guidata piattaforma Web è possibile che si verifichi un problema noto.</span><span class="sxs-lookup"><span data-stu-id="a5197-119">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="a5197-120">Se il computer richiede il riavvio a causa di aggiornamenti di sistema o di altre installazioni, gli aggiornamenti di `$env:PSModulePath` potrebbero non includere il percorso in cui è installato Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5197-120">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="a5197-121">Quando si tenta di caricare o eseguire i cmdlet dopo l'installazione, è possibile ricevere il messaggio di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="a5197-121">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

```
PS C:\> Connect-AzureRmAccount
Connect-AzureRmAccount : The term 'Connect-AzureRmAccount' is not recognized as the name of a cmdlet,
function, script file, or operable program. Check the spelling of the name, or if a path was
included, verify that the path is correct and try again.
At line:1 char:1
+ Connect-AzureRmAccount
+ ~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : ObjectNotFound: (Connect-AzureRmAccount:String) [], CommandNotFoundException
    + FullyQualifiedErrorId : CommandNotFoundException
```

<span data-ttu-id="a5197-122">Questo errore può essere corretto riavviando il computer o importando il modulo usando il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="a5197-122">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span> <span data-ttu-id="a5197-123">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="a5197-123">For example:</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-on-windows-using-the-msi-package"></a><span data-ttu-id="a5197-124">Eseguire l'installazione in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="a5197-124">Install on Windows using the MSI Package</span></span>

<span data-ttu-id="a5197-125">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="a5197-125">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="a5197-126">Se sono state installate versioni precedenti dei moduli di Azure, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a5197-126">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="a5197-127">Il pacchetto MSI consente di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`, ma non crea cartelle specifiche per la versione.</span><span class="sxs-lookup"><span data-stu-id="a5197-127">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="install-in-a-docker-container"></a><span data-ttu-id="a5197-128">Eseguire l'installazione in un contenitore Docker</span><span class="sxs-lookup"><span data-stu-id="a5197-128">Install in a Docker container</span></span>

<span data-ttu-id="a5197-129">È disponibile un'immagine Docker preconfigurata con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a5197-129">We maintain a Docker image preconfigured with Azure PowerShell.</span></span>

<span data-ttu-id="a5197-130">Eseguire il contenitore con `docker run`.</span><span class="sxs-lookup"><span data-stu-id="a5197-130">Run the container with `docker run`.</span></span>

```powershell
docker run azuresdk/azure-powershell
```

<span data-ttu-id="a5197-131">È inoltre disponibile un subset di cmdlet come contenitore di PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="a5197-131">In addition, we maintain a subset of cmdlets as a PowerShell Core container.</span></span>

<span data-ttu-id="a5197-132">Per Mac/Linux, usare l'immagine `latest`.</span><span class="sxs-lookup"><span data-stu-id="a5197-132">For Mac/Linux, use the `latest` image.</span></span>

```bash
docker run azuresdk/azure-powershell-core:latest
```

<span data-ttu-id="a5197-133">Per Windows, usare l'immagine `nanoserver`.</span><span class="sxs-lookup"><span data-stu-id="a5197-133">For Windows, use the `nanoserver` image.</span></span>

```powershell
docker run azuresdk/azure-powershell-core:nanoserver
```

<span data-ttu-id="a5197-134">Azure PowerShell è installato nell'immagine tramite `Install-Module` da [PowerShell Gallery](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="a5197-134">Azure PowerShell is installed on the image via `Install-Module` from the [PowerShell Gallery](https://www.powershellgallery.com/).</span></span>
