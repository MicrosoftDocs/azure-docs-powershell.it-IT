---
title: Elenco di tutte le modifiche apportate durante la migrazione da AzureRM ad Azure PowerShell Az 1.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano un'interruzione apportate ad Azure PowerShell nel rilascio della versione Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.openlocfilehash: ea7593cf2b753b210ff2955b7bd450030ad83596
ms.sourcegitcommit: f9445d1525eac8c165637e1a80fbc92b1ab005c2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/16/2019
ms.locfileid: "75035830"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="f4c0c-103">Modifiche che causano un'interruzione per Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f4c0c-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="f4c0c-104">Questo documento include informazioni dettagliate sulle modifiche apportate nella migrazione da AzureRM 6.x al nuovo modulo Az 1.x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="f4c0c-105">Il sommario include tutti i passaggi di un percorso di migrazione completo, incluse le modifiche specifiche dei singoli moduli che potrebbero influire sugli script.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="f4c0c-106">Per consigli di carattere generale su come iniziare una migrazione da AzureRM ad Az, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="f4c0c-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="f4c0c-107">Sommario</span><span class="sxs-lookup"><span data-stu-id="f4c0c-107">Table of Contents</span></span>

- [<span data-ttu-id="f4c0c-108">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="f4c0c-108">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="f4c0c-109">Modifiche apportate al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4c0c-109">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="f4c0c-110">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="f4c0c-110">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="f4c0c-111">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="f4c0c-111">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="f4c0c-112">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f4c0c-112">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="f4c0c-113">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4c0c-113">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="f4c0c-114">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="f4c0c-114">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="f4c0c-115">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="f4c0c-115">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="f4c0c-116">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-116">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="f4c0c-117">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-117">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="f4c0c-118">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-118">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="f4c0c-119">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-119">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="f4c0c-120">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-120">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="f4c0c-121">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-121">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="f4c0c-122">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-122">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="f4c0c-123">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-123">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="f4c0c-124">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-124">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="f4c0c-125">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-125">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="f4c0c-126">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-126">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="f4c0c-127">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-127">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="f4c0c-128">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-128">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="f4c0c-129">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-129">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="f4c0c-130">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-130">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="f4c0c-131">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-131">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="f4c0c-132">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-132">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="f4c0c-133">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-133">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="f4c0c-134">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="f4c0c-134">General breaking changes</span></span>

<span data-ttu-id="f4c0c-135">Questa sezione illustra in dettaglio le modifiche di rilievo di carattere generale incluse nella riprogettazione del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-135">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="f4c0c-136">Modifiche al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="f4c0c-136">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="f4c0c-137">Nel modulo AzureRM come prefisso dei nomi dei cmdlet si usava `AzureRM` o `Azure`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-137">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="f4c0c-138">Az semplifica e normalizza i nomi dei cmdlet, in modo che tutti i cmdlet usino 'Az' come prefisso dei nomi dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-138">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="f4c0c-139">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-139">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="f4c0c-140">È stato modificato in:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-140">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="f4c0c-141">Per semplificare la transizione a questi nuovi nomi dei cmdlet, Az introduce due nuovi cmdlet, ovvero [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) e [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4c0c-141">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="f4c0c-142">`Enable-AzureRmAlias` crea gli alias per i nomi dei cmdlet precedenti in AzureRM per i quali viene eseguito il mapping ai nuovi nomi dei cmdlet Az.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-142">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="f4c0c-143">Se si usa l'argomento `-Scope` con `Enable-AzureRmAlias`, è possibile scegliere dove abilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-143">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="f4c0c-144">Ad esempio, lo script seguente in AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-144">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4c0c-145">Può essere eseguito con modifiche minime usando `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-145">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4c0c-146">L'esecuzione di `Enable-AzureRmAlias -Scope CurrentUser` abilita gli alias per tutte le sessioni di PowerShell che vengono aperte, in modo che dopo l'esecuzione di questo cmdlet non sarà necessario modificare uno script simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-146">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f4c0c-147">Per informazioni dettagliate sull'utilizzo dei cmdlet alias, vedere la [guida di riferimento per Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4c0c-147">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="f4c0c-148">Quando si è pronti per disabilitare gli alias, usare `Disable-AzureRmAlias` per rimuovere gli alias creati.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-148">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="f4c0c-149">Per informazioni dettagliate, vedere la [guida di riferimento per Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="f4c0c-149">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4c0c-150">Quando si disabilitano gli alias, assicurarsi che vengano disabilitati per _tutti_ gli ambiti in cui erano abilitati.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-150">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="f4c0c-151">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="f4c0c-151">Module Name Changes</span></span>

<span data-ttu-id="f4c0c-152">I nomi dei moduli sono stati modificati da `AzureRM.*` a `Az.*`, fatta eccezione per i moduli seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-152">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="f4c0c-153">Modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="f4c0c-153">AzureRM module</span></span> | <span data-ttu-id="f4c0c-154">Modulo Az</span><span class="sxs-lookup"><span data-stu-id="f4c0c-154">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="f4c0c-155">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="f4c0c-155">Azure.Storage</span></span> | <span data-ttu-id="f4c0c-156">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="f4c0c-156">Az.Storage</span></span> |
| <span data-ttu-id="f4c0c-157">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4c0c-157">Azure.AnalysisServices</span></span> | <span data-ttu-id="f4c0c-158">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="f4c0c-158">Az.AnalysisServices</span></span> |
| <span data-ttu-id="f4c0c-159">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="f4c0c-159">AzureRM.Profile</span></span> | <span data-ttu-id="f4c0c-160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="f4c0c-160">Az.Accounts</span></span> |
| <span data-ttu-id="f4c0c-161">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="f4c0c-161">AzureRM.Insights</span></span> | <span data-ttu-id="f4c0c-162">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="f4c0c-162">Az.Monitor</span></span> |
| <span data-ttu-id="f4c0c-163">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="f4c0c-163">AzureRM.DataFactories</span></span> | <span data-ttu-id="f4c0c-164">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4c0c-164">Az.DataFactory</span></span> |
| <span data-ttu-id="f4c0c-165">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f4c0c-165">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="f4c0c-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="f4c0c-166">Az.DataFactory</span></span> |
| <span data-ttu-id="f4c0c-167">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="f4c0c-167">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="f4c0c-168">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4c0c-168">Az.RecoveryServices</span></span> |
| <span data-ttu-id="f4c0c-169">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="f4c0c-169">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="f4c0c-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="f4c0c-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="f4c0c-171">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="f4c0c-171">AzureRM.Tags</span></span> | <span data-ttu-id="f4c0c-172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="f4c0c-172">Az.Resources</span></span> |
| <span data-ttu-id="f4c0c-173">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="f4c0c-173">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="f4c0c-174">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="f4c0c-174">Az.MachineLearning</span></span> |
| <span data-ttu-id="f4c0c-175">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="f4c0c-175">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="f4c0c-176">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4c0c-176">Az.Billing</span></span> |
| <span data-ttu-id="f4c0c-177">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="f4c0c-177">AzureRM.Consumption</span></span> | <span data-ttu-id="f4c0c-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="f4c0c-178">Az.Billing</span></span> |

<span data-ttu-id="f4c0c-179">Le modifiche nei nomi dei moduli significano che tutti gli script che usano `#Requires` o `Import-Module` per caricare moduli specifici dovranno essere modificati per usare il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-179">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="f4c0c-180">Per i moduli in cui il suffisso del cmdlet non è cambiato, anche se il nome del modulo è cambiato il suffisso che indica lo spazio dell'operazione _non_ ha subito variazioni.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-180">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="f4c0c-181">Migrazione delle istruzioni #Requires e Import-Module</span><span class="sxs-lookup"><span data-stu-id="f4c0c-181">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="f4c0c-182">Gli script che usano `#Requires` o `Import-Module` per dichiarare una dipendenza dai moduli AzureRM devono essere aggiornati in modo che usino i nuovi nomi dei moduli.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-182">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="f4c0c-183">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-183">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="f4c0c-184">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-184">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="f4c0c-185">Per `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-185">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="f4c0c-186">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-186">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="f4c0c-187">Migrazione delle chiamate dei cmdlet complete</span><span class="sxs-lookup"><span data-stu-id="f4c0c-187">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="f4c0c-188">Gli script che usano le chiamate dei cmdlet qualificate di modulo, come:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-188">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="f4c0c-189">Devono essere modificati in modo che usino i nuovi nomi dei moduli e dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-189">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="f4c0c-190">Migrazione delle dipendenze del manifesto del modulo</span><span class="sxs-lookup"><span data-stu-id="f4c0c-190">Migrating module manifest dependencies</span></span>

<span data-ttu-id="f4c0c-191">I moduli che esprimono le dipendenze dai moduli AzureRM tramite un file del manifesto del modulo (con estensione psd1) dovranno aggiornare i nomi dei moduli nella sezione `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-191">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="f4c0c-192">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-192">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="f4c0c-193">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="f4c0c-193">Removed modules</span></span>

<span data-ttu-id="f4c0c-194">I moduli seguenti sono stati rimossi:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-194">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="f4c0c-195">Gli strumenti per questi servizi non sono più supportati attivamente.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-195">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="f4c0c-196">I clienti sono invitati a passare a servizi alternativi non appena possibile.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-196">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="f4c0c-197">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f4c0c-197">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="f4c0c-198">Per usare Az con PowerShell 5.1 per Windows è richiesta l'installazione di .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-198">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="f4c0c-199">Se invece si usa PowerShell Core 6.x o versioni successive, .NET Framework non è richiesto.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-199">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="f4c0c-200">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4c0c-200">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="f4c0c-201">A causa delle modifiche nel flusso di autenticazione per .NET Standard verrà temporaneamente rimosso l'accesso utente tramite PSCredential.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-201">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="f4c0c-202">Questa funzionalità sarà reintrodotta nella versione del 15/01/2019 per PowerShell 5.1 per Windows.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-202">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="f4c0c-203">Questa modifica è descritta in dettaglio in [questo problema di GitHub](https://github.com/Azure/azure-powershell/issues/7430).</span><span class="sxs-lookup"><span data-stu-id="f4c0c-203">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="f4c0c-204">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="f4c0c-204">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="f4c0c-205">A causa delle modifiche nel flusso di autenticazione per .NET Standard, viene usato l'accesso del dispositivo come flusso di accesso predefinito durante l'accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-205">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="f4c0c-206">L'accesso basato su Web browser verrà reintrodotto per PowerShell 5.1 per Windows come impostazione predefinita nella versione del 15/01/2019.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-206">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="f4c0c-207">A quel punto, gli utenti potranno scegliere l'accesso del dispositivo usando un parametro Switch.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-207">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="f4c0c-208">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="f4c0c-208">Module breaking changes</span></span>

<span data-ttu-id="f4c0c-209">Questa sezione illustra in dettaglio le modifiche di rilievo per singoli cmdlet e moduli.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-209">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="f4c0c-210">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-210">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="f4c0c-211">Sono stati rimossi i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-211">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="f4c0c-212">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4c0c-212">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="f4c0c-213">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f4c0c-213">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="f4c0c-214">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f4c0c-214">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="f4c0c-215">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c0c-215">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="f4c0c-216">Usare il cmdlet **Set-AzApiManagement** per impostare queste proprietà</span><span class="sxs-lookup"><span data-stu-id="f4c0c-216">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="f4c0c-217">Sono state rimosse le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-217">Removed the following properties:</span></span>
  - <span data-ttu-id="f4c0c-218">Sono state rimosse le proprietà `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` di tipo `PsApiManagementHostnameConfiguration` da `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-218">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="f4c0c-219">Usare `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` di tipo `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-219">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="f4c0c-220">È stata rimossa la proprietà `StaticIPs` da PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-220">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="f4c0c-221">La proprietà è stata suddivisa in `PublicIPAddresses` e `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-221">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="f4c0c-222">È stata rimossa la proprietà obbligatoria `Location` dal cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-222">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="f4c0c-223">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-223">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="f4c0c-224">Il parametro `InvoiceName` è stato rimosso dal cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-224">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="f4c0c-225">Gli script dovranno usare altri parametri di identità per la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-225">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="f4c0c-226">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-226">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="f4c0c-227">È stato rimosso il set di parametri `GetSkusWithAccountParamSetName` dal cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-227">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="f4c0c-228">È necessario ottenere gli SKU per tipo di account e posizione, anziché usare ResourceGroupName e nome account.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-228">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="f4c0c-229">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-229">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="f4c0c-230">`IdentityIds` è stato rimosso dalla proprietà `Identity` negli oggetti `PSVirtualMachine` e `PSVirtualMachineScaleSet`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-230">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="f4c0c-231">Il tipo della proprietà `InstanceView` dell'oggetto `PSVirtualMachineScaleSetVM` è stato modificato da `VirtualMachineInstanceView` a `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-231">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="f4c0c-232">Le proprietà `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` sono state rimosse dalla proprietà `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-232">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="f4c0c-233">Il tipo della proprietà `Sku` nell'oggetto `PSSnapshotUpdate` è stato modificato da `DiskSku` a `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-233">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="f4c0c-234">`VmScaleSetVMParameterSet` è stato rimosso dal cmdlet `Add-AzVMDataDisk`. Non è più possibile aggiungere singolarmente un disco dati a una macchina virtuale del set di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-234">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="f4c0c-235">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-235">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="f4c0c-236">Il parametro `GatewayName` è diventato obbligatorio nel cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-236">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="f4c0c-237">È stato rimosso il cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-237">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="f4c0c-238">È stato rimosso il parametro `LinkedServiceName` dal cmdlet `Get-AzDataFactoryV2ActivityRun`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-238">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="f4c0c-239">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-239">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="f4c0c-240">Sono stati rimossi i cmdlet deprecati: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` e `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-240">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="f4c0c-241">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-241">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="f4c0c-242">Il tipo del parametro `Encoding` dei cmdlet seguenti è stato modificato da `FileSystemCmdletProviderEncoding` a `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-242">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="f4c0c-243">Questa modifica rimuove i valori di codifica `String` e `Oem`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-243">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="f4c0c-244">Tutti gli altri valori di codifica precedenti rimangono.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-244">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="f4c0c-245">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4c0c-245">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="f4c0c-246">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f4c0c-246">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="f4c0c-247">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f4c0c-247">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="f4c0c-248">È stato rimosso l'alias della proprietà `Tags` deprecata dai cmdlet `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-248">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="f4c0c-249">Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f4c0c-249">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f4c0c-250">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f4c0c-250">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="f4c0c-251">Sono state rimosse le proprietà deprecate `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` dall'oggetto `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-251">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="f4c0c-252">Tutti gli script che usano `PSDatalakeStoreAccount` restituito da `Get-AzDataLakeStoreAccount` non devono fare riferimento a queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-252">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="f4c0c-253">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-253">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="f4c0c-254">La proprietà `PurgeDisabled` è stata rimossa dagli oggetti `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes`. Gli script non devono più fare riferimento alla proprietà ```PurgeDisabled``` per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-254">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="f4c0c-255">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-255">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="f4c0c-256">È stato rimosso l'alias della proprietà `Tags` deprecata dal cmdlet `New-AzMediaService`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f4c0c-256">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f4c0c-257">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f4c0c-257">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="f4c0c-258">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-258">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="f4c0c-259">Sono stati rimossi i nomi plurali del parametro `Categories` e `Timegrains` sostituendoli con nomi di parametro singolari dal cmdlet `Set-AzDiagnosticSetting`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f4c0c-259">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="f4c0c-260">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f4c0c-260">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="f4c0c-261">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-261">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="f4c0c-262">È stato rimosso il parametro `ResourceId` deprecato dal cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-262">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="f4c0c-263">È stata rimossa la proprietà `EnableVmProtection` deprecata dall'oggetto `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-263">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="f4c0c-264">È stato rimosso il cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` deprecato</span><span class="sxs-lookup"><span data-stu-id="f4c0c-264">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="f4c0c-265">Gli script non devono più prendere decisioni di elaborazione in base ai valori di questi campi.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-265">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="f4c0c-266">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-266">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="f4c0c-267">Il set di parametri predefinito per `Get-AzOperationalInsightsDataSource` è stato rimosso e `ByWorkspaceNameByKind` è diventato il set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="f4c0c-267">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="f4c0c-268">Gli script che elencano le origini dati usando</span><span class="sxs-lookup"><span data-stu-id="f4c0c-268">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="f4c0c-269">Devono essere modificati per specificare un tipo</span><span class="sxs-lookup"><span data-stu-id="f4c0c-269">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f4c0c-270">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-270">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="f4c0c-271">È stato rimosso il parametro `Encryption` dal cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-271">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="f4c0c-272">Il parametro `TargetStorageAccountName` è ora obbligatorio per il ripristino dei dischi gestiti nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-272">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f4c0c-273">Sono stati rimossi i parametri `StorageAccountName` e `StorageAccountResourceGroupName` nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-273">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f4c0c-274">È stato rimosso il parametro `Name` nel cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-274">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="f4c0c-275">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-275">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="f4c0c-276">È stato rimosso il parametro `Sku` dal cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-276">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="f4c0c-277">È stato rimosso il parametro `Password` dal cmdlet `New-AzADServicePrincipal` e `New-AzADSpCredential`. Le password vengono generate automaticamente e gli script che fornivano la password:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-277">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="f4c0c-278">Devono essere modificati per recuperare la password dall'output:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-278">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="f4c0c-279">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-279">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="f4c0c-280">Sono stati modificati i tipi restituiti di cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-280">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="f4c0c-281">La proprietà `ServiceTypeHealthPolicies` di tipo `ApplicationHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-281">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f4c0c-282">La proprietà `ApplicationHealthPolicies` di tipo `ClusterUpgradeDeltaHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-282">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f4c0c-283">La proprietà `OverrideUserUpgradePolicy` di tipo `ClusterUpgradePolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-283">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="f4c0c-284">Queste modifiche interessano i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-284">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="f4c0c-285">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c0c-285">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f4c0c-286">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c0c-286">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f4c0c-287">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f4c0c-287">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f4c0c-288">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f4c0c-288">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f4c0c-289">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f4c0c-289">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="f4c0c-290">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c0c-290">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f4c0c-291">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f4c0c-291">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f4c0c-292">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f4c0c-292">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f4c0c-293">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f4c0c-293">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f4c0c-294">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f4c0c-294">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f4c0c-295">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f4c0c-295">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f4c0c-296">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f4c0c-296">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="f4c0c-297">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="f4c0c-297">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="f4c0c-298">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f4c0c-298">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="f4c0c-299">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-299">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="f4c0c-300">Sono stati rimossi i parametri `State` e `ResourceId` dal cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-300">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f4c0c-301">Sono stati rimossi i cmdlet deprecati: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-301">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="f4c0c-302">È stato rimosso il parametro `Current` deprecato dal cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-302">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f4c0c-303">È stato rimosso il parametro `DatabaseName` deprecato dal cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-303">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="f4c0c-304">È stato rimosso il parametro `PrivilegedLogin` deprecato dal cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-304">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="f4c0c-305">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-305">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="f4c0c-306">Per supportare la creazione di un contesto di archiviazione Oauth con solo il nome dell'account di archiviazione, il set di parametri predefinito è stato modificato in `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-306">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="f4c0c-307">Esempio: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-307">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="f4c0c-308">Il parametro `Location` è diventato obbligatorio nel cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-308">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="f4c0c-309">I metodi dell'API di archiviazione usano ora il Modello asincrono basato su attività (TAP), invece delle chiamate API sincrone.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-309">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="f4c0c-310">Gli esempi seguenti illustrano i nuovi comandi asincroni:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-310">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="f4c0c-311">Snapshot del BLOB</span><span class="sxs-lookup"><span data-stu-id="f4c0c-311">Blob Snapshot</span></span>

<span data-ttu-id="f4c0c-312">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-312">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="f4c0c-313">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-313">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="f4c0c-314">Snapshot di condivisione</span><span class="sxs-lookup"><span data-stu-id="f4c0c-314">Share Snapshot</span></span>

<span data-ttu-id="f4c0c-315">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-315">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="f4c0c-316">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-316">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="f4c0c-317">Annullare l'eliminazione del BLOB eliminato temporaneamente</span><span class="sxs-lookup"><span data-stu-id="f4c0c-317">Undelete soft-deleted blob</span></span>

<span data-ttu-id="f4c0c-318">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-318">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="f4c0c-319">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-319">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="f4c0c-320">Impostare il livello di BLOB</span><span class="sxs-lookup"><span data-stu-id="f4c0c-320">Set Blob Tier</span></span>

<span data-ttu-id="f4c0c-321">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-321">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="f4c0c-322">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="f4c0c-322">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="f4c0c-323">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f4c0c-323">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="f4c0c-324">Sono state rimosse le proprietà deprecate dagli oggetti `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite`</span><span class="sxs-lookup"><span data-stu-id="f4c0c-324">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
