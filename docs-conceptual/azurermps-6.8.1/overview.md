---
title: Panoramica di Azure PowerShell | Microsoft Docs
description: Panoramica di Azure PowerShell con collegamenti a installazione e configurazione.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.manager: carmonm
ms.date: 09/11/2018
ms.openlocfilehash: fcb6213dab12f94796ab0ca9de4d5e391d570f4f
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/20/2018
ms.locfileid: "46304132"
---
# <a name="overview-of-azure-powershell"></a><span data-ttu-id="06c1d-103">Panoramica di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06c1d-103">Overview of Azure PowerShell</span></span>

<span data-ttu-id="06c1d-104">Azure PowerShell offre un set di cmdlet che usano il modello [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) per la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="06c1d-104">Azure PowerShell provides a set of cmdlets that use the [Azure Resource Manager](/azure/azure-resource-manager/resource-group-overview) model for managing your Azure resources.</span></span> <span data-ttu-id="06c1d-105">È possibile usarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale e usarlo in una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06c1d-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can install it on your local machine and use it in any PowerShell session.</span></span>

<span data-ttu-id="06c1d-106">Usare [Cloud Shell](/azure/cloud-shell/overview) per eseguire Azure PowerShell nel browser o [installarlo](install-azurerm-ps.md) nel computer.</span><span class="sxs-lookup"><span data-stu-id="06c1d-106">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the Azure PowerShell in your browser, or [install](install-azurerm-ps.md) it on own computer.</span></span> <span data-ttu-id="06c1d-107">Leggere quindi l'articolo [Get Started](get-started-azureps.md) (Introduzione) per iniziare a usarlo.</span><span class="sxs-lookup"><span data-stu-id="06c1d-107">Then read the [Get Started](get-started-azureps.md) article to begin using it.</span></span> <span data-ttu-id="06c1d-108">Per informazioni sulla versione più recente, vedere le [note sulla versione](release-notes-azureps.md).</span><span class="sxs-lookup"><span data-stu-id="06c1d-108">For information about the latest release, see the [release notes](release-notes-azureps.md).</span></span>

<span data-ttu-id="06c1d-109">Gli esempi seguenti aiutano a eseguire scenari comuni con Azure PowerShell:</span><span class="sxs-lookup"><span data-stu-id="06c1d-109">The following samples can help you learn how to perform common scenarios with Azure PowerShell:</span></span>

* [<span data-ttu-id="06c1d-110">Macchine virtuali Linux</span><span class="sxs-lookup"><span data-stu-id="06c1d-110">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="06c1d-111">Macchine virtuali Windows</span><span class="sxs-lookup"><span data-stu-id="06c1d-111">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="06c1d-112">App Web</span><span class="sxs-lookup"><span data-stu-id="06c1d-112">Web Apps</span></span>](/azure/app-service-web/app-service-powershell-samples?toc=/powershell/azure/toc.json)
* [<span data-ttu-id="06c1d-113">Database SQL</span><span class="sxs-lookup"><span data-stu-id="06c1d-113">SQL Databases</span></span>](/azure/sql-database/sql-database-powershell-samples?toc=/powershell/azure/toc.json)

> [!NOTE]
> <span data-ttu-id="06c1d-114">In presenza di distribuzioni che usano il modello di distribuzione classico non convertibile, è possibile installare la versione di Gestione dei servizi di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06c1d-114">If you have deployments that use the classic deployment model that cannot be converted, you can install the Service Management version of Azure PowerShell.</span></span> <span data-ttu-id="06c1d-115">Per altre informazioni, vedere [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps) (Installare il modulo Gestione dei servizi di Azure PowerShell).</span><span class="sxs-lookup"><span data-stu-id="06c1d-115">For more information, see [Install the Azure PowerShell Service Management module](/powershell/azure/servicemanagement/install-azure-ps).</span></span>

## <a name="learn-powershell-basics"></a><span data-ttu-id="06c1d-116">Nozioni di base di PowerShell</span><span class="sxs-lookup"><span data-stu-id="06c1d-116">Learn PowerShell basics</span></span>

<span data-ttu-id="06c1d-117">Se non si ha familiarità con PowerShell, potrebbe essere utile un'introduzione a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="06c1d-117">If you're unfamiliar with PowerShell, an introduction to PowerShell may be helpful.</span></span>

* [<span data-ttu-id="06c1d-118">Installazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="06c1d-118">Installing PowerShell</span></span>](/powershell/scripting/setup/installing-windows-powershell)
* [<span data-ttu-id="06c1d-119">Creazione di script con PowerShell</span><span class="sxs-lookup"><span data-stu-id="06c1d-119">Scripting with PowerShell</span></span>](/powershell/scripting/powershell-scripting)

<span data-ttu-id="06c1d-120">È inoltre possibile guardare questo video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1) (Nozioni di base su PowerShell: Introduzione a PowerShell, parte 1).</span><span class="sxs-lookup"><span data-stu-id="06c1d-120">You can also watch this video: [PowerShell Basics: (Part 1) Getting Started with PowerShell](https://channel9.msdn.com/Blogs/Taste-of-Premier/PowerShellBasicsPart1).</span></span>

<span data-ttu-id="06c1d-121">Oppure partecipare al corso [Introduzione a PowerShell](https://mva.microsoft.com/liveevents/powershell-jumpstart) di Microsoft Virtual Academy.</span><span class="sxs-lookup"><span data-stu-id="06c1d-121">Or attend the Microsoft Virtual Academy's [Getting Started with PowerShell Jumpstart](https://mva.microsoft.com/liveevents/powershell-jumpstart).</span></span>

## <a name="other-azure-powershell-modules"></a><span data-ttu-id="06c1d-122">Altri moduli di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="06c1d-122">Other Azure PowerShell modules</span></span>

* [<span data-ttu-id="06c1d-123">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="06c1d-123">Azure Active Directory</span></span>](/powershell/azure/active-directory/)
* [<span data-ttu-id="06c1d-124">Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="06c1d-124">Azure Information Protection</span></span>](/powershell/azure/aip/)
* [<span data-ttu-id="06c1d-125">Azure Service Fabric</span><span class="sxs-lookup"><span data-stu-id="06c1d-125">Azure Service Fabric</span></span>](/powershell/azure/service-fabric/)
* [<span data-ttu-id="06c1d-126">Azure ElasticDB</span><span class="sxs-lookup"><span data-stu-id="06c1d-126">Azure ElasticDB</span></span>](/powershell/azure/elasticdbjobs/)
