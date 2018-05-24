---
title: Installare e configurare Azure PowerShell in macOS e Linux | Microsoft Docs
description: Come installare e configurare Azure PowerShell per il primo uso in macOS e Linux.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/12/2018
ms.openlocfilehash: 9e4c727c9adc378b9f1a65d3cb3dda7af05c33f5
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="install-and-configure-azure-powershell-on-macos-and-linux"></a><span data-ttu-id="9ed14-103">Installare e configurare Azure PowerShell in macOS e Linux</span><span class="sxs-lookup"><span data-stu-id="9ed14-103">Install and configure Azure PowerShell on macOS and Linux</span></span>

<span data-ttu-id="9ed14-104">È ora possibile installare PowerShell Core v6 e Azure PowerShell in piattaforme non Windows.</span><span class="sxs-lookup"><span data-stu-id="9ed14-104">It is now possible to install PowerShell Core v6 and Azure PowerShell on non-Windows platforms.</span></span>
<span data-ttu-id="9ed14-105">Il processo di installazione di Azure PowerShell in macOS e Linux non è molto diverso da quello per Windows, ma è prima necessario installare PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="9ed14-105">The process of installing Azure PowerShell on macOS and Linux is not that different from Windows, however, you must first install PowerShell Core v6.</span></span>

> [!NOTE]

> <span data-ttu-id="9ed14-106">Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.</span><span class="sxs-lookup"><span data-stu-id="9ed14-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="9ed14-107">Il supporto per questi prodotti è limitato.</span><span class="sxs-lookup"><span data-stu-id="9ed14-107">Support for these products is limited.</span></span> <span data-ttu-id="9ed14-108">Se si verificano problemi o si trovano bug, registrare i problemi in GitHub.</span><span class="sxs-lookup"><span data-stu-id="9ed14-108">If you have problems or discover bugs, please file Issues in GitHub.</span></span>
>
> * [<span data-ttu-id="9ed14-109">Problemi per PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="9ed14-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="9ed14-110">Problemi per Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9ed14-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="step-1-install-powershell-core-v6"></a><span data-ttu-id="9ed14-111">Passaggio 1: Installare PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="9ed14-111">Step 1: Install PowerShell Core v6</span></span>

<span data-ttu-id="9ed14-112">Il processo di installazione di PowerShell Core v6 varia a seconda del sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ed14-112">The process of installing PowerShell Core v6 on varies depending on the target operating system.</span></span>
<span data-ttu-id="9ed14-113">Nonostante sia possibile installare PowerShell Core v6 in Windows, questo articolo è incentrato su macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="9ed14-113">While it is possible to install PowerShell Core v6 on Windows, this article focuses on macOS and Linux.</span></span> <span data-ttu-id="9ed14-114">Se si intende usare Azure PowerShell in Windows, vedere l'articolo dedicato all'[installazione](./install-azurerm-ps.md) per Windows.</span><span class="sxs-lookup"><span data-stu-id="9ed14-114">If you want to use Azure PowerShell on Windows, see the [install](./install-azurerm-ps.md) article for Windows.</span></span>

<span data-ttu-id="9ed14-115">L'installazione di **PowerShell Core v6** in Linux o macOS varia a seconda della distribuzione Linux e della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9ed14-115">Installing **PowerShell Core v6** on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="9ed14-116">Per istruzioni dettagliate, vedere l'articolo seguente:</span><span class="sxs-lookup"><span data-stu-id="9ed14-116">Detailed instructions can be found in the following article:</span></span>

- <span data-ttu-id="9ed14-117">[Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux) (Installazione di PowerShell Core in macOS e Linux)</span><span class="sxs-lookup"><span data-stu-id="9ed14-117">[Installing PowerShell Core on macOS and Linux](/powershell/scripting/setup/installing-powershell-core-on-macos-and-linux)</span></span>

## <a name="step-2-install-azure-powershell-for-net-core"></a><span data-ttu-id="9ed14-118">Passaggio 2: installare Azure PowerShell per .NET Core</span><span class="sxs-lookup"><span data-stu-id="9ed14-118">Step 2: Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="9ed14-119">PowerShell Core v6 viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="9ed14-119">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="9ed14-120">Ciò semplifica l'installazione di qualsiasi modulo pubblicato in PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="9ed14-120">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="9ed14-121">Per installare Azure PowerShell, aprire una nuova sessione di PowerShell ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="9ed14-121">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="step-3-load-the-azurermnetcore-module"></a><span data-ttu-id="9ed14-122">Passaggio 3: caricare il modulo AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="9ed14-122">Step 3: Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="9ed14-123">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ed14-123">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="9ed14-124">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="9ed14-124">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="9ed14-125">Al termine dell'importazione, è possibile testare il modulo appena installato eseguendo un tentativo di accesso ad Azure con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="9ed14-125">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Login-AzureRMAccount
```

<span data-ttu-id="9ed14-126">Il comando riportato sopra richiede di passare a `https://aka.ms/devicelogin` e immettere il codice fornito.</span><span class="sxs-lookup"><span data-stu-id="9ed14-126">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="9ed14-127">Cmdlet disponibili</span><span class="sxs-lookup"><span data-stu-id="9ed14-127">Available cmdlets</span></span>

<span data-ttu-id="9ed14-128">I moduli di Azure PowerShell per .NET Standard sono ancora in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="9ed14-128">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="9ed14-129">Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli.</span><span class="sxs-lookup"><span data-stu-id="9ed14-129">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="9ed14-130">Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="9ed14-130">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="9ed14-131">Gestione account</span><span class="sxs-lookup"><span data-stu-id="9ed14-131">Account management</span></span>
  - <span data-ttu-id="9ed14-132">Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9ed14-132">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="9ed14-133">Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="9ed14-133">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="9ed14-134">Environment</span><span class="sxs-lookup"><span data-stu-id="9ed14-134">Environment</span></span>
  - <span data-ttu-id="9ed14-135">Recupero di ambienti predefiniti di Microsoft Azure diversi</span><span class="sxs-lookup"><span data-stu-id="9ed14-135">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="9ed14-136">Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack</span><span class="sxs-lookup"><span data-stu-id="9ed14-136">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="9ed14-137">Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="9ed14-137">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="9ed14-138">Macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9ed14-138">Virtual Machine</span></span>
  - <span data-ttu-id="9ed14-139">Servizio app (siti Web)</span><span class="sxs-lookup"><span data-stu-id="9ed14-139">App Service (Websites)</span></span>
  - <span data-ttu-id="9ed14-140">Database SQL</span><span class="sxs-lookup"><span data-stu-id="9ed14-140">SQL Database</span></span>
  - <span data-ttu-id="9ed14-141">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="9ed14-141">Storage</span></span>
  - <span data-ttu-id="9ed14-142">Rete</span><span class="sxs-lookup"><span data-stu-id="9ed14-142">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="9ed14-143">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="9ed14-143">Next Steps</span></span>

<span data-ttu-id="9ed14-144">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9ed14-144">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
