---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="3f3a5-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="3f3a5-103">Release notes</span></span>

<span data-ttu-id="3f3a5-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="3f3a5-105">Versione 1.2.9</span><span class="sxs-lookup"><span data-stu-id="3f3a5-105">Version 1.2.9</span></span>

<span data-ttu-id="3f3a5-106">Modifiche di questa versione</span><span class="sxs-lookup"><span data-stu-id="3f3a5-106">Changes This Release</span></span>

* <span data-ttu-id="3f3a5-107">Modulo AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="3f3a5-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="3f3a5-108">Modifiche apportate al cmdlet Add-AzureRmResourceProviderRegistration per il supporto della divisione tra Azure Resource Manager per amministratori e Azure Resource Manager per tenant.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="3f3a5-109">Aggiunta del nuovo parametro -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="3f3a5-110">Rimozione dei parametri -AdminUri, -ApiVersion, -SubscriptionId e -Token da ogni cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="3f3a5-111">Dopo aver emesso avvisi relativi al fatto che questi parametri sarebbero stati deprecati, i parametri sono ora stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="3f3a5-112">Modulo AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="3f3a5-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="3f3a5-113">Aggiunta di nuovi cmdlet per supportare scenari di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="3f3a5-114">Rimozione dei cmdlet correlati a componenti interni e funzionalità sottostanti.</span><span class="sxs-lookup"><span data-stu-id="3f3a5-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="3f3a5-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="3f3a5-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="3f3a5-116">Creazione del nuovo modulo per gestire le versioni dei cmdlet di Azure PowerShell tramite l'uso dei profili di versione</span><span class="sxs-lookup"><span data-stu-id="3f3a5-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>