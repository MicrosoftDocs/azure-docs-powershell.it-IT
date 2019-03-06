---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 12/13/2018
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: 10665a72bc7dcae8ecf36b5ef4e2ab285a0e78b7
ms.sourcegitcommit: 5630030c5cfa9828c3c024b69de59248263ef17f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/26/2019
ms.locfileid: "56837674"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="135d9-103">Introduzione del nuovo modulo Az di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="135d9-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="135d9-104">A partire da dicembre 2018, il modulo Az di Azure PowerShell si trova nella versione di disponibilità generale ed è ora il modulo PowerShell desiderato per l'interazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="135d9-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="135d9-105">Az offre comandi più brevi, maggiore stabilità e supporto multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="135d9-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="135d9-106">Az offre anche parità delle funzionalità e un facile percorso di migrazione da AzureRM.</span><span class="sxs-lookup"><span data-stu-id="135d9-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="135d9-107">Az usa la libreria .NET Standard e viene pertanto eseguito in PowerShell 5 e PowerShell 6.</span><span class="sxs-lookup"><span data-stu-id="135d9-107">Az uses the .NET Standard library, which means it runs on PowerShell 5 and PowerShell 6.</span></span>
<span data-ttu-id="135d9-108">Dato che PowerShell 6 può essere eseguito in Linux, macOS e Windows, Azure PowerShell è ora disponibile per tutte le piattaforme.</span><span class="sxs-lookup"><span data-stu-id="135d9-108">Since PowerShell 6 can run on Linux, macOS, and Windows, Azure PowerShell is now available for all platforms.</span></span>
<span data-ttu-id="135d9-109">L'uso di .NET Standard consente di unificare la base di codice di Azure PowerShell con un impatto minimo sugli utenti.</span><span class="sxs-lookup"><span data-stu-id="135d9-109">Using .NET Standard allows us to unify the code base of Azure PowerShell with minimal impact on users.</span></span>

<span data-ttu-id="135d9-110">Dato che Az è un nuovo modulo, la versione è stata reimpostata su 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="135d9-110">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="135d9-111">Eseguire l'aggiornamento ad Az</span><span class="sxs-lookup"><span data-stu-id="135d9-111">Upgrade to Az</span></span>

<span data-ttu-id="135d9-112">È consigliabile che tutti gli utenti eseguano l'aggiornamento al nuovo modulo Az.</span><span class="sxs-lookup"><span data-stu-id="135d9-112">It's recommended that all users upgrade to the new Az module.</span></span> <span data-ttu-id="135d9-113">A tale scopo, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="135d9-113">To do so:</span></span>

* <span data-ttu-id="135d9-114">__CONSIGLIATO__: [Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="135d9-114">__RECOMMENDED__: [Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
* <span data-ttu-id="135d9-115">[Installare il modulo Az di Azure PowerShell](/powershell/azure/install-az-ps).</span><span class="sxs-lookup"><span data-stu-id="135d9-115">[Install the Azure PowerShell Az module](/powershell/azure/install-az-ps)</span></span>
* <span data-ttu-id="135d9-116">Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per aggiungere gli alias per i cmdlet di AzureRM con `Enable-AzureRMAlias`.</span><span class="sxs-lookup"><span data-stu-id="135d9-116">Enable compatibility mode to add aliases for AzureRM cmdlets with `Enable-AzureRMAlias` while you become familiar with the new command set.</span></span> <span data-ttu-id="135d9-117">Abilitare gli alias __solo__ se non è installato AzureRM.</span><span class="sxs-lookup"><span data-stu-id="135d9-117">__Only__ enable aliases if you do not have AzureRM installed.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="135d9-118">Eseguire la migrazione degli script esistenti ad Az</span><span class="sxs-lookup"><span data-stu-id="135d9-118">Migrate existing scripts to Az</span></span>

<span data-ttu-id="135d9-119">Gli aggiornamenti importanti possono essere impegnativi.</span><span class="sxs-lookup"><span data-stu-id="135d9-119">Major updates can be inconvenient.</span></span> <span data-ttu-id="135d9-120">Il modulo Az, tuttavia, offre una modalità compatibilità che consente di usare gli script esistenti mentre si completano gli aggiornamenti alla nuova sintassi.</span><span class="sxs-lookup"><span data-stu-id="135d9-120">However, the Az module has a compatibility mode to help you use existing scripts while you work on updates to the new syntax.</span></span> <span data-ttu-id="135d9-121">Usare il cmdlet `Enable-AzureRmAlias` per abilitare la modalità compatibilità per AzureRM.</span><span class="sxs-lookup"><span data-stu-id="135d9-121">Use the `Enable-AzureRmAlias` cmdlet to enable the AzureRM compatibility mode.</span></span> <span data-ttu-id="135d9-122">Questo cmdlet definisce i nomi dei cmdlet di AzureRM come alias dei nuovi nomi dei cmdlet di Az.</span><span class="sxs-lookup"><span data-stu-id="135d9-122">This cmdlet defines AzureRM cmdlet names as aliases for the new Az cmdlet names.</span></span>

<span data-ttu-id="135d9-123">I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare.</span><span class="sxs-lookup"><span data-stu-id="135d9-123">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="135d9-124">Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`.</span><span class="sxs-lookup"><span data-stu-id="135d9-124">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="135d9-125">Il precedente comando `New-AzureRMVm`, ad esempio, è diventato `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="135d9-125">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>

<span data-ttu-id="135d9-126">Per una descrizione completa del processo di migrazione, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="135d9-126">For a full description of the migration process, see [Migrate from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="the-future-of-support-for-azurerm"></a><span data-ttu-id="135d9-127">Futuro supporto per AzureRM</span><span class="sxs-lookup"><span data-stu-id="135d9-127">The future of support for AzureRM</span></span>

<span data-ttu-id="135d9-128">Il modulo AzureRM esistente non riceverà più i nuovi cmdlet o le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="135d9-128">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="135d9-129">AzureRM, tuttavia, continuerà a essere ufficialmente supportato e a ricevere correzioni di bug fino a dicembre 2020.</span><span class="sxs-lookup"><span data-stu-id="135d9-129">However, AzureRM is still officially maintained and will get bug fixes up through December 2020.</span></span> <span data-ttu-id="135d9-130">Per restare al passo con i servizi e le funzionalità più recenti di Azure, passare al modulo Az.</span><span class="sxs-lookup"><span data-stu-id="135d9-130">To keep up with the latest Azure services and features, switch to the Az module.</span></span>
