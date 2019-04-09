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
ms.openlocfilehash: 6568dc4e6c51e8f250aad2c4dd765c065fe6a8bf
ms.sourcegitcommit: d3069aba7d1ac248aff755e4b21533af1f73251d
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/02/2019
ms.locfileid: "58808061"
---
# <a name="azure-stack-module-171"></a><span data-ttu-id="436a4-103">Modulo di Azure Stack 1.7.1</span><span class="sxs-lookup"><span data-stu-id="436a4-103">Azure Stack Module 1.7.1</span></span>

## <a name="requirements"></a><span data-ttu-id="436a4-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="436a4-104">Requirements:</span></span>

<span data-ttu-id="436a4-105">La versione minima supportata di Azure Stack è 1901.</span><span class="sxs-lookup"><span data-stu-id="436a4-105">Minimum supported Azure Stack version is 1901.</span></span>

<span data-ttu-id="436a4-106">Note: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="436a4-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="436a4-107">Installa</span><span class="sxs-lookup"><span data-stu-id="436a4-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Install-Module -Name AzureRM -RequiredVersion 2.4.0

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.7.1
```

## <a name="release-notes"></a><span data-ttu-id="436a4-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="436a4-108">Release Notes</span></span>

* <span data-ttu-id="436a4-109">Supportato con l'aggiornamento 1901</span><span class="sxs-lookup"><span data-stu-id="436a4-109">Supported with 1901 update</span></span>
* <span data-ttu-id="436a4-110">Questa è una versione con modifiche che causano interruzioni.</span><span class="sxs-lookup"><span data-stu-id="436a4-110">This a breaking change release.</span></span> <span data-ttu-id="436a4-111">Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="436a4-111">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="436a4-112">Azs.Backup.Admin Module \* Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="436a4-112">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="436a4-113">Il supporto delle chiavi simmetriche è deprecato.</span><span class="sxs-lookup"><span data-stu-id="436a4-113">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="436a4-114">Azs.Fabric.Admin Module       \* Deprecato           \* Get-AzsInfrastructureVolume è deprecato; ora è fornito il nuovo Get-AzsVolume           \* Get-AzsStorageSystem è deprecato; ora è fornito il nuovo cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool è deprecato; l'oggetto StorageSubSystem ha la proprietà di capacità</span><span class="sxs-lookup"><span data-stu-id="436a4-114">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="436a4-115">Azs.Compute.Admin Module           \* Correzione dei bug: Add-AzsPlatformImage, Get-AzsPlatformImage : Chiamata a ConvertTo-PlatformImageObject solo nel percorso di riuscita           \* Correzione dei bug: Add-AzsVmExtension, Get-AzsVmExtension : Chiamata a ConvertTo-VmExtensionObject solo nel percorso di riuscita</span><span class="sxs-lookup"><span data-stu-id="436a4-115">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="436a4-116">Modulo Azs.Storage.Admin           \* Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.'</span><span class="sxs-lookup"><span data-stu-id="436a4-116">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
