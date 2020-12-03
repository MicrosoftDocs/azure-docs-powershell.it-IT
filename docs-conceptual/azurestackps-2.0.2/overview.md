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
ms.openlocfilehash: 10eaf23e5134ea9788a81477038d735fe3bd59e0
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96426987"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="9d365-103">Modulo di Hub di Azure Stack 2.0.2</span><span class="sxs-lookup"><span data-stu-id="9d365-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="9d365-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="9d365-104">Requirements:</span></span>

<span data-ttu-id="9d365-105">La versione minima supportata dell'hub di Azure Stack è la 2002.</span><span class="sxs-lookup"><span data-stu-id="9d365-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="9d365-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="9d365-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="9d365-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="9d365-107">Install</span></span>

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


## <a name="release-notes"></a><span data-ttu-id="9d365-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="9d365-108">Release Notes</span></span>

* <span data-ttu-id="9d365-109">Supportato con l'aggiornamento 2002.</span><span class="sxs-lookup"><span data-stu-id="9d365-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="9d365-110">L'hub di Azure Stack 2.0.0 rappresenta una modifica di rilievo.</span><span class="sxs-lookup"><span data-stu-id="9d365-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="9d365-111">Il modulo usa il modulo Az invece di AzureRM.</span><span class="sxs-lookup"><span data-stu-id="9d365-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="9d365-112">È possibile trovare una guida alla migrazione e un elenco di modifiche di rilievo in [Eseguire la migrazione da AzureRM ad Azure PowerShell Az nell'hub di Azure Stack](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="9d365-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>