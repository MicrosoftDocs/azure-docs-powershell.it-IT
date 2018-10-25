---
title: Modifiche di rilievo in Microsoft Azure PowerShell 6.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 6.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 8b7b1422ba2881ca172e65dba61d4c4808cca7de
ms.sourcegitcommit: 5f946a535eccca0b3ddf3db8f617b32564a88938
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2018
ms.locfileid: "50000879"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-600"></a><span data-ttu-id="1abfb-103">Modifiche di rilievo in Microsoft Azure PowerShell 6.0.0</span><span class="sxs-lookup"><span data-stu-id="1abfb-103">Breaking changes for Microsoft Azure PowerShell 6.0.0</span></span>

<span data-ttu-id="1abfb-104">Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1abfb-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="1abfb-105">Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="1abfb-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="1abfb-106">Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="1abfb-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="1abfb-107">Sommario</span><span class="sxs-lookup"><span data-stu-id="1abfb-107">Table of Contents</span></span>

- [<span data-ttu-id="1abfb-108">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="1abfb-108">General breaking changes</span></span>](#general-breaking-changes)
    - [<span data-ttu-id="1abfb-109">Versione minima richiesta di PowerShell innalzata alla 5.0</span><span class="sxs-lookup"><span data-stu-id="1abfb-109">Minimum PowerShell version required bumped to 5.0</span></span>](#minimum-powershell-version-required-bumped-to-50)
    - [<span data-ttu-id="1abfb-110">Salvataggio automatico del contesto abilitato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1abfb-110">Context autosaved enabled by default</span></span>](#context-autosave-enabled-by-default)
    - [<span data-ttu-id="1abfb-111">Rimozione dell'alias Tags</span><span class="sxs-lookup"><span data-stu-id="1abfb-111">Removal of Tags alias</span></span>](#removal-of-tags-alias)
- [<span data-ttu-id="1abfb-112">Modifiche di rilievo ai cmdlet di AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1abfb-112">Breaking changes to AzureRM.Compute cmdlets</span></span>](#breaking-changes-to-azurermcompute-cmdlets)
- [<span data-ttu-id="1abfb-113">Modifiche di rilievo ai cmdlet di AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1abfb-113">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>](#breaking-changes-to-azurermdatalakestore-cmdlets)
- [<span data-ttu-id="1abfb-114">Modifiche di rilievo ai cmdlet di AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1abfb-114">Breaking changes to AzureRM.Dns cmdlets</span></span>](#breaking-changes-to-azurermdns-cmdlets)
- [<span data-ttu-id="1abfb-115">Modifiche di rilievo ai cmdlet di AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1abfb-115">Breaking changes to AzureRM.Insights cmdlets</span></span>](#breaking-changes-to-azurerminsights-cmdlets)
- [<span data-ttu-id="1abfb-116">Modifiche di rilievo ai cmdlet di AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1abfb-116">Breaking changes to AzureRM.KeyVault cmdlets</span></span>](#breaking-changes-to-azurermkeyvault-cmdlets)
- [<span data-ttu-id="1abfb-117">Modifiche di rilievo ai cmdlet di AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1abfb-117">Breaking changes to AzureRM.Network cmdlets</span></span>](#breaking-changes-to-azurermnetwork-cmdlets)
- [<span data-ttu-id="1abfb-118">Modifiche di rilievo ai cmdlet di AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1abfb-118">Breaking changes to AzureRM.RedisCache cmdlets</span></span>](#breaking-changes-to-azurermrediscache-cmdlets)
- [<span data-ttu-id="1abfb-119">Modifiche di rilievo ai cmdlet di AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1abfb-119">Breaking changes to AzureRM.Resources cmdlets</span></span>](#breaking-changes-to-azurermresources-cmdlets)
- [<span data-ttu-id="1abfb-120">Modifiche di rilievo ai cmdlet di AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1abfb-120">Breaking changes to AzureRM.Storage cmdlets</span></span>](#breaking-changes-to-azurermstorage-cmdlets)
- [<span data-ttu-id="1abfb-121">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-121">Removed modules</span></span>](#removed-modules)
    - [`AzureRM.ServerManagement`](#azurermservermanagement)
    - [`AzureRM.SiteRecovery`](#azurermsiterecovery)

## <a name="general-breaking-changes"></a><span data-ttu-id="1abfb-122">Modifiche di rilievo di carattere generale</span><span class="sxs-lookup"><span data-stu-id="1abfb-122">General breaking changes</span></span>

### <a name="minimum-powershell-version-required-bumped-to-50"></a><span data-ttu-id="1abfb-123">Versione minima richiesta di PowerShell innalzata alla 5.0</span><span class="sxs-lookup"><span data-stu-id="1abfb-123">Minimum PowerShell version required bumped to 5.0</span></span>

<span data-ttu-id="1abfb-124">In precedenza per eseguire qualsiasi cmdlet con Azure PowerShell era necessaria _almeno_ la versione 3.0 di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1abfb-124">Previously, Azure PowerShell required _at least_ version 3.0 of PowerShell to run any cmdlet.</span></span> <span data-ttu-id="1abfb-125">In futuro, questo requisito verrà innalzato alla versione 5.0 di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1abfb-125">Moving forward, this requirement will be raised to version 5.0 of PowerShell.</span></span> <span data-ttu-id="1abfb-126">Per informazioni sull'aggiornamento a PowerShell 5.0, vedere [questa tabella](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span><span class="sxs-lookup"><span data-stu-id="1abfb-126">For information on upgrading to PowerShell 5.0, please see [this table](https://docs.microsoft.com/powershell/scripting/setup/installing-windows-powershell?view=powershell-6#upgrading-existing-windows-powershell).</span></span>

### <a name="context-autosave-enabled-by-default"></a><span data-ttu-id="1abfb-127">Salvataggio automatico del contesto abilitato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1abfb-127">Context autosave enabled by default</span></span>

<span data-ttu-id="1abfb-128">Per salvataggio automatico del contesto si intende l'archiviazione delle informazioni di accesso di Azure che è possibile usare tra sessioni nuove e diverse di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1abfb-128">Context autosave is the storage of Azure sign in information that can be used between new and different PowerShell sessions.</span></span> <span data-ttu-id="1abfb-129">Per altre informazioni sul salvataggio automatico del contesto, vedere [questo documento](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="1abfb-129">For more information on context autosave, please see [this document](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="1abfb-130">In precedenza, il salvataggio automatico del contesto era disabilitato per impostazione predefinita, di conseguenza le informazioni di autenticazione di Azure dell'utente non venivano archiviate tra una sessione e l'altra finché non veniva eseguito il cmdlet `Enable-AzureRmContextAutosave` per attivare la persistenza del contesto.</span><span class="sxs-lookup"><span data-stu-id="1abfb-130">Previously by default, context autosave was disabled, which meant the user's Azure authentication information was not stored between sessions until they ran the `Enable-AzureRmContextAutosave` cmdlet to turn on context persistence.</span></span> <span data-ttu-id="1abfb-131">In futuro il salvataggio automatico del contesto verrà abilitato per impostazione predefinita, di conseguenza il contesto degli utenti per i quali _non sono disponibili impostazioni salvate per il salvataggio automatico del contesto_ verrà archiviato al successivo accesso.</span><span class="sxs-lookup"><span data-stu-id="1abfb-131">Moving forward, context autosave will be enabled by default, which means that users _with no saved context autosave settings_ will have their context stored the next time they sign in.</span></span> <span data-ttu-id="1abfb-132">Gli utenti possono rifiutare esplicitamente questa funzionalità usando il cmdlet `Disable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-132">Users can opt out of this functionality by using the `Disable-AzureRmContextAutosave` cmdlet.</span></span>

<span data-ttu-id="1abfb-133">_Nota_: questa modifica non riguarderà gli utenti che in precedenza avevano disabilitato il salvataggio automatico del contesto oppure gli utenti con salvataggio automatico del contesto abilitato e contesti esistenti</span><span class="sxs-lookup"><span data-stu-id="1abfb-133">_Note_: users that previously disabled context autosave or users with context autosave enabled and existing contexts will not be affected by this change</span></span>

### <a name="removal-of-tags-alias"></a><span data-ttu-id="1abfb-134">Rimozione dell'alias Tags</span><span class="sxs-lookup"><span data-stu-id="1abfb-134">Removal of Tags alias</span></span>

<span data-ttu-id="1abfb-135">L'alias `Tags` per il parametro `Tag` è stato rimosso in numerosi cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abfb-135">The alias `Tags` for the `Tag` parameter has been removed across numerous cmdlets.</span></span> <span data-ttu-id="1abfb-136">Di seguito è riportato un elenco di moduli (e dei cmdlet corrispondenti) interessati:</span><span class="sxs-lookup"><span data-stu-id="1abfb-136">Below is a list of modules (and the corresponding cmdlets) affected by this:</span></span>

#### `AzureRM.ApiManagement`

- `New-AzureRmApiManagement`
- `New-AzureRmApiManagementProperty`
- `Set-AzureRmApiManagementProperty`

#### `AzureRM.Automation`
- `Set-AzureRmAutomationRunbook`

#### `AzureRM.Cdn`
- `New-AzureRmCdnEndpoint`
- `New-AzureRmCdnProfile`

#### `AzureRM.Compute`
- `New-AzureRmVM`
- `Update-AzureRmVM`

#### `AzureRM.DataFactories`
- `New-AzureRmDataFactories`

#### `AzureRM.DataLakeAnalytics`
- `New-AzureRmDataLakeAnalyticsAccount`

#### `AzureRM.DataLakeStore`
- `New-AzureRmDataLakeStoreAccount`
- `Set-AzureRmDataLakeStoreAccount`

#### `AzureRM.MachineLearning`
- `Update-AzureRmMlCommitmentPlan`

#### `AzureRM.Media`
- `Set-AzureRmMediaService`

#### `AzureRM.OperationalInsights`
- `New-AzureRmOperationalInsightsSavedSearch`
- `New-AzureRmOperationalInsightsWorkspace`
- `Set-AzureRmOperationalInsightsSavedSearch`
- `Set-AzureRmOperationalInsightsWorkspace`

## <a name="breaking-changes-to-azurermcompute-cmdlets"></a><span data-ttu-id="1abfb-137">Modifiche di rilievo ai cmdlet di AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="1abfb-137">Breaking changes to AzureRM.Compute cmdlets</span></span>

<span data-ttu-id="1abfb-138">**Varie**</span><span class="sxs-lookup"><span data-stu-id="1abfb-138">**Miscellaneous**</span></span>
- <span data-ttu-id="1abfb-139">La proprietà del nome dello SKU annidata nei tipi `PSDisk` e `PSSnapshot` è cambiata rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-139">The sku name property nested in types `PSDisk` and `PSSnapshot` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$disk = Get-AzureRmDisk -ResourceGroupName "MyResourceGroup" -DiskName "MyDiskName"
$disk.Sku.Name       # This will now return Standard_LRS or Premium_LRS

$snapshot = Get-AzureRmSnapshot -ResourceGroupName "MyResourceGroup" -SnapshotName "MySnapshotName"
$snapshot.Sku.Name   # This will now return Standard_LRS or Premium_LRS
```

- <span data-ttu-id="1abfb-140">La proprietà del tipo di account di archiviazione annidata nei tipi `PSVirtualMachine`, `PSVirtualMachineScaleSet` e `PSImage` è cambiata rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-140">The storage account type property nested in types `PSVirtualMachine`, `PSVirtualMachineScaleSet` and `PSImage` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

```powershell
$vm = Get-AzureRmVM -ResourceGroupName "MyResourceGroup" -Name "MyVM"
$vm.StorageProfile.DataDisks[0].ManagedDisk.StorageAccountType   # This will now return Standard_LRS or Premium_LRS
```

<span data-ttu-id="1abfb-141">**Add-AzureRmImageDataDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-141">**Add-AzureRmImageDataDisk**</span></span>
- <span data-ttu-id="1abfb-142">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-142">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-143">**Add-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-143">**Add-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="1abfb-144">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-144">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-145">**Add-AzureRmVmssDataDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-145">**Add-AzureRmVmssDataDisk**</span></span>
- <span data-ttu-id="1abfb-146">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-146">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-147">**New-AzureRmAvailabilitySet**</span><span class="sxs-lookup"><span data-stu-id="1abfb-147">**New-AzureRmAvailabilitySet**</span></span>
- <span data-ttu-id="1abfb-148">Il parametro `Managed` è stato rimosso a favore di `Sku`</span><span class="sxs-lookup"><span data-stu-id="1abfb-148">The parameter `Managed` was removed in favor of `Sku`</span></span>

```powershell
# Old
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Managed

# New
New-AzureRmAvailabilitySet -ResourceGroupName "MyRG" -Name "MyAvailabilitySet" -Location "West US" -Sku "Aligned"
```

<span data-ttu-id="1abfb-149">**New-AzureRmDiskConfig**</span><span class="sxs-lookup"><span data-stu-id="1abfb-149">**New-AzureRmDiskConfig**</span></span>
- <span data-ttu-id="1abfb-150">I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-150">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-151">**New-AzureRmDiskUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="1abfb-151">**New-AzureRmDiskUpdateConfig**</span></span>
- <span data-ttu-id="1abfb-152">I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-152">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-153">**New-AzureRmSnapshotConfig**</span><span class="sxs-lookup"><span data-stu-id="1abfb-153">**New-AzureRmSnapshotConfig**</span></span>
- <span data-ttu-id="1abfb-154">I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-154">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-155">**New-AzureRmSnapshotUpdateConfig**</span><span class="sxs-lookup"><span data-stu-id="1abfb-155">**New-AzureRmSnapshotUpdateConfig**</span></span>
- <span data-ttu-id="1abfb-156">I valori accettati per il parametro `SkuName` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-156">The accepted values for parameter `SkuName` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-157">**Set-AzureRmImageOsDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-157">**Set-AzureRmImageOsDisk**</span></span>
- <span data-ttu-id="1abfb-158">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-158">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-159">**Set-AzureRmVMAEMExtension**</span><span class="sxs-lookup"><span data-stu-id="1abfb-159">**Set-AzureRmVMAEMExtension**</span></span>
- <span data-ttu-id="1abfb-160">Il parametro `DisableWAD` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-160">The parameter `DisableWAD` was removed</span></span>
    -  <span data-ttu-id="1abfb-161">Diagnostica di Microsoft Azure è disabilitato per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="1abfb-161">Windows Azure Diagnostics is disabled by default</span></span>

<span data-ttu-id="1abfb-162">**Set-AzureRmVMDataDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-162">**Set-AzureRmVMDataDisk**</span></span>
- <span data-ttu-id="1abfb-163">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-163">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-164">**Set-AzureRmVMOSDisk**</span><span class="sxs-lookup"><span data-stu-id="1abfb-164">**Set-AzureRmVMOSDisk**</span></span>
- <span data-ttu-id="1abfb-165">I valori accettati per il parametro `StorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-165">The accepted values for parameter `StorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-166">**Set-AzureRmVmssStorageProfile**</span><span class="sxs-lookup"><span data-stu-id="1abfb-166">**Set-AzureRmVmssStorageProfile**</span></span>
- <span data-ttu-id="1abfb-167">I valori accettati per il parametro `ManagedDisk` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-167">The accepted values for parameter `ManagedDisk` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

<span data-ttu-id="1abfb-168">**Update-AzureRmVmss**</span><span class="sxs-lookup"><span data-stu-id="1abfb-168">**Update-AzureRmVmss**</span></span>
- <span data-ttu-id="1abfb-169">I valori accettati per il parametro `ManagedDiskStorageAccountType` sono cambiati rispettivamente da `StandardLRS` e `PremiumLRS` in `Standard_LRS` e `Premium_LRS`</span><span class="sxs-lookup"><span data-stu-id="1abfb-169">The accepted values for parameter `ManagedDiskStorageAccountType` changed from `StandardLRS` and `PremiumLRS` to `Standard_LRS` and `Premium_LRS`, respectively</span></span>

## <a name="breaking-changes-to-azurermdatalakestore-cmdlets"></a><span data-ttu-id="1abfb-170">Modifiche di rilievo ai cmdlet di AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="1abfb-170">Breaking changes to AzureRM.DataLakeStore cmdlets</span></span>

<span data-ttu-id="1abfb-171">**Export-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="1abfb-171">**Export-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="1abfb-172">I parametri `PerFileThreadCount` e `ConcurrentFileCount` sono stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="1abfb-172">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="1abfb-173">In futuro usare il parametro `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="1abfb-173">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Export-AzureRmDataLakeStoreItem -Account contoso -Path /test -Destination C:\test -Recurse -Resume -Concurrency 160
```

<span data-ttu-id="1abfb-174">**Import-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="1abfb-174">**Import-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="1abfb-175">I parametri `PerFileThreadCount` e `ConcurrentFileCount` sono stati rimossi.</span><span class="sxs-lookup"><span data-stu-id="1abfb-175">Parameters `PerFileThreadCount` and `ConcurrentFileCount` were removed.</span></span> <span data-ttu-id="1abfb-176">In futuro usare il parametro `Concurrency`</span><span class="sxs-lookup"><span data-stu-id="1abfb-176">Please use the `Concurrency` parameter moving forward</span></span>

```powershell
# Old
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -PerFileThreadCount 2 -ConcurrentFileCount 80

# New
Import-AzureRmDataLakeStoreItem -Account contoso -Path C:\test -Destination /test -Recurse -Resume -ForceBinary -Concurrency 160
```

<span data-ttu-id="1abfb-177">**Remove-AzureRmDataLakeStoreItem**</span><span class="sxs-lookup"><span data-stu-id="1abfb-177">**Remove-AzureRmDataLakeStoreItem**</span></span>
- <span data-ttu-id="1abfb-178">Il parametro `Clean` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-178">Parameter `Clean` was removed</span></span>

```powershell
# Old
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse -Clean

# New
Remove-AzureRmDataLakeStoreItem -Account "ContosoADL" -path /myFolder -Recurse
```

## <a name="breaking-changes-to-azurermdns-cmdlets"></a><span data-ttu-id="1abfb-179">Modifiche di rilievo ai cmdlet di AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="1abfb-179">Breaking changes to AzureRM.Dns cmdlets</span></span>

<span data-ttu-id="1abfb-180">**New-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="1abfb-180">**New-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="1abfb-181">Il parametro `Force` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-181">The parameter `Force` was removed</span></span>

<span data-ttu-id="1abfb-182">**Remove-AzureRmDnsRecordSet**</span><span class="sxs-lookup"><span data-stu-id="1abfb-182">**Remove-AzureRmDnsRecordSet**</span></span>
- <span data-ttu-id="1abfb-183">Il parametro `Force` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-183">The parameter `Force` was removed</span></span>

<span data-ttu-id="1abfb-184">**Remove-AzureRmDnsZone**</span><span class="sxs-lookup"><span data-stu-id="1abfb-184">**Remove-AzureRmDnsZone**</span></span>
- <span data-ttu-id="1abfb-185">Il parametro `Force` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-185">The parameter `Force` was removed</span></span>

## <a name="breaking-changes-to-azurerminsights-cmdlets"></a><span data-ttu-id="1abfb-186">Modifiche di rilievo ai cmdlet di AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="1abfb-186">Breaking changes to AzureRM.Insights cmdlets</span></span>

<span data-ttu-id="1abfb-187">**Add-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="1abfb-187">**Add-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="1abfb-188">Gli alias di parametro `AutoscaleProfiles` e `Notifications` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-188">The parameter aliases `AutoscaleProfiles` and `Notifications` were removed</span></span>

<span data-ttu-id="1abfb-189">**Add-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="1abfb-189">**Add-AzureRmLogProfile**</span></span>
- <span data-ttu-id="1abfb-190">Gli alias di parametro `Categories` e `Locations` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-190">The parameter aliases `Categories` and `Locations` were removed</span></span>

<span data-ttu-id="1abfb-191">**Add-AzureRmMetricAlertRule**</span><span class="sxs-lookup"><span data-stu-id="1abfb-191">**Add-AzureRmMetricAlertRule**</span></span>
- <span data-ttu-id="1abfb-192">L'alias di parametro `Actions` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-192">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="1abfb-193">**Add-AzureRmWebtestAlertRule**</span><span class="sxs-lookup"><span data-stu-id="1abfb-193">**Add-AzureRmWebtestAlertRule**</span></span>
- <span data-ttu-id="1abfb-194">L'alias di parametro `Actions` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-194">The parameter alias `Actions` was removed</span></span>

<span data-ttu-id="1abfb-195">**Get-AzureRmLog**</span><span class="sxs-lookup"><span data-stu-id="1abfb-195">**Get-AzureRmLog**</span></span>
- <span data-ttu-id="1abfb-196">Gli alias di parametro `MaxRecords` e `MaxEvents` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-196">The parameter aliases `MaxRecords` and `MaxEvents` were removed</span></span>

<span data-ttu-id="1abfb-197">**Get-AzureRmMetricDefinition**</span><span class="sxs-lookup"><span data-stu-id="1abfb-197">**Get-AzureRmMetricDefinition**</span></span>
- <span data-ttu-id="1abfb-198">L'alias di parametro `MetricNames` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-198">The parameter alias `MetricNames` was removed</span></span>

<span data-ttu-id="1abfb-199">**New-AzureRmAlertRuleEmail**</span><span class="sxs-lookup"><span data-stu-id="1abfb-199">**New-AzureRmAlertRuleEmail**</span></span>
- <span data-ttu-id="1abfb-200">Gli alias di parametro `CustomEmails` e `SendToServiceOwners` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-200">The parameter aliases `CustomEmails` and `SendToServiceOwners` were removed</span></span>

<span data-ttu-id="1abfb-201">**New-AzureRmAlertRuleWebhook**</span><span class="sxs-lookup"><span data-stu-id="1abfb-201">**New-AzureRmAlertRuleWebhook**</span></span>
- <span data-ttu-id="1abfb-202">L'alias di parametro `Properties` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-202">The parameter alias `Properties` was removed</span></span>

<span data-ttu-id="1abfb-203">**New-AzureRmAutoscaleNotification**</span><span class="sxs-lookup"><span data-stu-id="1abfb-203">**New-AzureRmAutoscaleNotification**</span></span>
- <span data-ttu-id="1abfb-204">Gli alias di parametro `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` e `Webhooks` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-204">The parameter aliases `CustomEmails`, `SendEmailToSubscriptionCoAdministrators` and `Webhooks` were removed</span></span>

<span data-ttu-id="1abfb-205">**New-AzureRmAutoscaleProfile**</span><span class="sxs-lookup"><span data-stu-id="1abfb-205">**New-AzureRmAutoscaleProfile**</span></span>
- <span data-ttu-id="1abfb-206">Gli alias di parametro `Rules`, `ScheduleDays`, `ScheduleHours` e `ScheduleMinutes` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-206">The parameter aliases `Rules`, `ScheduleDays`, `ScheduleHours` and `ScheduleMinutes` were removed</span></span>

<span data-ttu-id="1abfb-207">**New-AzureRmAutoscaleWebhook**</span><span class="sxs-lookup"><span data-stu-id="1abfb-207">**New-AzureRmAutoscaleWebhook**</span></span>
- <span data-ttu-id="1abfb-208">L'alias di parametro `Properties` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-208">The parameter alias `Properties` was removed</span></span>

## <a name="breaking-changes-to-azurermkeyvault-cmdlets"></a><span data-ttu-id="1abfb-209">Modifiche di rilievo ai cmdlet di AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="1abfb-209">Breaking changes to AzureRM.KeyVault cmdlets</span></span>

<span data-ttu-id="1abfb-210">**Add-AzureKeyVaultCertificate**</span><span class="sxs-lookup"><span data-stu-id="1abfb-210">**Add-AzureKeyVaultCertificate**</span></span>
- <span data-ttu-id="1abfb-211">Il parametro `CertificatePolicy` è diventato obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1abfb-211">The `CertificatePolicy` parameter has become mandatory.</span></span>

<span data-ttu-id="1abfb-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span><span class="sxs-lookup"><span data-stu-id="1abfb-212">**Set-AzureKeyVaultManagedStorageSasDefinition**</span></span>
- <span data-ttu-id="1abfb-213">Il cmdlet non accetta più parametri singoli che costituiscono il token di accesso, ma sostituisce i parametri di token espliciti, ad esempio `Service` oppure `Permissions`, con un parametro `TemplateUri` generico, che corrisponde a un token di accesso di esempio definito altrove, presumibilmente con i cmdlet PowerShell di Archiviazione o creato manualmente in base alla documentazione di Archiviazione. Il cmdlet mantiene il parametro `ValidityPeriod`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-213">The cmdlet no longer accepts individual parameters that compose the access token; instead, the cmdlet replaces explicit token parameters, such as `Service` or `Permissions`, with a generic `TemplateUri` parameter, corresponding to a sample access token defined elsewhere (presumably using Storage PowerShell cmdlets, or composed manually according to the Storage documentation.) The cmdlet retains the `ValidityPeriod` parameter.</span></span>

<span data-ttu-id="1abfb-214">Per altre informazioni sulla creazione di token di accesso condivisi per Archiviazione di Azure, vedere le pagine della documentazione e in particolare:</span><span class="sxs-lookup"><span data-stu-id="1abfb-214">For more information on composing shared access tokens for Azure Storage, please refer to the documentation pages, respectively:</span></span>
- <span data-ttu-id="1abfb-215">[Creazione di una firma di accesso condiviso del servizio] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span><span class="sxs-lookup"><span data-stu-id="1abfb-215">[Constructing a Service SAS] (https://docs.microsoft.com/rest/api/storageservices/Constructing-a-Service-SAS)</span></span>
- <span data-ttu-id="1abfb-216">[Creazione di una firma di accesso condiviso dell'account] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span><span class="sxs-lookup"><span data-stu-id="1abfb-216">[Constructing an Account SAS] (https://docs.microsoft.com/rest/api/storageservices/constructing-an-account-sas)</span></span>

```powershell
# Old
$sas = Set-AzureKeyVaultManagedStorageSasDefinition -VaultName myVault -Name myKey -Service Blob -Permissions 'rcw' -ValidityPeriod 180d

# New
$sctx=New-AzureStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
$start=[System.DateTime]::Now.AddDays(-1)
$end=[System.DateTime]::Now.AddMonths(1)
$at=New-AzureStorageAccountSasToken -Service blob -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
$sas=Set-AzureKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
```

<span data-ttu-id="1abfb-217">**Set-AzureKeyVaultCertificateIssuer**</span><span class="sxs-lookup"><span data-stu-id="1abfb-217">**Set-AzureKeyVaultCertificateIssuer**</span></span>
- <span data-ttu-id="1abfb-218">Il parametro `IssuerProvider` è diventato obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="1abfb-218">The `IssuerProvider` parameter has become mandatory.</span></span>

<span data-ttu-id="1abfb-219">**Undo-AzureKeyVaultCertificateRemoval**</span><span class="sxs-lookup"><span data-stu-id="1abfb-219">**Undo-AzureKeyVaultCertificateRemoval**</span></span>
- <span data-ttu-id="1abfb-220">L'output di questo cmdlet è cambiato da `CertificateBundle` in `PSKeyVaultCertificate`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-220">The output of this cmdlet has changed from `CertificateBundle` to `PSKeyVaultCertificate`.</span></span>

<span data-ttu-id="1abfb-221">**Undo-AzureRmKeyVaultRemoval**</span><span class="sxs-lookup"><span data-stu-id="1abfb-221">**Undo-AzureRmKeyVaultRemoval**</span></span>
- <span data-ttu-id="1abfb-222">`ResourceGroupName` è stato rimosso dal set di parametri di `InputObject` e viene invece ottenuto dalla proprietà `ResourceId` del parametro `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-222">`ResourceGroupName` has been removed from the `InputObject` parameter set, and is instead obtained from the `InputObject` parameter's `ResourceId` property.</span></span>

<span data-ttu-id="1abfb-223">**Set-AzureRmKeyVaultAccessPolicy**</span><span class="sxs-lookup"><span data-stu-id="1abfb-223">**Set-AzureRmKeyVaultAccessPolicy**</span></span>
- <span data-ttu-id="1abfb-224">L'autorizzazione `all` è stata rimossa da `PermissionsToKeys`, `PermissionsToSecrets` e `PermissionsToCertificates`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-224">The `all` permission was removed from `PermissionsToKeys`, `PermissionsToSecrets`, and `PermissionsToCertificates`.</span></span>

<span data-ttu-id="1abfb-225">**Generale**</span><span class="sxs-lookup"><span data-stu-id="1abfb-225">**General**</span></span>
- <span data-ttu-id="1abfb-226">La proprietà `ValueFromPipelineByPropertyName` è stata rimossa da tutti i cmdlet in cui era abilitato il piping tramite `InputObject`.</span><span class="sxs-lookup"><span data-stu-id="1abfb-226">The `ValueFromPipelineByPropertyName` property was removed from all cmdlets where piping by `InputObject` was enabled.</span></span>  <span data-ttu-id="1abfb-227">I cmdlet interessati sono:</span><span class="sxs-lookup"><span data-stu-id="1abfb-227">The cmdlets affected are:</span></span>
    - `Add-AzureKeyVaultCertificate`
    - `Add-AzureKeyVaultCertificateContact`
    - `Add-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultKey`
    - `Backup-AzureKeyVaultSecret`
    - `Get-AzureKeyVaultCertficate`
    - `Get-AzureKeyVaultCertificateContact`
    - `Get-AzureKeyVaultCertificateIssuer`
    - `Get-AzureKeyVaultCertificateOperation`
    - `Get-AzureKeyVaultCertificatePolicy`
    - `Get-AzureKeyVaultKey`
    - `Get-AzureKeyVaultManagedStorageAccount`
    - `Get-AzureKeyVaultManagedStorageSasDefinition`
    - `Get-AzureKeyVaultSecret`
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureRmKeyVaultAccessPolicy`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateContact`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Restore-AzureKeyVaultKey`
    - `Restore-AzureKeyVaultSecret`
    - `Set-AzureRmKeyVaultAccessPolicy`
    - `Set-AzureKeyVaultCertificateAttribute`
    - `Set-AzureKeyVaultCertificateIssuer`
    - `Set-AzureKeyVaultCertificatePolicy`
    - `Set-AzureKeyVaultKeyAttribute`
    - `Set-AzureKeyVaultManagedStorageSasDefinition`
    - `Set-AzureKeyVaultSecret`
    - `Set-AzureKeyVaultSecretAttribute`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Undo-AzureKeyVaultCertificateRemoval`
    - `Undo-AzureKeyVaultKeyRemoval`
    - `Undo-AzureRmKeyVaultRemoval`
    - `Undo-AzureKeyVaultSecretRemoval`
    - `Update-AzureKeyVaultManagedStorageAccount`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="1abfb-228">I livelli `ConfirmImpact` sono stati rimossi da tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abfb-228">`ConfirmImpact` levels were removed from all cmdlets.</span></span>  <span data-ttu-id="1abfb-229">I cmdlet interessati sono:</span><span class="sxs-lookup"><span data-stu-id="1abfb-229">The cmdlets affected are:</span></span>
    - `Remove-AzureRmKeyVault`
    - `Remove-AzureKeyVaultCertificate`
    - `Remove-AzureKeyVaultCertificateIssuer`
    - `Remove-AzureKeyVaultCertificateOperation`
    - `Remove-AzureKeyVaultKey`
    - `Remove-AzureKeyVaultManagedStorageAccount`
    - `Remove-AzureKeyVaultManagedStorageSasDefinition`
    - `Remove-AzureKeyVaultSecret`
    - `Stop-AzureKeyVaultCertificateOperation`
    - `Update-AzureKeyVaultManagedStorageAccountKey`

- <span data-ttu-id="1abfb-230">Il cmdlet `IKeyVaultDataServiceClient` è stato aggiornato in modo che tutte le operazioni relative ai certificati restituiscano PSTypes invece di tipi SDK.</span><span class="sxs-lookup"><span data-stu-id="1abfb-230">The `IKeyVaultDataServiceClient` was updated so all Certificate operations return PSTypes instead of SDK types.</span></span> <span data-ttu-id="1abfb-231">Sono inclusi:</span><span class="sxs-lookup"><span data-stu-id="1abfb-231">This includes:</span></span>
    - `SetCertificateContacts`
    - `GetCertificateContacts`
    - `GetCertificate`
    - `GetDeletedCertificate`
    - `MergeCertificate`
    - `ImportCertificate`
    - `DeleteCertificate`
    - `RecoverCertificate`
    - `EnrollCertificate`
    - `UpdateCertificate`
    - `GetCertificateOperation`
    - `DeleteCertificateOperation`
    - `CancelCertificateOperation`
    - `GetCertificatePolicy`
    - `UpdateCertificatePolicy`
    - `GetCertificateIssuer`
    - `SetCertificateIssuer`
    - `DeleteCertificateIssuer`

## <a name="breaking-changes-to-azurermnetwork-cmdlets"></a><span data-ttu-id="1abfb-232">Modifiche di rilievo ai cmdlet di AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="1abfb-232">Breaking changes to AzureRM.Network cmdlets</span></span>


<span data-ttu-id="1abfb-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="1abfb-233">**Add-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="1abfb-234">Il parametro `ProbeEnabled` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-234">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="1abfb-235">**Add-AzureRmVirtualNetworkPeering**</span><span class="sxs-lookup"><span data-stu-id="1abfb-235">**Add-AzureRmVirtualNetworkPeering**</span></span>
- <span data-ttu-id="1abfb-236">L'alias di parametro `AlloowGatewayTransit` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-236">The parameter alias `AlloowGatewayTransit` was removed</span></span>

<span data-ttu-id="1abfb-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="1abfb-237">**New-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="1abfb-238">Il parametro `ProbeEnabled` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-238">The parameter `ProbeEnabled` was removed</span></span>

<span data-ttu-id="1abfb-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span><span class="sxs-lookup"><span data-stu-id="1abfb-239">**Set-AzureRmApplicationGatewayBackendHttpSettings**</span></span>
- <span data-ttu-id="1abfb-240">Il parametro `ProbeEnabled` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-240">The parameter `ProbeEnabled` was removed</span></span>

## <a name="breaking-changes-to-azurermrediscache-cmdlets"></a><span data-ttu-id="1abfb-241">Modifiche di rilievo ai cmdlet di AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="1abfb-241">Breaking changes to AzureRM.RedisCache cmdlets</span></span>

<span data-ttu-id="1abfb-242">**New-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="1abfb-242">**New-AzureRmRedisCache**</span></span>
- <span data-ttu-id="1abfb-243">I parametri `Subnet` e `VirtualNetwork` sono stati rimossi a favore di `SubnetId`</span><span class="sxs-lookup"><span data-stu-id="1abfb-243">The parameters `Subnet` and `VirtualNetwork` were removed in favor of `SubnetId`</span></span>
- <span data-ttu-id="1abfb-244">Il parametro `RedisVersion` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-244">The parameter `RedisVersion` was removed</span></span>
- <span data-ttu-id="1abfb-245">Il parametro `MaxMemoryPolicy` è stato rimosso a favore di `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="1abfb-245">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -MaxMemoryPolicy "allkeys-lru"

# New
New-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -Location "North Central US" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

<span data-ttu-id="1abfb-246">**Set-AzureRmRedisCache**</span><span class="sxs-lookup"><span data-stu-id="1abfb-246">**Set-AzureRmRedisCache**</span></span>
- <span data-ttu-id="1abfb-247">Il parametro `MaxMemoryPolicy` è stato rimosso a favore di `RedisConfiguration`</span><span class="sxs-lookup"><span data-stu-id="1abfb-247">The parameter `MaxMemoryPolicy` was removed in favor of `RedisConfiguration`</span></span>

```powershell
# Old
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -MaxMemoryPolicy "allkeys-lru"

# New
Set-AzureRmRedisCache -ResourceGroupName "MyRG" -Name "MyRedisCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}
```

## <a name="breaking-changes-to-azurermresources-cmdlets"></a><span data-ttu-id="1abfb-248">Modifiche di rilievo ai cmdlet di AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="1abfb-248">Breaking changes to AzureRM.Resources cmdlets</span></span>

<span data-ttu-id="1abfb-249">**Find-AzureRmResource**</span><span class="sxs-lookup"><span data-stu-id="1abfb-249">**Find-AzureRmResource**</span></span>
- <span data-ttu-id="1abfb-250">Questo cmdlet è stato rimosso e la funzionalità è stata spostata in `Get-AzureRmResource`</span><span class="sxs-lookup"><span data-stu-id="1abfb-250">This cmdlet was removed and the functionality was moved into `Get-AzureRmResource`</span></span>

```powershell
# Old
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupNameContains "ResourceGroup"
Find-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceNameContains "test"

# New
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -ResourceGroupName "*ResourceGroup*"
Get-AzureRmResource -ResourceType "Microsoft.Web/sites" -Name "*test*"
```

<span data-ttu-id="1abfb-251">**Find-AzureRmResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="1abfb-251">**Find-AzureRmResourceGroup**</span></span>
- <span data-ttu-id="1abfb-252">Questo cmdlet è stato rimosso e la funzionalità è stata spostata in `Get-AzureRmResourceGroup`</span><span class="sxs-lookup"><span data-stu-id="1abfb-252">This cmdlet was removed and the functionality was moved into `Get-AzureRmResourceGroup`</span></span>

```powershell
# Old
Find-AzureRmResourceGroup
Find-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Find-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }

# New
Get-AzureRmResourceGroup
Get-AzureRmResourceGroup -Tag @{ "testtag" = $null }
Get-AzureRmResourceGroup -Tag @{ "testtag" = "testval" }
```

<span data-ttu-id="1abfb-253">**Get-AzureRmRoleDefinition**</span><span class="sxs-lookup"><span data-stu-id="1abfb-253">**Get-AzureRmRoleDefinition**</span></span>
- <span data-ttu-id="1abfb-254">Il parametro `AtScopeAndBelow` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="1abfb-254">Parameter `AtScopeAndBelow` was removed.</span></span>

```powershell

# Old
Get-AzureRmRoleDefinition [other required parameters] -AtScopeAndBelow

# New
Get-AzureRmRoleDefinition [other required parameters]
```

## <a name="breaking-changes-to-azurermstorage-cmdlets"></a><span data-ttu-id="1abfb-255">Modifiche di rilievo ai cmdlet di AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="1abfb-255">Breaking changes to AzureRM.Storage cmdlets</span></span>

<span data-ttu-id="1abfb-256">**New-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="1abfb-256">**New-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="1abfb-257">Il parametro `EnableEncryptionService` è stato rimosso</span><span class="sxs-lookup"><span data-stu-id="1abfb-257">The parameter `EnableEncryptionService` was removed</span></span>

<span data-ttu-id="1abfb-258">**Set-AzureRmStorageAccount**</span><span class="sxs-lookup"><span data-stu-id="1abfb-258">**Set-AzureRmStorageAccount**</span></span>
- <span data-ttu-id="1abfb-259">I parametri `EnableEncryptionService` e `DisableEncryptionService` sono stati rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-259">The parameters `EnableEncryptionService` and `DisableEncryptionService` were removed</span></span>

## <a name="removed-modules"></a><span data-ttu-id="1abfb-260">Moduli rimossi</span><span class="sxs-lookup"><span data-stu-id="1abfb-260">Removed modules</span></span>

### `AzureRM.ServerManagement`

<span data-ttu-id="1abfb-261">Il servizio Strumenti di gestione del server è stato [ritirato lo scorso anno](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), di conseguenza il modulo corrispondente del servizio, `AzureRM.ServerManagement`, è stato rimosso da `AzureRM` e non verrà più distribuito in futuro.</span><span class="sxs-lookup"><span data-stu-id="1abfb-261">The Server Management Tools service was [retired last year](https://blogs.technet.microsoft.com/servermanagement/2017/05/17/smt-preview-service-is-being-retired-on-june-30-2017/), and as a result, the corresponding module for SMT, `AzureRM.ServerManagement`, was removed from `AzureRM` and will stop shipping moving forward.</span></span>

### `AzureRM.SiteRecovery`

<span data-ttu-id="1abfb-262">Il modulo `AzureRM.SiteRecovery` verrà sostituito da `AzureRM.RecoveryServices.SiteRecovery`, che è un superset funzionale del modulo `AzureRM.SiteRecovery` e include un nuovo set di cmdlet equivalenti.</span><span class="sxs-lookup"><span data-stu-id="1abfb-262">The `AzureRM.SiteRecovery` module is being superseded by `AzureRM.RecoveryServices.SiteRecovery`, which is a functional superset of the `AzureRM.SiteRecovery` module and includes a new set of equivalent cmdlets.</span></span> <span data-ttu-id="1abfb-263">L'elenco completo dei mapping dei vecchi e nuovi cmdlet è disponibile di seguito:</span><span class="sxs-lookup"><span data-stu-id="1abfb-263">The full list of mappings from old to new cmdlets can be found below:</span></span>

| <span data-ttu-id="1abfb-264">Cmdlet deprecato</span><span class="sxs-lookup"><span data-stu-id="1abfb-264">Deprecated cmdlet</span></span>                                        | <span data-ttu-id="1abfb-265">Cmdlet equivalente</span><span class="sxs-lookup"><span data-stu-id="1abfb-265">Equivalent cmdlet</span></span>                                                | <span data-ttu-id="1abfb-266">Alias</span><span class="sxs-lookup"><span data-stu-id="1abfb-266">Aliases</span></span>                                  |
|----------------------------------------------------------|------------------------------------------------------------------|------------------------------------------|
| `Edit-AzureRmSiteRecoveryRecoveryPlan`                   | `Edit-AzureRmRecoveryServicesAsrRecoveryPlan`                    | `Edit-ASRRecoveryPlan`                   |
| `Get-AzureRmSiteRecoveryFabric`                          | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryJob`                             | `Get-AzureRmRecoveryServicesAsrJob`                              | `Get-ASRJob`                             |
| `Get-AzureRmSiteRecoveryNetwork`                         | `Get-AzureRmRecoveryServicesAsrNetwork`                          | `Get-ASRNetwork`                         |
| `Get-AzureRmSiteRecoveryNetworkMapping`                  | `Get-AzureRmRecoveryServicesAsrNetworkMapping`                   | `Get-ASRNetworkMapping`                  |
| `Get-AzureRmSiteRecoveryPolicy`                          | `Get-AzureRmRecoveryServicesAsrPolicy`                           | `Get-ASRPolicy`                          |
| `Get-AzureRmSiteRecoveryProtectableItem`                 | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryProtectionContainer`             | `Get-AzureRmRecoveryServicesAsrProtectionContainer`              | `Get-ASRProtectionContainer`             |
| `Get-AzureRmSiteRecoveryProtectionContainerMapping`      | `Get-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `Get-ASRProtectionContainerMapping`      |
| `Get-AzureRmSiteRecoveryProtectionEntity`                | `Get-AzureRmRecoveryServicesAsrProtectableItem`                  | `Get-ASRProtectableItem`                 |
| `Get-AzureRmSiteRecoveryRecoveryPlan`                    | `Get-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `Get-ASRRecoveryPlan`                    |
| `Get-AzureRmSiteRecoveryRecoveryPoint`                   | `Get-AzureRmRecoveryServicesAsrRecoveryPoint`                    | `Get-ASRRecoveryPoint`                   |
| `Get-AzureRmSiteRecoveryReplicationProtectedItem`        | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Get-AzureRmSiteRecoveryServer`                          | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoveryServicesProvider`                | `Get-AzureRmRecoveryServicesAsrServicesProvider`                 | `Get-ASRServicesProvider`                |
| `Get-AzureRmSiteRecoverySite`                            | `Get-AzureRmRecoveryServicesAsrFabric`                           | `Get-ASRFabric`                          |
| `Get-AzureRmSiteRecoveryStorageClassification`           | `Get-AzureRmRecoveryServicesAsrStorageClassification`            | `Get-ASRStorageClassification`           |
| `Get-AzureRmSiteRecoveryStorageClassificationMapping`    | `Get-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `Get-ASRStorageClassificationMapping`    |
| `Get-AzureRmSiteRecoveryVault`                           | `Get-AzureRmRecoveryServicesVault`                               |                                          |
| `Get-AzureRmSiteRecoveryVaultSettings`                   | `Get-AzureRmRecoveryServicesAsrVaultContext`                     |                                          |
| `Get-AzureRmSiteRecoveryVaultSettingsFile`               | `Get-AzureRmRecoveryServicesVaultSettingsFile`                   |                                          |
| `Get-AzureRmSiteRecoveryVM`                              | `Get-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Get-ASRReplicationProtectedItem`        |
| `Import-AzureRmSiteRecoveryVaultSettingsFile`            | `Import-AzureRmRecoveryServicesAsrVaultSettingsFile`             |                                          |
| `New-AzureRmSiteRecoveryFabric`                          | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryNetworkMapping`                  | `New-AzureRmRecoveryServicesAsrNetworkMapping`                   | `New-ASRNetworkMapping`                  |
| `New-AzureRmSiteRecoveryPolicy`                          | `New-AzureRmRecoveryServicesAsrPolicy`                           | `New-ASRPolicy`                          |
| `New-AzureRmSiteRecoveryProtectionContainerMapping`      | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `New-AzureRmSiteRecoveryRecoveryPlan`                    | `New-AzureRmRecoveryServicesAsrRecoveryPlan`                     | `New-ASRRecoveryPlan`                    |
| `New-AzureRmSiteRecoveryReplicationProtectedItem`        | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `New-AzureRmSiteRecoverySite`                            | `New-AzureRmRecoveryServicesAsrFabric`                           | `New-ASRFabric`                          |
| `New-AzureRmSiteRecoveryStorageClassificationMapping`    | `New-AzureRmRecoveryServicesAsrStorageClassificationMapping`     | `New-ASRStorageClassificationMapping`    |
| `New-AzureRmSiteRecoveryVault`                           | `New-AzureRmRecoveryServicesVault`                               |                                          |
| `Remove-AzureRmSiteRecoveryFabric`                       | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryNetworkMapping`               | `Remove-AzureRmRecoveryServicesAsrNetworkMapping`                | `Remove-ASRNetworkMapping`               |
| `Remove-AzureRmSiteRecoveryPolicy`                       | `Remove-AzureRmRecoveryServicesAsrPolicy`                        | `Remove-ASRPolicy`                       |
| `Remove-AzureRmSiteRecoveryProtectionContainerMapping`   | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Remove-AzureRmSiteRecoveryRecoveryPlan`                 | `Remove-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Remove-ASRRecoveryPlan`                 |
| `Remove-AzureRmSiteRecoveryReplicationProtectedItem`     | `Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem`      | `Remove-ASRReplicationProtectedItem`     |
| `Remove-AzureRmSiteRecoveryServer`                       | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              |                                          |
| `Remove-AzureRmSiteRecoveryServicesProvider`             | `Remove-AzureRmRecoveryServicesAsrServicesProvider`              | `Remove-ASRServicesProvider`             |
| `Remove-AzureRmSiteRecoverySite`                         | `Remove-AzureRmRecoveryServicesAsrFabric`                        | `Remove-ASRFabric`                       |
| `Remove-AzureRmSiteRecoveryStorageClassificationMapping` | `Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping`  | `Remove-ASRStorageClassificationMapping` |
| `Remove-AzureRmSiteRecoveryVault`                        | `Remove-AzureRmRecoveryServicesVault`                            |                                          |
| `Restart-AzureRmSiteRecoveryJob`                         | `Restart-AzureRmRecoveryServicesAsrJob`                          | `Restart-ASRJob`                         |
| `Resume-AzureRmSiteRecoveryJob`                          | `Resume-AzureRmRecoveryServicesAsrJob`                           | `Resume-ASRJob`                          |
| `Set-AzureRmSiteRecoveryProtectionEntity`                | `New-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `New-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryReplicationProtectedItem`        | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Set-AzureRmSiteRecoveryVaultSettings`                   | `Set-AzureRmRecoveryServicesAsrVaultContext`                     | `Set-ASRVaultContext`                    |
| `Set-AzureRmSiteRecoveryVM`                              | `Set-AzureRmRecoveryServicesAsrReplicationProtectedItem`         | `Set-ASRReplicationProtectedItem`        |
| `Start-AzureRmSiteRecoveryApplyRecoveryPoint`            | `Start-AzureRmRecoveryServicesAsrApplyRecoveryPoint`             | `Start-ASRApplyRecoveryPoint`            |
| `Start-AzureRmSiteRecoveryCommitFailoverJob`             | `Start-AzureRmRecoveryServicesAsrCommitFailoverJob`              | `Start-ASRCommitFailoverJob`             |
| `Start-AzureRmSiteRecoveryPlannedFailoverJob`            | `Start-AzureRmRecoveryServicesAsrPlannedFailoverJob`             | `Start-ASRPlannedFailoverJob`            |
| `Start-AzureRmSiteRecoveryPolicyAssociationJob`          | `New-AzureRmRecoveryServicesAsrProtectionContainerMapping`       | `New-ASRProtectionContainerMapping`      |
| `Start-AzureRmSiteRecoveryPolicyDissociationJob`         | `Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping`    | `Remove-ASRProtectionContainerMapping`   |
| `Start-AzureRmSiteRecoveryTestFailoverJob`               | `Start-AzureRmRecoveryServicesAsrTestFailoverJob`                | `Start-ASRTestFailoverJob`               |
| `Start-AzureRmSiteRecoveryUnplannedFailoverJob`          | `Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob`           | `Start-ASRUnplannedFailoverJob`          |
| `Stop-AzureRmSiteRecoveryJob`                            | `Stop-AzureRmRecoveryServicesAsrJob`                             | `Stop-ASRJob`                            |
| `Update-AzureRmSiteRecoveryPolicy`                       | `Update-AzureRmRecoveryServicesAsrPolicy`                        | `Update-ASRPolicy`                       |
| `Update-AzureRmSiteRecoveryProtectionDirection`          | `Update-AzureRmRecoveryServicesAsrProtectionDirection`           | `Update-ASRProtectionDirection`          |
| `Update-AzureRmSiteRecoveryRecoveryPlan`                 | `Update-AzureRmRecoveryServicesAsrRecoveryPlan`                  | `Update-ASRRecoveryPlan`                 |
| `Update-AzureRmSiteRecoveryServer`                       | `Update-AzureRmRecoveryServicesAsrServicesProvider`              | `Update-ASRServicesProvider`             |
| `Update-AzureRmSiteRecoveryServicesProvider`             | `Update-AzureRmRecoveryServicesAsrvCenter`                       | `Update-ASRvCenter`                      |
