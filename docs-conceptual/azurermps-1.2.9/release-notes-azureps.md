---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819712"
---
# <a name="release-notes"></a><span data-ttu-id="76e45-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="76e45-103">Release notes</span></span>

<span data-ttu-id="76e45-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="76e45-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="76e45-105">Versione 1.2.9</span><span class="sxs-lookup"><span data-stu-id="76e45-105">Version 1.2.9</span></span>

<span data-ttu-id="76e45-106">Modifiche di questa versione</span><span class="sxs-lookup"><span data-stu-id="76e45-106">Changes This Release</span></span>

* <span data-ttu-id="76e45-107">Modulo AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="76e45-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="76e45-108">Modifiche apportate al cmdlet Add-AzureRmResourceProviderRegistration per il supporto della divisione tra Azure Resource Manager per amministratori e Azure Resource Manager per tenant.</span><span class="sxs-lookup"><span data-stu-id="76e45-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="76e45-109">Aggiunta del nuovo parametro -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="76e45-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="76e45-110">Rimozione dei parametri -AdminUri, -ApiVersion, -SubscriptionId e -Token da ogni cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76e45-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="76e45-111">Dopo aver emesso avvisi relativi al fatto che questi parametri sarebbero stati deprecati, i parametri sono ora stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="76e45-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="76e45-112">Modulo AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="76e45-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="76e45-113">Aggiunta di nuovi cmdlet per supportare scenari di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="76e45-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="76e45-114">Rimozione dei cmdlet correlati a componenti interni e funzionalità sottostanti.</span><span class="sxs-lookup"><span data-stu-id="76e45-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="76e45-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="76e45-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="76e45-116">Creazione del nuovo modulo per gestire le versioni dei cmdlet di Azure PowerShell tramite l'uso dei profili di versione</span><span class="sxs-lookup"><span data-stu-id="76e45-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>