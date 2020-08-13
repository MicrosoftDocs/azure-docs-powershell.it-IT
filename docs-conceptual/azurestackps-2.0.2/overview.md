---
title: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 754038a312a20e0dd87075bdeb51b13a1f1810a1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "88022967"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="f4742-103">Modulo di Hub di Azure Stack 2.0.2</span><span class="sxs-lookup"><span data-stu-id="f4742-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="f4742-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="f4742-104">Requirements:</span></span>

<span data-ttu-id="f4742-105">La versione minima supportata dell'hub di Azure Stack è la 2002.</span><span class="sxs-lookup"><span data-stu-id="f4742-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="f4742-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="f4742-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="f4742-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="f4742-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="f4742-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="f4742-108">Release Notes</span></span>

* <span data-ttu-id="f4742-109">Supportato con l'aggiornamento 2002.</span><span class="sxs-lookup"><span data-stu-id="f4742-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="f4742-110">L'hub di Azure Stack 2.0.0 rappresenta una modifica di rilievo.</span><span class="sxs-lookup"><span data-stu-id="f4742-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="f4742-111">Il modulo usa il modulo Az invece di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="f4742-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="f4742-112">È possibile trovare una guida alla migrazione e un elenco di modifiche di rilievo in [Eseguire la migrazione da AzureRM ad Azure PowerShell Az nell'hub di Azure Stack](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="f4742-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
