---
title: Elenco di tutte le modifiche apportate durante la migrazione da AzureRM ad Azure PowerShell Az 1.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano un'interruzione apportate ad Azure PowerShell nel rilascio della versione Az 1.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 3ab12307f786c12422338835926802793a33713e
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407343"
---
# <a name="breaking-changes-for-az-100"></a><span data-ttu-id="9b373-103">Modifiche che causano un'interruzione per Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="9b373-103">Breaking changes for Az 1.0.0</span></span>

<span data-ttu-id="9b373-104">Questo documento include informazioni dettagliate sulle modifiche apportate nella migrazione da AzureRM 6.x al nuovo modulo Az 1.x e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="9b373-104">This document provides detailed information on the changes between AzureRM 6.x and the new Az module, version 1.x and later.</span></span> <span data-ttu-id="9b373-105">Il sommario include tutti i passaggi di un percorso di migrazione completo, incluse le modifiche specifiche dei singoli moduli che potrebbero influire sugli script.</span><span class="sxs-lookup"><span data-stu-id="9b373-105">The table of contents will help guide you through a full migration path, including module-specific changes that may affect your scripts.</span></span>

<span data-ttu-id="9b373-106">Per consigli di carattere generale su come iniziare una migrazione da AzureRM ad Az, vedere [Eseguire la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).</span><span class="sxs-lookup"><span data-stu-id="9b373-106">For general advice on getting started with a migration from AzureRM to Az, see [Start migration from AzureRM to Az](migrate-from-azurerm-to-az.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b373-107">Sono state apportate modifiche di rilievo anche tra le versioni 1.0.0 e 2.0.0 di Az.</span><span class="sxs-lookup"><span data-stu-id="9b373-107">There have been breaking changes between Az 1.0.0 and Az 2.0.0 as well.</span></span> <span data-ttu-id="9b373-108">Dopo aver seguito le indicazioni di questa guida per eseguire l'aggiornamento da AzureRM ad Az, vedere l'[elenco delle modifiche di rilievo di Az 2.0.0](migrate-az-2.0.0.md) per sapere se sono necessarie ulteriori modifiche.</span><span class="sxs-lookup"><span data-stu-id="9b373-108">After following this guide for updating from AzureRM to Az, see the [Az 2.0.0 breaking changes](migrate-az-2.0.0.md) to find out if you need to make additional changes.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="9b373-109">Sommario</span><span class="sxs-lookup"><span data-stu-id="9b373-109">Table of Contents</span></span>

- [<span data-ttu-id="9b373-110">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="9b373-110">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="9b373-111">Modifiche apportate al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b373-111">Cmdlet noun prefix changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="9b373-112">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="9b373-112">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="9b373-113">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="9b373-113">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="9b373-114">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="9b373-114">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="9b373-115">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="9b373-115">Temporary removal of user login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="9b373-116">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="9b373-116">Default device code login instead of web browser prompt</span></span>](#default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="9b373-117">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="9b373-117">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="9b373-118">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="9b373-118">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="9b373-119">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="9b373-119">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="9b373-120">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="9b373-120">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="9b373-121">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="9b373-121">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="9b373-122">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="9b373-122">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="9b373-123">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="9b373-123">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="9b373-124">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="9b373-124">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="9b373-125">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="9b373-125">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="9b373-126">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="9b373-126">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="9b373-127">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="9b373-127">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="9b373-128">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="9b373-128">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="9b373-129">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="9b373-129">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="9b373-130">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="9b373-130">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="9b373-131">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="9b373-131">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="9b373-132">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="9b373-132">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="9b373-133">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="9b373-133">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="9b373-134">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="9b373-134">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="9b373-135">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="9b373-135">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="9b373-136">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="9b373-136">General breaking changes</span></span>

<span data-ttu-id="9b373-137">Questa sezione illustra in dettaglio le modifiche di rilievo di carattere generale incluse nella riprogettazione del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="9b373-137">This section details the general breaking changes that are part of the redesign of the Az module.</span></span>

### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="9b373-138">Modifiche al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b373-138">Cmdlet Noun Prefix Changes</span></span>

<span data-ttu-id="9b373-139">Nel modulo AzureRM come prefisso dei nomi dei cmdlet si usava `AzureRM` o `Azure`.</span><span class="sxs-lookup"><span data-stu-id="9b373-139">In the AzureRM module, cmdlets used either `AzureRM` or `Azure` as a noun prefix.</span></span>  <span data-ttu-id="9b373-140">Az semplifica e normalizza i nomi dei cmdlet, in modo che tutti i cmdlet usino 'Az' come prefisso dei nomi dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b373-140">Az simplifies and normalizes cmdlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="9b373-141">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9b373-141">For example:</span></span>

```azurepowershell-interactive
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="9b373-142">È stato modificato in:</span><span class="sxs-lookup"><span data-stu-id="9b373-142">Has changed to:</span></span>

```azurepowershell-interactive
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="9b373-143">Per semplificare la transizione a questi nuovi nomi dei cmdlet, Az introduce due nuovi cmdlet, ovvero [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) e [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="9b373-143">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias) and [Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span></span>  <span data-ttu-id="9b373-144">`Enable-AzureRmAlias` crea gli alias per i nomi dei cmdlet precedenti in AzureRM per i quali viene eseguito il mapping ai nuovi nomi dei cmdlet Az.</span><span class="sxs-lookup"><span data-stu-id="9b373-144">`Enable-AzureRmAlias` creates aliases for the older cmdlet names in AzureRM that map to the newer Az cmdlet names.</span></span> <span data-ttu-id="9b373-145">Se si usa l'argomento `-Scope` con `Enable-AzureRmAlias`, è possibile scegliere dove abilitare gli alias.</span><span class="sxs-lookup"><span data-stu-id="9b373-145">Using the `-Scope` argument with `Enable-AzureRmAlias` allows you to choose where aliases are enabled.</span></span>

<span data-ttu-id="9b373-146">Ad esempio, lo script seguente in AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9b373-146">For example, the following script in AzureRM:</span></span>

```azurepowershell-interactive
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="9b373-147">Può essere eseguito con modifiche minime usando `Enable-AzureRmAlias`:</span><span class="sxs-lookup"><span data-stu-id="9b373-147">Can be run with minimal changes using `Enable-AzureRmAlias`:</span></span>

```azurepowershell-interactive
#Requires -Modules Az.Storage
Enable-AzureRmAlias -Scope Process
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="9b373-148">L'esecuzione di `Enable-AzureRmAlias -Scope CurrentUser` abilita gli alias per tutte le sessioni di PowerShell che vengono aperte, in modo che dopo l'esecuzione di questo cmdlet non sarà necessario modificare uno script simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="9b373-148">Running `Enable-AzureRmAlias -Scope CurrentUser` will enable the aliases for all PowerShell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>

```azurepowershell-interactive
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="9b373-149">Per informazioni dettagliate sull'utilizzo dei cmdlet alias, vedere la [guida di riferimento per Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="9b373-149">For complete details on the usage of the alias cmdlets, see the [Enable-AzureRmAlias reference](/powershell/module/az.accounts/enable-azurermalias).</span></span>

<span data-ttu-id="9b373-150">Quando si è pronti per disabilitare gli alias, usare `Disable-AzureRmAlias` per rimuovere gli alias creati.</span><span class="sxs-lookup"><span data-stu-id="9b373-150">When you're ready to disable aliases, `Disable-AzureRmAlias` removes the created aliases.</span></span> <span data-ttu-id="9b373-151">Per informazioni dettagliate, vedere la [guida di riferimento per Disable-AzureRmAlias](/powershell/module/az.accounts/disable-azurermalias).</span><span class="sxs-lookup"><span data-stu-id="9b373-151">For complete details, see the [Disable-AzureRmAlias reference](/powershell/module/az.accounts/disable-azurermalias).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b373-152">Quando si disabilitano gli alias, assicurarsi che vengano disabilitati per _tutti_ gli ambiti in cui erano abilitati.</span><span class="sxs-lookup"><span data-stu-id="9b373-152">When disabling aliases, make sure that they are disabled for _all_ scopes which had aliases enabled.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="9b373-153">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="9b373-153">Module Name Changes</span></span>

<span data-ttu-id="9b373-154">I nomi dei moduli sono stati modificati da `AzureRM.*` a `Az.*`, fatta eccezione per i moduli seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b373-154">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>

| <span data-ttu-id="9b373-155">Modulo AzureRM</span><span class="sxs-lookup"><span data-stu-id="9b373-155">AzureRM module</span></span> | <span data-ttu-id="9b373-156">Modulo Az</span><span class="sxs-lookup"><span data-stu-id="9b373-156">Az module</span></span> |
|----------------|-----------|
| <span data-ttu-id="9b373-157">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="9b373-157">Azure.Storage</span></span> | <span data-ttu-id="9b373-158">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="9b373-158">Az.Storage</span></span> |
| <span data-ttu-id="9b373-159">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9b373-159">Azure.AnalysisServices</span></span> | <span data-ttu-id="9b373-160">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="9b373-160">Az.AnalysisServices</span></span> |
| <span data-ttu-id="9b373-161">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="9b373-161">AzureRM.Profile</span></span> | <span data-ttu-id="9b373-162">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="9b373-162">Az.Accounts</span></span> |
| <span data-ttu-id="9b373-163">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="9b373-163">AzureRM.Insights</span></span> | <span data-ttu-id="9b373-164">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="9b373-164">Az.Monitor</span></span> |
| <span data-ttu-id="9b373-165">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="9b373-165">AzureRM.DataFactories</span></span> | <span data-ttu-id="9b373-166">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b373-166">Az.DataFactory</span></span> |
| <span data-ttu-id="9b373-167">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="9b373-167">AzureRM.DataFactoryV2</span></span> | <span data-ttu-id="9b373-168">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="9b373-168">Az.DataFactory</span></span> |
| <span data-ttu-id="9b373-169">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="9b373-169">AzureRM.RecoveryServices.Backup</span></span> | <span data-ttu-id="9b373-170">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9b373-170">Az.RecoveryServices</span></span> |
| <span data-ttu-id="9b373-171">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="9b373-171">AzureRM.RecoveryServices.SiteRecovery</span></span> | <span data-ttu-id="9b373-172">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="9b373-172">Az.RecoveryServices</span></span> |
| <span data-ttu-id="9b373-173">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="9b373-173">AzureRM.Tags</span></span> | <span data-ttu-id="9b373-174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="9b373-174">Az.Resources</span></span> |
| <span data-ttu-id="9b373-175">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="9b373-175">AzureRM.MachineLearningCompute</span></span> | <span data-ttu-id="9b373-176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="9b373-176">Az.MachineLearning</span></span> |
| <span data-ttu-id="9b373-177">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="9b373-177">AzureRM.UsageAggregates</span></span> | <span data-ttu-id="9b373-178">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9b373-178">Az.Billing</span></span> |
| <span data-ttu-id="9b373-179">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="9b373-179">AzureRM.Consumption</span></span> | <span data-ttu-id="9b373-180">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="9b373-180">Az.Billing</span></span> |

<span data-ttu-id="9b373-181">Le modifiche nei nomi dei moduli significano che tutti gli script che usano `#Requires` o `Import-Module` per caricare moduli specifici dovranno essere modificati per usare il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="9b373-181">The changes in module names mean that any script that uses `#Requires` or `Import-Module` to load specific modules will need to be changed to use the new module instead.</span></span> <span data-ttu-id="9b373-182">Per i moduli in cui il suffisso del cmdlet non è cambiato, anche se il nome del modulo è cambiato il suffisso che indica lo spazio dell'operazione _non_ ha subito variazioni.</span><span class="sxs-lookup"><span data-stu-id="9b373-182">For modules where the cmdlet suffix has not changed, this means that although the module name has changed, the suffix indicating the operation space has _not_.</span></span>

#### <a name="migrating-requires-and-import-module-statements"></a><span data-ttu-id="9b373-183">Migrazione delle istruzioni #Requires e Import-Module</span><span class="sxs-lookup"><span data-stu-id="9b373-183">Migrating #Requires and Import-Module Statements</span></span>

<span data-ttu-id="9b373-184">Gli script che usano `#Requires` o `Import-Module` per dichiarare una dipendenza dai moduli AzureRM devono essere aggiornati in modo che usino i nuovi nomi dei moduli.</span><span class="sxs-lookup"><span data-stu-id="9b373-184">Scripts that use `#Requires` or `Import-Module` to declare a dependency on AzureRM modules must be updated to use the new module names.</span></span> <span data-ttu-id="9b373-185">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="9b373-185">For example:</span></span>

```azurepowershell-interactive
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="9b373-186">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="9b373-186">Should be changed to:</span></span>

```azurepowershell-interactive
#Requires -Module Az.Compute
```

<span data-ttu-id="9b373-187">Per `Import-Module`:</span><span class="sxs-lookup"><span data-stu-id="9b373-187">For `Import-Module`:</span></span>

```azurepowershell-interactive
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="9b373-188">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="9b373-188">Should be changed to:</span></span>

```azurepowershell-interactive
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="9b373-189">Migrazione delle chiamate dei cmdlet complete</span><span class="sxs-lookup"><span data-stu-id="9b373-189">Migrating Fully-Qualified Cmdlet Invocations</span></span>

<span data-ttu-id="9b373-190">Gli script che usano le chiamate dei cmdlet qualificate di modulo, come:</span><span class="sxs-lookup"><span data-stu-id="9b373-190">Scripts that use module-qualified cmdlet invocations, such as:</span></span>

```azurepowershell-interactive
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="9b373-191">Devono essere modificati in modo che usino i nuovi nomi dei moduli e dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="9b373-191">Must be changed to use the new module and cmdlet names:</span></span>

```azurepowershell-interactive
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="9b373-192">Migrazione delle dipendenze del manifesto del modulo</span><span class="sxs-lookup"><span data-stu-id="9b373-192">Migrating module manifest dependencies</span></span>

<span data-ttu-id="9b373-193">I moduli che esprimono le dipendenze dai moduli AzureRM tramite un file del manifesto del modulo (con estensione psd1) dovranno aggiornare i nomi dei moduli nella sezione `RequiredModules`:</span><span class="sxs-lookup"><span data-stu-id="9b373-193">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their `RequiredModules` section:</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="9b373-194">Devono essere modificati in:</span><span class="sxs-lookup"><span data-stu-id="9b373-194">Must be changed to:</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="9b373-195">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="9b373-195">Removed modules</span></span>

<span data-ttu-id="9b373-196">I moduli seguenti sono stati rimossi:</span><span class="sxs-lookup"><span data-stu-id="9b373-196">The following modules have been removed:</span></span>

- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="9b373-197">Gli strumenti per questi servizi non sono più supportati attivamente.</span><span class="sxs-lookup"><span data-stu-id="9b373-197">The tools for these services are no longer actively supported.</span></span>  <span data-ttu-id="9b373-198">I clienti sono invitati a passare a servizi alternativi non appena possibile.</span><span class="sxs-lookup"><span data-stu-id="9b373-198">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="9b373-199">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="9b373-199">Windows PowerShell 5.1 and .NET 4.7.2</span></span>

<span data-ttu-id="9b373-200">Per usare Az con PowerShell 5.1 per Windows è richiesta l'installazione di .NET Framework 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="9b373-200">Using Az with PowerShell 5.1 for Windows requires the installation of .NET Framework 4.7.2.</span></span> <span data-ttu-id="9b373-201">Se invece si usa PowerShell Core 6.x o versioni successive, .NET Framework non è richiesto.</span><span class="sxs-lookup"><span data-stu-id="9b373-201">Using PowerShell Core 6.x or later does not require .NET Framework.</span></span>

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="9b373-202">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="9b373-202">Temporary removal of User login using PSCredential</span></span>

<span data-ttu-id="9b373-203">A causa delle modifiche nel flusso di autenticazione per .NET Standard verrà temporaneamente rimosso l'accesso utente tramite PSCredential.</span><span class="sxs-lookup"><span data-stu-id="9b373-203">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="9b373-204">Questa funzionalità sarà reintrodotta nella versione del 15/01/2019 per PowerShell 5.1 per Windows.</span><span class="sxs-lookup"><span data-stu-id="9b373-204">This capability will be re-introduced in the 1/15/2019 release for PowerShell 5.1 for Windows.</span></span> <span data-ttu-id="9b373-205">Questa modifica è descritta in dettaglio in [questo problema di GitHub](https://github.com/Azure/azure-powershell/issues/7430).</span><span class="sxs-lookup"><span data-stu-id="9b373-205">This is discussed in detail in [this GitHub issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="9b373-206">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="9b373-206">Default device code login instead of web browser prompt</span></span>

<span data-ttu-id="9b373-207">A causa delle modifiche nel flusso di autenticazione per .NET Standard, viene usato l'accesso del dispositivo come flusso di accesso predefinito durante l'accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="9b373-207">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="9b373-208">L'accesso basato su Web browser verrà reintrodotto per PowerShell 5.1 per Windows come impostazione predefinita nella versione del 15/01/2019.</span><span class="sxs-lookup"><span data-stu-id="9b373-208">Web browser based login will be re-introduced for PowerShell 5.1 for Windows as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="9b373-209">A quel punto, gli utenti potranno scegliere l'accesso del dispositivo usando un parametro Switch.</span><span class="sxs-lookup"><span data-stu-id="9b373-209">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="9b373-210">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="9b373-210">Module breaking changes</span></span>

<span data-ttu-id="9b373-211">Questa sezione illustra in dettaglio le modifiche di rilievo per singoli cmdlet e moduli.</span><span class="sxs-lookup"><span data-stu-id="9b373-211">This section details specific breaking changes for individual modules and cmdlets.</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="9b373-212">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="9b373-212">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>

- <span data-ttu-id="9b373-213">Sono stati rimossi i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b373-213">Removed the following cmdlets:</span></span>
  - <span data-ttu-id="9b373-214">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9b373-214">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="9b373-215">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="9b373-215">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="9b373-216">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="9b373-216">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="9b373-217">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="9b373-217">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="9b373-218">Usare il cmdlet **Set-AzApiManagement** per impostare queste proprietà</span><span class="sxs-lookup"><span data-stu-id="9b373-218">Use **Set-AzApiManagement** cmdlet to set these properties instead</span></span>
- <span data-ttu-id="9b373-219">Sono state rimosse le proprietà seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b373-219">Removed the following properties:</span></span>
  - <span data-ttu-id="9b373-220">Sono state rimosse le proprietà `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` di tipo `PsApiManagementHostnameConfiguration` da `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="9b373-220">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="9b373-221">Usare `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` di tipo `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="9b373-221">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="9b373-222">È stata rimossa la proprietà `StaticIPs` da PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9b373-222">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="9b373-223">La proprietà è stata suddivisa in `PublicIPAddresses` e `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="9b373-223">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="9b373-224">È stata rimossa la proprietà obbligatoria `Location` dal cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="9b373-224">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="9b373-225">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="9b373-225">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>

- <span data-ttu-id="9b373-226">Il parametro `InvoiceName` è stato rimosso dal cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="9b373-226">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="9b373-227">Gli script dovranno usare altri parametri di identità per la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="9b373-227">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="9b373-228">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="9b373-228">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>

- <span data-ttu-id="9b373-229">È stato rimosso il set di parametri `GetSkusWithAccountParamSetName` dal cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="9b373-229">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="9b373-230">È necessario ottenere gli SKU per tipo di account e posizione, anziché usare ResourceGroupName e nome account.</span><span class="sxs-lookup"><span data-stu-id="9b373-230">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="9b373-231">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="9b373-231">Az.Compute (previously AzureRM.Compute)</span></span>

- <span data-ttu-id="9b373-232">`IdentityIds` è stato rimosso dalla proprietà `Identity` negli oggetti `PSVirtualMachine` e `PSVirtualMachineScaleSet`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9b373-232">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="9b373-233">Il tipo della proprietà `InstanceView` dell'oggetto `PSVirtualMachineScaleSetVM` è stato modificato da `VirtualMachineInstanceView` a `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="9b373-233">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="9b373-234">Le proprietà `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` sono state rimosse dalla proprietà `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="9b373-234">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="9b373-235">Il tipo della proprietà `Sku` nell'oggetto `PSSnapshotUpdate` è stato modificato da `DiskSku` a `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="9b373-235">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="9b373-236">`VmScaleSetVMParameterSet` è stato rimosso dal cmdlet `Add-AzVMDataDisk`. Non è più possibile aggiungere singolarmente un disco dati a una macchina virtuale del set di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="9b373-236">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you can no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="9b373-237">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="9b373-237">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>

- <span data-ttu-id="9b373-238">Il parametro `GatewayName` è diventato obbligatorio nel cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="9b373-238">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="9b373-239">È stato rimosso il cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="9b373-239">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="9b373-240">È stato rimosso il parametro `LinkedServiceName` dal cmdlet `Get-AzDataFactoryV2ActivityRun`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9b373-240">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="9b373-241">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="9b373-241">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>

- <span data-ttu-id="9b373-242">Sono stati rimossi i cmdlet deprecati: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` e `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="9b373-242">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="9b373-243">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="9b373-243">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>

- <span data-ttu-id="9b373-244">Il tipo del parametro `Encoding` dei cmdlet seguenti è stato modificato da `FileSystemCmdletProviderEncoding` a `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="9b373-244">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="9b373-245">Questa modifica rimuove i valori di codifica `String` e `Oem`.</span><span class="sxs-lookup"><span data-stu-id="9b373-245">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="9b373-246">Tutti gli altri valori di codifica precedenti rimangono.</span><span class="sxs-lookup"><span data-stu-id="9b373-246">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="9b373-247">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9b373-247">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="9b373-248">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="9b373-248">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="9b373-249">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="9b373-249">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="9b373-250">È stato rimosso l'alias della proprietà `Tags` deprecata dai cmdlet `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="9b373-250">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="9b373-251">Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="9b373-251">Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="9b373-252">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="9b373-252">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="9b373-253">Sono state rimosse le proprietà deprecate `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` dall'oggetto `PSDataLakeStoreAccountBasic`.</span><span class="sxs-lookup"><span data-stu-id="9b373-253">Removed deprecated properties `Identity`, `EncryptionState`, `EncryptionProvisioningState`, `EncryptionConfig`, `FirewallState`, `FirewallRules`, `VirtualNetworkRules`, `TrustedIdProviderState`, `TrustedIdProviders`, `DefaultGroup`, `NewTier`, `CurrentTier`, `FirewallAllowAzureIps` from `PSDataLakeStoreAccountBasic` object.</span></span>  <span data-ttu-id="9b373-254">Tutti gli script che usano `PSDatalakeStoreAccount` restituito da `Get-AzDataLakeStoreAccount` non devono fare riferimento a queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="9b373-254">Any script that uses the `PSDatalakeStoreAccount` returned from `Get-AzDataLakeStoreAccount` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="9b373-255">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="9b373-255">Az.KeyVault (previously AzureRM.KeyVault)</span></span>

- <span data-ttu-id="9b373-256">La proprietà `PurgeDisabled` è stata rimossa dagli oggetti `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes`. Gli script non devono più fare riferimento alla proprietà ```PurgeDisabled``` per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="9b373-256">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts should no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="9b373-257">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="9b373-257">Az.Media (previously AzureRM.Media)</span></span>

- <span data-ttu-id="9b373-258">È stato rimosso l'alias della proprietà `Tags` deprecata dal cmdlet `New-AzMediaService`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="9b373-258">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="9b373-259">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="9b373-259">Should be changed to</span></span>
  ```azurepowershell-interactive
  New-AzMediaService -Tag @{TagName="TagValue"}
  ```

### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="9b373-260">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="9b373-260">Az.Monitor (previously AzureRM.Insights)</span></span>

- <span data-ttu-id="9b373-261">Sono stati rimossi i nomi plurali del parametro `Categories` e `Timegrains` sostituendoli con nomi di parametro singolari dal cmdlet `Set-AzDiagnosticSetting`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="9b373-261">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```azurepowershell-interactive
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="9b373-262">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="9b373-262">Should be changed to</span></span>
  ```azurepowershell-interactive
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```

### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="9b373-263">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="9b373-263">Az.Network (previously AzureRM.Network)</span></span>

- <span data-ttu-id="9b373-264">È stato rimosso il parametro `ResourceId` deprecato dal cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="9b373-264">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="9b373-265">È stata rimossa la proprietà `EnableVmProtection` deprecata dall'oggetto `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="9b373-265">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="9b373-266">È stato rimosso il cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` deprecato</span><span class="sxs-lookup"><span data-stu-id="9b373-266">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>

<span data-ttu-id="9b373-267">Gli script non devono più prendere decisioni di elaborazione in base ai valori di questi campi.</span><span class="sxs-lookup"><span data-stu-id="9b373-267">Scripts should no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="9b373-268">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="9b373-268">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>

- <span data-ttu-id="9b373-269">Il set di parametri predefinito per `Get-AzOperationalInsightsDataSource` è stato rimosso e `ByWorkspaceNameByKind` è diventato il set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="9b373-269">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="9b373-270">Gli script che elencano le origini dati usando</span><span class="sxs-lookup"><span data-stu-id="9b373-270">Scripts that listed data sources using</span></span>
  ```azurepowershell-interactive
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="9b373-271">Devono essere modificati per specificare un tipo</span><span class="sxs-lookup"><span data-stu-id="9b373-271">Should be changed to specify a Kind</span></span>
  ```azurepowershell-interactive
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="9b373-272">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="9b373-272">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>

- <span data-ttu-id="9b373-273">È stato rimosso il parametro `Encryption` dal cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="9b373-273">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="9b373-274">Il parametro `TargetStorageAccountName` è ora obbligatorio per il ripristino dei dischi gestiti nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="9b373-274">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="9b373-275">Sono stati rimossi i parametri `StorageAccountName` e `StorageAccountResourceGroupName` nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="9b373-275">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="9b373-276">È stato rimosso il parametro `Name` nel cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="9b373-276">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="9b373-277">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="9b373-277">Az.Resources (previously AzureRM.Resources)</span></span>

- <span data-ttu-id="9b373-278">È stato rimosso il parametro `Sku` dal cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="9b373-278">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="9b373-279">È stato rimosso il parametro `Password` dal cmdlet `New-AzADServicePrincipal` e `New-AzADSpCredential`. Le password vengono generate automaticamente e gli script che fornivano la password:</span><span class="sxs-lookup"><span data-stu-id="9b373-279">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>

  ```azurepowershell-interactive
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="9b373-280">Devono essere modificati per recuperare la password dall'output:</span><span class="sxs-lookup"><span data-stu-id="9b373-280">Should be changed to retrieve the password from the output:</span></span>

  ```azurepowershell-interactive
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="9b373-281">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="9b373-281">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>

- <span data-ttu-id="9b373-282">Sono stati modificati i tipi restituiti di cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b373-282">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="9b373-283">La proprietà `ServiceTypeHealthPolicies` di tipo `ApplicationHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="9b373-283">The property `ServiceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="9b373-284">La proprietà `ApplicationHealthPolicies` di tipo `ClusterUpgradeDeltaHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="9b373-284">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="9b373-285">La proprietà `OverrideUserUpgradePolicy` di tipo `ClusterUpgradePolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="9b373-285">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="9b373-286">Queste modifiche interessano i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="9b373-286">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="9b373-287">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9b373-287">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="9b373-288">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="9b373-288">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="9b373-289">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9b373-289">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="9b373-290">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="9b373-290">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="9b373-291">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="9b373-291">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="9b373-292">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="9b373-292">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="9b373-293">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="9b373-293">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="9b373-294">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="9b373-294">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="9b373-295">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="9b373-295">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="9b373-296">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="9b373-296">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="9b373-297">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="9b373-297">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="9b373-298">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="9b373-298">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="9b373-299">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="9b373-299">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="9b373-300">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="9b373-300">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="9b373-301">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="9b373-301">Az.Sql (previously AzureRM.Sql)</span></span>

- <span data-ttu-id="9b373-302">Sono stati rimossi i parametri `State` e `ResourceId` dal cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="9b373-302">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="9b373-303">Sono stati rimossi i cmdlet deprecati: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="9b373-303">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="9b373-304">È stato rimosso il parametro `Current` deprecato dal cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="9b373-304">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="9b373-305">È stato rimosso il parametro `DatabaseName` deprecato dal cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="9b373-305">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="9b373-306">È stato rimosso il parametro `PrivilegedLogin` deprecato dal cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="9b373-306">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="9b373-307">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="9b373-307">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>

- <span data-ttu-id="9b373-308">Per supportare la creazione di un contesto di archiviazione Oauth con solo il nome dell'account di archiviazione, il set di parametri predefinito è stato modificato in `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="9b373-308">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="9b373-309">Esempio: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="9b373-309">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="9b373-310">Il parametro `Location` è diventato obbligatorio nel cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="9b373-310">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="9b373-311">I metodi dell'API di archiviazione usano ora il Modello asincrono basato su attività (TAP), invece delle chiamate API sincrone.</span><span class="sxs-lookup"><span data-stu-id="9b373-311">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span> <span data-ttu-id="9b373-312">Gli esempi seguenti illustrano i nuovi comandi asincroni:</span><span class="sxs-lookup"><span data-stu-id="9b373-312">The following examples demonstrate the new asynchronous commands:</span></span>

#### <a name="blob-snapshot"></a><span data-ttu-id="9b373-313">Snapshot del BLOB</span><span class="sxs-lookup"><span data-stu-id="9b373-313">Blob Snapshot</span></span>

<span data-ttu-id="9b373-314">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9b373-314">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

<span data-ttu-id="9b373-315">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="9b373-315">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="share-snapshot"></a><span data-ttu-id="9b373-316">Snapshot di condivisione</span><span class="sxs-lookup"><span data-stu-id="9b373-316">Share Snapshot</span></span>

<span data-ttu-id="9b373-317">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9b373-317">AzureRM:</span></span>

```azurepowershell-interactive
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```

<span data-ttu-id="9b373-318">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="9b373-318">Az:</span></span>

```azurepowershell-interactive
$Share = Get-AzStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="undelete-soft-deleted-blob"></a><span data-ttu-id="9b373-319">Annullare l'eliminazione del BLOB eliminato temporaneamente</span><span class="sxs-lookup"><span data-stu-id="9b373-319">Undelete soft-deleted blob</span></span>

<span data-ttu-id="9b373-320">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9b373-320">AzureRM:</span></span>

```azurepowershell-interactive
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```

<span data-ttu-id="9b373-321">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="9b373-321">Az:</span></span>

```azurepowershell-interactive
$b = Get-AzStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="set-blob-tier"></a><span data-ttu-id="9b373-322">Impostare il livello di BLOB</span><span class="sxs-lookup"><span data-stu-id="9b373-322">Set Blob Tier</span></span>

<span data-ttu-id="9b373-323">Modulo AzureRM:</span><span class="sxs-lookup"><span data-stu-id="9b373-323">AzureRM:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

<span data-ttu-id="9b373-324">Modulo Az:</span><span class="sxs-lookup"><span data-stu-id="9b373-324">Az:</span></span>

```azurepowershell-interactive
$blockBlob = Get-AzStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="9b373-325">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="9b373-325">Az.Websites (previously AzureRM.Websites)</span></span>

- <span data-ttu-id="9b373-326">Sono state rimosse le proprietà deprecate dagli oggetti `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite`</span><span class="sxs-lookup"><span data-stu-id="9b373-326">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>
