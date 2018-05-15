---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 5fe7591855577e083aad5923aed37b18d0b2a40c
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="release-notes"></a><span data-ttu-id="657da-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="657da-103">Release notes</span></span>

<span data-ttu-id="657da-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="657da-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

## <a name="version-129"></a><span data-ttu-id="657da-105">Versione 1.2.9</span><span class="sxs-lookup"><span data-stu-id="657da-105">Version 1.2.9</span></span>

<span data-ttu-id="657da-106">Modifiche di questa versione</span><span class="sxs-lookup"><span data-stu-id="657da-106">Changes This Release</span></span>

* <span data-ttu-id="657da-107">Modulo AzureRm.AzureStackAdmin</span><span class="sxs-lookup"><span data-stu-id="657da-107">AzureRm.AzureStackAdmin Module</span></span>
    + <span data-ttu-id="657da-108">Modifiche apportate al cmdlet Add-AzureRmResourceProviderRegistration per il supporto della divisione tra Azure Resource Manager per amministratori e Azure Resource Manager per tenant.</span><span class="sxs-lookup"><span data-stu-id="657da-108">Changes in the Add-AzureRmResourceProviderRegistration cmdlet for the support of Admin Azure resource manager and tenant azure resource manager split.</span></span> <span data-ttu-id="657da-109">Aggiunta del nuovo parametro -ResourceManagerType.</span><span class="sxs-lookup"><span data-stu-id="657da-109">A new parameter -ResourceManagerType has been added.</span></span>
    + <span data-ttu-id="657da-110">Rimozione dei parametri -AdminUri, -ApiVersion, -SubscriptionId e -Token da ogni cmdlet.</span><span class="sxs-lookup"><span data-stu-id="657da-110">Removal of the parameters -AdminUri, -ApiVersion, -SubscriptionId and -Token from each cmdlets.</span></span> <span data-ttu-id="657da-111">Dopo aver emesso avvisi relativi al fatto che questi parametri sarebbero stati deprecati, i parametri sono ora stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="657da-111">We have been printing warnings that these parameters will be deprecated and now they got removed.</span></span>
* <span data-ttu-id="657da-112">Modulo AzureStackStorage</span><span class="sxs-lookup"><span data-stu-id="657da-112">AzureStackStorage module</span></span>
    + <span data-ttu-id="657da-113">Aggiunta di nuovi cmdlet per supportare scenari di migrazione dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="657da-113">Added new cmdlets to support container migration scenarios.</span></span>
    + <span data-ttu-id="657da-114">Rimozione dei cmdlet correlati a componenti interni e funzionalità sottostanti.</span><span class="sxs-lookup"><span data-stu-id="657da-114">Removed cmdlets referring to internal components and underlying features.</span></span>
* <span data-ttu-id="657da-115">AzureRM.BootStrapper</span><span class="sxs-lookup"><span data-stu-id="657da-115">AzureRM.BootStrapper</span></span>
    + <span data-ttu-id="657da-116">Creazione del nuovo modulo per gestire le versioni dei cmdlet di Azure PowerShell tramite l'uso dei profili di versione</span><span class="sxs-lookup"><span data-stu-id="657da-116">Created new module to manage versions of Azure PowerShell cmdlets through the use of version profiles</span></span>