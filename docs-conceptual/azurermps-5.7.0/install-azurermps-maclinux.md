---
title: Installare Azure PowerShell in macOS o Linux
description: Come installare Azure PowerShell in macOS o Linux.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 06/06/2018
ms.openlocfilehash: 17912c155255b6fdfd3cfb9242163b67d405dc03
ms.sourcegitcommit: bcf80dfd7fbe17e82e7ad029802cfe8a2f02b15c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2018
ms.locfileid: "35323255"
---
# <a name="install-azure-powershell-on-macos-or-linux"></a><span data-ttu-id="532ff-103">Installare Azure PowerShell in macOS o Linux</span><span class="sxs-lookup"><span data-stu-id="532ff-103">Install Azure PowerShell on macOS or Linux</span></span>

<span data-ttu-id="532ff-104">Per le piattaforme non Windows, è possibile eseguire Azure PowerShell con PowerShell Core v6.</span><span class="sxs-lookup"><span data-stu-id="532ff-104">For non-Windows platforms, it's possible to run Azure PowerShell on top of PowerShell Core v6.</span></span> <span data-ttu-id="532ff-105">Invece della versione standard di Azure PowerShell basata su .NET Framework per Windows, questo prodotto è pensato per .NET Core e può essere eseguito in qualsiasi piattaforma che supporti il runtime .Net Core.</span><span class="sxs-lookup"><span data-stu-id="532ff-105">Rather than the standard Azure PowerShell built on .NET Framework for Windows, this product is built for .NET Core and can run on any platform which supports the .Net Core runtime.</span></span>

> [!NOTE]
> <span data-ttu-id="532ff-106">Attualmente, sia PowerShell Core v6 che Azure PowerShell per .NET Core sono ancora in versione beta.</span><span class="sxs-lookup"><span data-stu-id="532ff-106">At this time, both PowerShell Core v6 and Azure PowerShell for .NET Core are still in beta.</span></span>
> <span data-ttu-id="532ff-107">Il supporto per questi prodotti è limitato.</span><span class="sxs-lookup"><span data-stu-id="532ff-107">Support for these products is limited.</span></span> <span data-ttu-id="532ff-108">Se si verificano problemi o si trovano bug, registrare un problema in GitHub.</span><span class="sxs-lookup"><span data-stu-id="532ff-108">If you have problems or discover bugs, please file an issue on GitHub.</span></span>
>
> * [<span data-ttu-id="532ff-109">Problemi per PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="532ff-109">Issues for PowerShell Core v6</span></span>](https://github.com/PowerShell/PowerShell/issues)
> * [<span data-ttu-id="532ff-110">Problemi per Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="532ff-110">Issues for Azure PowerShell</span></span>](https://github.com/azure/azure-docs-powershell/issues)

## <a name="install-powershell-core-v6"></a><span data-ttu-id="532ff-111">Installare PowerShell Core v6</span><span class="sxs-lookup"><span data-stu-id="532ff-111">Install PowerShell Core v6</span></span>

<span data-ttu-id="532ff-112">L'installazione di PowerShell Core v6 in Linux o macOS varia a seconda della distribuzione Linux e della versione del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="532ff-112">Installing PowerShell Core v6 on Linux or macOS varies depending on the Linux distribution and OS version.</span></span>
<span data-ttu-id="532ff-113">Per istruzioni dettagliate, vedere gli articoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="532ff-113">Detailed instructions can be found in the following articles:</span></span>

- [<span data-ttu-id="532ff-114">Installare PowerShell Core in macOS</span><span class="sxs-lookup"><span data-stu-id="532ff-114">Install PowerShell Core on macOS</span></span>](/powershell/scripting/setup/installing-powershell-core-on-macos)
- [<span data-ttu-id="532ff-115">Installare PowerShell Core in Linux</span><span class="sxs-lookup"><span data-stu-id="532ff-115">Install PowerShell Core on Linux</span></span>](/powershell/scripting/setup/installing-powershell-core-on-linux)

## <a name="install-azure-powershell-for-net-core"></a><span data-ttu-id="532ff-116">Installare Azure PowerShell per .NET Core</span><span class="sxs-lookup"><span data-stu-id="532ff-116">Install Azure PowerShell for .NET Core</span></span>

<span data-ttu-id="532ff-117">PowerShell Core v6 viene fornito con il modulo PowerShellGet già installato.</span><span class="sxs-lookup"><span data-stu-id="532ff-117">PowerShell Core v6 comes with the PowerShellGet module already installed.</span></span> <span data-ttu-id="532ff-118">Ciò semplifica l'installazione di qualsiasi modulo pubblicato in PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="532ff-118">This makes it easy to install any module that is published to the PowerShell Gallery.</span></span> <span data-ttu-id="532ff-119">Per installare Azure PowerShell, aprire una nuova sessione di PowerShell ed eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="532ff-119">To install Azure PowerShell, open a new PowerShell session and run the following command:</span></span>

```powershell
Install-Module AzureRM.NetCore
```

## <a name="load-the-azurermnetcore-module"></a><span data-ttu-id="532ff-120">Caricare il modulo AzureRM.Netcore</span><span class="sxs-lookup"><span data-stu-id="532ff-120">Load the AzureRM.Netcore module</span></span>

<span data-ttu-id="532ff-121">Dopo aver installato il modulo, è necessario caricarlo nella sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="532ff-121">Once the module is installed, you need to load the module into your PowerShell session.</span></span> <span data-ttu-id="532ff-122">I moduli vengono caricati usando il cmdlet `Import-Module`, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="532ff-122">Modules are loaded using the `Import-Module` cmdlet, as follows:</span></span>

```powershell
Import-Module AzureRM.Netcore
Import-Module AzureRM.Profile.Netcore
```

<span data-ttu-id="532ff-123">Al termine dell'importazione, è possibile testare il modulo appena installato eseguendo un tentativo di accesso ad Azure con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="532ff-123">After the import completes, you can test your newly installed and module by attempting to sign into Azure using the following command:</span></span>

```powershell
Connect-AzureRmAccount
```

<span data-ttu-id="532ff-124">Il comando riportato sopra richiede di passare a `https://aka.ms/devicelogin` e immettere il codice fornito.</span><span class="sxs-lookup"><span data-stu-id="532ff-124">The above command should prompt you to go to `https://aka.ms/devicelogin` and enter the provided code.</span></span>

## <a name="available-cmdlets"></a><span data-ttu-id="532ff-125">Cmdlet disponibili</span><span class="sxs-lookup"><span data-stu-id="532ff-125">Available cmdlets</span></span>

<span data-ttu-id="532ff-126">I moduli di Azure PowerShell per .NET Standard sono ancora in fase di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="532ff-126">The Azure PowerShell modules for .NET Standard are still in development.</span></span> <span data-ttu-id="532ff-127">Questi moduli non offrono il set completo di cmdlet disponibili per la versione Windows dei moduli.</span><span class="sxs-lookup"><span data-stu-id="532ff-127">These modules do not provide the full set of cmdlets that are available for the Windows version of the modules.</span></span> <span data-ttu-id="532ff-128">Le funzioni seguenti sono implementate nei moduli AzureRM.Netcore:</span><span class="sxs-lookup"><span data-stu-id="532ff-128">The following functions are implemented in AzureRM.Netcore modules:</span></span>

* <span data-ttu-id="532ff-129">Gestione account</span><span class="sxs-lookup"><span data-stu-id="532ff-129">Account management</span></span>
  - <span data-ttu-id="532ff-130">Accesso con account Microsoft, account dell'organizzazione o entità servizio tramite Microsoft Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="532ff-130">Login with Microsoft account, Organizational account, or Service Principal through Microsoft Azure Active Directory</span></span>
  - <span data-ttu-id="532ff-131">Salvataggio delle credenziali su disco con Save-AzureRmContext e caricamento delle credenziali salvate con Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="532ff-131">Save Credentials to disk with Save-AzureRmContext and load saved credentials using Import-AzureRmContext</span></span>
* <span data-ttu-id="532ff-132">Environment</span><span class="sxs-lookup"><span data-stu-id="532ff-132">Environment</span></span>
  - <span data-ttu-id="532ff-133">Recupero di ambienti predefiniti di Microsoft Azure diversi</span><span class="sxs-lookup"><span data-stu-id="532ff-133">Get the different out-of-box Microsoft Azure environments</span></span>
  - <span data-ttu-id="532ff-134">Aggiunta/impostazione/rimozione di ambienti personalizzati, come gli ambienti Azure Stack o Windows Azure Pack</span><span class="sxs-lookup"><span data-stu-id="532ff-134">Add/Set/Remove customized environments (like your Azure Stack or Windows Azure Pack environments)</span></span>
* <span data-ttu-id="532ff-135">Cmdlet del piano di gestione per i servizi di Azure tramite le interfacce di Resource Manager e di gestione dei servizi.</span><span class="sxs-lookup"><span data-stu-id="532ff-135">Management plane cmdlets for Azure services using Resource Manager and Service Management interfaces.</span></span>
  - <span data-ttu-id="532ff-136">Macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="532ff-136">Virtual Machine</span></span>
  - <span data-ttu-id="532ff-137">Servizio app (siti Web)</span><span class="sxs-lookup"><span data-stu-id="532ff-137">App Service (Websites)</span></span>
  - <span data-ttu-id="532ff-138">Database SQL</span><span class="sxs-lookup"><span data-stu-id="532ff-138">SQL Database</span></span>
  - <span data-ttu-id="532ff-139">Archiviazione</span><span class="sxs-lookup"><span data-stu-id="532ff-139">Storage</span></span>
  - <span data-ttu-id="532ff-140">Rete</span><span class="sxs-lookup"><span data-stu-id="532ff-140">Network</span></span>

## <a name="next-steps"></a><span data-ttu-id="532ff-141">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="532ff-141">Next Steps</span></span>

<span data-ttu-id="532ff-142">Per altre informazioni sull'uso di Azure PowerShell, vedere l'articolo [Introduzione ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="532ff-142">For more information about using Azure PowerShell, see the [Get started with Azure PowerShell](get-started-azureps.md) article.</span></span>
