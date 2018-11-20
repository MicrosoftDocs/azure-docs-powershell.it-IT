---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 11/07/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: b0f31341d4344bdac5b4d657a1f66acfd9984dda
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574805"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="48a89-103">Introduzione del nuovo modulo Az di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="48a89-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="48a89-104">A partire da novembre 2018, il modulo `Az` di Azure PowerShell è disponibile in anteprima pubblica completa.</span><span class="sxs-lookup"><span data-stu-id="48a89-104">Starting in November 2018, the Azure PowerShell `Az` module is available for full public preview.</span></span>
<span data-ttu-id="48a89-105">Az offre comandi più brevi e maggiore stabilità e supporta Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="48a89-105">Az offers shorter commands, improved stability, and supports Windows, macOS, and Linux.</span></span> <span data-ttu-id="48a89-106">Az offre anche parità delle funzionalità e un facile percorso di migrazione da AzureRM.</span><span class="sxs-lookup"><span data-stu-id="48a89-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="48a89-107">Az usa la libreria .NET Standard e viene pertanto eseguito in PowerShell 5.x e PowerShell 6.x.</span><span class="sxs-lookup"><span data-stu-id="48a89-107">Az uses the .NET Standard library, which means it runs on PowerShell 5.x and PowerShell 6.x.</span></span>
<span data-ttu-id="48a89-108">Dato che PowerShell 6.x può essere eseguito in Linux, macOS e Windows, Az è disponibile per tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="48a89-108">Since PowerShell 6.x can run on Linux, macOS, and Windows, that means Az is available for all platforms.</span></span>
<span data-ttu-id="48a89-109">L'uso di .NET Standard consente di unificare la base di codice di Azure PowerShell con un impatto minimo sugli utenti.</span><span class="sxs-lookup"><span data-stu-id="48a89-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="48a89-110">Dato che Az è un nuovo modulo, la versione è stata reimpostata.</span><span class="sxs-lookup"><span data-stu-id="48a89-110">Az is a new module, so the version has been reset.</span></span> <span data-ttu-id="48a89-111">La prima versione stabile sarà la 1.0, ma il modulo offre parità delle funzionalità rispetto ad AzureRM da novembre 2018.</span><span class="sxs-lookup"><span data-stu-id="48a89-111">The first stable release will be 1.0, but the module has feature parity with AzureRm as of November 2018.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="48a89-112">Eseguire l'aggiornamento ad Az</span><span class="sxs-lookup"><span data-stu-id="48a89-112">Upgrade to Az</span></span>

<span data-ttu-id="48a89-113">È consigliabile che gli utenti eseguano l'aggiornamento al nuovo modulo `Az`.</span><span class="sxs-lookup"><span data-stu-id="48a89-113">It's recommended that users upgrade to the new `Az` module.</span></span> <span data-ttu-id="48a89-114">A tale scopo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="48a89-114">To do so:</span></span>

* <span data-ttu-id="48a89-115">[Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-azurerm-ps).</span><span class="sxs-lookup"><span data-stu-id="48a89-115">[Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-azurerm-ps)</span></span>
* <span data-ttu-id="48a89-116">[Installare il modulo Az di Azure PowerShell](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="48a89-116">[Install the Azure PowerShell Az module](/powershell/azure/install-az-ps)</span></span>
* <span data-ttu-id="48a89-117">Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per AzureRM con `Enable-AzureRMAlias`.</span><span class="sxs-lookup"><span data-stu-id="48a89-117">Enable compatibility mode for AzureRM with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="48a89-118">Eseguire la migrazione degli script esistenti ad Az</span><span class="sxs-lookup"><span data-stu-id="48a89-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="48a89-119">Gli aggiornamenti importanti possono essere impegnativi.</span><span class="sxs-lookup"><span data-stu-id="48a89-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="48a89-120">Il modulo `Az`, tuttavia, offre una modalità compatibilità che consente di usare gli script esistenti mentre si completano gli aggiornamenti alla nuova sintassi.</span><span class="sxs-lookup"><span data-stu-id="48a89-120">However, the `Az` module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="48a89-121">Usare il cmdlet `Enable-AzureRmAlias` per abilitare la modalità compatibilità per `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="48a89-121">Use the `Enable-AzureRmAlias` cmdlet to enable the `AzureRM` compatibility mode.</span></span> <span data-ttu-id="48a89-122">Questo cmdlet definisce i nomi dei cmdlet di `AzureRM` come alias dei nuovi nomi dei cmdlet di `Az`.</span><span class="sxs-lookup"><span data-stu-id="48a89-122">This cmdlet defines `AzureRM` cmdlet names as aliases for the new `Az` cmdlet names.</span></span>

<span data-ttu-id="48a89-123">I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare.</span><span class="sxs-lookup"><span data-stu-id="48a89-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="48a89-124">Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`.</span><span class="sxs-lookup"><span data-stu-id="48a89-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="48a89-125">Il precedente comando `New-AzureRmVm`, ad esempio, è diventato `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="48a89-125">For example, the old command `New-AzureRmVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="48a89-126">Per una descrizione completa del processo di migrazione, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="48a89-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="48a89-127">Futuro supporto per AzureRM</span><span class="sxs-lookup"><span data-stu-id="48a89-127">The future of support for AzureRM</span></span>

<span data-ttu-id="48a89-128">Dopo il rilascio della versione 1.0 di `Az` nel mese di dicembre 2018, non verranno più resi disponibili nuovi cmdlet o funzionalità per il modulo `AzureRM` esistente.</span><span class="sxs-lookup"><span data-stu-id="48a89-128">The existing `AzureRM` module will no longer receive new cmdlets or features when `Az` version 1.0 is released in December 2018.</span></span> <span data-ttu-id="48a89-129">`AzureRM`, tuttavia, continuerà a essere ufficialmente supportato e a ricevere correzioni di bug.</span><span class="sxs-lookup"><span data-stu-id="48a89-129">However, `AzureRM` is still officially maintained and will get bug fixes.</span></span> <span data-ttu-id="48a89-130">Per restare al passo con i servizi e le funzionalità più recenti di Azure, è consigliabile passare al modulo `Az`.</span><span class="sxs-lookup"><span data-stu-id="48a89-130">To keep up with the latest Azure services and features, you should switch to the `Az` module.</span></span>