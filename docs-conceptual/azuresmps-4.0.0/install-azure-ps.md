---
title: Installare e configurare il modulo Gestione dei servizi di Azure PowerShell | Documenti di Microsoft
description: Come installare e configurare Azure PowerShell per il primo uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: a4911e72f687c07b31805c07fd23263a6b7f33b4
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718798"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="957c6-103">Installare il modulo Gestione dei servizi di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="957c6-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="957c6-104">L'installazione di Azure PowerShell da [PowerShell Gallery](https://www.powershellgallery.com/) è il metodo preferito di installazione.</span><span class="sxs-lookup"><span data-stu-id="957c6-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="957c6-105">Passaggio 1: Installare PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="957c6-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="957c6-106">L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="957c6-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="957c6-107">Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="957c6-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="957c6-108">Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="957c6-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="957c6-109">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="957c6-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="957c6-110">Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="957c6-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="957c6-111">Passaggio 2: Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="957c6-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="957c6-112">Eseguire il comando seguente dalla console di Windows PowerShell come amministratore:</span><span class="sxs-lookup"><span data-stu-id="957c6-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="957c6-113">Il modulo Azure è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="957c6-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="957c6-114">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure non installato precedentemente viene scaricato e installato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="957c6-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="957c6-115">Il modulo di Gestione dei servizi di Azure condivide le dipendenze con i moduli di Gestione risorse di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="957c6-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="957c6-116">Se sono stati installati i moduli di Gestione risorse di Azure PowerShell, sarà necessario aggiungere il parametro `-AllowClobber` al comando di installazione.</span><span class="sxs-lookup"><span data-stu-id="957c6-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="957c6-117">In questo modo le dipendenze condivise esistenti verranno aggiornate.</span><span class="sxs-lookup"><span data-stu-id="957c6-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="957c6-118">Senza questo parametro, si verifica un errore di installazione del modulo.</span><span class="sxs-lookup"><span data-stu-id="957c6-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="957c6-119">Dopo aver installato il modulo, è possibile importarlo eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="957c6-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="957c6-120">Usare i cmdlet</span><span class="sxs-lookup"><span data-stu-id="957c6-120">To use the cmdlets</span></span>

<span data-ttu-id="957c6-121">Per iniziare a lavorare con i cmdlet di Gestione dei servizi di Azure, accedere al proprio account Azure.</span><span class="sxs-lookup"><span data-stu-id="957c6-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="957c6-122">Per accedere al proprio account, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="957c6-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="957c6-123">Dopo l'accesso ad Azure, Azure PowerShell crea un contesto per la sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="957c6-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="957c6-124">Tale contesto contiene l'ambiente Azure PowerShell, l'account, il tenant e la sottoscrizione che verranno usati per tutti i cmdlet della sessione.</span><span class="sxs-lookup"><span data-stu-id="957c6-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="957c6-125">È ora possibile usare i moduli seguenti.</span><span class="sxs-lookup"><span data-stu-id="957c6-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="957c6-126">Cmdlet di Gestione dei servizi di Azure</span><span class="sxs-lookup"><span data-stu-id="957c6-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="957c6-127">I moduli di Azure PowerShell vengono aggiornati di frequente.</span><span class="sxs-lookup"><span data-stu-id="957c6-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="957c6-128">Se si nota che la guida dei cmdlet online include cmdlet o parametri non presenti nel modulo, scaricare e installare la versione più recente del modulo.</span><span class="sxs-lookup"><span data-stu-id="957c6-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="957c6-129">Per conoscere la versione del modulo, digitare: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="957c6-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="957c6-130">Per gli script di esempio che consentono di automatizzare alcune delle attività comuni in Azure, vedere lo [Script Center di Windows Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="957c6-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="957c6-131">Per informazioni generali sull'installazione, la formazione, l'uso e la personalizzazione di Windows PowerShell, vedere [Scripting con Windows PowerShell](https://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="957c6-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](https://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="957c6-132">Come ottenere PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="957c6-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="957c6-133">Versione sistema operativo</span><span class="sxs-lookup"><span data-stu-id="957c6-133">OS Version</span></span>|<span data-ttu-id="957c6-134">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="957c6-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="957c6-135">Il sistema operativo è Windows 10 o Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="957c6-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="957c6-136">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="957c6-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="957c6-137">Si vuole eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="957c6-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="957c6-138">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="957c6-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|
|<span data-ttu-id="957c6-139">È in esecuzione una versione di Windows con PowerShell 3 o 4</span><span class="sxs-lookup"><span data-stu-id="957c6-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="957c6-140">Ottenere i moduli PackageManagement</span><span class="sxs-lookup"><span data-stu-id="957c6-140">Get the PackageManagement modules</span></span>](https://go.microsoft.com/fwlink/?LinkID=746217)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="957c6-141">Controllo della versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="957c6-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="957c6-142">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono di supporto.</span><span class="sxs-lookup"><span data-stu-id="957c6-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="957c6-143">Per determinare la versione di Azure PowerShell installata, eseguire `Get-InstalledModule Azure` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="957c6-143">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
