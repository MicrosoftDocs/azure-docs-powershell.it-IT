---
title: Modifiche di rilievo in Microsoft Azure PowerShell 5.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche che causano interruzioni apportate ad Azure PowerShell nella versione 5.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: f8dc413a91876e53e62d25cc38ac3b3ef6afda8e
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534597"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-500"></a>Modifiche di rilievo in Microsoft Azure PowerShell 5.0.0

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

Questo documento funge sia da notifica delle modifiche di rilievo che da guida alla migrazione per gli utenti dei cmdlet di Microsoft Azure PowerShell. Ogni sezione descrive sia l'impulso alla base della modifica di rilievo che il percorso di migrazione più semplice. Per un approfondimento del contesto, vedere la richiesta pull associata a ogni modifica.

## <a name="table-of-contents"></a>Sommario

- [Modifiche di rilievo ai cmdlet per Gestione API](#breaking-changes-to-apimanagement-cmdlets)
- [Modifiche di rilievo ai cmdlet per Batch](#breaking-changes-to-batch-cmdlets)
- [Modifiche di rilievo ai cmdlet per le risorse di calcolo](#breaking-changes-to-compute-cmdlets)
- [Modifiche di rilievo ai cmdlet per Hub eventi](#breaking-changes-to-eventhub-cmdlets)
- [Modifiche di rilievo ai cmdlet per Insights](#breaking-changes-to-insights-cmdlets)
- [Modifiche di rilievo ai cmdlet per le reti](#breaking-changes-to-network-cmdlets)
- [Modifiche di rilievo ai cmdlet per le risorse](#breaking-changes-to-resources-cmdlets)
- [Modifiche di rilievo ai cmdlet per il bus di servizio](#breaking-changes-to-servicebus-cmdlets)

## <a name="breaking-changes-to-apimanagement-cmdlets"></a>Modifiche di rilievo ai cmdlet per Gestione API

### <a name="new-azurermapimanagementbackendproxy"></a>**New-AzureRmApiManagementBackendProxy**
- Sostituzione dei parametri "UserName" e "Password" con PSCredential

```powershell-interactive
# Old
New-AzureRmApiManagementBackendProxy [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
New-AzureRmApiManagementBackendProxy [other required parameters] -Credential $PSCredentialVariable
```

### <a name="new-azurermapimanagementuser"></a>**New-AzureRmApiManagementUser**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapimanagementuser"></a>**Set-AzureRmApiManagementUser**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
Set-AzureRmApiManagementUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApiManagementUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-batch-cmdlets"></a>Modifiche di rilievo ai cmdlet per Batch

### <a name="new-azurebatchcertificate"></a>**New-AzureBatchCertificate**
- Sostituzione del parametro `Password` con una stringa sicura

```powershell-interactive
# Old
New-AzureBatchCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureBatchCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchcomputenodeuser"></a>**New-AzureBatchComputeNodeUser**
- Sostituzione del parametro `Password` con una stringa sicura

```powershell-interactive
# Old
New-AzureBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
New-AzureBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermbatchcomputenodeuser"></a>**Set-AzureRmBatchComputeNodeUser**
- Sostituzione del parametro `Password` con una stringa sicura

```powershell-interactive
# Old
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmBatchComputeNodeUser [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurebatchtask"></a>**New-AzureBatchTask**
 - Rimozione dell'opzione `RunElevated` e relativa sostituzione con `UserIdentity`.

```powershell-interactive
# Old
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -RunElevated $TRUE

# New
$autoUser = New-Object Microsoft.Azure.Commands.Batch.Models.PSAutoUserSpecification -ArgumentList @("Task", "Admin")
$userIdentity = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserIdentity $autoUser
New-AzureBatchTask -Id $taskId1 -JobId $jobId -CommandLine "cmd /c echo hello" -UserIdentity $userIdentity
```

Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.

### <a name="psmultiinstancesettings"></a>**PSMultiInstanceSettings**

- Il costruttore `PSMultiInstanceSettings` non accetta più un parametro `numberOfInstances` obbligatorio. Accetta invece un parametro `coordinationCommandLine` obbligatorio.

```powershell-interactive
# Old
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @(2)
$settings.CoordinationCommandLine = "cmd /c echo hello"
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings

# New
$settings = New-Object Microsoft.Azure.Commands.Batch.Models.PSMultiInstanceSettings -ArgumentList @("cmd /c echo hello", 2)
New-AzureBatchTask [other parameters] -MultiInstanceSettings $settings
```

### <a name="get-azurebatchtask"></a>**Get-AzureBatchTask**
 - Rimozione della proprietà `RunElevated` per `PSCloudTask`. Per sostituire `RunElevated` è stata aggiunta la proprietà `UserIdentity`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.RunElevated

# New
$task = Get-AzureBatchTask [parameters]
$task.UserIdentity.AutoUser.ElevationLevel
```

Questo ha un impatto anche sulla proprietà `RunElevated` per `PSCloudTask`, `PSStartTask`, `PSJobManagerTask`, `PSJobPreparationTask` e `PSJobReleaseTask`.

### <a name="multiple-types"></a>**Più tipi**

- Ridenominazione della proprietà `SchedulingError` per `PSExitConditions` in `PreProcessingError`.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExitConditions.PreProcessingError
```

### <a name="multiple-types"></a>**Più tipi**

- Ridenominazione della proprietà `SchedulingError` per `PSJobPreparationTaskExecutionInformation`, `PSJobReleaseTaskExecutionInformation`, `PSStartTaskInformation`, `PSSubtaskInformation` e `PSTaskExecutionInformation` in `FailureInformation`.
  - Ogni volta che si verifica un errore delle attività viene restituito `FailureInformation`. Questo include tutti i precedenti casi di errori di pianificazione, nonché i codici di uscita delle attività diversi da zero e gli errori di caricamento file della nuova funzionalità per i file di output.
  - È stata mantenuta la struttura precedente e non sono quindi necessarie modifiche di codice quando si usa questo tipo.

```powershell-interactive
# Old
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.SchedulingError

# New
$task = Get-AzureBatchTask [parameters]
$task.ExecutionInformation.FailureInformation
```

Questo influisce anche su: Get-AzureBatchPool, Get-AzureBatchSubtask e Get-AzureBatchJobPreparationAndReleaseTaskStatus

### <a name="new-azurebatchpool"></a>**New-AzureBatchPool**
 - Rimozione di `TargetDedicated` e relativa sostituzione con `TargetDedicatedComputeNodes` e `TargetLowPriorityComputeNodes`.
 - `TargetDedicatedComputeNodes` ha un alias `TargetDedicated`.

```powershell-interactive
# Old
New-AzureBatchPool [other parameters] [-TargetDedicated <Int32>]

# New
New-AzureBatchPool [other parameters] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
```

Questo influisce anche su: Start-AzureBatchPoolResize

### <a name="get-azurebatchpool"></a>**Get-AzureBatchPool**
 - Ridenominazione delle proprietà `TargetDedicated` e `CurrentDedicated` per `PSCloudPool` in `TargetDedicatedComputeNodes` e `CurrentDedicatedComputeNodes`.

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

### <a name="type-pscloudpool"></a>**Tipo PSCloudPool**

- Ridenominazione di `ResizeError` in `ResizeErrors`, che è ora una raccolta, per `PSCloudPool`.

```powershell-interactive
# Old
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeError

# New
$pool = Get-AzureBatchPool [parameters]
$pool.ResizeErrors[0]
```

### <a name="new-azurebatchjob"></a>**New-AzureBatchJob**
- Ridenominazione della proprietà `TargetDedicated` per `PSPoolSpecification` in `TargetDedicatedComputeNodes`.

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

### <a name="get-azurebatchnodefile"></a>**Get-AzureBatchNodeFile**
 - Rimozione di `Name` e relativa sostituzione con `Path`.
 - `Path` ha un alias `Name`.

```powershell-interactive
# Old
Get-AzureBatchNodeFile [other parameters] [[-Name] <String>]

# New
Get-AzureBatchNodeFile [other parameters] [[-Path] <String>]
```

Questo influisce anche su: Get-AzureBatchNodeFileContent, Remove-AzureBatchNodeFile

### <a name="type-psnodefile"></a>Tipo **PSNodeFile**

 - Ridenominazione della proprietà `Name` per `PSNodeFile` in `Path`.

```powershell-interactive
# Old
$file = Get-AzureBatchNodeFile [parameters]
$file.Name

# New
$file = Get-AzureBatchNodeFile [parameters]
$file.Path
```

### <a name="get-azurebatchsubtask"></a>**Get-AzureBatchSubtask**
- Le proprietà `PreviousState` e `State` di `PSSubtaskInformation` non sono più di tipo `TaskState` e sono invece di tipo `SubtaskState`.
  - A differenza di `TaskState`, `SubtaskState` non ha un valore `Active` perché le sottoattività non possono essere in stato `Active`.

```powershell-interactive
# Old
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.TaskState.Running) { }

# New
$subtask = Get-AzureBatchSubtask [parameters]
if ($subtask.State -eq Microsoft.Azure.Batch.Common.SubtaskState.Running) { }
```

## <a name="breaking-changes-to-compute-cmdlets"></a>Modifiche di rilievo ai cmdlet per le risorse di calcolo

### <a name="set-azurermvmaccessextension"></a>**Set-AzureRmVMAccessExtension**
- Sostituzione dei parametri "UserName" e "Password" con PSCredential

```powershell-interactive
# Old
Set-AzureRmVMAccessExtension [other required parameters] -UserName "plain-text string" -Password "plain-text string"

# New
Set-AzureRmVMAccessExtension [other required parameters] -Credential $PSCredential
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a>Modifiche di rilievo ai cmdlet per Hub eventi

### <a name="new-azurermeventhubnamespaceauthorizationrule"></a>**New-AzureRmEventHubNamespaceAuthorizationRule**
- Rimozione del cmdlet "New-AzureRmEventHubNamespaceAuthorizationRule". Usare il cmdlet "New-AzureRmEventHubAuthorizationRule"
    
### <a name="get-azurermeventhubnamespaceauthorizationrule"></a>**Get-AzureRmEventHubNamespaceAuthorizationRule**
- Rimozione del cmdlet "Get-AzureRmEventHubNamespaceAuthorizationRule". Usare il cmdlet "Get-AzureRmEventHubAuthorizationRule"
    
### <a name="set-azurermeventhubnamespaceauthorizationrule"></a>**Set-AzureRmEventHubNamespaceAuthorizationRule**
- Rimozione del cmdlet "Set-AzureRmEventHubNamespaceAuthorizationRule". Usare il cmdlet "Set-AzureRmEventHubAuthorizationRule"
    
### <a name="remove-azurermeventhubnamespaceauthorizationrule"></a>**Remove-AzureRmEventHubNamespaceAuthorizationRule**
- Rimozione del cmdlet "Remove-AzureRmEventHubNamespaceAuthorizationRule". Usare il cmdlet "Remove-AzureRmEventHubAuthorizationRule"
    
### <a name="new-azurermeventhubnamespacekey"></a>**New-AzureRmEventHubNamespaceKey**
- Rimozione del cmdlet "New-AzureRmEventHubNamespaceKey". Usare il cmdlet "New-AzureRmEventHubKey"
    
### <a name="get-azurermeventhubnamespacekey"></a>**Get-AzureRmEventHubNamespaceKey**
- Rimozione del cmdlet "Get-AzureRmEventHubNamespaceKey". Usare il cmdlet "Get-AzureRmEventHubKey"
    
### <a name="new-azurermeventhubnamespace"></a>**New-AzureRmEventHubNamespace**
- Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes. 

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
    
### <a name="get-azurermeventhubnamespace"></a>**Get-AzureRmEventHubNamespace**
- Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes. 

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
    
### <a name="set-azurermeventhubnamespace"></a>**Set-AzureRmEventHubNamespace**
- Rimozione delle proprietà "Status" e "Enabled" da NamespceAttributes. 

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
  
### <a name="new-azurermeventhubconsumergroup"></a>**New-AzureRmEventHubConsumerGroup**
- Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = New-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="set-azurermeventhubconsumergroup"></a>**Set-AzureRmEventHubConsumerGroup**
- Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Set-AzureRmEventHubConsumerGroup <parameters>
```
    
### <a name="get-azurermeventhubconsumergroup"></a>**Get-AzureRmEventHubConsumerGroup**
- Rimozione della proprietà "EventHubPath" da ConsumerGroupAttributes.

```powershell-interactive
# Old
# The $consumergroup has EventHubPath property 
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
$consumergroup.EventHubPath

# New
# The call remains the same, but the returned values ConsumerGroup object will not have the EventHubPath property    
$consumergroup = Get-AzureRmEventHubConsumerGroup <parameters>
```

## <a name="breaking-changes-to-insights-cmdlets"></a>Modifiche di rilievo ai cmdlet per Insights

### <a name="add-azurermlogalertrule"></a>**Add-AzureRMLogAlertRule**
- Il cmdlet **Add-AzureRMLogAlertRule** è stato deprecato.
- Dopo il 1° ottobre, l'uso di questo cmdlet non avrà più alcun effetto a causa della transizione di questa funzionalità agli avvisi del log attività. Per altre informazioni, vedere https://aka.ms/migratemealerts.

### <a name="get-azurermusage"></a>**Get-AzureRMUsage**
- Il cmdlet **Get-AzureRMUsage** è stato deprecato.

### <a name="get-azurermalerthistory--get-azurermautoscalehistory--get-azurermlogs"></a>**Get-AzureRmAlertHistory** / **Get-AzureRmAutoscaleHistory** / **Get-AzureRmLogs**
- Modifica a livello di output: il campo EventChannels dell'oggetto EventData, restituito da questi cmdlet, verrà deprecato perché viene ora restituito un valore costante (Admin,Operation).

### <a name="get-azurermalertrule"></a>**Get-AzureRmAlertRule**
- Modifica a livello di output: l'output di questo cmdlet verrà reso flat, ad esempio con l'eliminazione del campo properties, per migliorare l'esperienza utente.

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

### <a name="get-azurermautoscalesetting"></a>**Get-AzureRmAutoscaleSetting**
- Modifica a livello di output: il campo AutoscaleSettingResourceName verrà deprecato perché è sempre uguale al campo Name.

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

### <a name="remove-azurermalertrule--remove-azurermlogprofile"></a>**Remove-AzureRmAlertRule** / **Remove-AzureRmLogProfile**
- Modifica a livello di output: il tipo dell'output verrà modificato in modo da restituire un singolo oggetto contenente ID richiesta e codice di stato.

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

## <a name="breaking-changes-to-network-cmdlets"></a>Modifiche di rilievo ai cmdlet per le reti

### <a name="add-azurermapplicationgatewaysslcertificate"></a>**Add-AzureRmApplicationGatewaySslCertificate**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Add-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermapplicationgatewaysslcertificate"></a>**New-AzureRmApplicationGatewaySslCertificate**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
New-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermapplicationgatewaysslcertificate"></a>**Set-AzureRmApplicationGatewaySslCertificate**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password "plain-text string"

# New
Set-AzureRmApplicationGatewaySslCertificate [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-resources-cmdlets"></a>Modifiche di rilievo ai cmdlet per le risorse

### <a name="new-azurermadappcredential"></a>**New-AzureRmADAppCredential**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmADAppCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADAppCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadapplication"></a>**New-AzureRmADApplication**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmADApplication [other required parameters] -Password "plain-text string"

# New
New-AzureRmADApplication [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadserviceprincipal"></a>**New-AzureRmADServicePrincipal**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmADServicePrincipal [other required parameters] -Password "plain-text string"

# New
New-AzureRmADServicePrincipal [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermadspcredential"></a>**New-AzureRmADSpCredential**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmADSpCredential [other required parameters] -Password "plain-text string"

# New
New-AzureRmADSpCredential [other required parameters] -Password $SecureStringVariable
```

### <a name="new-azurermaduser"></a>**New-AzureRmADUser**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
New-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
New-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

### <a name="set-azurermaduser"></a>**Set-AzureRmADUser**
- Sostituzione del parametro "Password" con SecureString

```powershell-interactive
# Old
Set-AzureRmADUser [other required parameters] -Password "plain-text string"

# New
Set-AzureRmADUser [other required parameters] -Password $SecureStringVariable
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a>Modifiche di rilievo ai cmdlet per il bus di servizio

### <a name="get-azurermservicebustopicauthorizationrule"></a>**Get-AzureRmServiceBusTopicAuthorizationRule**
- Rimozione del cmdlet "Get-AzureRmServiceBusTopicAuthorizationRule". Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".    

### <a name="get-azurermservicebustopickey"></a>**Get-AzureRmServiceBusTopicKey**
- Rimozione del cmdlet "Get-AzureRmServiceBusTopicKey". Usare il cmdlet "Get-AzureRmServiceBusKey".

### <a name="new-azurermservicebustopicauthorizationrule"></a>**New-AzureRmServiceBusTopicAuthorizationRule**
- Rimozione del cmdlet "New-AzureRmServiceBusTopicAuthorizationRule". Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".

### <a name="new-azurermservicebustopickey"></a>**New-AzureRmServiceBusTopicKey**
- Rimozione del cmdlet "New-AzureRmServiceBusTopicKey". Usare il cmdlet "New-AzureRmServiceBusKey".

### <a name="remove-azurermservicebustopicauthorizationrule"></a>**Remove-AzureRmServiceBusTopicAuthorizationRule**
- Rimozione del cmdlet "Remove-AzureRmServiceBusTopicAuthorizationRule". Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".

### <a name="set-azurermservicebustopicauthorizationrule"></a>**Set-AzureRmServiceBusTopicAuthorizationRule**
- Rimozione del cmdlet "Set-AzureRmServiceBusTopicAuthorizationRule". Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".

### <a name="new-azurermservicebusnamespacekey"></a>**New-AzureRmServiceBusNamespaceKey**
- Rimozione del cmdlet "New-AzureRmServiceBusNamespaceKey". Usare il cmdlet "New-AzureRmServiceBusKey".

### <a name="get-azurermservicebusqueueauthorizationrule"></a>**Get-AzureRmServiceBusQueueAuthorizationRule**
- Rimozione del cmdlet "Get-AzureRmServiceBusQueueAuthorizationRule". Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".

### <a name="get-azurermservicebusqueuekey"></a>**Get-AzureRmServiceBusQueueKey**
- Rimozione del cmdlet "Get-AzureRmServiceBusQueueKey". Usare il cmdlet "Get-AzureRmServiceBusKey".

### <a name="new-azurermservicebusqueueauthorizationrule"></a>**New-AzureRmServiceBusQueueAuthorizationRule**
- Rimozione del cmdlet "New-AzureRmServiceBusQueueAuthorizationRule". Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".

### <a name="new-azurermservicebusqueuekey"></a>**New-AzureRmServiceBusQueueKey**
- Rimozione del cmdlet "New-AzureRmServiceBusQueueKey". Usare il cmdlet "New-AzureRmServiceBusKey".

### <a name="remove-azurermservicebusqueueauthorizationrule"></a>**Remove-AzureRmServiceBusQueueAuthorizationRule**
- Rimozione del cmdlet "Remove-AzureRmServiceBusQueueAuthorizationRule". Usare il cmdlet "GRemove-AzureRmServiceBusAuthorizationRule".

### <a name="set-azurermservicebusqueueauthorizationrule"></a>**Set-AzureRmServiceBusQueueAuthorizationRule**
- Rimozione del cmdlet "Set-AzureRmServiceBusQueueAuthorizationRule". Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".

### <a name="get-azurermservicebusnamespaceauthorizationrule"></a>**Get-AzureRmServiceBusNamespaceAuthorizationRule**
- Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceAuthorizationRule". Usare il cmdlet "Get-AzureRmServiceBusAuthorizationRule".

### <a name="get-azurermservicebusnamespacekey"></a>**Get-AzureRmServiceBusNamespaceKey**
- Rimozione del cmdlet "Get-AzureRmServiceBusNamespaceKey". Usare il cmdlet "Get-AzureRmServiceBusKey".

### <a name="new-azurermservicebusnamespaceauthorizationrule"></a>**New-AzureRmServiceBusNamespaceAuthorizationRule**
- Rimozione del cmdlet "New-AzureRmServiceBusNamespaceAuthorizationRule". Usare il cmdlet "New-AzureRmServiceBusAuthorizationRule".

### <a name="remove-azurermservicebusnamespaceauthorizationrule"></a>**Remove-AzureRmServiceBusNamespaceAuthorizationRule**
- Rimozione del cmdlet "Remove-AzureRmServiceBusNamespaceAuthorizationRule". Usare il cmdlet "Remove-AzureRmServiceBusAuthorizationRule".

### <a name="set-azurermservicebusnamespaceauthorizationrule"></a>**Set-AzureRmServiceBusNamespaceAuthorizationRule**
- Rimozione del cmdlet "Set-AzureRmServiceBusNamespaceAuthorizationRule". Usare il cmdlet "Set-AzureRmServiceBusAuthorizationRule".

### <a name="type-namespaceattributes"></a>**Tipo NamespaceAttributes**
- Le proprietà seguenti sono state rimosse:
    - Attivato
    - Stato
   
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

### <a name="type-queueattribute"></a>**Tipo QueueAttribute**
- Le proprietà seguenti sono state contrassegnate come obsolete:
    - EnableBatchedOperations
    - EntityAvailabilityStatus
    - IsAnonymousAccessible
    - SupportOrdering

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
   
### <a name="type-topicattribute"></a>**Tipo TopicAttribute**
- Le proprietà seguenti sono state contrassegnate come obsolete:
    - Location
    - IsExpress
    - IsAnonymousAccessible
    - FilteringMessagesBeforePublishing
    - EnableSubscriptionPartitioning
    - EntityAvailabilityStatus

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
   
### <a name="type-subscriptionattribute"></a>**Tipo SubscriptionAttribute**
- Le proprietà seguenti sono state contrassegnate come obsolete:
    - DeadLetteringOnFilterEvaluationExceptions
    - EntityAvailabilityStatus
    - IsReadOnly
    - Location
   
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