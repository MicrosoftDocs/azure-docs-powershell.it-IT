---
title: Modifiche di rilievo in Microsoft Azure PowerShell 5.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano interruzioni apportate ad Azure PowerShell nella versione 5.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: b4cbeb1b523664fb49c4640eaafd56e3b843ebaa
ms.sourcegitcommit: 2054a8f74cd9bf5a50ea7fdfddccaa632c842934
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2019
ms.locfileid: "56144559"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="ad6fd-103">Modifiche di rilievo in Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="ad6fd-103">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="ad6fd-104">Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ad6fd-105">Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="ad6fd-106">Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="ad6fd-107">Sommario</span><span class="sxs-lookup"><span data-stu-id="ad6fd-107">Table of Contents</span></span>

- [<span data-ttu-id="ad6fd-108">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="ad6fd-108">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="ad6fd-109">Modifiche di rilievo ai cmdlet per Batch</span><span class="sxs-lookup"><span data-stu-id="ad6fd-109">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="ad6fd-110">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="ad6fd-110">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="ad6fd-111">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="ad6fd-111">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="ad6fd-112">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="ad6fd-112">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="ad6fd-113">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="ad6fd-113">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="ad6fd-114">Modifiche di rilievo ai cmdlet per le risorse</span><span class="sxs-lookup"><span data-stu-id="ad6fd-114">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="ad6fd-115">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="ad6fd-115">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="ad6fd-116">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="ad6fd-116">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="ad6fd-117">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-117">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="ad6fd-118">Sostituzione dei parametri "UserName" e "Password" con PSCredential</span><span class="sxs-lookup"><span data-stu-id="ad6fd-118">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="ad6fd-119">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-119">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ad6fd-120">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="ad6fd-121">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-121">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="ad6fd-122">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-122">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="ad6fd-123">Modifiche di rilievo ai cmdlet per Batch</span><span class="sxs-lookup"><span data-stu-id="ad6fd-123">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="ad6fd-124">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-124">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="ad6fd-125">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="ad6fd-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="ad6fd-126">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-126">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ad6fd-127">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="ad6fd-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="ad6fd-128">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-128">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="ad6fd-129">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="ad6fd-129">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="ad6fd-130">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-130">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="ad6fd-131">Rimozione dell'opzione `RunElevated` e relativa sostituzione con `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-131">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="ad6fd-132">Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-132">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="ad6fd-133">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-133">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="ad6fd-134">Il costruttore `PSMultiInstanceSettings` non accetta più un parametro `numberOfInstances` obbligatorio. Accetta invece un parametro `coordinationCommandLine` obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-134">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="ad6fd-135">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-135">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="ad6fd-136">Rimozione della proprietà `RunElevated` per `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-136">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="ad6fd-137">Per sostituire `RunElevated` è stata aggiunta la proprietà `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-137">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="ad6fd-138">Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-138">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="ad6fd-139">**Più tipi**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-139">**Multiple types**</span></span>

- <span data-ttu-id="ad6fd-140">Ridenominazione della proprietà `SchedulingError` per `PSExitConditions` in `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-140">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="ad6fd-141">**Più tipi**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-141">**Multiple types**</span></span>

- <span data-ttu-id="ad6fd-142">Ridenominazione della proprietà `SchedulingError` per `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` e `PSTaskExecutionInformation` in `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-142">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="ad6fd-143">Ogni volta che si verifica un errore delle attività viene restituito `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-143">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="ad6fd-144">Questo include tutti i precedenti casi di errori di pianificazione, nonché i codici di uscita delle attività diversi da zero e gli errori di caricamento file della nuova funzionalità per i file di output.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-144">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="ad6fd-145">È stata mantenuta la struttura precedente e non sono quindi necessarie modifiche di codice quando si usa questo tipo.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-145">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="ad6fd-146">Questo influisce anche su: Get-AzureBatchPool, Get-AzureBatchSubtask e Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="ad6fd-146">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="ad6fd-147">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-147">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="ad6fd-148">Rimozione di `TargetDedicated` e relativa sostituzione con `TargetDedicatedComputeNodes` e `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-148">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="ad6fd-149">`TargetDedicatedComputeNodes` ha un alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-149">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="ad6fd-150">Questo influisce anche su: Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="ad6fd-150">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="ad6fd-151">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-151">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="ad6fd-152">Ridenominazione delle proprietà `TargetDedicated` e `CurrentDedicated` per `PSCloudPool` in `TargetDedicatedComputeNodes` e `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-152">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="ad6fd-153">**Tipo PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-153">**Type PSCloudPool**</span></span>

- <span data-ttu-id="ad6fd-154">Ridenominazione di `ResizeError` in `ResizeErrors`, che è ora una raccolta, per `PSCloudPool`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-154">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="ad6fd-155">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-155">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="ad6fd-156">Ridenominazione della proprietà `TargetDedicated` per `PSPoolSpecification` in `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-156">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell-interactive
# Old
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicated = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo

# New
$poolInfo = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolInformation
$poolInfo.AutoPoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification = New-Object Microsoft.Azure.Commands.Batch.Models.PSPoolSpecification
$poolInfo.AutoPoolSpecification.PoolSpecification.TargetDedicatedComputeNodes = 5
New-AzureBatchJob [other parameters] -PoolInformation $poolInfo
```

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="ad6fd-157">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-157">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="ad6fd-158">Rimozione di `Name` e relativa sostituzione con `Path`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-158">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="ad6fd-159">`Path` ha un alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-159">`Path` has an alias `Name`.</span></span>

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="ad6fd-160">Questo influisce anche su: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="ad6fd-160">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="ad6fd-161">Tipo **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-161">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="ad6fd-162">Ridenominazione della proprietà `Name` per `PSNodeFile` in `Path`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-162">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="ad6fd-163">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-163">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="ad6fd-164">Le proprietà `PreviousState` e `State` di `PSSubtaskInformation` non sono più di tipo `TaskState` e sono invece di tipo `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-164">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="ad6fd-165">A differenza di `TaskState`, `SubtaskState` non ha un valore `Active` perché le sottoattività non possono essere in stato `Active`.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-165">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="ad6fd-166">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="ad6fd-166">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="ad6fd-167">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-167">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="ad6fd-168">Sostituzione dei parametri "UserName" e "Password" con PSCredential</span><span class="sxs-lookup"><span data-stu-id="ad6fd-168">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="ad6fd-169">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="ad6fd-169">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-170">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-171">Rimozione del cmdlet "New-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-171">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-172">Usare il cmdlet "New-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-172">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-173">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-174">Rimozione del cmdlet "Get-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-174">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-175">Usare il cmdlet "Get-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-175">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-176">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-177">Rimozione del cmdlet "Set-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-177">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-178">Usare il cmdlet "Set-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-178">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-179">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-180">Rimozione del cmdlet "Remove-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-180">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-181">Usare il cmdlet "Remove-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-181">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="ad6fd-182">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-182">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ad6fd-183">Rimozione del cmdlet "New-AzureRmEventHubNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-183">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-184">Usare il cmdlet "New-AzureRmEventHubKey"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-184">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="ad6fd-185">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-185">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="ad6fd-186">Rimozione del cmdlet "Get-AzureRmEventHubNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-186">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-187">Usare il cmdlet "Get-AzureRmEventHubKey"</span><span class="sxs-lookup"><span data-stu-id="ad6fd-187">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="ad6fd-188">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-188">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ad6fd-189">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="ad6fd-190">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-190">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ad6fd-191">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="ad6fd-192">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-192">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="ad6fd-193">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-193">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="ad6fd-194">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-194">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ad6fd-195">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="ad6fd-196">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-196">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ad6fd-197">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="ad6fd-198">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-198">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="ad6fd-199">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-199">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="ad6fd-200">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="ad6fd-200">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="ad6fd-201">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-201">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="ad6fd-202">Il cmdlet **Add-AzureRMLogAlertRule** è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-202">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="ad6fd-203">Dopo il 1° ottobre, l'uso di questo cmdlet non avrà più alcun effetto a causa della transizione di questa funzionalità agli avvisi del log attività.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-203">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="ad6fd-204">Per altre informazioni, vedere https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-204">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="ad6fd-205">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-205">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="ad6fd-206">Il cmdlet **Get-AzureRMUsage** è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-206">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="ad6fd-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-207">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="ad6fd-208">Modifica a livello di output: il campo EventChannels dell'oggetto EventData, restituito da questi cmdlet, verrà deprecato perché viene ora restituito un valore costante (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="ad6fd-208">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="ad6fd-209">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-209">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="ad6fd-210">Modifica a livello di output: l'output di questo cmdlet verrà reso flat, ad esempio con l'eliminazione del campo properties, per migliorare l'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-210">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground Red "Error updating alert rule"
    Write-Host $rules[0].Id
    Write-Host $rules[0].Properties.IsEnabled
    Write-Host $rules[0].Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -Foreground red "Error updating alert rule"
    Write-Host $rules[0].Id

    # Properties will remain for a while
    Write-Host $rules[0].Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules[0].IsEnabled
    Write-Host $rules[0].Condition
}
```

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="ad6fd-211">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-211">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="ad6fd-212">Modifica a livello di output: il campo AutoscaleSettingResourceName verrà deprecato perché è sempre uguale al campo Name.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-212">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell-interactive
# Old
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# there won't be a AutoscaleSettingResourceName
Write-Host $s1.Name    
```

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="ad6fd-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-213">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="ad6fd-214">Modifica a livello di output: il tipo dell'output verrà modificato in modo da restituire un singolo oggetto contenente ID richiesta e codice di stato.</span><span class="sxs-lookup"><span data-stu-id="ad6fd-214">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell-interactive
# Old
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
if ($s1 -ne $null)
{
    $r = $s1[0].RequestId
    $s = $s1[0].StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name $ruleName
$r = $s1.RequestId
$s = $s1.StatusCode
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="ad6fd-215">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="ad6fd-215">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ad6fd-216">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-216">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ad6fd-217">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ad6fd-218">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-218">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ad6fd-219">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="ad6fd-220">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-220">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="ad6fd-221">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-221">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="ad6fd-222">Modifiche di rilievo ai cmdlet per le risorse</span><span class="sxs-lookup"><span data-stu-id="ad6fd-222">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="ad6fd-223">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-223">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="ad6fd-224">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="ad6fd-225">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-225">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="ad6fd-226">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="ad6fd-227">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-227">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="ad6fd-228">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="ad6fd-229">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-229">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="ad6fd-230">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="ad6fd-231">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-231">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="ad6fd-232">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="ad6fd-233">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-233">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="ad6fd-234">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="ad6fd-234">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="ad6fd-235">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="ad6fd-235">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ad6fd-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-236">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-237">Rimozione del cmdlet "Get-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-237">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-238">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-238">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="ad6fd-239">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-239">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ad6fd-240">Rimozione del cmdlet "Get-AzureRmServiceBusTopicKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-240">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-241">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-241">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ad6fd-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-242">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-243">Rimozione del cmdlet "New-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-243">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-244">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-244">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="ad6fd-245">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-245">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="ad6fd-246">Rimozione del cmdlet "New-AzureRmServiceBusTopicKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-246">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-247">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-247">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ad6fd-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-248">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-249">Rimozione del cmdlet "Remove-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-249">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-250">Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-250">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="ad6fd-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-251">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-252">Rimozione del cmdlet "Set-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-252">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-253">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-253">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="ad6fd-254">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-254">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ad6fd-255">Rimozione del cmdlet "New-AzureRmServiceBusNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-255">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-256">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-256">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ad6fd-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-257">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-258">Rimozione del cmdlet "Get-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-258">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-259">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-259">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="ad6fd-260">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-260">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ad6fd-261">Rimozione del cmdlet "Get-AzureRmServiceBusQueueKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-261">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-262">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-262">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ad6fd-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-263">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-264">Rimozione del cmdlet "New-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-264">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-265">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-265">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="ad6fd-266">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-266">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="ad6fd-267">Rimozione del cmdlet "New-AzureRmServiceBusQueueKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-267">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-268">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-268">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ad6fd-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-269">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-270">Rimozione del cmdlet "Remove-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-270">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-271">Usare il cmdlet "GRemove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-271">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="ad6fd-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-272">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-273">Rimozione del cmdlet "Set-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-273">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-274">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-274">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-275">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-276">Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-276">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-277">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-277">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="ad6fd-278">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-278">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="ad6fd-279">Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-279">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-280">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-280">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-281">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-282">Rimozione del cmdlet "New-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-282">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-283">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-283">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-284">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-285">Rimozione del cmdlet "Remove-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-285">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-286">Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-286">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="ad6fd-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-287">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="ad6fd-288">Rimozione del cmdlet "Set-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-288">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="ad6fd-289">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="ad6fd-289">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="ad6fd-290">**Tipo NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-290">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="ad6fd-291">Le proprietà seguenti sono state rimosse:</span><span class="sxs-lookup"><span data-stu-id="ad6fd-291">The following properties have been removed</span></span>
    - <span data-ttu-id="ad6fd-292">Attivato</span><span class="sxs-lookup"><span data-stu-id="ad6fd-292">Enabled</span></span>
    - <span data-ttu-id="ad6fd-293">Stato</span><span class="sxs-lookup"><span data-stu-id="ad6fd-293">Status</span></span>
   
```powershell-interactive
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="ad6fd-294">**Tipo QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-294">**Type QueueAttribute**</span></span>
- <span data-ttu-id="ad6fd-295">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="ad6fd-295">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ad6fd-296">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ad6fd-296">EnableBatchedOperations</span></span>
    - <span data-ttu-id="ad6fd-297">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ad6fd-297">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ad6fd-298">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="ad6fd-298">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ad6fd-299">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="ad6fd-299">SupportOrdering</span></span>

```powershell-interactive
# Old
# The $queue has EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties
$queue = Get-AzureRmServiceBusQueue <parameters>
$queue.EntityAvailabilityStatus
$queue.EnableBatchedOperations
$queue.IsAnonymousAccessible
$queue.SupportOrdering  

# New
# The call remains the same, but the returned values Queue object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$queue = Get-AzureRmServiceBusQueue <parameters>
```
   
### <a name="type-topicattribute"></a><span data-ttu-id="ad6fd-300">**Tipo TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-300">**Type TopicAttribute**</span></span>
- <span data-ttu-id="ad6fd-301">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="ad6fd-301">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="ad6fd-302">Località</span><span class="sxs-lookup"><span data-stu-id="ad6fd-302">Location</span></span>
    - <span data-ttu-id="ad6fd-303">IsExpress</span><span class="sxs-lookup"><span data-stu-id="ad6fd-303">IsExpress</span></span>
    - <span data-ttu-id="ad6fd-304">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="ad6fd-304">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="ad6fd-305">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="ad6fd-305">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="ad6fd-306">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="ad6fd-306">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="ad6fd-307">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ad6fd-307">EntityAvailabilityStatus</span></span>

```powershell-interactive
# Old
# The $topic has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$topic = Get-AzureRmServiceBusTopic <parameters>
$topic.EntityAvailabilityStatus
$topic.EnableSubscriptionPartitioning
$topic.IsAnonymousAccessible
$topic.IsExpress
$topic.FilteringMessagesBeforePublishing
$topic.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$topic = Get-AzureRmServiceBusTopic <parameters>
```
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="ad6fd-308">**Tipo SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="ad6fd-308">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="ad6fd-309">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="ad6fd-309">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="ad6fd-310">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="ad6fd-310">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="ad6fd-311">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="ad6fd-311">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="ad6fd-312">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad6fd-312">IsReadOnly</span></span>
    - <span data-ttu-id="ad6fd-313">Località</span><span class="sxs-lookup"><span data-stu-id="ad6fd-313">Location</span></span>
   
```powershell-interactive
# Old
# The $subscription has EntityAvailabilityStatus, EnableSubscriptionPartitioning, IsAnonymousAccessible, IsExpress, Location and FilteringMessagesBeforePublishing properties
$subscription = Get-AzureRmServiceBussubscription <parameters>
$subscription.EntityAvailabilityStatus
$subscription.EnableSubscriptionPartitioning
$subscription.IsAnonymousAccessible
$subscription.IsExpress
$subscription.FilteringMessagesBeforePublishing
$subscription.Location

# New
# The call remains the same, but the returned values Topic object will not have the EntityAvailabilityStatus, EnableBatchedOperations, IsAnonymousAccessible and SupportOrdering properties    
$subscription = Get-AzureRmServiceBussubscription <parameters>
```