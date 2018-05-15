# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a><span data-ttu-id="29966-101">Modifiche di rilievo in Microsoft Azure PowerShell 5.0.0</span><span class="sxs-lookup"><span data-stu-id="29966-101">Breaking changes for Microsoft Azure PowerShell 5.0.0</span></span>

<span data-ttu-id="29966-102">Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29966-102">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="29966-103">Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice.</span><span class="sxs-lookup"><span data-stu-id="29966-103">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="29966-104">Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.</span><span class="sxs-lookup"><span data-stu-id="29966-104">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="29966-105">Sommario</span><span class="sxs-lookup"><span data-stu-id="29966-105">Table of Contents</span></span>

- [<span data-ttu-id="29966-106">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="29966-106">Breaking changes to ApiManagement cmdlets</span></span>](#breaking-changes-to-apimanagement-cmdlets)
- [<span data-ttu-id="29966-107">Modifiche di rilievo ai cmdlet per Batch</span><span class="sxs-lookup"><span data-stu-id="29966-107">Breaking changes to Batch cmdlets</span></span>](#breaking-changes-to-batch-cmdlets)
- [<span data-ttu-id="29966-108">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="29966-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="29966-109">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="29966-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="29966-110">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="29966-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="29966-111">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="29966-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="29966-112">Modifiche di rilievo ai cmdlet per le risorse</span><span class="sxs-lookup"><span data-stu-id="29966-112">Breaking changes to Resources cmdlets</span></span>](#breaking-changes-to-resources-cmdlets)
- [<span data-ttu-id="29966-113">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="29966-113">Breaking Changes to ServiceBus Cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a><span data-ttu-id="29966-114">Modifiche di rilievo ai cmdlet per Gestione API</span><span class="sxs-lookup"><span data-stu-id="29966-114">Breaking changes to ApiManagement cmdlets</span></span>

### <a name="new-azurermapimanagementbackendproxy"></a><span data-ttu-id="29966-115">**New-AzureRmApiManagementBackendProxy**</span><span class="sxs-lookup"><span data-stu-id="29966-115">**New-AzureRmApiManagementBackendProxy**</span></span>
- <span data-ttu-id="29966-116">Sostituzione dei parametri "UserName" e "Password" con PSCredential</span><span class="sxs-lookup"><span data-stu-id="29966-116">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a><span data-ttu-id="29966-117">**New-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="29966-117">**New-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="29966-118">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-118">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a><span data-ttu-id="29966-119">**Set-AzureRmApiManagementUser**</span><span class="sxs-lookup"><span data-stu-id="29966-119">**Set-AzureRmApiManagementUser**</span></span>
- <span data-ttu-id="29966-120">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-120">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a><span data-ttu-id="29966-121">Modifiche di rilievo ai cmdlet per Batch</span><span class="sxs-lookup"><span data-stu-id="29966-121">Breaking changes to Batch cmdlets</span></span>

### <a name="new-azurebatchcertificate"></a><span data-ttu-id="29966-122">**New-AzureBatchCertificate**</span><span class="sxs-lookup"><span data-stu-id="29966-122">**New-AzureBatchCertificate**</span></span>
- <span data-ttu-id="29966-123">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="29966-123">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a><span data-ttu-id="29966-124">**New-AzureBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="29966-124">**New-AzureBatchComputeNodeUser**</span></span>
- <span data-ttu-id="29966-125">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="29966-125">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a><span data-ttu-id="29966-126">**Set-AzureRmBatchComputeNodeUser**</span><span class="sxs-lookup"><span data-stu-id="29966-126">**Set-AzureRmBatchComputeNodeUser**</span></span>
- <span data-ttu-id="29966-127">Sostituzione del parametro `Password` con una stringa sicura</span><span class="sxs-lookup"><span data-stu-id="29966-127">Parameter `Password` being replaced in favor of a Secure string</span></span>

```powershell
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a><span data-ttu-id="29966-128">**New-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="29966-128">**New-AzureBatchTask**</span></span>
 - <span data-ttu-id="29966-129">Rimozione dell'opzione `RunElevated` e relativa sostituzione con `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="29966-129">Removed the `RunElevated` switch and replaced it with `UserIdentity`.</span></span>

```powershell
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

<span data-ttu-id="29966-130">Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="29966-130">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="psmultiinstancesettings"></a><span data-ttu-id="29966-131">**PSMultiInstanceSettings**</span><span class="sxs-lookup"><span data-stu-id="29966-131">**PSMultiInstanceSettings**</span></span>

- <span data-ttu-id="29966-132">Il costruttore `PSMultiInstanceSettings` non accetta più un parametro `numberOfInstances` obbligatorio. Accetta invece un parametro `coordinationCommandLine` obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="29966-132">`PSMultiInstanceSettings` constructor no longer takes a required `numberOfInstances` parameter, instead it takes a required `coordinationCommandLine` parameter.</span></span>

```powershell
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a><span data-ttu-id="29966-133">**Get-AzureBatchTask**</span><span class="sxs-lookup"><span data-stu-id="29966-133">**Get-AzureBatchTask**</span></span>
 - <span data-ttu-id="29966-134">Rimozione della proprietà `RunElevated` per `PSCloudTask`.</span><span class="sxs-lookup"><span data-stu-id="29966-134">Removed the `RunElevated` property on `PSCloudTask`.</span></span> <span data-ttu-id="29966-135">Per sostituire `RunElevated` è stata aggiunta la proprietà `UserIdentity`.</span><span class="sxs-lookup"><span data-stu-id="29966-135">The `UserIdentity` property has been added to replace `RunElevated`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

<span data-ttu-id="29966-136">Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.</span><span class="sxs-lookup"><span data-stu-id="29966-136">This additionally impacts the `RunElevated` property on `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask`, and `PSJobReleaseTask`.</span></span>

### <a name="multiple-types"></a><span data-ttu-id="29966-137">**Più tipi**</span><span class="sxs-lookup"><span data-stu-id="29966-137">**Multiple types**</span></span>

- <span data-ttu-id="29966-138">Ridenominazione della proprietà `SchedulingError` per `PSExitConditions` in `PreProcessingError`.</span><span class="sxs-lookup"><span data-stu-id="29966-138">Renamed the `SchedulingError` property on `PSExitConditions` to `PreProcessingError`.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a><span data-ttu-id="29966-139">**Più tipi**</span><span class="sxs-lookup"><span data-stu-id="29966-139">**Multiple types**</span></span>

- <span data-ttu-id="29966-140">Ridenominazione della proprietà `SchedulingError` per `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` e `PSTaskExecutionInformation` in `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="29966-140">Renamed the `SchedulingError` property on `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation`, and `PSTaskExecutionInformation` to `FailureInformation`.</span></span>
  - <span data-ttu-id="29966-141">Ogni volta che si verifica un errore delle attività viene restituito `FailureInformation`.</span><span class="sxs-lookup"><span data-stu-id="29966-141">`FailureInformation` is returned any time there is a task failure.</span></span> <span data-ttu-id="29966-142">Questo include tutti i precedenti casi di errori di pianificazione, nonché i codici di uscita delle attività diversi da zero e gli errori di caricamento file della nuova funzionalità per i file di output.</span><span class="sxs-lookup"><span data-stu-id="29966-142">This includes all previous scheduling error cases, as well as nonzero task exit codes, and file upload failures from the new output files feature.</span></span>
  - <span data-ttu-id="29966-143">È stata mantenuta la struttura precedente e non sono quindi necessarie modifiche di codice quando si usa questo tipo.</span><span class="sxs-lookup"><span data-stu-id="29966-143">This is structured the same as before, so no code change is needed when using this type.</span></span>

```powershell
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

<span data-ttu-id="29966-144">Questo ha un impatto anche su Get-AzureBatchPool, Get-AzureBatchSubtask e Get-AzureBatchJobPreparationAndReleaseTaskStatus</span><span class="sxs-lookup"><span data-stu-id="29966-144">This additionally impacts: Get-AzureBatchPool, Get-AzureBatchSubtask, and Get-AzureBatchJobPreparationAndReleaseTaskStatus</span></span>

### <a name="new-azurebatchpool"></a><span data-ttu-id="29966-145">**New-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="29966-145">**New-AzureBatchPool**</span></span>
 - <span data-ttu-id="29966-146">Rimozione di `TargetDedicated` e relativa sostituzione con `TargetDedicatedComputeNodes` e `TargetLowPriorityComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="29966-146">Removed `TargetDedicated` and replaced it with `TargetDedicatedComputeNodes` and `TargetLowPriorityComputeNodes`.</span></span>
 - <span data-ttu-id="29966-147">`TargetDedicatedComputeNodes` ha un alias `TargetDedicated`.</span><span class="sxs-lookup"><span data-stu-id="29966-147">`TargetDedicatedComputeNodes` has an alias `TargetDedicated`.</span></span>

```powershell
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

<span data-ttu-id="29966-148">Questo ha un impatto anche su Start-AzureBatchPoolResize</span><span class="sxs-lookup"><span data-stu-id="29966-148">This also impacts: Start-AzureBatchPoolResize</span></span>

### <a name="get-azurebatchpool"></a><span data-ttu-id="29966-149">**Get-AzureBatchPool**</span><span class="sxs-lookup"><span data-stu-id="29966-149">**Get-AzureBatchPool**</span></span>
 - <span data-ttu-id="29966-150">Ridenominazione delle proprietà `TargetDedicated` e `CurrentDedicated` per `PSCloudPool` in `TargetDedicatedComputeNodes` e `CurrentDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="29966-150">Renamed the `TargetDedicated` and `CurrentDedicated` properties on `PSCloudPool` to `TargetDedicatedComputeNodes` and `CurrentDedicatedComputeNodes`.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicated
$pool.CurrentDedicated

# New
$pool = Get-AzureBatchPool [parameters]
$pool.TargetDedicatedComputeNodes
$pool.CurrentDedicatedComputeNodes
```

### <a name="type-pscloudpool"></a><span data-ttu-id="29966-151">**Tipo PSCloudPool**</span><span class="sxs-lookup"><span data-stu-id="29966-151">**Type PSCloudPool**</span></span>

- <span data-ttu-id="29966-152">Ridenominazione di `ResizeError` in `ResizeErrors`, che è ora una raccolta, per `PSCloudPool`.</span><span class="sxs-lookup"><span data-stu-id="29966-152">Renamed `ResizeError` to `ResizeErrors` on `PSCloudPool`, and it is now a collection.</span></span>

```powershell
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a><span data-ttu-id="29966-153">**New-AzureBatchJob**</span><span class="sxs-lookup"><span data-stu-id="29966-153">**New-AzureBatchJob**</span></span>
- <span data-ttu-id="29966-154">Ridenominazione della proprietà `TargetDedicated` per `PSPoolSpecification` in `TargetDedicatedComputeNodes`.</span><span class="sxs-lookup"><span data-stu-id="29966-154">Renamed the `TargetDedicated` property on `PSPoolSpecification` to `TargetDedicatedComputeNodes`.</span></span>

```powershell
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

### <a name="get-azurebatchnodefile"></a><span data-ttu-id="29966-155">**Get-AzureBatchNodeFile**</span><span class="sxs-lookup"><span data-stu-id="29966-155">**Get-AzureBatchNodeFile**</span></span>
 - <span data-ttu-id="29966-156">Rimozione di `Name` e relativa sostituzione con `Path`.</span><span class="sxs-lookup"><span data-stu-id="29966-156">Removed `Name` and replaced it with `Path`.</span></span>
 - <span data-ttu-id="29966-157">`Path` ha un alias `Name`.</span><span class="sxs-lookup"><span data-stu-id="29966-157">`Path` has an alias `Name`.</span></span>

```powershell
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

<span data-ttu-id="29966-158">Questo ha un impatto anche su Get-AzureBatchNodeFileContent e Remove-AzureBatchNodeFile</span><span class="sxs-lookup"><span data-stu-id="29966-158">This also impacts: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile</span></span>

### <a name="type-psnodefile"></a><span data-ttu-id="29966-159">Tipo **PSNodeFile**</span><span class="sxs-lookup"><span data-stu-id="29966-159">Type **PSNodeFile**</span></span>

 - <span data-ttu-id="29966-160">Ridenominazione della proprietà `Name` per `PSNodeFile` in `Path`.</span><span class="sxs-lookup"><span data-stu-id="29966-160">Renamed the `Name` property on `PSNodeFile` to `Path`.</span></span>

```powershell
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a><span data-ttu-id="29966-161">**Get-AzureBatchSubtask**</span><span class="sxs-lookup"><span data-stu-id="29966-161">**Get-AzureBatchSubtask**</span></span>
- <span data-ttu-id="29966-162">Le proprietà `PreviousState` e `State` di `PSSubtaskInformation` non sono più di tipo `TaskState` e sono invece di tipo `SubtaskState`.</span><span class="sxs-lookup"><span data-stu-id="29966-162">The `PreviousState` and `State` properties of `PSSubtaskInformation` are no longer of type `TaskState`, instead they are of type `SubtaskState`.</span></span>
  - <span data-ttu-id="29966-163">A differenza di `TaskState`, `SubtaskState` non ha un valore `Active` perché le sottoattività non possono essere in stato `Active`.</span><span class="sxs-lookup"><span data-stu-id="29966-163">Unlike `TaskState`, `SubtaskState` has no `Active` value, since it is not possible for subtasks to be in an `Active` state.</span></span>

```powershell
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="29966-164">Modifiche di rilievo ai cmdlet per le risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="29966-164">Breaking changes to Compute cmdlets</span></span>

### <a name="set-azurermvmaccessextension"></a><span data-ttu-id="29966-165">**Set-AzureRmVMAccessExtension**</span><span class="sxs-lookup"><span data-stu-id="29966-165">**Set-AzureRmVMAccessExtension**</span></span>
- <span data-ttu-id="29966-166">Sostituzione dei parametri "UserName" e "Password" con PSCredential</span><span class="sxs-lookup"><span data-stu-id="29966-166">Parameters "UserName" and "Password" are being replaced in favor of a PSCredential</span></span>

```powershell
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="29966-167">Modifiche di rilievo ai cmdlet per Hub eventi</span><span class="sxs-lookup"><span data-stu-id="29966-167">Breaking changes to EventHub cmdlets</span></span>

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="29966-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-168">**New-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-169">Rimozione del cmdlet "New-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-169">The 'New-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-170">Usare il cmdlet "New-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="29966-170">Please use the 'New-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="29966-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-171">**Get-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-172">Rimozione del cmdlet "Get-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-172">The 'Get-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-173">Usare il cmdlet "Get-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="29966-173">Please use the 'Get-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="29966-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-174">**Set-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-175">Rimozione del cmdlet "Set-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-175">The 'Set-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-176">Usare il cmdlet "Set-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="29966-176">Please use the 'Set-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a><span data-ttu-id="29966-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-177">**Remove-AzureRmEventHubNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-178">Rimozione del cmdlet "Remove-AzureRmEventHubNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-178">The 'Remove-AzureRmEventHubNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-179">Usare il cmdlet "Remove-AzureRmEventHubAuthorizationRule"</span><span class="sxs-lookup"><span data-stu-id="29966-179">Please use the 'Remove-AzureRmEventHubAuthorizationRule' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespacekey"></a><span data-ttu-id="29966-180">**New-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="29966-180">**New-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="29966-181">Rimozione del cmdlet "New-AzureRmEventHubNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="29966-181">The 'New-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-182">Usare il cmdlet "New-AzureRmEventHubKey"</span><span class="sxs-lookup"><span data-stu-id="29966-182">Please use the 'New-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="get-azurermeventhubnamespacekey"></a><span data-ttu-id="29966-183">**Get-AzureRmEventHubNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="29966-183">**Get-AzureRmEventHubNamespaceKey**</span></span>
- <span data-ttu-id="29966-184">Rimozione del cmdlet "Get-AzureRmEventHubNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="29966-184">The 'Get-AzureRmEventHubNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-185">Usare il cmdlet "Get-AzureRmEventHubKey"</span><span class="sxs-lookup"><span data-stu-id="29966-185">Please use the 'Get-AzureRmEventHubKey' cmdlet</span></span>
    
### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="29966-186">**New-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="29966-186">**New-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="29966-187">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-187">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property  
$namespace = New-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="29966-188">**Get-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="29966-188">**Get-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="29966-189">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-189">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Get-AzureRmEventHubNamespace <parameters>
```
    
### <a name="set-azurermeventhubnamespace"></a><span data-ttu-id="29966-190">**Set-AzureRmEventHubNamespace**</span><span class="sxs-lookup"><span data-stu-id="29966-190">**Set-AzureRmEventHubNamespace**</span></span>
- <span data-ttu-id="29966-191">Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-191">The property 'Status' and 'Enabled' from the NamespceAttributes will be removed.</span></span> 

```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Set-AzureRmEventHubNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Status and Enabled property    
$namespace = Set-AzureRmEventHubNamespace <parameters>
``` 
  
### <a name="new-azurermeventhubconsumergroup"></a><span data-ttu-id="29966-192">**New-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="29966-192">**New-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="29966-193">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-193">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a><span data-ttu-id="29966-194">**Set-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="29966-194">**Set-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="29966-195">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-195">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a><span data-ttu-id="29966-196">**Get-AzureRmEventHubConsumerGroup**</span><span class="sxs-lookup"><span data-stu-id="29966-196">**Get-AzureRmEventHubConsumerGroup**</span></span>
- <span data-ttu-id="29966-197">Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.</span><span class="sxs-lookup"><span data-stu-id="29966-197">The property 'EventHubPath' from the ConsumerGroupAttributes will be removed.</span></span>

```powershell
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="29966-198">Modifiche di rilievo ai cmdlet per Insights</span><span class="sxs-lookup"><span data-stu-id="29966-198">Breaking changes to Insights cmdlets</span></span>

### <a name="add-azurermlogalertrule"></a><span data-ttu-id="29966-199">**Add-AzureRMLogAlertRule**</span><span class="sxs-lookup"><span data-stu-id="29966-199">**Add-AzureRMLogAlertRule**</span></span>
- <span data-ttu-id="29966-200">Il cmdlet **Add-AzureRMLogAlertRule** è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="29966-200">The **Add-AzureRMLogAlertRule** cmdlet has been deprecated</span></span>
- <span data-ttu-id="29966-201">Dopo il 1° ottobre, l'uso di questo cmdlet non avrà più alcun effetto a causa della transizione di questa funzionalità agli avvisi del log attività.</span><span class="sxs-lookup"><span data-stu-id="29966-201">After October 1st using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="29966-202">Per altre informazioni, vedere https://aka.ms/migratemealerts.</span><span class="sxs-lookup"><span data-stu-id="29966-202">Please see https://aka.ms/migratemealerts for more information.</span></span>

### <a name="get-azurermusage"></a><span data-ttu-id="29966-203">**Get-AzureRMUsage**</span><span class="sxs-lookup"><span data-stu-id="29966-203">**Get-AzureRMUsage**</span></span>
- <span data-ttu-id="29966-204">Il cmdlet **Get-AzureRMUsage** è stato deprecato.</span><span class="sxs-lookup"><span data-stu-id="29966-204">The **Get-AzureRMUsage** cmdlet has been deprecated</span></span>

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a><span data-ttu-id="29966-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span><span class="sxs-lookup"><span data-stu-id="29966-205">**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**</span></span>
- <span data-ttu-id="29966-206">Modifica a livello di output: il campo EventChannels dell'oggetto EventData, restituito da questi cmdlet, verrà deprecato perché viene ora restituito un valore costante (Admin,Operation).</span><span class="sxs-lookup"><span data-stu-id="29966-206">Output change: The field EventChannels from the EventData object (returned by these cmdlets) is being deprecated since it now returns a constant value (Admin,Operation.)</span></span>

### <a name="get-azurermalertrule"></a><span data-ttu-id="29966-207">**Get-AzureRmAlertRule**</span><span class="sxs-lookup"><span data-stu-id="29966-207">**Get-AzureRmAlertRule**</span></span>
- <span data-ttu-id="29966-208">Modifica a livello di output: l'output di questo cmdlet verrà reso flat, con l'eliminazione del campo properties, per migliorare l'esperienza utente.</span><span class="sxs-lookup"><span data-stu-id="29966-208">Output change: The output of this cmdlet will be flattened, i.e. elimination of the properties field, to improve the user experience.</span></span>

```powershell
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

### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="29966-209">**Get-AzureRmAutoscaleSetting**</span><span class="sxs-lookup"><span data-stu-id="29966-209">**Get-AzureRmAutoscaleSetting**</span></span>
- <span data-ttu-id="29966-210">Modifica a livello di output: il campo AutoscaleSettingResourceName verrà deprecato perché è sempre uguale al campo Name.</span><span class="sxs-lookup"><span data-stu-id="29966-210">Output change: The AutoscaleSettingResourceName field will be deprecated since it always equals the Name field.</span></span>

```powershell
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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a><span data-ttu-id="29966-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span><span class="sxs-lookup"><span data-stu-id="29966-211">**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**</span></span>
- <span data-ttu-id="29966-212">Modifica a livello di output: il tipo dell'output verrà modificato in modo da restituire un singolo oggetto contenente ID richiesta e codice di stato.</span><span class="sxs-lookup"><span data-stu-id="29966-212">Output change: The type of the output will change to return a single object containing the request Id and the status code.</span></span>

```powershell
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

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="29966-213">Modifiche di rilievo ai cmdlet per le reti</span><span class="sxs-lookup"><span data-stu-id="29966-213">Breaking changes to Network cmdlets</span></span>

### <a name="add-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="29966-214">**Add-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="29966-214">**Add-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="29966-215">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-215">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="29966-216">**New-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="29966-216">**New-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="29966-217">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-217">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a><span data-ttu-id="29966-218">**Set-AzureRmApplicationGatewaySslCertificate**</span><span class="sxs-lookup"><span data-stu-id="29966-218">**Set-AzureRmApplicationGatewaySslCertificate**</span></span>
- <span data-ttu-id="29966-219">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-219">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a><span data-ttu-id="29966-220">Modifiche di rilievo ai cmdlet per le risorse</span><span class="sxs-lookup"><span data-stu-id="29966-220">Breaking changes to Resources cmdlets</span></span>

### <a name="new-azurermadappcredential"></a><span data-ttu-id="29966-221">**New-AzureRmADAppCredential**</span><span class="sxs-lookup"><span data-stu-id="29966-221">**New-AzureRmADAppCredential**</span></span>
- <span data-ttu-id="29966-222">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-222">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a><span data-ttu-id="29966-223">**New-AzureRmADApplication**</span><span class="sxs-lookup"><span data-stu-id="29966-223">**New-AzureRmADApplication**</span></span>
- <span data-ttu-id="29966-224">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-224">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a><span data-ttu-id="29966-225">**New-AzureRmADServicePrincipal**</span><span class="sxs-lookup"><span data-stu-id="29966-225">**New-AzureRmADServicePrincipal**</span></span>
- <span data-ttu-id="29966-226">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-226">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a><span data-ttu-id="29966-227">**New-AzureRmADSpCredential**</span><span class="sxs-lookup"><span data-stu-id="29966-227">**New-AzureRmADSpCredential**</span></span>
- <span data-ttu-id="29966-228">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-228">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a><span data-ttu-id="29966-229">**New-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="29966-229">**New-AzureRmADUser**</span></span>
- <span data-ttu-id="29966-230">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-230">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a><span data-ttu-id="29966-231">**Set-AzureRmADUser**</span><span class="sxs-lookup"><span data-stu-id="29966-231">**Set-AzureRmADUser**</span></span>
- <span data-ttu-id="29966-232">Sostituzione del parametro "Password" con SecureString</span><span class="sxs-lookup"><span data-stu-id="29966-232">Parameter "Password" being replaced in favor of a SecureString</span></span>

```powershell
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="29966-233">Modifiche di rilievo ai cmdlet per il bus di servizio</span><span class="sxs-lookup"><span data-stu-id="29966-233">Breaking changes to ServiceBus cmdlets</span></span>

### <a name="get-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="29966-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-234">**Get-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="29966-235">Rimozione del cmdlet "Get-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-235">The 'Get-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-236">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-236">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>    

### <a name="get-azurermservicebustopickey"></a><span data-ttu-id="29966-237">**Get-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="29966-237">**Get-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="29966-238">Rimozione del cmdlet "Get-AzureRmServiceBusTopicKey".</span><span class="sxs-lookup"><span data-stu-id="29966-238">The 'Get-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-239">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-239">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="29966-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-240">**New-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="29966-241">Rimozione del cmdlet "New-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-241">The 'New-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-242">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-242">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebustopickey"></a><span data-ttu-id="29966-243">**New-AzureRmServiceBusTopicKey**</span><span class="sxs-lookup"><span data-stu-id="29966-243">**New-AzureRmServiceBusTopicKey**</span></span>
- <span data-ttu-id="29966-244">Rimozione del cmdlet "New-AzureRmServiceBusTopicKey".</span><span class="sxs-lookup"><span data-stu-id="29966-244">The 'New-AzureRmServiceBusTopicKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-245">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-245">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="29966-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-246">**Remove-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="29966-247">Rimozione del cmdlet "Remove-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-247">The 'Remove-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-248">Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-248">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebustopicauthorizationrule"></a><span data-ttu-id="29966-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-249">**Set-AzureRmServiceBusTopicAuthorizationRule**</span></span>
- <span data-ttu-id="29966-250">Rimozione del cmdlet "Set-AzureRmServiceBusTopicAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-250">The 'Set-AzureRmServiceBusTopicAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-251">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-251">Please use the 'Set-AzureRmServiceBusAuthorizationRule'cmdlet.</span></span>

### <a name="new-azurermservicebusnamespacekey"></a><span data-ttu-id="29966-252">**New-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="29966-252">**New-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="29966-253">Rimozione del cmdlet "New-AzureRmServiceBusNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="29966-253">The 'New-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-254">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-254">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="get-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="29966-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-255">**Get-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="29966-256">Rimozione del cmdlet "Get-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-256">The 'Get-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-257">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-257">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusqueuekey"></a><span data-ttu-id="29966-258">**Get-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="29966-258">**Get-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="29966-259">Rimozione del cmdlet "Get-AzureRmServiceBusQueueKey".</span><span class="sxs-lookup"><span data-stu-id="29966-259">The 'Get-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-260">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-260">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="29966-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-261">**New-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="29966-262">Rimozione del cmdlet "New-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-262">The 'New-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-263">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-263">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="new-azurermservicebusqueuekey"></a><span data-ttu-id="29966-264">**New-AzureRmServiceBusQueueKey**</span><span class="sxs-lookup"><span data-stu-id="29966-264">**New-AzureRmServiceBusQueueKey**</span></span>
- <span data-ttu-id="29966-265">Rimozione del cmdlet "New-AzureRmServiceBusQueueKey".</span><span class="sxs-lookup"><span data-stu-id="29966-265">The 'New-AzureRmServiceBusQueueKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-266">Usare il cmdlet "New-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-266">Please use the 'New-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="remove-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="29966-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-267">**Remove-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="29966-268">Rimozione del cmdlet "Remove-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-268">The 'Remove-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-269">Usare il cmdlet "GRemove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-269">Please use the 'GRemove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusqueueauthorizationrule"></a><span data-ttu-id="29966-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-270">**Set-AzureRmServiceBusQueueAuthorizationRule**</span></span>
- <span data-ttu-id="29966-271">Rimozione del cmdlet "Set-AzureRmServiceBusQueueAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-271">The 'Set-AzureRmServiceBusQueueAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-272">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-272">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="29966-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-273">**Get-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-274">Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-274">The 'Get-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-275">Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-275">Please use the 'Get-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="get-azurermservicebusnamespacekey"></a><span data-ttu-id="29966-276">**Get-AzureRmServiceBusNamespaceKey**</span><span class="sxs-lookup"><span data-stu-id="29966-276">**Get-AzureRmServiceBusNamespaceKey**</span></span>
- <span data-ttu-id="29966-277">Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceKey".</span><span class="sxs-lookup"><span data-stu-id="29966-277">The 'Get-AzureRmServiceBusNamespaceKey' cmdlet has been removed.</span></span> <span data-ttu-id="29966-278">Usare il cmdlet "Get-AzureRmServiceBusKey".</span><span class="sxs-lookup"><span data-stu-id="29966-278">Please use the 'Get-AzureRmServiceBusKey' cmdlet.</span></span>

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="29966-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-279">**New-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-280">Rimozione del cmdlet "New-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-280">The 'New-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-281">Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-281">Please use the 'New-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="29966-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-282">**Remove-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-283">Rimozione del cmdlet "Remove-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-283">The 'Remove-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-284">Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-284">Please use the 'Remove-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a><span data-ttu-id="29966-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span><span class="sxs-lookup"><span data-stu-id="29966-285">**Set-AzureRmServiceBusNamespaceAuthorizationRule**</span></span>
- <span data-ttu-id="29966-286">Rimozione del cmdlet "Set-AzureRmServiceBusNamespaceAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-286">The 'Set-AzureRmServiceBusNamespaceAuthorizationRule' cmdlet has been removed.</span></span> <span data-ttu-id="29966-287">Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".</span><span class="sxs-lookup"><span data-stu-id="29966-287">Please use the 'Set-AzureRmServiceBusAuthorizationRule' cmdlet.</span></span>

### <a name="type-namespaceattributes"></a><span data-ttu-id="29966-288">**Tipo NamespaceAttributes**</span><span class="sxs-lookup"><span data-stu-id="29966-288">**Type NamespaceAttributes**</span></span>
- <span data-ttu-id="29966-289">Le proprietà seguenti sono state rimosse:</span><span class="sxs-lookup"><span data-stu-id="29966-289">The following properties have been removed</span></span>
    - <span data-ttu-id="29966-290">Attivato</span><span class="sxs-lookup"><span data-stu-id="29966-290">Enabled</span></span>
    - <span data-ttu-id="29966-291">Status</span><span class="sxs-lookup"><span data-stu-id="29966-291">Status</span></span>
   
```powershell
# Old
# The $namespace has Status and Enabled property 
$namespace = Get-AzureRmServiceBusNamespace <parameters>
$namespace.Status
$namespace.Enabled

# New
# The call remains the same, but the returned values NameSpace object will not have the Enabled and Status properties    
$namespace = Get-AzureRmServiceBusNamespace <parameters>
```

### <a name="type-queueattribute"></a><span data-ttu-id="29966-292">**Tipo QueueAttribute**</span><span class="sxs-lookup"><span data-stu-id="29966-292">**Type QueueAttribute**</span></span>
- <span data-ttu-id="29966-293">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="29966-293">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="29966-294">EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="29966-294">EnableBatchedOperations</span></span>
    - <span data-ttu-id="29966-295">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="29966-295">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="29966-296">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="29966-296">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="29966-297">SupportOrdering</span><span class="sxs-lookup"><span data-stu-id="29966-297">SupportOrdering</span></span>

```powershell
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
   
### <a name="type-topicattribute"></a><span data-ttu-id="29966-298">**Tipo TopicAttribute**</span><span class="sxs-lookup"><span data-stu-id="29966-298">**Type TopicAttribute**</span></span>
- <span data-ttu-id="29966-299">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="29966-299">The following properties are marked as obsolete:</span></span>
    - <span data-ttu-id="29966-300">Località</span><span class="sxs-lookup"><span data-stu-id="29966-300">Location</span></span>
    - <span data-ttu-id="29966-301">IsExpress</span><span class="sxs-lookup"><span data-stu-id="29966-301">IsExpress</span></span>
    - <span data-ttu-id="29966-302">IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="29966-302">IsAnonymousAccessible</span></span>
    - <span data-ttu-id="29966-303">FilteringMessagesBeforePublishing</span><span class="sxs-lookup"><span data-stu-id="29966-303">FilteringMessagesBeforePublishing</span></span>
    - <span data-ttu-id="29966-304">EnableSubscriptionPartitioning</span><span class="sxs-lookup"><span data-stu-id="29966-304">EnableSubscriptionPartitioning</span></span>
    - <span data-ttu-id="29966-305">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="29966-305">EntityAvailabilityStatus</span></span>

```powershell
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
   
### <a name="type-subscriptionattribute"></a><span data-ttu-id="29966-306">**Tipo SubscriptionAttribute**</span><span class="sxs-lookup"><span data-stu-id="29966-306">**Type SubscriptionAttribute**</span></span>
- <span data-ttu-id="29966-307">Le proprietà seguenti sono state contrassegnate come obsolete:</span><span class="sxs-lookup"><span data-stu-id="29966-307">The following properties are marked as obsolete</span></span>
    - <span data-ttu-id="29966-308">DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="29966-308">DeadLetteringOnFilterEvaluationExceptions</span></span>
    - <span data-ttu-id="29966-309">EntityAvailabilityStatus</span><span class="sxs-lookup"><span data-stu-id="29966-309">EntityAvailabilityStatus</span></span>
    - <span data-ttu-id="29966-310">IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="29966-310">IsReadOnly</span></span>
    - <span data-ttu-id="29966-311">Località</span><span class="sxs-lookup"><span data-stu-id="29966-311">Location</span></span>
   
```powershell
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