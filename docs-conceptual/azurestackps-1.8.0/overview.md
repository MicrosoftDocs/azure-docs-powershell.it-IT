---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "78264411"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="1cb76-103">Modulo di Azure Stack 1.8.0</span><span class="sxs-lookup"><span data-stu-id="1cb76-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb76-104">Requisiti:</span><span class="sxs-lookup"><span data-stu-id="1cb76-104">Requirements:</span></span>

<span data-ttu-id="1cb76-105">La versione minima supportata di Azure Stack è la 1910.</span><span class="sxs-lookup"><span data-stu-id="1cb76-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="1cb76-106">Nota: Per le versioni precedenti di Azure Stack, vedere [Installare PowerShell per Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span><span class="sxs-lookup"><span data-stu-id="1cb76-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="1cb76-107">Installazione</span><span class="sxs-lookup"><span data-stu-id="1cb76-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="1cb76-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="1cb76-108">Release Notes</span></span>

* <span data-ttu-id="1cb76-109">Supportato con l'aggiornamento 1910</span><span class="sxs-lookup"><span data-stu-id="1cb76-109">Supported with 1910 update</span></span>
* <span data-ttu-id="1cb76-110">Le modifiche includono:</span><span class="sxs-lookup"><span data-stu-id="1cb76-110">Changes include:</span></span>

    - <span data-ttu-id="1cb76-111">**Nuovo modulo di amministrazione DRP**: DRP (Deployment Resource Provider) consente distribuzioni orchestrate di provider di risorse all'hub di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="1cb76-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="1cb76-112">Questi comandi interagiscono con il livello di Azure Resource Manager per interagire con DRP.</span><span class="sxs-lookup"><span data-stu-id="1cb76-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="1cb76-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="1cb76-113">**BRP**:</span></span>
        - <span data-ttu-id="1cb76-114">Supporto del ripristino del ruolo singolo per il backup dell'infrastruttura di Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="1cb76-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="1cb76-115">Aggiunta del parametro `RoleName` al cmdlet R`estore-AzsBackup`.</span><span class="sxs-lookup"><span data-stu-id="1cb76-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="1cb76-116">**FRP**: Modifiche di rilievo per le risorse di tipo **Unità** e **Volume** con l'API versione 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="1cb76-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="1cb76-117">Le funzionalità sono supportate dall'hub di Azure Stack 1910 e versioni successive:</span><span class="sxs-lookup"><span data-stu-id="1cb76-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="1cb76-118">Il valore di ID, `Name`, `HealthStatus` e `OperationalStatus` sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="1cb76-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="1cb76-119">Sono supportate le nuove proprietà `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` e `StoragePool` per le risorse di tipo **Unità**.</span><span class="sxs-lookup"><span data-stu-id="1cb76-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="1cb76-120">Le proprietà `CanPool` e `CannotPoolReason` delle risorse di tipo **Unità** sono state deprecate. In alternativa, usare `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="1cb76-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
