---
title: Panoramica di Azure PowerShell
description: Panoramica del modulo Az di Azure PowerShell con informazioni su come installare e iniziare a usare il modulo.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 01/10/2019
ms.openlocfilehash: 45ab083dd133c8c7b8dbe902484c92564bc216b9
ms.sourcegitcommit: 89066b7c4b527357bb2024e1ad708df84c131804
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/09/2019
ms.locfileid: "59364163"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="1be8e-103">Panoramica di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="1be8e-104">Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="1be8e-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="1be8e-105">Azure PowerShell usa .NET Standard, rendendolo disponibile per Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="1be8e-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="1be8e-106">Azure PowerShell è disponibile anche in Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="1be8e-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="1be8e-107">Informazioni sul nuovo modulo Az</span><span class="sxs-lookup"><span data-stu-id="1be8e-107">About the new Az module</span></span>

<span data-ttu-id="1be8e-108">Questa documentazione descrive il nuovo modulo Az per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1be8e-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="1be8e-109">Questo nuovo modulo è scritto da zero in .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="1be8e-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="1be8e-110">L'uso di .NET Standard consente di eseguire Azure PowerShell in PowerShell 5 con Windows oppure PowerShell 6 in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="1be8e-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5 on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="1be8e-111">Il modulo Az è ora la modalità desiderata per interagire con Azure tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1be8e-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="1be8e-112">AzureRM continuerà a ottenere le correzioni di bug, ma non riceverà più le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1be8e-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="1be8e-113">Per tutti i dettagli sul nuovo modulo, compreso il modo in cui sono stati rinominati i comandi e i piani di manutenzione per AzureRM, vedere [Introduzione del modulo Az di Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="1be8e-114">Se si vuole iniziare a usare immediatamente il nuovo modulo, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="1be8e-115">È anche disponibile la [documentazione di AzureRM](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="1be8e-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="1be8e-116">Mentre la documentazione di Azure è in fase di aggiornamento per riflettere i nuovi nomi dei cmdlet del modulo, gli articoli possono ancora usare i comandi di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="1be8e-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="1be8e-117">Dopo aver installato il modulo Az, è consigliabile abilitare gli alias dei cmdlet di AzureRM con `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="1be8e-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="1be8e-118">Per altri dettagli, vedere l'articolo [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="1be8e-119">Esecuzione o installazione</span><span class="sxs-lookup"><span data-stu-id="1be8e-119">Run or install</span></span>

<span data-ttu-id="1be8e-120">È possibile installare Azure PowerShell in PowerShell 5.1 o versione successiva con Windows, PowerShell 6 in qualsiasi piattaforma oppure eseguirlo in Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="1be8e-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell 6 on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="1be8e-121">Per l'esecuzione nel browser con Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="1be8e-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="1be8e-122">Per l'installazione di Azure PowerShell nel sistema, vedere [Installare Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="1be8e-123">Per informazioni sulla versione più recente di Azure PowerShell, vedere le [note sulla versione](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="1be8e-124">Attività iniziali</span><span class="sxs-lookup"><span data-stu-id="1be8e-124">Get Started</span></span>

<span data-ttu-id="1be8e-125">Per apprendere le nozioni di base di Azure PowerShell, vedere l'articolo [Guida introduttiva ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="1be8e-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="1be8e-126">Se non si ha familiarità con PowerShell, potrebbe essere utile un'introduzione a PowerShell:</span><span class="sxs-lookup"><span data-stu-id="1be8e-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="1be8e-127">Installare PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="1be8e-128">Creazione di script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="1be8e-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)
* <span data-ttu-id="1be8e-130">Corso di [introduzione a PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) di Microsoft Virtual Academy</span><span class="sxs-lookup"><span data-stu-id="1be8e-130">Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart)</span></span>

<span data-ttu-id="1be8e-131">Gli esempi seguenti possono essere utili per alcuni usi comuni di Azure:</span><span class="sxs-lookup"><span data-stu-id="1be8e-131">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="1be8e-132">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="1be8e-132">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1be8e-133">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="1be8e-133">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1be8e-134">App Web</span><span class="sxs-lookup"><span data-stu-id="1be8e-134">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="1be8e-135">DATABASE SQL</span><span class="sxs-lookup"><span data-stu-id="1be8e-135">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="1be8e-136">Sviluppare le proprie competenze con Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="1be8e-136">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="1be8e-137">Automatizzare le attività di Azure usando gli script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-137">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="1be8e-138">Altre risorse di apprendimento interattivo...</span><span class="sxs-lookup"><span data-stu-id="1be8e-138">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="1be8e-139">Altri moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1be8e-139">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="1be8e-140">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="1be8e-140">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="1be8e-141">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="1be8e-141">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="1be8e-142">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="1be8e-142">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
