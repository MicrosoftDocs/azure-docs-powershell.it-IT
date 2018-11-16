---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/20/2018
ms.openlocfilehash: f9293d2715b36161c3e6d0d9469b6f18ab35d6c8
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574907"
---
# <a name="install-azure-powershell-on-windows-with-msi-or-web-platform-installer"></a><span data-ttu-id="10206-103">Installare Azure PowerShell in Windows con il pacchetto MSI o l'Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="10206-103">Install Azure PowerShell on Windows with MSI or Web Platform Installer</span></span>

<span data-ttu-id="10206-104">Questo articolo illustra come installare Azure PowerShell in Windows usando un pacchetto MSI o l'Installazione guidata piattaforma Web (WebPI).</span><span class="sxs-lookup"><span data-stu-id="10206-104">This article explains how to install Azure PowerShell on Windows using an MSI or Web Platform Installer (WebPI).</span></span>  
<span data-ttu-id="10206-105">Usare questi metodi di installazione solo se sono necessari per il sistema.</span><span class="sxs-lookup"><span data-stu-id="10206-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="10206-106">È consigliabile installare Azure PowerShell in Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="10206-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="10206-107">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="10206-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

<span data-ttu-id="10206-108">Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="10206-108">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="10206-109">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="10206-109">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="10206-110">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span><span class="sxs-lookup"><span data-stu-id="10206-110">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/tag/v5.7.0-April2018).</span></span> <span data-ttu-id="10206-111">Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="10206-111">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="10206-112">Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="10206-112">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="10206-113">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="10206-113">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="10206-114">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="10206-114">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="10206-115">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="10206-115">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="10206-116">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="10206-116">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="10206-117">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="10206-117">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="10206-118">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="10206-118">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="install-or-update-on-windows-using-the-web-platform-installer"></a><span data-ttu-id="10206-119">Eseguire l'installazione o l'aggiornamento in Windows con Installazione guidata piattaforma Web</span><span class="sxs-lookup"><span data-stu-id="10206-119">Install or update on Windows using the Web Platform Installer</span></span>

<span data-ttu-id="10206-120">Scaricare il [pacchetto per l'Installazione guidata piattaforma Web di Azure PowerShell](http://aka.ms/webpi-azps) e avviare l'installazione.</span><span class="sxs-lookup"><span data-stu-id="10206-120">Download the [Azure PowerShell WebPI package](http://aka.ms/webpi-azps) and start the install.</span></span> <span data-ttu-id="10206-121">Se le versioni precedenti dei moduli di Azure sono state installate da un pacchetto MSI o con l'Installazione guidata piattaforma Web, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="10206-121">If you have installed previous versions of Azure modules from an MSI or with WebPI, the installer automatically removes them.</span></span> <span data-ttu-id="10206-122">I moduli vengono installati in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="10206-122">Modules are installed into `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="10206-123">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="10206-123">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="10206-124">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="10206-124">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="10206-125">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="10206-125">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell-interactive
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="10206-126">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="10206-126">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="10206-127">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="10206-127">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="10206-128">Per informazioni su come conservare l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="10206-128">To learn how to persist your Azure sign in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
