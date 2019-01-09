---
title: Panoramica di Azure PowerShell
description: Panoramica del modulo Az di Azure PowerShell con informazioni su come installare e iniziare a usare il modulo.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 10/29/2018
ms.openlocfilehash: 7982e122d49db4d558648231d1ab8bfeed80be2d
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736461"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="f0734-103">Panoramica di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="f0734-104">Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0734-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="f0734-105">Azure PowerShell usa .NET Standard, rendendolo disponibile per Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="f0734-105">Azure PowerShell uses .NET Standard, making it available for Windows, macOS, and Linux.</span></span>
<span data-ttu-id="f0734-106">Azure PowerShell è disponibile anche da Azure Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="f0734-106">Azure PowerShell is also available from Azure Cloud Shell.</span></span>

<span data-ttu-id="f0734-107">Usare [Azure Cloud Shell](/azure/cloud-shell/overview) per eseguire Azure PowerShell nel browser o [installarlo in locale](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-107">Use [Azure Cloud Shell](/azure/cloud-shell/overview) to run Azure PowerShell in your browser, or [install locally](install-az-ps.md).</span></span> <span data-ttu-id="f0734-108">Per apprendere le nozioni di base di Azure PowerShell e iniziare a usare Azure, vedere l'articolo [Introduzione](get-started-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-108">Check out the [Get Started](get-started-azureps.md) article to learn the Azure PowerShell basics and get started with Azure.</span></span>

<span data-ttu-id="f0734-109">Per informazioni sulla versione più recente di Azure PowerShell, vedere le [note sulla versione](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-109">For information about the latest Azure PowerShell release, see the [release notes](release-notes-azureps.md).</span></span>

## <a name="about-the-new-az-module"></a><span data-ttu-id="f0734-110">Informazioni sul nuovo modulo Az</span><span class="sxs-lookup"><span data-stu-id="f0734-110">About the new Az module</span></span>

<span data-ttu-id="f0734-111">Questa documentazione descrive il nuovo modulo Az per Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0734-111">This documentation describes the new Az module for Azure PowerShell.</span></span> <span data-ttu-id="f0734-112">Questo nuovo modulo è scritto da zero in .NET Standard.</span><span class="sxs-lookup"><span data-stu-id="f0734-112">This new module is written from the ground up in .NET Standard.</span></span> <span data-ttu-id="f0734-113">L'uso di .NET Standard consente di eseguire Azure PowerShell in PowerShell 5.x in Windows o PowerShell 6 in qualsiasi piattaforma.</span><span class="sxs-lookup"><span data-stu-id="f0734-113">Using .NET Standard allows Azure PowerShell to run under PowerShell 5.x on Windows or PowerShell 6 on any platform.</span></span> <span data-ttu-id="f0734-114">Il modulo Az è ora la modalità desiderata per interagire con Azure tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0734-114">The Az module is now the intended way to interact with Azure through PowerShell.</span></span>
<span data-ttu-id="f0734-115">AzureRM continuerà a ottenere le correzioni di bug, ma non riceverà più le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="f0734-115">AzureRM will continue to get bug fixes, but no longer receive new features.</span></span>

<span data-ttu-id="f0734-116">Per tutti i dettagli sul nuovo modulo, compreso il modo in cui sono stati rinominati i comandi e i piani di manutenzione per AzureRM, vedere [Introduzione del modulo Az di Azure PowerShell](new-azureps-module-az.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-116">Learn the full details about the new module, including how commands have been renamed and the maintenance plans for AzureRM, in the [Introducing the Azure PowerShell Az module](new-azureps-module-az.md).</span></span> <span data-ttu-id="f0734-117">Se si vuole iniziare a usare immediatamente il nuovo modulo, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-117">If you want to get started with using the new module right away, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

<span data-ttu-id="f0734-118">È anche disponibile la [documentazione di AzureRM](/powershell/azure/azurerm).</span><span class="sxs-lookup"><span data-stu-id="f0734-118">The [AzureRM documentation](/powershell/azure/azurerm) is also available.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="f0734-119">Mentre la documentazione di Azure è in fase di aggiornamento per riflettere i nuovi nomi dei cmdlet del modulo, gli articoli possono ancora usare i comandi di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="f0734-119">While the Azure documentation is being updated to reflect the new module cmdlet names, articles may still use the AzureRM commands.</span></span> <span data-ttu-id="f0734-120">Dopo aver installato il modulo Az, è consigliabile abilitare gli alias dei cmdlet di AzureRM con `Enable-AzureRmAlias`.</span><span class="sxs-lookup"><span data-stu-id="f0734-120">After installing the Az module, it's recommended that you enable the AzureRM cmdlet aliases with `Enable-AzureRmAlias`.</span></span> <span data-ttu-id="f0734-121">Per altri dettagli, vedere l'articolo [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="f0734-121">See the [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md) article for more details.</span></span>

## <a name="common-scenarios"></a><span data-ttu-id="f0734-122">Scenari comuni</span><span class="sxs-lookup"><span data-stu-id="f0734-122">Common scenarios</span></span>

<span data-ttu-id="f0734-123">Gli esempi seguenti aiutano a eseguire scenari comuni con Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f0734-123">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="f0734-124">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="f0734-124">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f0734-125">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="f0734-125">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f0734-126">App Web</span><span class="sxs-lookup"><span data-stu-id="f0734-126">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="f0734-127">Database SQL</span><span class="sxs-lookup"><span data-stu-id="f0734-127">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="f0734-128">Nozioni di base di PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-128">Learn PowerShell basics</span></span>

<span data-ttu-id="f0734-129">Se non si ha familiarità con PowerShell, potrebbe essere utile un'introduzione a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f0734-129">If you're unfamiliar with PowerShell, an introduction may be helpful.</span></span>

* [<span data-ttu-id="f0734-130">Installazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-130">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="f0734-131">Creazione di script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-131">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="f0734-132">È anche possibile guardare questo video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="f0734-132">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="f0734-133">Oppure partecipare al corso [Introduzione a PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) di Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="f0734-133">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="f0734-134">Sviluppare le proprie competenze con Microsoft Learn</span><span class="sxs-lookup"><span data-stu-id="f0734-134">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="f0734-135">Automatizzare le attività di Azure usando gli script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-135">Automate Azure tasks using scripts with PowerShell</span></span>](/learn/modules/automate-azure-tasks-with-powershell/)
- [<span data-ttu-id="f0734-136">Altre risorse di apprendimento interattivo</span><span class="sxs-lookup"><span data-stu-id="f0734-136">More interactive learning...</span></span>](/learn/browse/?term=powershell)

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="f0734-137">Altri moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="f0734-137">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="f0734-138">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="f0734-138">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="f0734-139">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="f0734-139">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="f0734-140">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="f0734-140">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="f0734-141">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="f0734-141">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
