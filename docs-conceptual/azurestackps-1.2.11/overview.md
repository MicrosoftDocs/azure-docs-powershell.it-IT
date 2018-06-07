---
title: Panoramica di PowerShell per Azure Stack | Microsoft Docs
description: Panoramica dell'installazione e della configurazione di PowerShell per Azure Stack.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: 3f55ff613004f0726e20255126b29bf7f64662b8
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820202"
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="5389d-103">PowerShell per Azure Stack</span><span class="sxs-lookup"><span data-stu-id="5389d-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="5389d-104">Azure Stack richiede i due moduli PowerShell seguenti:</span><span class="sxs-lookup"><span data-stu-id="5389d-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="5389d-105">Il modulo **AzureRM** compatibile con Azure Stack, disponibile installando il profilo di versione API **2017-03-09-profile**.</span><span class="sxs-lookup"><span data-stu-id="5389d-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="5389d-106">I cmdlet installati con questo profilo possono essere usati solo dagli operatori e dagli utenti di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5389d-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="5389d-107">La versione più recente è l'installazione **1.2.11** del modulo **AzureStack**.</span><span class="sxs-lookup"><span data-stu-id="5389d-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="5389d-108">I cmdlet installati con questo modulo possono essere usati solo dagli operatori di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="5389d-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="5389d-109">Un operatore può eseguire operazioni come la gestione di offerte, piani, servizi, quote e così via usando i cmdlet di PowerShell disponibili in questo modulo.</span><span class="sxs-lookup"><span data-stu-id="5389d-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="5389d-110">Per informazioni sui cmdlet di PowerShell disponibili in questo modulo, vedere i contenuti di riferimento su [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) e [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage).</span><span class="sxs-lookup"><span data-stu-id="5389d-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5389d-111">Passaggi successivi</span><span class="sxs-lookup"><span data-stu-id="5389d-111">Next Steps</span></span>

* [<span data-ttu-id="5389d-112">Installare PowerShell per Azure Stack</span><span class="sxs-lookup"><span data-stu-id="5389d-112">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="5389d-113">Configurare PowerShell per l'uso con Azure Stack</span><span class="sxs-lookup"><span data-stu-id="5389d-113">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
