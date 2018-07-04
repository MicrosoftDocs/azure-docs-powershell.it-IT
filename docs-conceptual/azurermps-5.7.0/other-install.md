---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f6c52b413aa2981dc24c7e60fe832e37dcbc8baa
ms.sourcegitcommit: 4c775721461210431bd913f28d1f1e6f1976880a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/28/2018
ms.locfileid: "37091453"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="cdb3e-103">Installare Azure PowerShell in Windows con il pacchetto MSI o l'Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="cdb3e-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="cdb3e-104">Questo articolo illustra come installare Azure PowerShell in Windows usando un pacchetto MSI o l'Installazione guidata piattaforma Web (WebPI).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="cdb3e-105">Usare questi metodi di installazione solo se sono necessari per il sistema.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="cdb3e-106">È consigliabile installare Azure PowerShell in Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="cdb3e-107">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="cdb3e-108">Per eseguire Azure PowerShell in un contenitore Docker, vedere [Eseguire Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-108">To run Azure PowerShell in a Docker container, see [Run Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span></span>

<span data-ttu-id="cdb3e-109">Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-109">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="cdb3e-110">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="cdb3e-110">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="cdb3e-111">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-111">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="cdb3e-112">Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-112">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="cdb3e-113">Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-113">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="cdb3e-114">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-114">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="cdb3e-115">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-115">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="cdb3e-116">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-116">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="cdb3e-117">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-117">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="cdb3e-118">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-118">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="cdb3e-119">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-119">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="cdb3e-120">Eseguire l'installazione o l'aggiornamento in Windows con Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="cdb3e-120">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="cdb3e-121">Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](http://aka.ms/webpi-azps) e avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-121">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="cdb3e-122">Se le versioni precedenti dei moduli di Azure sono state installate da un pacchetto MSI o con l'Installazione guidata piattaforma Web, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-122">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="cdb3e-123">I moduli vengono installati in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-123">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="cdb3e-124">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-124">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="cdb3e-125">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-125">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="cdb3e-126">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-126">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="cdb3e-127">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="cdb3e-127">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="cdb3e-128">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-128">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="cdb3e-129">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="cdb3e-129">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>