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
ms.openlocfilehash: 72974ac2fec42da962513c161c506e83f047bfb6
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427378"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="36803-103">Modulo di Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="36803-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="36803-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="36803-104">Requirements:</span></span>

<span data-ttu-id="36803-105">La versione minima supportata di Azure Stack è la 1904.</span><span class="sxs-lookup"><span data-stu-id="36803-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="36803-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="36803-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="36803-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="36803-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.5.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

## <a name="release-notes"></a><span data-ttu-id="36803-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="36803-108">Release Notes</span></span>

* <span data-ttu-id="36803-109">Supportato con l'aggiornamento 1904</span><span class="sxs-lookup"><span data-stu-id="36803-109">Supported with 1904 update</span></span>
* <span data-ttu-id="36803-110">Questa è una versione con modifiche che causano interruzioni.</span><span class="sxs-lookup"><span data-stu-id="36803-110">This a breaking change release.</span></span> <span data-ttu-id="36803-111">Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="36803-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="36803-112">Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="36803-112">Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="36803-113">Il supporto delle chiavi simmetriche è deprecato.</span><span class="sxs-lookup"><span data-stu-id="36803-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="36803-114">Per informazioni dettagliate, fare riferimento a https://aka.ms/azspshmigration170</span><span class="sxs-lookup"><span data-stu-id="36803-114">For details on the breaking changes, refer to https://aka.ms/azspshmigration170</span></span>
* <span data-ttu-id="36803-115">Modulo Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="36803-115">Azs.Storage.Admin Module</span></span> 
* <span data-ttu-id="36803-116">Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.</span><span class="sxs-lookup"><span data-stu-id="36803-116">Bug fix - New Storage Quota uses defaults if none provided.</span></span>