---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/06/2019
ms.openlocfilehash: 1b3d707e862dd0c21e9e6b0a89f429ff21b1a99d
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "68861335"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="bc289-103">Modulo di Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="bc289-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="bc289-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="bc289-104">Requirements:</span></span>

<span data-ttu-id="bc289-105">La versione minima supportata di Azure Stack è la 1904.</span><span class="sxs-lookup"><span data-stu-id="bc289-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="bc289-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="bc289-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="bc289-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="bc289-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="bc289-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="bc289-108">Release Notes</span></span>

* <span data-ttu-id="bc289-109">Supportato con l'aggiornamento 1904</span><span class="sxs-lookup"><span data-stu-id="bc289-109">Supported with 1904 update</span></span>
* <span data-ttu-id="bc289-110">Questa è una versione con modifiche che causano interruzioni.</span><span class="sxs-lookup"><span data-stu-id="bc289-110">This a breaking change release.</span></span> <span data-ttu-id="bc289-111">Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="bc289-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="bc289-112">Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="bc289-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="bc289-113">Il supporto delle chiavi simmetriche è deprecato.</span><span class="sxs-lookup"><span data-stu-id="bc289-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="bc289-114">Per informazioni dettagliate, fare riferimento a https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="bc289-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="bc289-115">Modulo Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="bc289-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="bc289-116">Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.</span><span class="sxs-lookup"><span data-stu-id="bc289-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>
