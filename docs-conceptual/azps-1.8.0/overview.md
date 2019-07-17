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
ms.openlocfilehash: 1978ba5415a27349ac68175144cca0d89fa26d96
ms.sourcegitcommit: 0b644bfecf4224b2ea83520d1a6a956734d9fba4
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/12/2019
ms.locfileid: "67863882"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="9240d-103">Panoramica di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="9240d-104">Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="9240d-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="9240d-105">Azure PowerShell usa .NET Standard, rendendolo disponibile per Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="9240d-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="9240d-106">Azure PowerShell è disponibile anche in Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9240d-106">Azure PowerShell is also available on Azure Cloud Shell.</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="9240d-107">Informazioni sul nuovo modulo Az</span><span class="sxs-lookup"><span data-stu-id="9240d-107">About the new Az module</span></span>

<span data-ttu-id="9240d-108">Questa documentazione descrive il nuovo modulo Az per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9240d-108">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="9240d-109">Questo nuovo modulo è scritto da zero in .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="9240d-109">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="9240d-110">L'uso di .NET Standard consente di eseguire Azure PowerShell in PowerShell 5.1 in Windows oppure PowerShell Core 6.x e versioni successive in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="9240d-110">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.1 on Windows or PowerShell Core 6.x and later on any platform.</span></span> <span data-ttu-id="9240d-111">Il modulo Az è ora la modalità desiderata per interagire con Azure tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9240d-111">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="9240d-112">AzureRM continuerà a ottenere le correzioni di bug, ma non riceverà più le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="9240d-112">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="9240d-113">Per tutti i dettagli sul nuovo modulo, compreso il modo in cui sono stati rinominati i comandi e i piani di manutenzione per AzureRM, vedere [Introduzione del modulo Az di Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-113">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="9240d-114">Se si vuole iniziare a usare immediatamente il nuovo modulo, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-114">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="9240d-115">È anche disponibile la [documentazione di AzureRM](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="9240d-115">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="9240d-116">Mentre la documentazione di Azure è in fase di aggiornamento per riflettere i nuovi nomi dei cmdlet del modulo, gli articoli possono ancora usare i comandi di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="9240d-116">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="9240d-117">Dopo aver installato il modulo Az, è consigliabile abilitare gli alias dei cmdlet di AzureRM con `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="9240d-117">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="9240d-118">Per altri dettagli, vedere l'articolo [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-118">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="run-or-install"></a><span data-ttu-id="9240d-119">Esecuzione o installazione</span><span class="sxs-lookup"><span data-stu-id="9240d-119">Run or install</span></span>

<span data-ttu-id="9240d-120">È possibile installare Azure PowerShell in PowerShell 5.1 o versione successiva in Windows, PowerShell Core 6.x e versioni successive in qualsiasi piattaforma oppure eseguirlo in Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9240d-120">You can install Azure PowerShell on PowerShell 5.1 or higher on Windows, PowerShell Core 6.x and later on any platform, or run in Azure Cloud Shell.</span></span>

* <span data-ttu-id="9240d-121">Per l'esecuzione nel browser con Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span><span class="sxs-lookup"><span data-stu-id="9240d-121">To run in your browser with Azure Cloud Shell, see [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="9240d-122">Per l'installazione di Azure PowerShell nel sistema, vedere [Installare Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-122">To install Azure PowerShell on your system, see [Install Azure PowerShell](install-az-ps.md).</span></span>

<span data-ttu-id="9240d-123">Per informazioni sulla versione più recente di Azure PowerShell, vedere le [note sulla versione](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-123">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="get-started"></a><span data-ttu-id="9240d-124">Attività iniziali</span><span class="sxs-lookup"><span data-stu-id="9240d-124">Get Started</span></span>

<span data-ttu-id="9240d-125">Per apprendere le nozioni di base di Azure PowerShell, vedere l'articolo [Guida introduttiva ad Azure PowerShell](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="9240d-125">Read the [Get Started with Azure PowerShell](get-started-azureps.md) article to learn the Azure PowerShell basics.</span></span> <span data-ttu-id="9240d-126">Se non si ha familiarità con PowerShell, potrebbe essere utile un'introduzione a PowerShell:</span><span class="sxs-lookup"><span data-stu-id="9240d-126">If you're not familiar with PowerShell, an introduction might be helpful:</span></span>

* [<span data-ttu-id="9240d-127">Installare PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-127">Install PowerShell</span></span>](/powershell/scripting/install/installing-powershell)
* [<span data-ttu-id="9240d-128">Creazione di script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-128">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)
* [<span data-ttu-id="9240d-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-129">PowerShell Basics: (Part 1) Getting Started with PowerShell</span></span>](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1)

<span data-ttu-id="9240d-130">Gli esempi seguenti possono essere utili per alcuni usi comuni di Azure:</span><span class="sxs-lookup"><span data-stu-id="9240d-130">The following samples can help you with some common uses of Azure:</span></span>

* [<span data-ttu-id="9240d-131">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="9240d-131">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9240d-132">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="9240d-132">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9240d-133">App Web</span><span class="sxs-lookup"><span data-stu-id="9240d-133">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="9240d-134">Database SQL</span><span class="sxs-lookup"><span data-stu-id="9240d-134">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="9240d-135">Sviluppare le proprie competenze con Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="9240d-135">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="9240d-136">Automatizzare le attività di Azure usando gli script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-136">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="9240d-137">Altre risorse di apprendimento interattivo</span><span class="sxs-lookup"><span data-stu-id="9240d-137">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="9240d-138">Altri moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="9240d-138">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="9240d-139">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="9240d-139">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="9240d-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9240d-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="9240d-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="9240d-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
