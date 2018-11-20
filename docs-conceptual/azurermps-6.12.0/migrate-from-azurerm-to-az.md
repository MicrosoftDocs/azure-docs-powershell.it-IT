---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/07/2018
ms.openlocfilehash: 0c73e7ac1d47a2a97b6136fa481d0adce8de33db
ms.sourcegitcommit: 4afdba3cd7e1d348876ce59f3503fdcd258f79ab
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/15/2018
ms.locfileid: "51574414"
---
# <a name="migrate-from-azurerm-to-azure-powershell-az"></a><span data-ttu-id="20a64-103">Eseguire la migrazione da AzureRM ad Az di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="20a64-103">Migrate from AzureRM to Azure PowerShell Az</span></span>

<span data-ttu-id="20a64-104">Il modulo Az offre parità delle funzionalità rispetto ad AzureRM, ma usa nomi di cmdlet più brevi e coerenti.</span><span class="sxs-lookup"><span data-stu-id="20a64-104">The Az module has feature parity with AzureRM, but uses shorter and more consistent cmdlet names.</span></span>
<span data-ttu-id="20a64-105">Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="20a64-105">Scripts written for the AzureRM cmdlets won't automatically work with the new module.</span></span> <span data-ttu-id="20a64-106">Per facilitare la transizione, Az offre strumenti che consentono di eseguire gli script esistenti con AzureRM.</span><span class="sxs-lookup"><span data-stu-id="20a64-106">To make the transition easier, Az offers tools to allow you to run your existing scripts using AzureRM.</span></span> <span data-ttu-id="20a64-107">Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="20a64-107">No migration to a new command set is ever convenient, but this article will help you get started on transitioning to the new module.</span></span>

## <a name="ensure-your-existing-scripts-work-with-the-latest-azurerm-release"></a><span data-ttu-id="20a64-108">Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM</span><span class="sxs-lookup"><span data-stu-id="20a64-108">Ensure your existing scripts work with the latest AzureRM release</span></span>

<span data-ttu-id="20a64-109">È il passaggio più importante.</span><span class="sxs-lookup"><span data-stu-id="20a64-109">This is the most important step!</span></span> <span data-ttu-id="20a64-110">Eseguire gli script esistenti e verificarne il funzionamento con l'_ultima_ versione di AzureRM (__6.12.0__).</span><span class="sxs-lookup"><span data-stu-id="20a64-110">Run your existing scripts, and make sure that they work with the _latest_ release of AzureRM (__6.12.0__).</span></span> <span data-ttu-id="20a64-111">Se gli script non funzionano, vedere la [guida alla migrazione per AzureRM](migration-guide.6.0.0.md).</span><span class="sxs-lookup"><span data-stu-id="20a64-111">If your scripts don't work, make sure to read the [AzureRM migration guide](migration-guide.6.0.0.md).</span></span>

## <a name="install-the-azure-powershell-az-module"></a><span data-ttu-id="20a64-112">Installare il modulo Az di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="20a64-112">Install the Azure PowerShell Az module</span></span>

<span data-ttu-id="20a64-113">Il primo passaggio consiste nell'installare il modulo Az nella piattaforma.</span><span class="sxs-lookup"><span data-stu-id="20a64-113">The first step is to install the Az module on your platform.</span></span> <span data-ttu-id="20a64-114">Per installare Az, è necessario disinstallare AzureRM.</span><span class="sxs-lookup"><span data-stu-id="20a64-114">To install Az, you need to uninstall AzureRM.</span></span>
<span data-ttu-id="20a64-115">I passaggi riportati di seguito illustreranno come continuare a eseguire gli script esistenti e abilitare la compatibilità per i nomi dei cmdlet precedenti.</span><span class="sxs-lookup"><span data-stu-id="20a64-115">In the following steps, you'll learn how to keep running your existing scripts and enable compatibility for old cmdlet names.</span></span>

<span data-ttu-id="20a64-116">Per installare il modulo Az di Azure PowerShell, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="20a64-116">To install the Azure PowerShell Az module, follow these steps:</span></span>

* <span data-ttu-id="20a64-117">[Disinstallare il modulo AzureRM](uninstall-azurerm-ps.md).</span><span class="sxs-lookup"><span data-stu-id="20a64-117">[Uninstall the AzureRM module](uninstall-azurerm-ps.md).</span></span> <span data-ttu-id="20a64-118">Assicurarsi di rimuovere _tutte_ le versioni installate di AzureRM, non solo quella più recente.</span><span class="sxs-lookup"><span data-stu-id="20a64-118">Make sure that you remove _all_ installed versions of AzureRM, not just the most recent version.</span></span>
* <span data-ttu-id="20a64-119">[Installare il modulo Az](install-az-ps.md).</span><span class="sxs-lookup"><span data-stu-id="20a64-119">[Install the Az module](install-az-ps.md)</span></span>

## <a name="a-namealiasesenable-azurerm-alias-mode"></a><span data-ttu-id="20a64-120"><a name="aliases"/>Abilitare la modalità alias per AzureRM</span><span class="sxs-lookup"><span data-stu-id="20a64-120"><a name="aliases"/>Enable AzureRM alias mode</span></span>

<span data-ttu-id="20a64-121">Dopo la verifica del funzionamento degli script con l'ultima versione di AzureRM e la disinstallazione di AzureRM, è necessario abilitare la modalità compatibilità per il modulo Az.</span><span class="sxs-lookup"><span data-stu-id="20a64-121">With AzureRM uninstalled and your scripts working with the latest AzureRM version, now is the time to enable the compatibility mode for the Az module.</span></span> <span data-ttu-id="20a64-122">La compatibilità viene abilitata con questo comando:</span><span class="sxs-lookup"><span data-stu-id="20a64-122">Compatibility is enabled with the command:</span></span>

```powershell-interactive
Enable-AzureRmAlias -Scope CurrentUser
```

<span data-ttu-id="20a64-123">Gli alias offrono la possibilità di usare i nomi dei cmdlet precedenti con il modulo `Az` installato.</span><span class="sxs-lookup"><span data-stu-id="20a64-123">Aliases enable the ability to use old cmdlet names with the `Az` module installed.</span></span> <span data-ttu-id="20a64-124">Gli alias vengono scritti nel profilo utente per l'ambito selezionato.</span><span class="sxs-lookup"><span data-stu-id="20a64-124">These aliases are written to the user profile for the selected scope.</span></span> <span data-ttu-id="20a64-125">Se non esistono profili utente, ne viene creato uno.</span><span class="sxs-lookup"><span data-stu-id="20a64-125">If no user profile exists, one is created.</span></span>

> [!WARNING]
>
> <span data-ttu-id="20a64-126">È possibile usare un valore di `-Scope` diverso per il comando, ma non è consigliabile.</span><span class="sxs-lookup"><span data-stu-id="20a64-126">You can use a different `-Scope` for this command, but it's not recommended!</span></span> <span data-ttu-id="20a64-127">Dato che gli alias vengono scritti nel profilo utente per l'ambito selezionato, abilitarli per un ambito il più limitato possibile.</span><span class="sxs-lookup"><span data-stu-id="20a64-127">Aliases are written to the user profile for the selected scope, so keep enabling them to as limited a scope as possible.</span></span> <span data-ttu-id="20a64-128">L'abilitazione degli alias a livello di sistema potrebbe anche causare problemi per altri utenti nel cui ambito locale è installato `AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="20a64-128">Enabling aliases system-wide could also cause issues for other users which have `AzureRM` installed in their local scope.</span></span>

<span data-ttu-id="20a64-129">Dopo aver abilitato la modalità alias, eseguire di nuovo gli script per verificare che continuino a funzionare come previsto.</span><span class="sxs-lookup"><span data-stu-id="20a64-129">Once the alias mode is enabled, run your scripts again to confirm that they still function as expected.</span></span> 

## <a name="change-module-imports-and-cmdlet-names"></a><span data-ttu-id="20a64-130">Modificare i nomi dei cmdlet e le importazioni del modulo</span><span class="sxs-lookup"><span data-stu-id="20a64-130">Change module imports and cmdlet names</span></span>

<span data-ttu-id="20a64-131">In generale, i nomi del modulo e i cmdlet sono stati modificati sostituendo `AzureRM` e `Azure` con `Az`.</span><span class="sxs-lookup"><span data-stu-id="20a64-131">In general, the module names have been changed so that `AzureRM` and `Azure` become `Az`, and the same for cmdlets.</span></span>
<span data-ttu-id="20a64-132">Il modulo `AzureRM.Compute`, ad esempio, è stato rinominato `Az.Compute`.</span><span class="sxs-lookup"><span data-stu-id="20a64-132">For example, the `AzureRM.Compute` module has been renamed to `Az.Compute`.</span></span> <span data-ttu-id="20a64-133">`New-AzureRmVM` è diventato `New-AzVM` e `Get-AzureStorageBlob` è ora `Get-AzStorageBlob`.</span><span class="sxs-lookup"><span data-stu-id="20a64-133">`New-AzureRmVM` has become `New-AzVM`, and `Get-AzureStorageBlob` is now `Get-AzStorageBlob`.</span></span>

<span data-ttu-id="20a64-134">Prima di eseguire qualsiasi ridenominazione è opportuno essere a conoscenza delle eccezioni a tale modifica dei nomi:</span><span class="sxs-lookup"><span data-stu-id="20a64-134">There are exceptions to this naming change that you should be aware of before doing any renaming:</span></span>

| <span data-ttu-id="20a64-135">Modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="20a64-135">AzureRM module</span></span> | <span data-ttu-id="20a64-136">Modulo Az</span><span class="sxs-lookup"><span data-stu-id="20a64-136">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="20a64-137">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="20a64-137">AzureRM.DataFactories</span></span> | <span data-ttu-id="20a64-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20a64-138">Az.DataFactory</span></span> |
| <span data-ttu-id="20a64-139">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="20a64-139">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="20a64-140">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="20a64-140">Az.DataFactory</span></span> |
| <span data-ttu-id="20a64-141">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="20a64-141">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="20a64-142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20a64-142">Az.RecoveryServices</span></span> |
| <span data-ttu-id="20a64-143">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="20a64-143">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="20a64-144">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="20a64-144">Az.RecoveryServices</span></span> |

## <a name="summary"></a><span data-ttu-id="20a64-145">Summary</span><span class="sxs-lookup"><span data-stu-id="20a64-145">Summary</span></span>

<span data-ttu-id="20a64-146">Seguendo questi passaggi è possibile aggiornare tutti gli script esistenti in modo da usare il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="20a64-146">By following these steps, you can update all of your existing scripts to use the new module.</span></span> <span data-ttu-id="20a64-147">In caso di domande o problemi con questi passaggi che hanno reso difficile la migrazione, lasciare un commento su questo articolo per consentire un miglioramento delle istruzioni.</span><span class="sxs-lookup"><span data-stu-id="20a64-147">If you have any questions or problems with these steps that made your migration difficult, please comment on this article so that we can improve the instructions.</span></span>