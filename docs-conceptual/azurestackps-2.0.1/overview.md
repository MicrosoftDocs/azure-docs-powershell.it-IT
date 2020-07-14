---
title: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per l'amministrazione dell'hub di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: 860a32d120e203093038130a535e8b6801e2bce2
ms.sourcegitcommit: 7b368a9be1cea2ac4e7d269e1a51529271269a42
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 07/08/2020
ms.locfileid: "86098832"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="73673-103">Modulo hub di Azure Stack 2.0.1</span><span class="sxs-lookup"><span data-stu-id="73673-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="73673-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="73673-104">Requirements:</span></span>

<span data-ttu-id="73673-105">La versione minima supportata dell'hub di Azure Stack è la 2002.</span><span class="sxs-lookup"><span data-stu-id="73673-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="73673-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="73673-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="73673-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="73673-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="73673-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="73673-108">Release Notes</span></span>

* <span data-ttu-id="73673-109">Supportato con l'aggiornamento 2002.</span><span class="sxs-lookup"><span data-stu-id="73673-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="73673-110">L'hub di Azure Stack 2.0.0 rappresenta una modifica di rilievo.</span><span class="sxs-lookup"><span data-stu-id="73673-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="73673-111">Il modulo usa il modulo Az invece di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="73673-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="73673-112">È possibile trovare una guida alla migrazione e un elenco di modifiche di rilievo in [Eseguire la migrazione da AzureRM ad Azure PowerShell Az nell'hub di Azure Stack](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="73673-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>