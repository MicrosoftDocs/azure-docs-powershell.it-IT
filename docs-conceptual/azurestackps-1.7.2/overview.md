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
ms.openlocfilehash: af0343e5ad92fa7f2b5c10e3e67cb7e10feb81c6
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/17/2019
ms.locfileid: "65855789"
---
# <a name="azure-stack-module-172"></a><span data-ttu-id="4a59f-103">Modulo di Azure Stack 1.7.2</span><span class="sxs-lookup"><span data-stu-id="4a59f-103">Azure Stack Module 1.7.2</span></span>

## <a name="requirements"></a><span data-ttu-id="4a59f-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="4a59f-104">Requirements:</span></span>

<span data-ttu-id="4a59f-105">La versione minima supportata di Azure Stack è la 1904.</span><span class="sxs-lookup"><span data-stu-id="4a59f-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="4a59f-106">Note: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="4a59f-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/en-us/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install-powershell-for-azure-stack"></a><span data-ttu-id="4a59f-107">Installare PowerShell per Azure Stack</span><span class="sxs-lookup"><span data-stu-id="4a59f-107">Install PowerShell for Azure Stack</span></span>

<span data-ttu-id="4a59f-108">L'installazione prevede tre passaggi:</span><span class="sxs-lookup"><span data-stu-id="4a59f-108">Installation has three steps:</span></span>

1. <span data-ttu-id="4a59f-109">Installare PowerShell per Azure Stack in base alla versione di Azure Stack</span><span class="sxs-lookup"><span data-stu-id="4a59f-109">Install Azure Stack PowerShell depending on your version of Azure Stack</span></span>
2. <span data-ttu-id="4a59f-110">Abilitare funzionalità aggiuntive di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a59f-110">Enable additional storage features</span></span>
3. <span data-ttu-id="4a59f-111">Verificare l'installazione di PowerShell</span><span class="sxs-lookup"><span data-stu-id="4a59f-111">Confirm the installation of PowerShell</span></span>

### <a name="install-azure-stack-powershell"></a><span data-ttu-id="4a59f-112">Installare PowerShell per Azure Stack</span><span class="sxs-lookup"><span data-stu-id="4a59f-112">Install Azure Stack PowerShell</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install the AzureRM.BootStrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRM.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Get-AzureRmProfile -Update
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force
Install-Module -Name AzureStack -RequiredVersion 1.7.2
```

### <a name="enable-additional-storage-features"></a><span data-ttu-id="4a59f-113">Abilitare funzionalità aggiuntive di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4a59f-113">Enable additional storage features</span></span>

```
# Install the Azure.Storage module version 4.5.0
Install-Module -Name Azure.Storage -RequiredVersion 4.5.0 -Force -AllowClobber

# Install the AzureRm.Storage module version 5.0.4
Install-Module -Name AzureRM.Storage -RequiredVersion 5.0.4 -Force -AllowClobber

# Remove incompatible storage module installed by AzureRM.Storage
Uninstall-Module Azure.Storage -RequiredVersion 4.6.1 -Force

# Load the modules explicitly specifying the versions
Import-Module -Name Azure.Storage -RequiredVersion 4.5.0
Import-Module -Name AzureRM.Storage -RequiredVersion 5.0.4
```

## <a name="release-notes"></a><span data-ttu-id="4a59f-114">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="4a59f-114">Release Notes</span></span>

* <span data-ttu-id="4a59f-115">Supportato con l'aggiornamento 1904</span><span class="sxs-lookup"><span data-stu-id="4a59f-115">Supported with 1904 update</span></span>
* <span data-ttu-id="4a59f-116">Questa è una versione con modifiche che causano interruzioni.</span><span class="sxs-lookup"><span data-stu-id="4a59f-116">This a breaking change release.</span></span> <span data-ttu-id="4a59f-117">Per informazioni dettagliate, fare riferimento a <https://aka.ms/azspshmigration170></span><span class="sxs-lookup"><span data-stu-id="4a59f-117">For details on the breaking changes, refer to <https://aka.ms/azspshmigration170></span></span>
* <span data-ttu-id="4a59f-118">Azs.Backup.Admin Module \* Modifica che causa un'interruzione: passaggio dal backup alla modalità di crittografia basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="4a59f-118">Azs.Backup.Admin Module \* Breaking change: Backup changes to cert-based encryption mode.</span></span> <span data-ttu-id="4a59f-119">Il supporto delle chiavi simmetriche è deprecato.</span><span class="sxs-lookup"><span data-stu-id="4a59f-119">Support for symmetric keys is deprecated.</span></span>
* <span data-ttu-id="4a59f-120">Azs.Fabric.Admin Module       \* Deprecato           \* Get-AzsInfrastructureVolume è deprecato; ora è fornito il nuovo Get-AzsVolume           \* Get-AzsStorageSystem è deprecato; ora è fornito il nuovo cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool è deprecato; l'oggetto StorageSubSystem ha la proprietà di capacità</span><span class="sxs-lookup"><span data-stu-id="4a59f-120">Azs.Fabric.Admin Module       \* Deprecation           \* Get-AzsInfrastructureVolume has been deprecated, we provide new cmdlet Get-AzsVolume           \* Get-AzsStorageSystem has been deprecated, we provide new cmdlet Get-AzsStorageSubSystem           \* Get-AzsStoragePool has been deprecated, the StorageSubSystem object has the capacity property</span></span>
* <span data-ttu-id="4a59f-121">Azs.Compute.Admin Module           \* Correzione dei bug: Add-AzsPlatformImage, Get-AzsPlatformImage : Chiamata a ConvertTo-PlatformImageObject solo nel percorso di riuscita           \* Correzione dei bug: Add-AzsVmExtension, Get-AzsVmExtension : Chiamata a ConvertTo-VmExtensionObject solo nel percorso di riuscita</span><span class="sxs-lookup"><span data-stu-id="4a59f-121">Azs.Compute.Admin Module           \* BugFix: Add-AzsPlatformImage, Get-AzsPlatformImage : Calling ConvertTo-PlatformImageObject only in the success path           \* BugFix: Add-AzsVmExtension, Get-AzsVmExtension : Calling ConvertTo-VmExtensionObject only in the success path</span></span>
* <span data-ttu-id="4a59f-122">Modulo Azs.Storage.Admin           \* Correzione dei bug - In assenza di valori, la nuova quota di archiviazione usa quelli predefiniti.'</span><span class="sxs-lookup"><span data-stu-id="4a59f-122">Azs.Storage.Admin Module           \* Bug fix - New Storage Quota uses defaults if none provided.'</span></span>
