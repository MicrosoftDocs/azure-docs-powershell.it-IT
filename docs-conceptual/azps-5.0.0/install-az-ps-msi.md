---
title: Installare Azure PowerShell con un file MSI
description: Come installare Azure PowerShell senza PowerShellGet usando un programma di installazione MSI
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 193e8c5d14f1bf2fe9c84a9da2defac50be97ec7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753710"
---
# <a name="install-azure-powershell-on-windows-with-msi"></a><span data-ttu-id="94737-103">Installare Azure PowerShell in Windows con un programma di installazione MSI</span><span class="sxs-lookup"><span data-stu-id="94737-103">Install Azure PowerShell on Windows with MSI</span></span>

<span data-ttu-id="94737-104">Questo articolo illustra come installare Azure PowerShell in Windows con un programma di installazione MSI.</span><span class="sxs-lookup"><span data-stu-id="94737-104">This article explains how to install Azure PowerShell on Windows using an MSI installer.</span></span> <span data-ttu-id="94737-105">Il programma di installazione MSI viene fornito per gli ambienti in cui PowerShell Gallery può essere bloccato da un firewall oppure è necessario un programma di installazione offline.</span><span class="sxs-lookup"><span data-stu-id="94737-105">The MSI installer is provided for environments where the PowerShell Gallery may be blocked by a firewall, or an offline installer is needed.</span></span> <span data-ttu-id="94737-106">È consigliabile installare Azure PowerShell con PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="94737-106">The recommended way to install Azure PowerShell is with PowerShellGet.</span></span> <span data-ttu-id="94737-107">Per istruzioni sull'uso di PowerShellGet per installare Azure PowerShell, vedere [Installare Azure PowerShell con PowerShellGet ](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="94737-107">For instructions on using PowerShellGet to install Azure PowerShell, see [Install Azure PowerShell with PowerShellGet](install-az-ps.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94737-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="94737-108">Requirements</span></span>

<span data-ttu-id="94737-109">Il programma di installazione MSI in Windows è progettato per installare solo Azure PowerShell per PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="94737-109">The MSI installer on Windows is designed to install Azure PowerShell for PowerShell 5.1 only.</span></span> <span data-ttu-id="94737-110">Per l'installazione su piattaforme diverse da Windows o in versioni successive di PowerShell, [eseguire l'installazione con PowerShellGet](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="94737-110">For installation on non-Windows platforms or later versions of PowerShell, [Install with PowerShellGet](install-az-ps.md).</span></span> <span data-ttu-id="94737-111">Per controllare la versione di PowerShell, eseguire il comando:</span><span class="sxs-lookup"><span data-stu-id="94737-111">To check your PowerShell version, run the command:</span></span>

```powershell-interactive
$PSVersionTable.PSVersion
```

<span data-ttu-id="94737-112">Per usare Azure PowerShell in PowerShell 5.1, è necessario:</span><span class="sxs-lookup"><span data-stu-id="94737-112">To use Azure PowerShell in PowerShell 5.1, you need to:</span></span>

1. <span data-ttu-id="94737-113">Se necessario, eseguire l'aggiornamento a [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="94737-113">Update to [Windows PowerShell 5.1](/powershell/scripting/windows-powershell/install/installing-windows-powershell#upgrading-existing-windows-powershell) if needed.</span></span> <span data-ttu-id="94737-114">Se si usa Windows 10, PowerShell 5.1 è già installato.</span><span class="sxs-lookup"><span data-stu-id="94737-114">If you're on Windows 10, you already have PowerShell 5.1 installed.</span></span>
2. <span data-ttu-id="94737-115">Installare [.NET Framework 4.7.2 o versioni successive](/dotnet/framework/install).</span><span class="sxs-lookup"><span data-stu-id="94737-115">Install [.NET Framework 4.7.2 or later](/dotnet/framework/install).</span></span>

## <a name="install-or-update-on-windows-using-the-msi-package"></a><span data-ttu-id="94737-116">Eseguire l'installazione o l'aggiornamento in Windows tramite il pacchetto MSI</span><span class="sxs-lookup"><span data-stu-id="94737-116">Install or update on Windows using the MSI Package</span></span>

<span data-ttu-id="94737-117">Il pacchetto MSI per Azure PowerShell è disponibile in [GitHub](https://github.com/Azure/azure-powershell/releases):</span><span class="sxs-lookup"><span data-stu-id="94737-117">The MSI package for Azure PowerShell is available from [GitHub](https://github.com/Azure/azure-powershell/releases):</span></span>

1. <span data-ttu-id="94737-118">Passare a https://github.com/Azure/azure-powershell/releases.</span><span class="sxs-lookup"><span data-stu-id="94737-118">Go to https://github.com/Azure/azure-powershell/releases.</span></span>
2. <span data-ttu-id="94737-119">Cercare il modulo della raccolta più recente per Azure PowerShell. Tali versioni sono elencate in ordine cronologico e sono in genere solo una versione di rilascio senza nome, ad esempio "4.7.0".</span><span class="sxs-lookup"><span data-stu-id="94737-119">Look for the most recent Gallery Module for Azure PowerShell (these are listed chronologically and are typically just a release version with no name like "4.7.0").</span></span>
3. <span data-ttu-id="94737-120">Scorrere fino alla fine delle note sulla patch e fare clic sulla freccia accanto ad "Asset" per visualizzare le opzioni del pacchetto MSI.</span><span class="sxs-lookup"><span data-stu-id="94737-120">Scroll down to the bottom of the patch notes and click on the arrow next to "Assets" to reveal the MSI options.</span></span>
4. <span data-ttu-id="94737-121">Fare clic sul pacchetto MSI Az-Cmdlets scelto per avviare il download.</span><span class="sxs-lookup"><span data-stu-id="94737-121">Click on the Az-Cmdlets MSI of your choice to start the download.</span></span>

<span data-ttu-id="94737-122">Se le versioni precedenti dei moduli di Azure PowerShell sono state installate con il pacchetto MSI, il programma di installazione le rimuove automaticamente.</span><span class="sxs-lookup"><span data-stu-id="94737-122">If you have installed earlier versions of Azure PowerShell using the MSI, the installer automatically removes them.</span></span> <span data-ttu-id="94737-123">Il pacchetto MSI installa i moduli in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span><span class="sxs-lookup"><span data-stu-id="94737-123">The MSI package installs modules in `${env:ProgramFiles}\WindowsPowerShell\Modules`.</span></span>

<span data-ttu-id="94737-124">Per iniziare a usare Azure PowerShell, accedere con le credenziali di Azure.</span><span class="sxs-lookup"><span data-stu-id="94737-124">To start working with Azure PowerShell, sign in with your Azure credentials.</span></span>

```powershell-interactive
# Connect to Azure with an interactive dialog for sign-in
Connect-AzAccount
```

> [!NOTE]
> <span data-ttu-id="94737-125">Se il caricamento automatico dei moduli è stato disabilitato, è necessario importare manualmente il modulo con `Import-Module Az`.</span><span class="sxs-lookup"><span data-stu-id="94737-125">If you've disabled module autoloading, you need to manually import the module with `Import-Module Az`.</span></span> <span data-ttu-id="94737-126">A causa del modo in cui è strutturato il modulo, l'operazione può richiedere fino a un minuto.</span><span class="sxs-lookup"><span data-stu-id="94737-126">Because of the way the module is structured, this can take up to a minute.</span></span>

<span data-ttu-id="94737-127">È necessario ripetere questo passaggio per ogni nuova sessione di PowerShell avviata.</span><span class="sxs-lookup"><span data-stu-id="94737-127">You'll need to repeat this step for every new PowerShell session you start.</span></span> <span data-ttu-id="94737-128">Per informazioni su come mantenere l'accesso ad Azure da una sessione di PowerShell all'altra, vedere [Conservare le credenziali utente tra le sessioni di PowerShell](context-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="94737-128">To learn how to persist your Azure sign-in across PowerShell sessions, see [Persist user credentials across PowerShell sessions](context-persistence.md).</span></span>

## <a name="provide-feedback"></a><span data-ttu-id="94737-129">Fornire commenti e suggerimenti</span><span class="sxs-lookup"><span data-stu-id="94737-129">Provide feedback</span></span>

<span data-ttu-id="94737-130">Se si trova un bug in Azure PowerShell, [segnalare un problema in GitHub](https://github.com/Azure/azure-powershell/issues).</span><span class="sxs-lookup"><span data-stu-id="94737-130">If you find a bug in Azure PowerShell, [file an issue on GitHub](https://github.com/Azure/azure-powershell/issues).</span></span> <span data-ttu-id="94737-131">Per inviare feedback dalla riga di comando, usare il cmdlet [Send-Feedback](/powershell/module/az.accounts/send-feedback).</span><span class="sxs-lookup"><span data-stu-id="94737-131">To provide feedback from the command line, use the [Send-Feedback](/powershell/module/az.accounts/send-feedback) cmdlet.</span></span>

## <a name="next-steps"></a><span data-ttu-id="94737-132">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="94737-132">Next Steps</span></span>

<span data-ttu-id="94737-133">Per altre informazioni sui moduli di Azure PowerShell e sulle relative funzionalità, vedere [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="94737-133">To learn more about the Azure PowerShell modules and their features, see [Get Started with Azure PowerShell](get-started-azureps.md).</span></span> <span data-ttu-id="94737-134">Se si ha familiarità con Azure PowerShell ed è necessario eseguire la migrazione da AzureRM, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="94737-134">If you're familiar with Azure PowerShell and need to migrate from AzureRM, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>
