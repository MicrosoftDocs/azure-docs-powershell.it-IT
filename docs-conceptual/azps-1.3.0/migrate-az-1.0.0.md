---
title: Modifiche che causano un'interruzione in Microsoft Azure PowerShell Az 1.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano un'interruzione apportate ad Azure PowerShell nel rilascio della versione Az 1.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/14/2018
ms.openlocfilehash: be3e19dc4b689adbc63b933dd9f3454122d5344a
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56153475"
---
# <a name="migration-guide-for-az-100"></a><span data-ttu-id="f310f-103">Guida alla migrazione per Az 1.0.0</span><span class="sxs-lookup"><span data-stu-id="f310f-103">Migration Guide for Az 1.0.0</span></span>

<span data-ttu-id="f310f-104">Questo documento descrive le modifiche tra le versioni 6.x di AzureRM e la versione Az 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="f310f-104">This document describes the changes between the 6.x versions of AzureRM and Az version 1.0.0.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="f310f-105">Sommario</span><span class="sxs-lookup"><span data-stu-id="f310f-105">Table of Contents</span></span>
- [<span data-ttu-id="f310f-106">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="f310f-106">General breaking changes</span></span>](#general-breaking-changes)
  - [<span data-ttu-id="f310f-107">Modifiche al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="f310f-107">Cmdlet Noun Prefix Changes</span></span>](#cmdlet-noun-prefix-changes)
  - [<span data-ttu-id="f310f-108">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="f310f-108">Module name changes</span></span>](#module-name-changes)
  - [<span data-ttu-id="f310f-109">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="f310f-109">Removed modules</span></span>](#removed-modules)
  - [<span data-ttu-id="f310f-110">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f310f-110">Windows PowerShell 5.1 and .NET 4.7.2</span></span>](#windows-powershell-51-and-net-472)
  - [<span data-ttu-id="f310f-111">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="f310f-111">Temporary removal of User login using PSCredential</span></span>](#temporary-removal-of-user-login-using-pscredential)
  - [<span data-ttu-id="f310f-112">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="f310f-112">Default Device Code login instead of Web Browser prompt</span></span>](#temporary-default-device-code-login-instead-of-web-browser-prompt)
- [<span data-ttu-id="f310f-113">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="f310f-113">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="f310f-114">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f310f-114">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>](#azapimanagement-previously-azurermapimanagement)
  - [<span data-ttu-id="f310f-115">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f310f-115">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>](#azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates)
  - [<span data-ttu-id="f310f-116">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f310f-116">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>](#azcognitiveservices-previously-azurermcognitiveservices)
  - [<span data-ttu-id="f310f-117">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f310f-117">Az.Compute (previously AzureRM.Compute)</span></span>](#azcompute-previously-azurermcompute)
  - [<span data-ttu-id="f310f-118">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f310f-118">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>](#azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2)
  - [<span data-ttu-id="f310f-119">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f310f-119">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>](#azdatalakeanalytics-previously-azurermdatalakeanalytics)
  - [<span data-ttu-id="f310f-120">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f310f-120">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>](#azdatalakestore-previously-azurermdatalakestore)
  - [<span data-ttu-id="f310f-121">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f310f-121">Az.KeyVault (previously AzureRM.KeyVault)</span></span>](#azkeyvault-previously-azurermkeyvault)
  - [<span data-ttu-id="f310f-122">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f310f-122">Az.Media (previously AzureRM.Media)</span></span>](#azmedia-previously-azurermmedia)
  - [<span data-ttu-id="f310f-123">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f310f-123">Az.Monitor (previously AzureRM.Insights)</span></span>](#azmonitor-previously-azurerminsights)
  - [<span data-ttu-id="f310f-124">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f310f-124">Az.Network (previously AzureRM.Network)</span></span>](#aznetwork-previously-azurermnetwork)
  - [<span data-ttu-id="f310f-125">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f310f-125">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>](#azoperationalinsights-previously-azurermoperationalinsights)
  - [<span data-ttu-id="f310f-126">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f310f-126">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>](#azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery)
  - [<span data-ttu-id="f310f-127">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f310f-127">Az.Resources (previously AzureRM.Resources)</span></span>](#azresources-previously-azurermresources)
  - [<span data-ttu-id="f310f-128">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f310f-128">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>](#azservicefabric-previously-azurermservicefabric)
  - [<span data-ttu-id="f310f-129">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f310f-129">Az.Sql (previously AzureRM.Sql)</span></span>](#azsql-previously-azurermsql)
  - [<span data-ttu-id="f310f-130">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f310f-130">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>](#azstorage-previously-azurestorage-and-azurermstorage)
  - [<span data-ttu-id="f310f-131">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f310f-131">Az.Websites (previously AzureRM.Websites)</span></span>](#azwebsites-previously-azurermwebsites)

## <a name="general-breaking-changes"></a><span data-ttu-id="f310f-132">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="f310f-132">General breaking changes</span></span>
### <a name="cmdlet-noun-prefix-changes"></a><span data-ttu-id="f310f-133">Modifiche al prefisso dei nomi dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="f310f-133">Cmdlet Noun Prefix Changes</span></span>
<span data-ttu-id="f310f-134">In AzureRM i cmdlet usavano 'AzureRM' o 'Azure' come prefisso dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f310f-134">In AzureRM, cmdlets used either 'AzureRM' or 'Azure' as a noun prefix.</span></span>  <span data-ttu-id="f310f-135">Az semplifica e normalizza i nomi dei cmdlet, in modo che tutti i cmdlet usano 'Az' come prefisso dei nomi dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f310f-135">Az simplifies and normalizes cmndlet names, so that all cmdlets use 'Az' as their cmdlet noun prefix.</span></span> <span data-ttu-id="f310f-136">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="f310f-136">For example:</span></span>
```powershell
Get-AzureRMVM
Get-AzureKeyVaultSecret
```

<span data-ttu-id="f310f-137">Sono stati modificati in</span><span class="sxs-lookup"><span data-stu-id="f310f-137">Have changed to</span></span>
```powershell
Get-AzVM
Get-AzKeyVaultSecret
```

<span data-ttu-id="f310f-138">Per semplificare la transizione a questi nuovi nomi dei cmdlet, Az introduce due nuovi cmdlet, ```Enable-AzureRmAlias``` e ```Disable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="f310f-138">To make the transition to these new cmdlet names simpler, Az introduces two new cmdlets, ```Enable-AzureRmAlias``` and ```Disable-AzureRmAlias```.</span></span>  <span data-ttu-id="f310f-139">```Enable-AzureRmAlias``` crea gli alias dai nomi dei cmdlet precedenti in AzureRM per i nuovi nomi dei cmdlet Az.</span><span class="sxs-lookup"><span data-stu-id="f310f-139">```Enable-AzureRmAlias``` creates aliases from the older cmdlet names in AzureRM to the newer Az cmdlet names.</span></span>  <span data-ttu-id="f310f-140">Il cmdlet consente di creare gli alias nella sessione corrente o in tutte le sessioni modificando il profilo dell'utente o del computer.</span><span class="sxs-lookup"><span data-stu-id="f310f-140">The cmdlet allows creating aliases in the current session, or across all sessions by changing your user or machine profile.</span></span> 

<span data-ttu-id="f310f-141">Ad esempio, lo script seguente in AzureRM:</span><span class="sxs-lookup"><span data-stu-id="f310f-141">For example, the following script in AzureRM:</span></span>
```powershell
#Requires -Modules AzureRM.Storage
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f310f-142">Potrebbe essere eseguito con modifiche minime usando ```Enable-AzureRmAlias```:</span><span class="sxs-lookup"><span data-stu-id="f310f-142">Could be run with minimal changes using ```Enable-AzureRmAlias```:</span></span>
```powershell
#Requires -Modules Az.Storage
Enable-AzureRmAlias
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f310f-143">L'esecuzione di ```Enable-AzureRmAlias -Scope CurrentUser``` abilita gli alias per tutte le sessioni di powershell che vengono aperte, in modo che dopo l'esecuzione di questo cmdlet non sarà necessario modificare uno script simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="f310f-143">Running ```Enable-AzureRmAlias -Scope CurrentUser``` will enable the aliases for all powershell sessions you open, so that after executing this cmdlet, a script like this would not need to be changed at all:</span></span>
```powershell
Get-AzureRmStorageAccount | Get-AzureStorageContainer | Get-AzureStorageBlob
```

<span data-ttu-id="f310f-144">Per informazioni dettagliate sull'utilizzo dei cmdlet alias, eseguire ```Get-Help -Online Enable-AzureRmAlias``` dal prompt di powershell.</span><span class="sxs-lookup"><span data-stu-id="f310f-144">For complete details on the usage of the alias cmdlets, execute ```Get-Help -Online Enable-AzureRmAlias``` from the powershell prompt.</span></span>

<span data-ttu-id="f310f-145">```Disable-AzureRmAlias``` rimuove gli alias dei cmdlet di AzureRM creati da ```Enable-AzureRmAlias```.</span><span class="sxs-lookup"><span data-stu-id="f310f-145">```Disable-AzureRmAlias``` removes AzureRM cmdlet aliases created by ```Enable-AzureRmAlias```.</span></span>  <span data-ttu-id="f310f-146">Per informazioni dettagliate, eseguire ```Get-Help -Online Disable-AzureRmAlias``` dal prompt di powershell.</span><span class="sxs-lookup"><span data-stu-id="f310f-146">For complete details, execute ```Get-Help -Online Disable-AzureRmAlias``` from the powershell prompt.</span></span>

### <a name="module-name-changes"></a><span data-ttu-id="f310f-147">Modifiche ai nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="f310f-147">Module Name Changes</span></span>
- <span data-ttu-id="f310f-148">I nomi dei moduli sono stati modificati da `AzureRM.*` a `Az.*`, fatta eccezione per i moduli seguenti:</span><span class="sxs-lookup"><span data-stu-id="f310f-148">The module names have changed from `AzureRM.*` to `Az.*`, except for the following modules:</span></span>
```
AzureRM.Profile                       -> Az.Accounts
Azure.AnalysisServices                -> Az.AnalysisServices
AzureRM.Consumption                   -> Az.Billing
AzureRM.UsageAggregates               -> Az.Billing
AzureRM.DataFactories                 -> Az.DataFactory
AzureRM.DataFactoryV2                 -> Az.DataFactory
AzureRM.MachineLearningCompute        -> Az.MachineLearning
AzureRM.Insights                      -> Az.Monitor
AzureRM.RecoveryServices.Backup       -> Az.RecoveryServices
AzureRM.RecoveryServices.SiteRecovery -> Az.RecoveryServices
AzureRM.Tags                          -> Az.Resources
Azure.Storage                         -> Az.Storage
```

<span data-ttu-id="f310f-149">Le modifiche nei nomi dei moduli significano che tutti gli script che usano ```#Requires``` o ```Import-Module``` per caricare moduli specifici dovranno essere modificati per usare il nuovo modulo.</span><span class="sxs-lookup"><span data-stu-id="f310f-149">The changes in module names mean that any script that uses ```#Requires``` or ```Import-Module``` to load specific modules will need to be changed to use the new module instead.</span></span>

#### <a name="migrating-requires-statements"></a><span data-ttu-id="f310f-150">Migrazione delle istruzioni #Requires</span><span class="sxs-lookup"><span data-stu-id="f310f-150">Migrating #Requires Statements</span></span>
<span data-ttu-id="f310f-151">Gli script che usano #Requires per dichiarare una dipendenza dai moduli AzureRM devono essere aggiornati per usare i nuovi nomi dei moduli</span><span class="sxs-lookup"><span data-stu-id="f310f-151">Scripts that use #Requires to declare a dependency on AzureRM modules should be updated to use the new module names</span></span>
```powershell
#Requires -Module AzureRM.Compute
```

<span data-ttu-id="f310f-152">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-152">Should be changed to</span></span>
```powershell
#Requires -Module Az.Compute
```

#### <a name="migrating-import-module-statements"></a><span data-ttu-id="f310f-153">Migrazione delle istruzioni Import-Module</span><span class="sxs-lookup"><span data-stu-id="f310f-153">Migrating Import-Module Statements</span></span>
<span data-ttu-id="f310f-154">Gli script che usano ```Import-Module``` per caricare i moduli AzureRM dovranno essere aggiornato per riflettere i nuovi nomi dei moduli.</span><span class="sxs-lookup"><span data-stu-id="f310f-154">Scripts that use ```Import-Module``` to load AzureRM modules will need to be updated to reflect the new module names.</span></span>
```powershell
Import-Module -Name AzureRM.Compute
```

<span data-ttu-id="f310f-155">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-155">Should be changed to</span></span>
```powershell
Import-Module -Name Az.Compute
```

### <a name="migrating-fully-qualified-cmdlet-invocations"></a><span data-ttu-id="f310f-156">Migrazione delle chiamate dei cmdlet complete</span><span class="sxs-lookup"><span data-stu-id="f310f-156">Migrating Fully-Qualified Cmdlet Invocations</span></span>
<span data-ttu-id="f310f-157">Gli script che usano le chiamate dei cmdlet qualificate di modulo, ad esempio</span><span class="sxs-lookup"><span data-stu-id="f310f-157">Scripts that use module-qualified cmdlet invocations, like</span></span>
```powershell
AzureRM.Compute\Get-AzureRmVM
```

<span data-ttu-id="f310f-158">Devono essere modificati per usare i nuovi nomi dei moduli e dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="f310f-158">Should be changed to use the new module and cmdlet names</span></span>
```powershell
Az.Compute\Get-AzVM
```

### <a name="migrating-module-manifest-dependencies"></a><span data-ttu-id="f310f-159">Migrazione delle dipendenze del manifesto del modulo</span><span class="sxs-lookup"><span data-stu-id="f310f-159">Migrating Module Manifest Dependencies</span></span>
<span data-ttu-id="f310f-160">I moduli che esprimono le dipendenze dai moduli AzureRM tramite un file del manifesto del modulo (con estensione psd1) dovranno aggiornare i nomi dei moduli nella sezione 'RequiredModules'</span><span class="sxs-lookup"><span data-stu-id="f310f-160">Modules that express dependencies on AzureRM modules through a module manifest (.psd1) file will need to updated the module names in their 'RequiredModules' section</span></span>

```powershell
RequiredModules = @(@{ModuleName="AzureRM.Profile"; ModuleVersion="5.8.2"})
```

<span data-ttu-id="f310f-161">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-161">Should be changed to</span></span>

```powershell
RequiredModules = @(@{ModuleName="Az.Profile"; ModuleVersion="1.0.0"})
```

### <a name="removed-modules"></a><span data-ttu-id="f310f-162">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="f310f-162">Removed modules</span></span>
- `AzureRM.Backup`
- `AzureRM.Compute.ManagedService`
- `AzureRM.Scheduler`

<span data-ttu-id="f310f-163">Gli strumenti per questi servizi non sono più supportati attivamente.</span><span class="sxs-lookup"><span data-stu-id="f310f-163">The tooling for these services are no longer actively supported.</span></span>  <span data-ttu-id="f310f-164">I clienti sono invitati a passare a servizi alternativi non appena possibile.</span><span class="sxs-lookup"><span data-stu-id="f310f-164">Customers are encouraged to move to alternative services as soon as it is convenient.</span></span>

### <a name="windows-powershell-51-and-net-472"></a><span data-ttu-id="f310f-165">Windows PowerShell 5.1 e .NET 4.7.2</span><span class="sxs-lookup"><span data-stu-id="f310f-165">Windows PowerShell 5.1 and .NET 4.7.2</span></span>
- <span data-ttu-id="f310f-166">L'uso di Az con Windows PowerShell 5.1 richiede l'installazione di .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="f310f-166">Using Az with Windows PowerShell 5.1 requires the installation of .NET 4.7.2.</span></span> <span data-ttu-id="f310f-167">Tuttavia, l'uso di Az con PowerShell Core non richiede .NET 4.7.2.</span><span class="sxs-lookup"><span data-stu-id="f310f-167">However, using Az with PowerShell Core does not require .NET 4.7.2.</span></span> 

### <a name="temporary-removal-of-user-login-using-pscredential"></a><span data-ttu-id="f310f-168">Rimozione temporanea dell'accesso utente con PSCredential</span><span class="sxs-lookup"><span data-stu-id="f310f-168">Temporary removal of User login using PSCredential</span></span>
- <span data-ttu-id="f310f-169">A causa delle modifiche nel flusso di autenticazione per .NET Standard verrà temporaneamente rimosso l'accesso utente tramite PSCredential.</span><span class="sxs-lookup"><span data-stu-id="f310f-169">Due to changes in the authentication flow for .NET Standard, we are temporarily removing user login via PSCredential.</span></span> <span data-ttu-id="f310f-170">Questa funzionalità sarà reintrodotta nella versione del 15/01/2019 per Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="f310f-170">This capability will be re-introduced in the 1/15/2019 release for Windows PowerShell 5.1.</span></span> <span data-ttu-id="f310f-171">Questo problema è spiegato in dettaglio [qui.](https://github.com/Azure/azure-powershell/issues/7430)</span><span class="sxs-lookup"><span data-stu-id="f310f-171">This is duscussed in detail in [this issue.](https://github.com/Azure/azure-powershell/issues/7430)</span></span>

### <a name="default-device-code-login-instead-of-web-browser-prompt"></a><span data-ttu-id="f310f-172">Accesso predefinito del codice dispositivo anziché del prompt del Web browser</span><span class="sxs-lookup"><span data-stu-id="f310f-172">Default Device Code login instead of Web Browser prompt</span></span>
- <span data-ttu-id="f310f-173">A causa delle modifiche nel flusso di autenticazione per .NET Standard, viene usato l'accesso del dispositivo come flusso di accesso predefinito durante l'accesso interattivo.</span><span class="sxs-lookup"><span data-stu-id="f310f-173">Due to changes in the authentication flow for .NET Standard, we are using device login as the default login flow during interactive login.</span></span> <span data-ttu-id="f310f-174">L'accesso basato su Web browser verrà reintrodotto per Windows PowerShell 5.1 come impostazione predefinita nella versione del 15/01/2019.</span><span class="sxs-lookup"><span data-stu-id="f310f-174">Web browser based login will be re-introduced for Windows PowerShell 5.1 as the default in the 1/15/2019 release.</span></span> <span data-ttu-id="f310f-175">A quel punto, gli utenti potranno scegliere l'accesso del dispositivo usando un parametro Switch.</span><span class="sxs-lookup"><span data-stu-id="f310f-175">At that time, users will be able to choose device login using a Switch parameter.</span></span>

## <a name="module-breaking-changes"></a><span data-ttu-id="f310f-176">Modifiche che causano un'interruzione dei moduli</span><span class="sxs-lookup"><span data-stu-id="f310f-176">Module breaking changes</span></span>

### <a name="azapimanagement-previously-azurermapimanagement"></a><span data-ttu-id="f310f-177">Az.ApiManagement (in precedenza AzureRM.ApiManagement)</span><span class="sxs-lookup"><span data-stu-id="f310f-177">Az.ApiManagement (previously AzureRM.ApiManagement)</span></span>
- <span data-ttu-id="f310f-178">Rimozione dei cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f310f-178">Removing the following cmdlets:</span></span>
  - <span data-ttu-id="f310f-179">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f310f-179">New-AzureRmApiManagementHostnameConfiguration</span></span>
  - <span data-ttu-id="f310f-180">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f310f-180">Set-AzureRmApiManagementHostnames</span></span>
  - <span data-ttu-id="f310f-181">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="f310f-181">Update-AzureRmApiManagementDeployment</span></span>
  - <span data-ttu-id="f310f-182">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f310f-182">Import-AzureRmApiManagementHostnameCertificate</span></span>
  - <span data-ttu-id="f310f-183">Usare il cmdlet **Set-AzApiManagement** per impostare queste proprietà</span><span class="sxs-lookup"><span data-stu-id="f310f-183">Use **Set-AzApiManagement** cmdlet to set these properites instead</span></span>
- <span data-ttu-id="f310f-184">Sono state rimosse le proprietà seguenti</span><span class="sxs-lookup"><span data-stu-id="f310f-184">Following properties were removed</span></span>
  - <span data-ttu-id="f310f-185">Sono state rimosse le proprietà `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` e `ScmHostnameConfiguration` di tipo `PsApiManagementHostnameConfiguration` da `PsApiManagementContext`.</span><span class="sxs-lookup"><span data-stu-id="f310f-185">Removed property `PortalHostnameConfiguration`, `ProxyHostnameConfiguration`, `ManagementHostnameConfiguration` and `ScmHostnameConfiguration` of type `PsApiManagementHostnameConfiguration` from `PsApiManagementContext`.</span></span> <span data-ttu-id="f310f-186">Usare `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` e `ScmCustomHostnameConfiguration` di tipo `PsApiManagementCustomHostNameConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="f310f-186">Instead use `PortalCustomHostnameConfiguration`, `ProxyCustomHostnameConfiguration`, `ManagementCustomHostnameConfiguration` and `ScmCustomHostnameConfiguration` of type `PsApiManagementCustomHostNameConfiguration`.</span></span>
  - <span data-ttu-id="f310f-187">È stata rimossa la proprietà `StaticIPs` da PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f310f-187">Removed property `StaticIPs` from PsApiManagementContext.</span></span> <span data-ttu-id="f310f-188">La proprietà è stata suddivisa in `PublicIPAddresses` e `PrivateIPAddresses`.</span><span class="sxs-lookup"><span data-stu-id="f310f-188">The property has been split into `PublicIPAddresses` and `PrivateIPAddresses`.</span></span>
  - <span data-ttu-id="f310f-189">È stata rimossa la proprietà obbligatoria `Location` dal cmdlet New-AzureApiManagementVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="f310f-189">Removed required property `Location` from New-AzureApiManagementVirtualNetwork cmdlet.</span></span>

### <a name="azbilling-previously-azurermbilling-azurermconsumption-and-azurermusageaggregates"></a><span data-ttu-id="f310f-190">Az.Billing (in precedenza AzureRM.Billing, AzureRM.Consumption e AzureRM.UsageAggregates)</span><span class="sxs-lookup"><span data-stu-id="f310f-190">Az.Billing (previously AzureRM.Billing, AzureRM.Consumption, and AzureRM.UsageAggregates)</span></span>
- <span data-ttu-id="f310f-191">Il parametro `InvoiceName` è stato rimosso dal cmdlet `Get-AzConsumptionUsageDetail`.</span><span class="sxs-lookup"><span data-stu-id="f310f-191">The `InvoiceName` parameter was removed from the `Get-AzConsumptionUsageDetail` cmdlet.</span></span>  <span data-ttu-id="f310f-192">Gli script dovranno usare altri parametri di identità per la fatturazione.</span><span class="sxs-lookup"><span data-stu-id="f310f-192">Scripts will need to use other identity parameters for the invoice.</span></span>

### <a name="azcognitiveservices-previously-azurermcognitiveservices"></a><span data-ttu-id="f310f-193">Az.CognitiveServices (in precedenza AzureRM.CognitiveServices)</span><span class="sxs-lookup"><span data-stu-id="f310f-193">Az.CognitiveServices (previously AzureRM.CognitiveServices)</span></span>
- <span data-ttu-id="f310f-194">È stato rimosso il set di parametri `GetSkusWithAccountParamSetName` dal cmdlet `Get-AzCognitiveServicesAccountSkus`.</span><span class="sxs-lookup"><span data-stu-id="f310f-194">Removed `GetSkusWithAccountParamSetName` parameter set from `Get-AzCognitiveServicesAccountSkus` cmdlet.</span></span>  <span data-ttu-id="f310f-195">È necessario ottenere gli SKU per tipo di account e posizione, anziché usare ResourceGroupName e nome account.</span><span class="sxs-lookup"><span data-stu-id="f310f-195">You must get Skus by Account Type and Location, instead of using ResourceGroupName and Account Name.</span></span>

### <a name="azcompute-previously-azurermcompute"></a><span data-ttu-id="f310f-196">Az.Compute (in precedenza AzureRM.Compute)</span><span class="sxs-lookup"><span data-stu-id="f310f-196">Az.Compute (previously AzureRM.Compute)</span></span>
- <span data-ttu-id="f310f-197">`IdentityIds` è stato rimosso dalla proprietà `Identity` negli oggetti `PSVirtualMachine` e `PSVirtualMachineScaleSet`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f310f-197">`IdentityIds` are removed from `Identity` property in `PSVirtualMachine` and `PSVirtualMachineScaleSet` objects Scripts should no longer use the value of this field to make processing decisions.</span></span>
- <span data-ttu-id="f310f-198">Il tipo della proprietà `InstanceView` dell'oggetto `PSVirtualMachineScaleSetVM` è stato modificato da `VirtualMachineInstanceView` a `VirtualMachineScaleSetVMInstanceView`</span><span class="sxs-lookup"><span data-stu-id="f310f-198">The type of `InstanceView` property of `PSVirtualMachineScaleSetVM` object is changed from `VirtualMachineInstanceView` to `VirtualMachineScaleSetVMInstanceView`</span></span>
- <span data-ttu-id="f310f-199">Le proprietà `AutoOSUpgradePolicy` e `AutomaticOSUpgrade` sono state rimosse dalla proprietà `UpgradePolicy`</span><span class="sxs-lookup"><span data-stu-id="f310f-199">`AutoOSUpgradePolicy` and `AutomaticOSUpgrade` properties are removed from `UpgradePolicy` property</span></span>
- <span data-ttu-id="f310f-200">Il tipo della proprietà `Sku` nell'oggetto `PSSnapshotUpdate` è stato modificato da `DiskSku` a `SnapshotSku`</span><span class="sxs-lookup"><span data-stu-id="f310f-200">The type of `Sku` property in `PSSnapshotUpdate` object is changed from `DiskSku` to `SnapshotSku`</span></span>
- <span data-ttu-id="f310f-201">`VmScaleSetVMParameterSet` è stato rimosso dal cmdlet `Add-AzVMDataDisk`. Non è più possibile aggiungere singolarmente un disco dati a una macchina virtuale del set di scalabilità.</span><span class="sxs-lookup"><span data-stu-id="f310f-201">`VmScaleSetVMParameterSet` is removed from `Add-AzVMDataDisk` cmdlet, you cna no longer add a data disk individually to a ScaleSet VM.</span></span>

### <a name="azdatafactory-previously-azurermdatafactories-and-azurermdatafactoryv2"></a><span data-ttu-id="f310f-202">Az.DataFactory (in precedenza AzureRM.DataFactories e AzureRM.DataFactoryV2)</span><span class="sxs-lookup"><span data-stu-id="f310f-202">Az.DataFactory (previously AzureRM.DataFactories and AzureRM.DataFactoryV2)</span></span>
- <span data-ttu-id="f310f-203">Il parametro `GatewayName` è diventato obbligatorio nel cmdlet `New-AzDataFactoryEncryptValue`</span><span class="sxs-lookup"><span data-stu-id="f310f-203">The `GatewayName` parameter has become mandatory in the `New-AzDataFactoryEncryptValue` cmdlet</span></span>
- <span data-ttu-id="f310f-204">È stato rimosso il cmdlet `New-AzDataFactoryGatewayKey`</span><span class="sxs-lookup"><span data-stu-id="f310f-204">Removed `New-AzDataFactoryGatewayKey` cmdlet</span></span>
- <span data-ttu-id="f310f-205">È stato rimosso il parametro `LinkedServiceName` dal cmdlet `Get-AzDataFactoryV2ActivityRun`. Gli script non devono più usare il valore di questo campo per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f310f-205">Removed `LinkedServiceName` parameter from `Get-AzDataFactoryV2ActivityRun` cmdlet Scripts should no longer use the value of this field to make processing decisions.</span></span>

### <a name="azdatalakeanalytics-previously-azurermdatalakeanalytics"></a><span data-ttu-id="f310f-206">Az.DataLakeAnalytics (in precedenza AzureRM.DataLakeAnalytics)</span><span class="sxs-lookup"><span data-stu-id="f310f-206">Az.DataLakeAnalytics (previously AzureRM.DataLakeAnalytics)</span></span>
- <span data-ttu-id="f310f-207">Sono stati rimossi i cmdlet deprecati: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret` e `Set-AzDataLakeAnalyticsCatalogSecret`</span><span class="sxs-lookup"><span data-stu-id="f310f-207">Removed deprecated cmdlets: `New-AzDataLakeAnalyticsCatalogSecret`, `Remove-AzDataLakeAnalyticsCatalogSecret`, and `Set-AzDataLakeAnalyticsCatalogSecret`</span></span>

### <a name="azdatalakestore-previously-azurermdatalakestore"></a><span data-ttu-id="f310f-208">Az.DataLakeStore (in precedenza AzureRM.DataLakeStore)</span><span class="sxs-lookup"><span data-stu-id="f310f-208">Az.DataLakeStore (previously AzureRM.DataLakeStore)</span></span>
- <span data-ttu-id="f310f-209">Il tipo del parametro `Encoding` dei cmdlet seguenti è stato modificato da `FileSystemCmdletProviderEncoding` a `System.Text.Encoding`.</span><span class="sxs-lookup"><span data-stu-id="f310f-209">The following cmdlets have had the `Encoding` parameter changed from the type `FileSystemCmdletProviderEncoding` to `System.Text.Encoding`.</span></span> <span data-ttu-id="f310f-210">Questa modifica rimuove i valori di codifica `String` e `Oem`.</span><span class="sxs-lookup"><span data-stu-id="f310f-210">This change removes the encoding values `String` and `Oem`.</span></span> <span data-ttu-id="f310f-211">Tutti gli altri valori di codifica precedenti rimangono.</span><span class="sxs-lookup"><span data-stu-id="f310f-211">All the other prior encoding values remain.</span></span>
  - <span data-ttu-id="f310f-212">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f310f-212">New-AzureRmDataLakeStoreItem</span></span>
  - <span data-ttu-id="f310f-213">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f310f-213">Add-AzureRmDataLakeStoreItemContent</span></span>
  - <span data-ttu-id="f310f-214">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f310f-214">Get-AzureRmDataLakeStoreItemContent</span></span>
- <span data-ttu-id="f310f-215">È stato rimosso l'alias della proprietà `Tags` deprecata dai cmdlet `New-AzDataLakeStoreAccount` e `Set-AzDataLakeStoreAccount`</span><span class="sxs-lookup"><span data-stu-id="f310f-215">Removed deprecated `Tags` property alias from `New-AzDataLakeStoreAccount` and `Set-AzDataLakeStoreAccount` cmdlets</span></span>

  <span data-ttu-id="f310f-216">Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f310f-216">Scripts using</span></span>
  ```powershell
  New-AzureRMDataLakeStoreAccount -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f310f-217">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-217">Should be changed to</span></span>
  ```powershell
  New-AzDataLakeStoreAccount -Tag @{TagName="TagValue"}
  ```

- <span data-ttu-id="f310f-218">Sono state rimosse le proprietà deprecate ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` dall'oggetto ```PSDataLakeStoreAccountBasic```.</span><span class="sxs-lookup"><span data-stu-id="f310f-218">Removed deprecated properties ```Identity```, ```EncryptionState```, ```EncrypotionProvisioningState```, ```EncryptionConfig```, ```FirewallState```, ```FirewallRules```, ```VirtualNetworkRules```, ```TrustedIdProviderState```, ```TrustedIdProviders```, ```DefaultGroup```, ```NewTier```, ```CurrentTier```, ```FirewallAllowAzureIps``` from ```PSDataLakeStoreAccountBasic``` object.</span></span>  <span data-ttu-id="f310f-219">Tutti gli script che usano ```PSDatalakeStoreAccount``` restituito da ```Get-AzDataLakeStoreAccount``` non devono fare riferimento a queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="f310f-219">Any script that uses the ```PSDatalakeStoreAccount``` returned from ```Get-AzDataLakeStoreAccount``` should not reference these properties.</span></span>

### <a name="azkeyvault-previously-azurermkeyvault"></a><span data-ttu-id="f310f-220">Az.KeyVault (in precedenza AzureRM.KeyVault)</span><span class="sxs-lookup"><span data-stu-id="f310f-220">Az.KeyVault (previously AzureRM.KeyVault)</span></span>
- <span data-ttu-id="f310f-221">La proprietà `PurgeDisabled` è stata rimossa dagli oggetti `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem` e `PSKeyVaultSecretAttributes`. Gli script non devono più fare riferimento alla proprietà ```PurgeDisabled``` per le decisioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="f310f-221">The `PurgeDisabled` property was removed from the `PSKeyVaultKeyAttributes`, `PSKeyVaultKeyIdentityItem`, and `PSKeyVaultSecretAttributes` objects Scripts shoudl no longer reference the ```PurgeDisabled``` property to make processing decisions.</span></span>

### <a name="azmedia-previously-azurermmedia"></a><span data-ttu-id="f310f-222">Az.Media (in precedenza AzureRM.Media)</span><span class="sxs-lookup"><span data-stu-id="f310f-222">Az.Media (previously AzureRM.Media)</span></span>
- <span data-ttu-id="f310f-223">È stato rimosso l'alias della proprietà `Tags` deprecata dal cmdlet `New-AzMediaService`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f310f-223">Remove deprecated `Tags` property alias from `New-AzMediaService` cmdlet Scripts using</span></span>
  ```powershell
  New-AzureRMMediaService -Tags @{TagName="TagValue"}
  ```

  <span data-ttu-id="f310f-224">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-224">Should be changed to</span></span>
  ```powershell
  New-AzMMediaService -Tag @{TagName="TagValue"}
  ```
### <a name="azmonitor-previously-azurerminsights"></a><span data-ttu-id="f310f-225">Az.Monitor (in precedenza AzureRM.Insights)</span><span class="sxs-lookup"><span data-stu-id="f310f-225">Az.Monitor (previously AzureRM.Insights)</span></span>
- <span data-ttu-id="f310f-226">Sono stati rimossi i nomi plurali del parametro `Categories` e `Timegrains` sostituendoli con nomi di parametro singolari dal cmdlet `Set-AzDiagnosticSetting`. Lo script che usa</span><span class="sxs-lookup"><span data-stu-id="f310f-226">Removed plural names `Categories` and `Timegrains` parameter in favor of singular parameter names from `Set-AzDiagnosticSetting` cmdlet Scripts using</span></span>
  ```powershell
  Set-AzureRmDiagnosticSetting -Timegrains PT1M -Categories Category1, Category2
  ```

  <span data-ttu-id="f310f-227">Deve essere modificato in</span><span class="sxs-lookup"><span data-stu-id="f310f-227">Should be changed to</span></span>
  ```powershell
  Set-AzDiagnosticSetting -Timegrain PT1M -Category Category1, Category2
  ```
### <a name="aznetwork-previously-azurermnetwork"></a><span data-ttu-id="f310f-228">Az.Network (in precedenza AzureRM.Network)</span><span class="sxs-lookup"><span data-stu-id="f310f-228">Az.Network (previously AzureRM.Network)</span></span>
- <span data-ttu-id="f310f-229">È stato rimosso il parametro `ResourceId` deprecato dal cmdlet `Get-AzServiceEndpointPolicyDefinition`</span><span class="sxs-lookup"><span data-stu-id="f310f-229">Removed deprecated `ResourceId` parameter from `Get-AzServiceEndpointPolicyDefinition` cmdlet</span></span>
- <span data-ttu-id="f310f-230">È stata rimossa la proprietà `EnableVmProtection` deprecata dall'oggetto `PSVirtualNetwork`</span><span class="sxs-lookup"><span data-stu-id="f310f-230">Removed deprecated `EnableVmProtection` property from `PSVirtualNetwork` object</span></span>
- <span data-ttu-id="f310f-231">È stato rimosso il cmdlet `Set-AzVirtualNetworkGatewayVpnClientConfig` deprecato</span><span class="sxs-lookup"><span data-stu-id="f310f-231">Removed deprecated `Set-AzVirtualNetworkGatewayVpnClientConfig` cmdlet</span></span>
  
<span data-ttu-id="f310f-232">Gli script non devono più prendere decisioni di elaborazione in base ai valori di questi campi.</span><span class="sxs-lookup"><span data-stu-id="f310f-232">Scripts shoudl no longer make processing decisions based on the values fo these fields.</span></span>

### <a name="azoperationalinsights-previously-azurermoperationalinsights"></a><span data-ttu-id="f310f-233">Az.OperationalInsights (in precedenza AzureRM.OperationalInsights)</span><span class="sxs-lookup"><span data-stu-id="f310f-233">Az.OperationalInsights (previously AzureRM.OperationalInsights)</span></span>
- <span data-ttu-id="f310f-234">Il set di parametri predefinito per `Get-AzOperationalInsightsDataSource` è stato rimosso e `ByWorkspaceNameByKind` è diventato il set di parametri predefinito</span><span class="sxs-lookup"><span data-stu-id="f310f-234">Default parameter set for `Get-AzOperationalInsightsDataSource` is removed, and `ByWorkspaceNameByKind` has become the default parameter set</span></span>

  <span data-ttu-id="f310f-235">Gli script che elencano le origini dati usando</span><span class="sxs-lookup"><span data-stu-id="f310f-235">Scripts that listed data sources using</span></span>
  ```powershell
  Get-AzureRmOperationalInsightsDataSource
  ```

  <span data-ttu-id="f310f-236">Devono essere modificati per specificare un tipo</span><span class="sxs-lookup"><span data-stu-id="f310f-236">Should be changed to specify a Kind</span></span>
  ```powershell
  Get-AzOperationalInsightsDataSource -Kind AzureActivityLog
  ```

### <a name="azrecoveryservices-previously-azurermrecoveryservices-azurermrecoveryservicesbackup-and-azurermrecoveryservicessiterecovery"></a><span data-ttu-id="f310f-237">Az.RecoveryServices (in precedenza AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup e AzureRM.RecoveryServices.SiteRecovery)</span><span class="sxs-lookup"><span data-stu-id="f310f-237">Az.RecoveryServices (previously AzureRM.RecoveryServices, AzureRM.RecoveryServices.Backup, and AzureRM.RecoveryServices.SiteRecovery)</span></span>
- <span data-ttu-id="f310f-238">È stato rimosso il parametro `Encryption` dal cmdlet `New/Set-AzRecoveryServicesAsrPolicy`</span><span class="sxs-lookup"><span data-stu-id="f310f-238">Removed `Encryption` parameter from `New/Set-AzRecoveryServicesAsrPolicy` cmdlet</span></span>
- <span data-ttu-id="f310f-239">Il parametro `TargetStorageAccountName` è ora obbligatorio per il ripristino dei dischi gestiti nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f310f-239">`TargetStorageAccountName` parameter is now mandatory for managed disk restores in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f310f-240">Sono stati rimossi i parametri `StorageAccountName` e `StorageAccountResourceGroupName` nel cmdlet `Restore-AzRecoveryServicesBackupItem`</span><span class="sxs-lookup"><span data-stu-id="f310f-240">Removed `StorageAccountName` and `StorageAccountResourceGroupName` parameters in `Restore-AzRecoveryServicesBackupItem` cmdlet</span></span>
- <span data-ttu-id="f310f-241">È stato rimosso il parametro `Name` nel cmdlet `Get-AzRecoveryServicesBackupContainer`</span><span class="sxs-lookup"><span data-stu-id="f310f-241">Removed `Name`parameter in `Get-AzRecoveryServicesBackupContainer` cmdlet</span></span>

### <a name="azresources-previously-azurermresources"></a><span data-ttu-id="f310f-242">Az.Resources (in precedenza AzureRM.Resources)</span><span class="sxs-lookup"><span data-stu-id="f310f-242">Az.Resources (previously AzureRM.Resources)</span></span>
- <span data-ttu-id="f310f-243">È stato rimosso il parametro `Sku` dal cmdlet `New/Set-AzPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="f310f-243">Removed `Sku` parameter from `New/Set-AzPolicyAssignment` cmdlet</span></span>
- <span data-ttu-id="f310f-244">È stato rimosso il parametro `Password` dal cmdlet `New-AzADServicePrincipal` e `New-AzADSpCredential`. Le password vengono generate automaticamente e gli script che fornivano la password:</span><span class="sxs-lookup"><span data-stu-id="f310f-244">Removed `Password` parameter from `New-AzADServicePrincipal` and `New-AzADSpCredential` cmdlet Passwords are automatically generated, scripts that provided the password:</span></span>
  ```powershell
  New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $secPassword
  ```

  <span data-ttu-id="f310f-245">Devono essere modificati per recuperare la password dall'output:</span><span class="sxs-lookup"><span data-stu-id="f310f-245">Should be changed to retriedve the password from the output:</span></span>
  ```powershell
  $credential = New-AzAdSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
  $secPassword = $credential.Secret
  ```

### <a name="azservicefabric-previously-azurermservicefabric"></a><span data-ttu-id="f310f-246">Az.ServiceFabric (in precedenza AzureRM.ServiceFabric)</span><span class="sxs-lookup"><span data-stu-id="f310f-246">Az.ServiceFabric (previously AzureRM.ServiceFabric)</span></span>
- <span data-ttu-id="f310f-247">Sono stati modificati i tipi restituiti di cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f310f-247">The following cmdlet return types have been changed:</span></span>
  - <span data-ttu-id="f310f-248">La proprietà `SerivceTypeHealthPolicies` di tipo `ApplicationHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f310f-248">The property `SerivceTypeHealthPolicies` of type `ApplicationHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f310f-249">La proprietà `ApplicationHealthPolicies` di tipo `ClusterUpgradeDeltaHealthPolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f310f-249">The property `ApplicationHealthPolicies` of type `ClusterUpgradeDeltaHealthPolicy` has been removed.</span></span>
  - <span data-ttu-id="f310f-250">La proprietà `OverrideUserUpgradePolicy` di tipo `ClusterUpgradePolicy` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="f310f-250">The property `OverrideUserUpgradePolicy` of type `ClusterUpgradePolicy` has been removed.</span></span>
  - <span data-ttu-id="f310f-251">Queste modifiche interessano i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="f310f-251">These changes affect the following cmdlets:</span></span>
    - <span data-ttu-id="f310f-252">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f310f-252">Add-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f310f-253">Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f310f-253">Add-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f310f-254">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f310f-254">Add-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f310f-255">Add-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f310f-255">Add-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f310f-256">Get-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f310f-256">Get-AzServiceFabricCluster</span></span>
    - <span data-ttu-id="f310f-257">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="f310f-257">Remove-AzServiceFabricClientCertificate</span></span>
    - <span data-ttu-id="f310f-258">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="f310f-258">Remove-AzServiceFabricClusterCertificate</span></span>
    - <span data-ttu-id="f310f-259">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="f310f-259">Remove-AzServiceFabricNode</span></span>
    - <span data-ttu-id="f310f-260">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="f310f-260">Remove-AzServiceFabricNodeType</span></span>
    - <span data-ttu-id="f310f-261">Remove-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f310f-261">Remove-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f310f-262">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="f310f-262">Set-AzServiceFabricSetting</span></span>
    - <span data-ttu-id="f310f-263">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="f310f-263">Set-AzServiceFabricUpgradeType</span></span>
    - <span data-ttu-id="f310f-264">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="f310f-264">Update-AzServiceFabricDurability</span></span>
    - <span data-ttu-id="f310f-265">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="f310f-265">Update-AzServiceFabricReliability</span></span>

### <a name="azsql-previously-azurermsql"></a><span data-ttu-id="f310f-266">Az.Sql (in precedenza AzureRM.Sql)</span><span class="sxs-lookup"><span data-stu-id="f310f-266">Az.Sql (previously AzureRM.Sql)</span></span>
- <span data-ttu-id="f310f-267">Sono stati rimossi i parametri `State` e `ResourceId` dal cmdlet `Set-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f310f-267">Removed `State` and `ResourceId` parameters from `Set-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f310f-268">Sono stati rimossi i cmdlet deprecati: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span><span class="sxs-lookup"><span data-stu-id="f310f-268">Removed deprecated cmdlets: `Get/Set-AzSqlServerBackupLongTermRetentionVault`, `Get/Start/Stop-AzSqlServerUpgrade`, `Get/Set-AzSqlDatabaseAuditingPolicy`, `Get/Set-AzSqlServerAuditingPolicy`, `Remove-AzSqlDatabaseAuditing`, `Remove-AzSqlServerAuditing`</span></span>
- <span data-ttu-id="f310f-269">È stato rimosso il parametro `Current` deprecato dal cmdlet `Get-AzSqlDatabaseBackupLongTermRetentionPolicy`</span><span class="sxs-lookup"><span data-stu-id="f310f-269">Removed deprecated parameter `Current` from `Get-AzSqlDatabaseBackupLongTermRetentionPolicy` cmdlet</span></span>
- <span data-ttu-id="f310f-270">È stato rimosso il parametro `DatabaseName` deprecato dal cmdlet `Get-AzSqlServerServiceObjective`</span><span class="sxs-lookup"><span data-stu-id="f310f-270">Removed deprecated parameter `DatabaseName` from `Get-AzSqlServerServiceObjective` cmdlet</span></span>
- <span data-ttu-id="f310f-271">È stato rimosso il parametro `PrivilegedLogin` deprecato dal cmdlet `Set-AzSqlDatabaseDataMaskingPolicy`</span><span class="sxs-lookup"><span data-stu-id="f310f-271">Removed deprecated parameter `PrivilegedLogin` from `Set-AzSqlDatabaseDataMaskingPolicy` cmdlet</span></span>

### <a name="azstorage-previously-azurestorage-and-azurermstorage"></a><span data-ttu-id="f310f-272">Az.Storage (in precedenza Azure.Storage e AzureRM.Storage)</span><span class="sxs-lookup"><span data-stu-id="f310f-272">Az.Storage (previously Azure.Storage and AzureRM.Storage)</span></span>
- <span data-ttu-id="f310f-273">Per supportare la creazione di un contesto di archiviazione Oauth con solo il nome dell'account di archiviazione, il set di parametri predefinito è stato modificato in `OAuthParameterSet`</span><span class="sxs-lookup"><span data-stu-id="f310f-273">To support creating an Oauth storage context with only the storage account name, the default parameter set has been changed to `OAuthParameterSet`</span></span>
  - <span data-ttu-id="f310f-274">Esempio: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span><span class="sxs-lookup"><span data-stu-id="f310f-274">Example: `$ctx = New-AzureStorageContext -StorageAccountName $accountName`</span></span>
- <span data-ttu-id="f310f-275">Il parametro `Location` è diventato obbligatorio nel cmdlet `Get-AzStorageUsage`</span><span class="sxs-lookup"><span data-stu-id="f310f-275">The `Location` parameter has become mandatory in the `Get-AzStorageUsage` cmdlet</span></span>
- <span data-ttu-id="f310f-276">I metodi dell'API di archiviazione usano ora il Modello asincrono basato su attività (TAP), invece delle chiamate API sincrone.</span><span class="sxs-lookup"><span data-stu-id="f310f-276">The Storage API methods now use the Task-based Asynchronous Pattern (TAP), instead of synchronous API calls.</span></span>
#### <a name="1-blob-snapshot"></a><span data-ttu-id="f310f-277">1. Snapshot del BLOB</span><span class="sxs-lookup"><span data-stu-id="f310f-277">1. Blob Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="f310f-278">Prima:</span><span class="sxs-lookup"><span data-stu-id="f310f-278">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$b.ICloudBlob.Snapshot()
```

##### <a name="after"></a><span data-ttu-id="f310f-279">Dopo:</span><span class="sxs-lookup"><span data-stu-id="f310f-279">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -Context $ctx
$task = $b.ICloudBlob.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="2-share-snapshot"></a><span data-ttu-id="f310f-280">2. Snapshot di condivisione</span><span class="sxs-lookup"><span data-stu-id="f310f-280">2. Share Snapshot</span></span>
##### <a name="before"></a><span data-ttu-id="f310f-281">Prima:</span><span class="sxs-lookup"><span data-stu-id="f310f-281">Before:</span></span>
```powershell
$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$snapshot = $Share.Snapshot()
```
#####  <a name="after"></a><span data-ttu-id="f310f-282">Dopo:</span><span class="sxs-lookup"><span data-stu-id="f310f-282">After:</span></span>
```powershell

$Share = Get-AzureStorageShare -Name $containerName -Context $ctx
$task = $Share.SnapshotAsync()
$task.Wait()
$snapshot = $task.Result
```

#### <a name="3-undelete-a-soft-delete-blob"></a><span data-ttu-id="f310f-283">3. Annullare l'eliminazione di un BLOB di eliminazione temporanea</span><span class="sxs-lookup"><span data-stu-id="f310f-283">3. Undelete a soft delete blob</span></span>
##### <a name="before"></a><span data-ttu-id="f310f-284">Prima:</span><span class="sxs-lookup"><span data-stu-id="f310f-284">Before:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$b.ICloudBlob.Undelete()
```
##### <a name="after"></a><span data-ttu-id="f310f-285">Dopo:</span><span class="sxs-lookup"><span data-stu-id="f310f-285">After:</span></span>
```powershell
$b = Get-AzureStorageBlob -Container $containerName -Blob $blobName -IncludeDeleted -Context $ctx
$task = $b.ICloudBlob.UndeleteAsync()
$task.Wait()
```

#### <a name="4-set-blob-tier"></a><span data-ttu-id="f310f-286">4. Impostare il livello di BLOB</span><span class="sxs-lookup"><span data-stu-id="f310f-286">4. Set Blob Tier</span></span>
##### <a name="before"></a><span data-ttu-id="f310f-287">Prima:</span><span class="sxs-lookup"><span data-stu-id="f310f-287">Before:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$blockBlob.ICloudBlob.SetStandardBlobTier("hot")

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$pageBlob.ICloudBlob.SetPremiumBlobTier("P4")
```

##### <a name="after"></a><span data-ttu-id="f310f-288">Dopo:</span><span class="sxs-lookup"><span data-stu-id="f310f-288">After:</span></span>
```powershell
$blockBlob = Get-AzureStorageBlob -Container $containerName -Blob $blockBlobName -Context $ctx
$task = $blockBlob.ICloudBlob.SetStandardBlobTierAsync("hot")
$task.Wait()

$pageBlob = Get-AzureStorageBlob -Container $containerName -Blob $pageBlobName -Context $ctx
$task = $pageBlob.ICloudBlob.SetPremiumBlobTierAsync("P4")
$task.Wait()
```

### <a name="azwebsites-previously-azurermwebsites"></a><span data-ttu-id="f310f-289">Az.Websites (in precedenza AzureRM.Websites)</span><span class="sxs-lookup"><span data-stu-id="f310f-289">Az.Websites (previously AzureRM.Websites)</span></span>
- <span data-ttu-id="f310f-290">Sono state rimosse le proprietà deprecate dagli oggetti `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo` e `PSSite`</span><span class="sxs-lookup"><span data-stu-id="f310f-290">Removed deprecated properties from the `PSAppServicePlan`, `PSCertificate`, `PSCloningInfo`, and `PSSite` objects</span></span>