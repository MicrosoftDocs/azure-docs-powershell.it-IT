---
title: Introduzione del modulo Az di Azure PowerShell
description: Introduzione del nuovo modulo Az di Azure PowerShell, in sostituzione del modulo AzureRM.
ms.date: 05/10/2019
author: sptramer
ms.author: sttramer
ms.manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.openlocfilehash: da1d7ec9a196068db237d871834b92f8b077b42c
ms.sourcegitcommit: 020c69430358b13cbd99fedd5d56607c9b10047b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/29/2019
ms.locfileid: "66365689"
---
# <a name="introducing-the-new-azure-powershell-az-module"></a><span data-ttu-id="1bae0-103">Introduzione del nuovo modulo Az di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="1bae0-103">Introducing the new Azure PowerShell Az module</span></span>

<span data-ttu-id="1bae0-104">A partire da dicembre 2018, il modulo Az di Azure PowerShell si trova nella versione di disponibilità generale ed è ora il modulo PowerShell desiderato per l'interazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1bae0-104">Starting in December 2018, the Azure PowerShell Az module is in general release and now the intended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="1bae0-105">Az offre comandi più brevi, maggiore stabilità e supporto multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="1bae0-105">Az offers shorter commands, improved stability, and cross-platform support.</span></span> <span data-ttu-id="1bae0-106">Az offre anche parità delle funzionalità e un facile percorso di migrazione da AzureRM.</span><span class="sxs-lookup"><span data-stu-id="1bae0-106">Az also offers feature parity and an easy migration path from AzureRM.</span></span>

<span data-ttu-id="1bae0-107">Con il modulo Az, Azure PowerShell è ora compatibile con PowerShell 5.1 in Windows e PowerShell Core 6.x e versioni successive in tutte le piattaforme supportate, tra cui Windows, macOS e Linux.</span><span class="sxs-lookup"><span data-stu-id="1bae0-107">With the Az module, Azure PowerShell is now compatible with PowerShell 5.1 on Windows and PowerShell Core 6.x and later on all supported platforms - including Windows, macOS, and Linux.</span></span>

<span data-ttu-id="1bae0-108">Dato che Az è un nuovo modulo, la versione è stata reimpostata su 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="1bae0-108">Az is a new module, so the version has been reset to 1.0.0.</span></span>

## <a name="why-a-new-module"></a><span data-ttu-id="1bae0-109">Perché è stato creato un nuovo modulo?</span><span class="sxs-lookup"><span data-stu-id="1bae0-109">Why a new module?</span></span>

<span data-ttu-id="1bae0-110">Gli aggiornamenti principali possono risultare poco pratici, di conseguenza è importante informare gli utenti in merito ai motivi per cui si è deciso di introdurre un nuovo set di moduli, con nuovi cmdlet, per l'interazione con Azure da PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1bae0-110">Major updates can be inconvenient, so it's important that we let you know why the decision was made to introduce a new set of modules, with new cmdlets, for interacting with Azure from PowerShell.</span></span>

<span data-ttu-id="1bae0-111">La principale modifica è che in seguito all'introduzione di [PowerShell Core 6.x](/powershell/scripting/overview), basato sulla libreria .NET Standard, PowerShell è diventato un prodotto multipiattaforma.</span><span class="sxs-lookup"><span data-stu-id="1bae0-111">The biggest and most important change is that PowerShell has been a cross-platform product since the introduction of [PowerShell Core 6.x](/powershell/scripting/overview), based on the .NET Standard library.</span></span>
<span data-ttu-id="1bae0-112">Dal momento che è intenzione di Microsoft includere il supporto per Azure in tutte le piattaforme, era necessario aggiornare i moduli di Azure PowerShell in modo che potessero usare .NET Standard e fossero compatibili con PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="1bae0-112">We're committed to bringing Azure support to all platforms, which means that the Azure PowerShell modules needed to be updated to use .NET Standard and be compatible with PowerShell Core.</span></span> <span data-ttu-id="1bae0-113">Invece di usare il modulo AzureRM esistente e introdurre modifiche complesse per aggiungere questo supporto, è stato creato il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="1bae0-113">Rather than taking the existing AzureRM module and introduce complex changes to add this support, the Az module was created.</span></span>

<span data-ttu-id="1bae0-114">La creazione di un nuovo modulo ha inoltre offerto ai nostri sviluppatori l'opportunità di uniformare la progettazione e la denominazione di cmdlet e moduli.</span><span class="sxs-lookup"><span data-stu-id="1bae0-114">Creating a new module also gave our engineers the opportunity to make the design and naming of cmdlets and modules consistent.</span></span> <span data-ttu-id="1bae0-115">Ora i nomi di tutti i moduli iniziano con il prefisso `Az.` e i cmdlet usano tutti il formato _verbo_-`Az`_sostantivo_.</span><span class="sxs-lookup"><span data-stu-id="1bae0-115">All modules now start with the `Az.` prefix and cmdlets all use the _Verb_-`Az`_Noun_ form.</span></span> <span data-ttu-id="1bae0-116">In precedenza, i nomi dei cmdlet non solo erano più lunghi, ma risultavano incoerenti.</span><span class="sxs-lookup"><span data-stu-id="1bae0-116">Previously, cmdlet names were not only longer, there were inconsistencies in cmdlet names.</span></span>

<span data-ttu-id="1bae0-117">È stato inoltre ridotto il numero di moduli: alcuni moduli usati con gli stessi servizi sono stati raggruppati e ora i cmdlet del piano di gestione e del piano dati sono tutti contenuti in singoli moduli per i relativi servizi.</span><span class="sxs-lookup"><span data-stu-id="1bae0-117">The number of modules was also reduced: Some modules which worked with the same services have been rolled together, and management plane and data plane cmdlets are now contained all within single modules for their services.</span></span> <span data-ttu-id="1bae0-118">Questo approccio semplifica le operazioni eseguite dagli utenti che gestiscono manualmente dipendenze e importazioni.</span><span class="sxs-lookup"><span data-stu-id="1bae0-118">For those of you who manually manage dependencies and imports, this makes things much simpler.</span></span>

<span data-ttu-id="1bae0-119">Apportando queste importanti modifiche che hanno richiesto la creazione di un nuovo modulo di Azure PowerShell, il team si è impegnato a rendere ancor più semplice usare Azure con i cmdlet di PowerShell e su un numero di piattaforme maggiore rispetto alle versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="1bae0-119">By making these important changes that required building a new Azure PowerShell module, the team has committed to making it easier than ever, and on more platforms than previously possible, to use Azure with PowerShell cmdlets.</span></span>

## <a name="upgrade-to-az"></a><span data-ttu-id="1bae0-120">Eseguire l'aggiornamento ad Az</span><span class="sxs-lookup"><span data-stu-id="1bae0-120">Upgrade to Az</span></span>

<span data-ttu-id="1bae0-121">Per restare al passo con le funzionalità più recenti di Azure in PowerShell, è opportuno eseguire al più presto la migrazione al modulo Az.</span><span class="sxs-lookup"><span data-stu-id="1bae0-121">To keep up with the latest Azure features in PowerShell, you should migrate to the Az module as soon as possible.</span></span> <span data-ttu-id="1bae0-122">Se non si è pronti a installare il modulo Az in sostituzione di AzureRM, sono disponibili alcune opzioni per provare Az:</span><span class="sxs-lookup"><span data-stu-id="1bae0-122">If you're not ready to install the Az module as a replacement for AzureRM, you have a couple of options available to experiment with Az:</span></span>

* <span data-ttu-id="1bae0-123">Usare un ambiente `PowerShell` con [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview).</span><span class="sxs-lookup"><span data-stu-id="1bae0-123">Use a `PowerShell` environment with [Azure Cloud Shell](https://docs.microsoft.com/en-us/azure/cloud-shell/overview).</span></span>
  <span data-ttu-id="1bae0-124">Azure Cloud Shell è un ambiente di shell basato su browser che è disponibile quando si installa il modulo Az e si abilita gli alias per la compatibilità con `Enable-AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="1bae0-124">Azure Cloud Shell is a browser-based shell environment which comes with the Az module installed and `Enable-AzureRM` compatibility aliases enabled.</span></span>
* <span data-ttu-id="1bae0-125">Mantenere installato il modulo AzureRM con PowerShell 5.1 per Windows, ma installare il modulo Az per PowerShell Core 6.x o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="1bae0-125">Keep the AzureRM module installed with PowerShell 5.1 for Windows, but install the Az module for PowerShell Core 6.x or later.</span></span> <span data-ttu-id="1bae0-126">PowerShell 5.1 per Windows e PowerShell Core usano raccolte di moduli separate.</span><span class="sxs-lookup"><span data-stu-id="1bae0-126">PowerShell 5.1 for Windows and PowerShell Core use separate collections of modules.</span></span> <span data-ttu-id="1bae0-127">Seguire le istruzioni per [installare PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) e quindi [installare il modulo Az](install-az-ps.md) da un terminale di PowerShell Core.</span><span class="sxs-lookup"><span data-stu-id="1bae0-127">Follow the instructions to [install PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) and then [install the Az module](install-az-ps.md) from a PowerShell Core terminal.</span></span>

<span data-ttu-id="1bae0-128">Per eseguire l'aggiornamento da un'installazione esistente di AzureRM:</span><span class="sxs-lookup"><span data-stu-id="1bae0-128">To upgrade from an existing AzureRM install:</span></span>

1. <span data-ttu-id="1bae0-129">[Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).</span><span class="sxs-lookup"><span data-stu-id="1bae0-129">[Uninstall the Azure PowerShell AzureRM module](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module)</span></span>
2. <span data-ttu-id="1bae0-130">[Installare il modulo Az di Azure PowerShell](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="1bae0-130">[Install the Azure PowerShell Az module](install-az-ps.md)</span></span>
3. <span data-ttu-id="1bae0-131">__FACOLTATIVO__: Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per aggiungere gli alias per i cmdlet di AzureRM con [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="1bae0-131">__OPTIONAL__: Enable compatibility mode to add aliases for AzureRM cmdlets with [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias) while you become familiar with the new command set.</span></span> <span data-ttu-id="1bae0-132">Per maggiori dettagli, vedere la sezione successiva oppure [avviare la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="1bae0-132">See the next section or [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md) for more details.</span></span>

## <a name="migrate-existing-scripts-to-az"></a><span data-ttu-id="1bae0-133">Eseguire la migrazione degli script esistenti ad Az</span><span class="sxs-lookup"><span data-stu-id="1bae0-133">Migrate existing scripts to Az</span></span>

<span data-ttu-id="1bae0-134">I nuovi nomi dei cmdlet sono stati progettati per essere facili da imparare.</span><span class="sxs-lookup"><span data-stu-id="1bae0-134">The new cmdlet names have been designed to be easy to learn.</span></span> <span data-ttu-id="1bae0-135">Invece di usare `AzureRm` o `Azure` nei nomi dei cmdlet, usare `Az`.</span><span class="sxs-lookup"><span data-stu-id="1bae0-135">Instead of using `AzureRm` or `Azure` in cmdlet names, use `Az`.</span></span> <span data-ttu-id="1bae0-136">Il precedente comando `New-AzureRMVm`, ad esempio, è diventato `New-AzVm`.</span><span class="sxs-lookup"><span data-stu-id="1bae0-136">For example, the old command `New-AzureRMVm` has become `New-AzVm`.</span></span>
<span data-ttu-id="1bae0-137">La migrazione, tuttavia, non implica solo acquisire familiarità con i nuovi nomi dei cmdlet: sono presenti altre importanti modifiche, tra cui moduli e parametri rinominati.</span><span class="sxs-lookup"><span data-stu-id="1bae0-137">Migration is more than just becoming familiar with the new cmdlet names, though: There are renamed modules, parameters, and other important changes.</span></span>

<span data-ttu-id="1bae0-138">Per facilitare il processo di migrazione da AzureRM ad Az, sono disponibili numerose risorse:</span><span class="sxs-lookup"><span data-stu-id="1bae0-138">To help you with the process of migration from AzureRM to Az, we've got a number of resources:</span></span>

* [<span data-ttu-id="1bae0-139">Introduzione alla migrazione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="1bae0-139">Get started with migration from AzureRM to Az</span></span>](migrate-from-azurerm-to-az.md)
* [<span data-ttu-id="1bae0-140">Elenco completo delle modifiche di rilievo apportate durante la migrazione da AzureRM ad Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="1bae0-140">Full list of breaking changes from AzureRM to Az 1.0.0</span></span>](migrate-az-1.0.0.md)
* <span data-ttu-id="1bae0-141">Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)</span><span class="sxs-lookup"><span data-stu-id="1bae0-141">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet</span></span>

<span data-ttu-id="1bae0-142">Il modulo Az offre una modalità compatibilità che consente di usare gli script esistenti mentre esegue l'aggiornamento alla nuova sintassi.</span><span class="sxs-lookup"><span data-stu-id="1bae0-142">The Az module has a compatibility mode to help you use existing scripts while you update to the new syntax.</span></span> <span data-ttu-id="1bae0-143">Il cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) abilita una modalità compatibilità tramite alias, per consentire agli utenti di usare script esistenti con modifiche minime mentre si predispone una migrazione completa ad Az.</span><span class="sxs-lookup"><span data-stu-id="1bae0-143">The [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) cmdlet enables a compatibility mode through aliases, to allow you to use existing scripts with minimal modification while working towards a full migration to Az.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bae0-144">Anche se sono stati creati alias per i nomi dei cmdlet, possono esistere comunque parametri nuovi o rinominati oppure valori restituiti modificati per i cmdlet di Az.</span><span class="sxs-lookup"><span data-stu-id="1bae0-144">Even though the cmdlet names are aliased, there may still be new (or renamed) parameters or changed return values for the Az cmdlets.</span></span> <span data-ttu-id="1bae0-145">Tenere presente che l'abilitazione degli alias non implica l'esecuzione automatica della migrazione.</span><span class="sxs-lookup"><span data-stu-id="1bae0-145">Don't expect enabling aliases to take care of the migration for you!</span></span> <span data-ttu-id="1bae0-146">Per individuare le parti degli script che potrebbero richiedere aggiornamenti, vedere l'[elenco completo delle modifiche di rilievo](migrate-az-1.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="1bae0-146">See the [full breaking changes list](migrate-az-1.0.0.md) to find where your scripts may require updates.</span></span>

## <a name="continued-support-for-azurerm"></a><span data-ttu-id="1bae0-147">Disponibilità del supporto per AzureRM</span><span class="sxs-lookup"><span data-stu-id="1bae0-147">Continued support for AzureRM</span></span>

<span data-ttu-id="1bae0-148">Il modulo AzureRM esistente non riceverà più i nuovi cmdlet o le nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1bae0-148">The existing AzureRM module will no longer receive new cmdlets or features.</span></span> <span data-ttu-id="1bae0-149">AzureRM, tuttavia, continuerà a essere ufficialmente supportato e a ricevere correzioni di bug almeno fino a dicembre 2020.</span><span class="sxs-lookup"><span data-stu-id="1bae0-149">However, AzureRM is still officially maintained and will get bug fixes up through at least December 2020.</span></span>

<span data-ttu-id="1bae0-150">Se si è preoccupati del fatto che il modulo Az sia un prodotto completo, testato o pronto per il passaggio in produzione, tenere presente che tutte le iniziative tecniche previste per AzureRM sono state dirottate su Az, incluso il massimo riutilizzo possibile del codice di moduli esistenti e test completi per rendere i nuovi moduli compatibili con le funzionalità esistenti.</span><span class="sxs-lookup"><span data-stu-id="1bae0-150">If you have concerns about whether or not the Az module is as fully-featured, tested, or production ready: All of the engineering work that went into AzureRM has now been focused on Az, including as much code reuse of the existing modules as was possible, and extensive testing to make the new modules feature-compatible.</span></span> <span data-ttu-id="1bae0-151">Il passaggio ad Az deve essere basato unicamente sulla pianificazione dell'organizzazione, senza attendere l'aggiunta di funzionalità specifiche.</span><span class="sxs-lookup"><span data-stu-id="1bae0-151">Moving onto Az should be influenced by your organization's schedule alone, without needing to wait on specific features to appear.</span></span>