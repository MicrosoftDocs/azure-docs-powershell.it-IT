---
title: Panoramica di Azure PowerShell | Microsoft Docs
description: Panoramica di Azure PowerShell con collegamenti a installazione e configurazione.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 08/31/2017
ms.openlocfilehash: e5c344ca59de37eeb59bba538e7437d4a0c26ed7
ms.sourcegitcommit: 4acddc7026522c4fe39de2c4424917d88ee01b7e
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/21/2018
ms.locfileid: "53736410"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="d2ca1-103">Panoramica di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2ca1-103">Overview of Azure PowerShell</span></span>

[!INCLUDE[az-replacing-azurerm.md](../includes/az-replacing-azurerm.md)]

<span data-ttu-id="d2ca1-104">Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="d2ca1-105">È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale e usarlo in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="d2ca1-106">Usare [Cloud Shell](/azure/cloud-shell/overview) per eseguire Azure PowerShell nel browser o [installarlo](install-azurerm-ps.md) nel computer.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="d2ca1-107">Leggere quindi l'articolo [Get Started](get-started-azureps.md) (Introduzione) per iniziare a usarlo.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="d2ca1-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="d2ca1-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="d2ca1-109">Gli esempi seguenti aiutano a eseguire scenari comuni con Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="d2ca1-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="d2ca1-110">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="d2ca1-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d2ca1-111">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="d2ca1-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d2ca1-112">App Web</span><span class="sxs-lookup"><span data-stu-id="d2ca1-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="d2ca1-113">Database SQL</span><span class="sxs-lookup"><span data-stu-id="d2ca1-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

## <a name="learn-powershell-basics"></a><span data-ttu-id="d2ca1-114">Nozioni di base di PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2ca1-114">Learn PowerShell basics</span></span>

<span data-ttu-id="d2ca1-115">Se non si ha familiarità con PowerShell, un'introduzione a PowerShell può risultare utile.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-115">If you are unfamiliar with PowerShell, you may find an introduction to PowerShell helpful.</span></span>

* [<span data-ttu-id="d2ca1-116">Installazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2ca1-116">Installing PowerShell</span></span>](/powershell/scripting/installing-windows-powershell)
* [<span data-ttu-id="d2ca1-117">Creazione di script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2ca1-117">Scripting with PowerShell</span></span>](/powershell/scripting/scripting-with-windows-powershell)

<span data-ttu-id="d2ca1-118">È anche possibile guardare questo video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span><span class="sxs-lookup"><span data-stu-id="d2ca1-118">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="d2ca1-119">Oppure partecipare al corso [Introduzione a PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) di Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="d2ca1-119">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="d2ca1-120">Altri moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="d2ca1-120">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="d2ca1-121">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d2ca1-121">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="d2ca1-122">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="d2ca1-122">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="d2ca1-123">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d2ca1-123">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="d2ca1-124">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="d2ca1-124">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
