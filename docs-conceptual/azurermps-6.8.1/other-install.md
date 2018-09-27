---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 6bf66e312557f047a9393e26b9de736c1c55c261
ms.sourcegitcommit: 3a02e0c85c83de873981dd392500bc82c1cf9286
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/24/2018
ms.locfileid: "46560202"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="94d7a-103">Installare Azure PowerShell in Windows con un programma di installazione MSI</span><span class="sxs-lookup"><span data-stu-id="94d7a-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="94d7a-104">Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI.</span><span class="sxs-lookup"><span data-stu-id="94d7a-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="94d7a-105">Usare questi metodi di installazione solo se sono necessari per il sistema.</span><span class="sxs-lookup"><span data-stu-id="94d7a-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="94d7a-106">È consigliabile installare Azure PowerShell in Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="94d7a-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="94d7a-107">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="94d7a-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="94d7a-108">Il metodo Installazione guidata piattaforma Web non è più disponibile a partire dalla versione 6 di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94d7a-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="94d7a-109">Se si richiede l'uso dell'Installazione guidata piattaforma Web, prendere invece in considerazione un programma di installazione MSI oppure installare una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94d7a-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="94d7a-110">Per eseguire Azure PowerShell in un contenitore Docker, vedere [Eseguire Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span><span class="sxs-lookup"><span data-stu-id="94d7a-110">To run Azure PowerShell in a Docker container, see [Run Azure PowerShell in Docker](azurerm-ps-in-docker.md).</span></span>

<span data-ttu-id="94d7a-111">Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="94d7a-111">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="94d7a-112">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="94d7a-112">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="94d7a-113">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="94d7a-113">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="94d7a-114">Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="94d7a-114">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="94d7a-115">Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="94d7a-115">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="94d7a-116">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="94d7a-116">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="94d7a-117">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="94d7a-117">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="94d7a-118">Per iniziare a usare Azure PowerShell è necessario caricare `AzureRM` nella sessione corrente di PowerShell con il cmdlet [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module), quindi accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="94d7a-118">To start working with Azure PowerShell, you need to load `AzureRM` into your current PowerShell session with the [Import-Module](/powershell/module/Microsoft.PowerShell.Core/Import-Module) cmdlet, and then sign in with your Azure credentials.</span></span>

```powershell
# Import the module into the PowerShell session
Import-Module AzureRM
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

<span data-ttu-id="94d7a-119">È necessario ripetere questi passaggi per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="94d7a-119">You'll need to repeat these steps for every new PowerShell session you start.</span></span> <span data-ttu-id="94d7a-120">L'importazione automatica del modulo `AzureRM` richiede la configurazione di un profilo di PowerShell. Vedere [Informazioni sui profili](/powershell/module/microsoft.powershell.core/about/about_profiles).</span><span class="sxs-lookup"><span data-stu-id="94d7a-120">Automatically importing the `AzureRM` module requires setting up a PowerShell profile, which you can learn about in [About Profiles](/powershell/module/microsoft.powershell.core/about/about_profiles).</span></span>
<span data-ttu-id="94d7a-121">Per informazioni su come mantenere l'accesso ad Azure da una sessione all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="94d7a-121">To learn how to persist your Azure sign-in across sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>