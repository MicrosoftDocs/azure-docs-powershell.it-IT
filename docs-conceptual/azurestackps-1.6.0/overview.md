---
title: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack | Microsoft Docs
description: Panoramica di PowerShell per il modulo di amministrazione di Azure Stack con istruzioni per l'installazione e la configurazione.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: 4e1174236796e7da929ff276addb32e42c18b707
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/12/2019
ms.locfileid: "54240136"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="f30cd-103">Modulo di Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="f30cd-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="f30cd-104">Requirements:</span><span class="sxs-lookup"><span data-stu-id="f30cd-104">Requirements:</span></span>
<span data-ttu-id="f30cd-105">La versione minima supportata di Azure Stack è 1811.</span><span class="sxs-lookup"><span data-stu-id="f30cd-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="f30cd-106">Note: Se si usa una versione precedente, installare la versione 1.6.0</span><span class="sxs-lookup"><span data-stu-id="f30cd-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="f30cd-107">Installa</span><span class="sxs-lookup"><span data-stu-id="f30cd-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="f30cd-108">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="f30cd-108">Release Notes</span></span>
* <span data-ttu-id="f30cd-109">Supportato con l'aggiornamento 1811</span><span class="sxs-lookup"><span data-stu-id="f30cd-109">Supported with 1811 update</span></span>
* <span data-ttu-id="f30cd-110">Modulo Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="f30cd-111">Risoluzione del problema relativo al prefisso Azs mancante per New-DataDiskObject e aggiunta dell'alias con l'avviso di una futura deprecazione.</span><span class="sxs-lookup"><span data-stu-id="f30cd-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="f30cd-112">Modulo Azs.Update.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="f30cd-113">Aggiunta di un avviso per consigliare di eseguire Test-AzureStack prima di Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="f30cd-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="f30cd-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="f30cd-115">Nuovo cmdlet (le funzionalità sono supportate da Azure Stack 1811+)</span><span class="sxs-lookup"><span data-stu-id="f30cd-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="f30cd-116">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="f30cd-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="f30cd-117">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="f30cd-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="f30cd-118">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="f30cd-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="f30cd-119">Deprecazione</span><span class="sxs-lookup"><span data-stu-id="f30cd-119">Deprecation</span></span>
        * <span data-ttu-id="f30cd-120">Get-AzsInfrastructureVolume è ora un alias per il cmdlet Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="f30cd-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="f30cd-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="f30cd-122">Aggiunta del nuovo cmdlet Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="f30cd-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="f30cd-123">Azs.Storage.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="f30cd-124">Correzione del bug in cui non vengono usati i valori di quota predefiniti</span><span class="sxs-lookup"><span data-stu-id="f30cd-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="f30cd-125">Modulo Azs.Subscriptions.Admin</span><span class="sxs-lookup"><span data-stu-id="f30cd-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="f30cd-126">Risoluzione del problema relativo al prefisso Azs mancante per New-AddonPlanDefinitionObject e aggiunta dell'alias con l'avviso di una futura deprecazione.</span><span class="sxs-lookup"><span data-stu-id="f30cd-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>