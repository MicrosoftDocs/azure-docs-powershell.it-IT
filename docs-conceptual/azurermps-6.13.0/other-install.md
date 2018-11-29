---
title: Altre modalità di installazione di Azure PowerShell
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/16/2018
ms.openlocfilehash: b442da364a01cd6022c14cbb32a9b633676ca8c7
ms.sourcegitcommit: 558436c824d9b59731aa9b963cdc8df4dea932e7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/29/2018
ms.locfileid: "52586973"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="0a660-103">Installare Azure PowerShell in Windows con un programma di installazione MSI</span><span class="sxs-lookup"><span data-stu-id="0a660-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="0a660-104">Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI.</span><span class="sxs-lookup"><span data-stu-id="0a660-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span>  
<span data-ttu-id="0a660-105">Usare questi metodi di installazione solo se sono necessari per il sistema.</span><span class="sxs-lookup"><span data-stu-id="0a660-105">Use these installation methods only if they're necessary for your system.</span></span> <span data-ttu-id="0a660-106">È consigliabile installare Azure PowerShell in Windows con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="0a660-106">The recommended way to install Azure PowerShell on Windows is with PowerShellGet.</span></span> <span data-ttu-id="0a660-107">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="0a660-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-azurerm-ps.md).</span></span>

> [!NOTE]
> <span data-ttu-id="0a660-108">Il metodo Installazione guidata piattaforma Web non è più disponibile a partire dalla versione 6 di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a660-108">The Web Platform Installer method of installation is no longer available for versions of Azure PowerShell 6.x and higher.</span></span> <span data-ttu-id="0a660-109">Se si richiede l'uso dell'Installazione guidata piattaforma Web, prendere invece in considerazione un programma di installazione MSI oppure installare una versione precedente di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0a660-109">If you require use of the Web Platform Installer please consider using the MSI instead, or you can install an earlier version of Azure PowerShell.</span></span>

<span data-ttu-id="0a660-110">Per l'installazione in ambienti Linux o macOS, vedere [Installare Azure PowerShell in macOS o Linux ](install-azurermps-maclinux.md).</span><span class="sxs-lookup"><span data-stu-id="0a660-110">To install on Linux or macOS environments, see [Install Azure PowerShell on macOS or Linux](install-azurermps-maclinux.md).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="0a660-111">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="0a660-111">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="0a660-112">Azure PowerShell può essere installato usando il file MSI disponibile su [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span><span class="sxs-lookup"><span data-stu-id="0a660-112">Azure PowerShell can be installed using the MSI file available from [GitHub](https://github.com/Azure/azure-powershell/releases/latest).</span></span> <span data-ttu-id="0a660-113">Se le versioni precedenti dei moduli di Azure sono state installate come pacchetto MSI, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0a660-113">If you have installed previous versions of Azure modules as an MSI, the installer automatically removes them.</span></span> <span data-ttu-id="0a660-114">Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="0a660-114">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span> <span data-ttu-id="0a660-115">Vengono installati sia il modulo `AzureRM` che il modulo `Azure`.</span><span class="sxs-lookup"><span data-stu-id="0a660-115">Both the `AzureRM` and `Azure` modules are installed.</span></span>

> [!NOTE]
> <span data-ttu-id="0a660-116">Usare il modulo `Azure` solo se si usa il modello di distribuzione classica di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a660-116">Only use the `Azure` module if you are working with the Azure classic deployment model.</span></span>

<span data-ttu-id="0a660-117">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a660-117">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzureRmAccount
```

> [!NOTE]
>
> <span data-ttu-id="0a660-118">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="0a660-118">If you've disabled module autoloading, you need to manually import the module with `Import-Module AzureRM`.</span></span> <span data-ttu-id="0a660-119">L'operazione potrebbe richiedere qualche secondo a causa del modo in cui è strutturato il modulo.</span><span class="sxs-lookup"><span data-stu-id="0a660-119">Because of the way the module is structured, this can take a few seconds.</span></span>

<span data-ttu-id="0a660-120">È necessario ripetere questo passaggio per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="0a660-120">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="0a660-121">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="0a660-121">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>
