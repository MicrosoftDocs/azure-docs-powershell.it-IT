---
title: Installare e configurare il modulo Gestione dei servizi di Azure PowerShell | Documenti di Microsoft
description: Come installare e configurare Azure PowerShell per il primo uso.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 23ea4bcbd182cf1b063f2ae90921217de74a7044
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401522"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="42bdf-103">Installare il modulo Gestione dei servizi di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="42bdf-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="42bdf-104">L'installazione di Azure PowerShell da [PowerShell Gallery](https://www.powershellgallery.com/) è il metodo preferito di installazione.</span><span class="sxs-lookup"><span data-stu-id="42bdf-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="42bdf-105">Passaggio 1: installare PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="42bdf-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="42bdf-106">L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="42bdf-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="42bdf-107">Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema.</span><span class="sxs-lookup"><span data-stu-id="42bdf-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="42bdf-108">Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="42bdf-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="42bdf-109">Verrà visualizzata una schermata simile all'output seguente:</span><span class="sxs-lookup"><span data-stu-id="42bdf-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="42bdf-110">Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="42bdf-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="42bdf-111">Passaggio 2: Installare Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="42bdf-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="42bdf-112">Eseguire il comando seguente dalla console di Windows PowerShell come amministratore:</span><span class="sxs-lookup"><span data-stu-id="42bdf-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="42bdf-113">Il modulo Azure è un modulo di rollup per i cmdlet di Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="42bdf-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="42bdf-114">Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure non installato precedentemente viene scaricato e installato da PowerShell Gallery.</span><span class="sxs-lookup"><span data-stu-id="42bdf-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="42bdf-115">Il modulo di Gestione dei servizi di Azure condivide le dipendenze con i moduli di Gestione risorse di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42bdf-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="42bdf-116">Se sono stati installati i moduli di Gestione risorse di Azure PowerShell, sarà necessario aggiungere il parametro `-AllowClobber` al comando di installazione.</span><span class="sxs-lookup"><span data-stu-id="42bdf-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="42bdf-117">In questo modo le dipendenze condivise esistenti verranno aggiornate.</span><span class="sxs-lookup"><span data-stu-id="42bdf-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="42bdf-118">Senza questo parametro, si verifica un errore di installazione del modulo.</span><span class="sxs-lookup"><span data-stu-id="42bdf-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="42bdf-119">Dopo aver installato il modulo, è possibile importarlo eseguendo il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="42bdf-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="42bdf-120">Usare i cmdlet</span><span class="sxs-lookup"><span data-stu-id="42bdf-120">To use the cmdlets</span></span>

<span data-ttu-id="42bdf-121">Per iniziare a lavorare con i cmdlet di Gestione dei servizi di Azure, accedere al proprio account Azure.</span><span class="sxs-lookup"><span data-stu-id="42bdf-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="42bdf-122">Per accedere al proprio account, eseguire il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="42bdf-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="42bdf-123">Dopo l'accesso ad Azure, Azure PowerShell crea un contesto per la sessione specificata.</span><span class="sxs-lookup"><span data-stu-id="42bdf-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="42bdf-124">Tale contesto contiene l'ambiente Azure PowerShell, l'account, il tenant e la sottoscrizione che verranno usati per tutti i cmdlet della sessione.</span><span class="sxs-lookup"><span data-stu-id="42bdf-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="42bdf-125">È ora possibile usare i moduli seguenti.</span><span class="sxs-lookup"><span data-stu-id="42bdf-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="42bdf-126">Cmdlet di Gestione dei servizi di Azure</span><span class="sxs-lookup"><span data-stu-id="42bdf-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="42bdf-127">I moduli di Azure PowerShell vengono aggiornati di frequente.</span><span class="sxs-lookup"><span data-stu-id="42bdf-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="42bdf-128">Se si nota che la guida dei cmdlet online include cmdlet o parametri non presenti nel modulo, scaricare e installare la versione più recente del modulo.</span><span class="sxs-lookup"><span data-stu-id="42bdf-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="42bdf-129">Per conoscere la versione del modulo, digitare: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="42bdf-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="42bdf-130">Per gli script di esempio che consentono di automatizzare alcune delle attività comuni in Azure, vedere lo [Script Center di Windows Azure](https://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="42bdf-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](https://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="42bdf-131">Per informazioni generali sull'installazione, la formazione, l'uso e la personalizzazione di Windows PowerShell, vedere [Scripting con Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span><span class="sxs-lookup"><span data-stu-id="42bdf-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="42bdf-132">Come ottenere PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="42bdf-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="42bdf-133">Versione sistema operativo</span><span class="sxs-lookup"><span data-stu-id="42bdf-133">OS Version</span></span>|<span data-ttu-id="42bdf-134">Istruzioni di installazione</span><span class="sxs-lookup"><span data-stu-id="42bdf-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="42bdf-135">Il sistema operativo è Windows 10 o Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="42bdf-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="42bdf-136">Integrato in Windows Management Framework (WMF) 5.0 incluso nel sistema operativo</span><span class="sxs-lookup"><span data-stu-id="42bdf-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="42bdf-137">Si vuole eseguire l'aggiornamento a PowerShell 5</span><span class="sxs-lookup"><span data-stu-id="42bdf-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="42bdf-138">Installare la versione più recente di WMF</span><span class="sxs-lookup"><span data-stu-id="42bdf-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="42bdf-139">Controllo della versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="42bdf-139">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="42bdf-140">Anche se si consiglia di eseguire l'aggiornamento alla versione più recente il prima possibile, alcune versioni di Azure PowerShell sono di supporto.</span><span class="sxs-lookup"><span data-stu-id="42bdf-140">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="42bdf-141">Per determinare la versione di Azure PowerShell installata, eseguire `Get-InstalledModule Azure` dalla riga di comando.</span><span class="sxs-lookup"><span data-stu-id="42bdf-141">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
