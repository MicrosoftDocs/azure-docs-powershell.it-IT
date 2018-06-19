---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell usando il pacchetto MSI o l'Installazione guidata piattaforma Web.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 0919583d9cb05a75fae3b812eed84109be8b28aa
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323272"
---
# <a name="other-installation-methods"></a><span data-ttu-id="b4c40-103">Altri metodi di installazione</span><span class="sxs-lookup"><span data-stu-id="b4c40-103">Other installation methods</span></span>

<span data-ttu-id="b4c40-104">Questo articolo illustra come installare Azure PowerShell usando un pacchetto MSI o Installazione guidata piattaforma Web (WebPI).</span><span class="sxs-lookup"><span data-stu-id="b4c40-104">This article explains how to install Azure PowerShell using an MSI or Web Platform Installer (WebPI).</span></span> <span data-ttu-id="b4c40-105">Azure PowerShell può essere eseguito anche dall'interno di un contenitore Docker.</span><span class="sxs-lookup"><span data-stu-id="b4c40-105">You can also run Azure PowerShell from inside of a Docker container.</span></span> <span data-ttu-id="b4c40-106">Usare questi metodi di installazione solo se sono necessari per il sistema.</span><span class="sxs-lookup"><span data-stu-id="b4c40-106">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="b4c40-107">Il modo canonico per installare Azure PowerShell è tramite PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="b4c40-107">The canonical way to install Azure PowerShell is through PowerShellGet.</span></span> <span data-ttu-id="b4c40-108">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="b4c40-108">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="b4c40-109">Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="b4c40-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="b4c40-110">Eseguire l'installazione o l'aggiornamento in Windows con Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="b4c40-110">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="b4c40-111">L'installazione della versione più recente di Azure PowerShell dall'Installazione guidata piattaforma Web è uguale a quella per le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b4c40-111">Installing the latest Azure PowerShell from WebPI is the same as it was for previous versions.</span></span>
<span data-ttu-id="b4c40-112">Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](http://aka.ms/webpi-azps) e avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4c40-112">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span>

> [!NOTE]
> <span data-ttu-id="b4c40-113">Se sono stati installati precedentemente moduli Azure da PowerShell Gallery, il programma di installazione li rimuoverà automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b4c40-113">If you have previously installed Azure modules from the PowerShell Gallery, the installer automatically removes them.</span></span> <span data-ttu-id="b4c40-114">Ciò semplifica l'ambiente, garantendo l'installazione di una sola versione di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4c40-114">This simplifies your environment by ensuring that only one version of Azure PowerShell is installed.</span></span> <span data-ttu-id="b4c40-115">Tuttavia, esistono scenari in cui sono necessarie più versioni installate nello stesso momento.</span><span class="sxs-lookup"><span data-stu-id="b4c40-115">However, there are scenarios where you may need multiple versions installed at the same time.</span></span>
>
> <span data-ttu-id="b4c40-116">I moduli di PowerShell Gallery consentono di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="b4c40-116">PowerShell Gallery modules install modules in `$env:ProgramFiles\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="b4c40-117">Al contrario, il programma di Installazione guidata piattaforma Web installerà i moduli di Azure in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span><span class="sxs-lookup"><span data-stu-id="b4c40-117">In contrast, the WebPI installer installs the Azure modules in `$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\`.</span></span>
>
> <span data-ttu-id="b4c40-118">Se si verifica un errore durante l'installazione, è possibile rimuovere manualmente le cartelle `Azure*` dalla cartella `$env:ProgramFiles\WindowsPowerShell\Modules` e riprovare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="b4c40-118">If an error occurs during install, you can manually remove the `Azure*` folders in your `$env:ProgramFiles\WindowsPowerShell\Modules` folder, and try the installation again.</span></span>

<span data-ttu-id="b4c40-119">Al termine dell'installazione, l'impostazione `$env:PSModulePath` includerà le directory contenenti i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4c40-119">Once the installation completes, your `$env:PSModulePath` setting should include the directories containing the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b4c40-120">È possibile usare il comando seguente per verificare che Azure PowerShell sia installato correttamente:</span><span class="sxs-lookup"><span data-stu-id="b4c40-120">The following command can be used to verify that the Azure PowerShell is installed properly:</span></span>

```powershell
# To make sure the Azure PowerShell module is available after you install
Get-Module -ListAvailable Azure* | Select-Object Name, Version, Path
```

> [!NOTE]
> <span data-ttu-id="b4c40-121">Durante l'uso dell'Installazione guidata piattaforma Web è possibile che si verifichi un problema noto.</span><span class="sxs-lookup"><span data-stu-id="b4c40-121">There is a known issue that can occur when installing from WebPI.</span></span> <span data-ttu-id="b4c40-122">Se il computer richiede il riavvio a causa di aggiornamenti di sistema o di altre installazioni, gli aggiornamenti di `$env:PSModulePath` potrebbero non includere il percorso in cui è installato Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4c40-122">If your computer requires a restart due to system updates or other installations, it may cause updates to `$env:PSModulePath` to fail to include the path where Azure PowerShell is installed.</span></span>

<span data-ttu-id="b4c40-123">Quando si tenta di caricare o eseguire i cmdlet dopo l'installazione, è possibile ricevere il messaggio di errore seguente:</span><span class="sxs-lookup"><span data-stu-id="b4c40-123">When attempting to load or execute cmdlets after installation, you can receive the following error message:</span></span>

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

<span data-ttu-id="b4c40-124">Questo errore può essere corretto riavviando il computer o importando il modulo usando il percorso completo.</span><span class="sxs-lookup"><span data-stu-id="b4c40-124">This error can be corrected by restarting the machine or importing the module using the fully qualified path.</span></span>

```powershell
Import-Module "$env:ProgramFiles(x86)\Microsoft SDKs\Azure\PowerShell\AzureRM.psd1"
```

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="b4c40-125">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="b4c40-125">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="b4c40-126">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://aka.ms/azps-release).</span><span class="sxs-lookup"><span data-stu-id="b4c40-126">Azure PowerShell can be installed using the MSI file available from [GitHub](https://aka.ms/azps-release).</span></span> <span data-ttu-id="b4c40-127">Se sono state installate versioni precedenti dei moduli di Azure, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="b4c40-127">If you have installed previous versions of Azure modules, the installer automatically removes them.</span></span> <span data-ttu-id="b4c40-128">Il pacchetto MSI consente di installare i moduli in `$env:ProgramFiles\WindowsPowerShell\Modules`, ma non crea cartelle specifiche per la versione.</span><span class="sxs-lookup"><span data-stu-id="b4c40-128">The MSI package installs modules in `$env:ProgramFiles\WindowsPowerShell\Modules` but does not create version-specific folders.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="b4c40-129">Eseguire in un contenitore Docker</span><span class="sxs-lookup"><span data-stu-id="b4c40-129">Run in a Docker container</span></span>

<span data-ttu-id="b4c40-130">È disponibile un set di immagini Docker preconfigurate con Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4c40-130">We maintain a set of Docker images preconfigured with Azure PowerShell.</span></span> <span data-ttu-id="b4c40-131">Sono disponibili due tipi di contenitori: quelli che eseguono la versione tradizionale di PowerShell in Windows e un contenitore che esegue PowerShell Core in Windows o Linux.</span><span class="sxs-lookup"><span data-stu-id="b4c40-131">There are two types of containers available: Those running traditional PowerShell on Windows, and a container running PowerShell Core on either Windows or Linux.</span></span>

| <span data-ttu-id="b4c40-132">Environment</span><span class="sxs-lookup"><span data-stu-id="b4c40-132">Environment</span></span> | <span data-ttu-id="b4c40-133">Immagine Docker</span><span class="sxs-lookup"><span data-stu-id="b4c40-133">Docker image</span></span> |
|-------------|--------------|
| <span data-ttu-id="b4c40-134">PowerShell in Windows</span><span class="sxs-lookup"><span data-stu-id="b4c40-134">PowerShell on Windows</span></span> | [<span data-ttu-id="b4c40-135">azuresdk/azure-powershell</span><span class="sxs-lookup"><span data-stu-id="b4c40-135">azuresdk/azure-powershell</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell/) |
| <span data-ttu-id="b4c40-136">PowerShell Core in Windows</span><span class="sxs-lookup"><span data-stu-id="b4c40-136">PowerShell Core on Windows</span></span> | [<span data-ttu-id="b4c40-137">azuresdk/azure-powershell-core:nanoserver</span><span class="sxs-lookup"><span data-stu-id="b4c40-137">azuresdk/azure-powershell-core:nanoserver</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |
| <span data-ttu-id="b4c40-138">PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="b4c40-138">PowerShell Core on Linux</span></span> | [<span data-ttu-id="b4c40-139">azuresdk/azure-powershell-core:latest</span><span class="sxs-lookup"><span data-stu-id="b4c40-139">azuresdk/azure-powershell-core:latest</span></span>](https://hub.docker.com/r/azuresdk/azure-powershell-core/) |

<span data-ttu-id="b4c40-140">Per eseguire uno di questi contenitori, usare `docker run -it $ImageName` per ottenere un terminale interattivo.</span><span class="sxs-lookup"><span data-stu-id="b4c40-140">To run any of these containers, you use `docker run -it $ImageName` to get an interactive terminal.</span></span> <span data-ttu-id="b4c40-141">Ad esempio, per eseguire PowerShell Core in un contenitore Linux usare:</span><span class="sxs-lookup"><span data-stu-id="b4c40-141">For example, to run the PowerShell Core on Linux container, use:</span></span>

```powershell
docker run -it azuresdk/azure-powershell-core:latest
```

> [!NOTE]
> <span data-ttu-id="b4c40-142">Per eseguire un contenitore Windows in Docker, il sistema operativo host deve essere Windows e Docker deve essere impostato per l'esecuzione dei contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="b4c40-142">To run a Windows container in Docker, your host OS must be Windows and Docker must be set to run Windows containers.</span></span> <span data-ttu-id="b4c40-143">Per informazioni su come passare da un ambiente Windows a un ambiente Linux in Docker, vedere il documento Docker [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers) (Passare dai contenitori Windows ai contenitori Linux).</span><span class="sxs-lookup"><span data-stu-id="b4c40-143">To learn about switching between Windows and Linux environments in Docker, see the Docker documentation [Switch between Windows and Linux containers](https://docs.docker.com/docker-for-windows/#switch-between-windows-and-linux-containers).</span></span>