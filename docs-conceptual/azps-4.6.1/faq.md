---
title: Domande frequenti
description: Domande frequenti su Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89239384"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="1a7f3-103">Domande frequenti su Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a7f3-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="1a7f3-104">Che cos'è Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="1a7f3-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="1a7f3-105">Azure PowerShell è un set di cmdlet che consente di gestire le risorse di Azure direttamente con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1a7f3-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="1a7f3-106">Nel dicembre 2018 il modulo Az PowerShell è diventato disponibile a livello generale.</span><span class="sxs-lookup"><span data-stu-id="1a7f3-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="1a7f3-107">Ora è il modulo PowerShell consigliato per l'interazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a7f3-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="1a7f3-108">Per altre informazioni sul modulo Az PowerShell, vedere [Introduzione del nuovo modulo Az di Azure PowerShell](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="1a7f3-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="1a7f3-109">Come si disabilitano i messaggi di avviso relativi a modifiche che causano interruzioni in Azure PowerShell?</span><span class="sxs-lookup"><span data-stu-id="1a7f3-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="1a7f3-110">Per non visualizzare i messaggi di avviso relativi a modifiche che causano interruzioni in Azure PowerShell, è necessario impostare la variabile di ambiente `SuppressAzurePowerShellBreakingChangeWarnings` su `true`.</span><span class="sxs-lookup"><span data-stu-id="1a7f3-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
