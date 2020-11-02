---
title: Guida alla migrazione per Az 5.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 5.0.0 di Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 3a82e738bcb652ddc38886f7064e7373b5fb8cc1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753826"
---
# <a name="migration-guide-for-az-500"></a>Guida alla migrazione per Az 5.0.0

Questo documento descrive le modifiche apportate tra le versioni 4.0.0 e 5.0.0 del modulo Az.

- [Guida alla migrazione per Az 5.0.0](#migration-guide-for-az-500)
  - [Az.Aks](#azaks)
    - [New-AzAksCluster](#new-azakscluster)
    - [Set-AzAksCluster](#set-azakscluster)
  - [Az.ContainerRegistry](#azcontainerregistry)
    - [New-AzContainerRegistry](#new-azcontainerregistry)
  - [Az.Functions](#azfunctions)
    - [Get-AzFunctionApp](#get-azfunctionapp)
    - [New-AzFunctionApp](#new-azfunctionapp)
  - [Az.KeyVault](#azkeyvault)
    - [New-AzKeyVault](#new-azkeyvault)
    - [Update-AzKeyVault](#update-azkeyvault)
    - [Get-AzKeyVaultSecret](#get-azkeyvaultsecret)
  - [Az.ManagedServices](#azmanagedservices)
    - [Get-AzManagedServicesDefinition](#get-azmanagedservicesdefinition)
    - [New-AzManagedServicesAssignment](#new-azmanagedservicesassignment)
    - [Remove-AzManagedServicesAssignment](#remove-azmanagedservicesassignment)
    - [Remove-AzManagedServicesDefinition](#remove-azmanagedservicesdefinition)
  - [Az.ResourceManager](#azresourcemanager)
    - [Get-AzManagementGroupDeployment](#get-azmanagementgroupdeployment)
    - [Get-AzManagementGroupDeploymentOperation](#get-azmanagementgroupdeploymentoperation)
    - [Get-AzDeployment](#get-azdeployment)
    - [Get-AzDeploymentOperation](#get-azdeploymentoperation)
    - [Get-AzDeploymentWhatIfResult](#get-azdeploymentwhatifresult)
    - [Get-AzTenantDeployment](#get-aztenantdeployment)
    - [Get-AzTenantDeploymentOperation](#get-aztenantdeploymentoperation)
    - [New-AzManagementGroupDeployment](#new-azmanagementgroupdeployment)
    - [New-AzDeployment](#new-azdeployment)
    - [New-AzTenantDeployment](#new-aztenantdeployment)
    - [Remove-AzManagementGroupDeployment](#remove-azmanagementgroupdeployment)
    - [Remove-AzDeployment](#remove-azdeployment)
    - [Remove-AzTenantDeployment](#remove-aztenantdeployment)
    - [Save-AzManagementGroupDeploymentTemplate](#save-azmanagementgroupdeploymenttemplate)
    - [Save-AzDeploymentTemplate](#save-azdeploymenttemplate)
    - [Save-AzTenantDeploymentTemplate](#save-aztenantdeploymenttemplate)
    - [Stop-AzManagementGroupDeployment](#stop-azmanagementgroupdeployment)
    - [Stop-AzDeployment](#stop-azdeployment)
    - [Stop-AzTenantDeployment](#stop-aztenantdeployment)
    - [Test-AzManagementGroupDeployment](#test-azmanagementgroupdeployment)
    - [Test-AzDeployment](#test-azdeployment)
    - [Test-AzTenantDeployment](#test-aztenantdeployment)
    - [Get-AzResourceGroupDeployment](#get-azresourcegroupdeployment)
    - [Get-AzResourceGroupDeploymentOperation](#get-azresourcegroupdeploymentoperation)
    - [Get-AzResourceGroupDeploymentWhatIfResult](#get-azresourcegroupdeploymentwhatifresult)
    - [New-AzResourceGroupDeployment](#new-azresourcegroupdeployment)
    - [Remove-AzResourceGroupDeployment](#remove-azresourcegroupdeployment)
    - [Save-AzResourceGroupDeploymentTemplate](#save-azresourcegroupdeploymenttemplate)
    - [Stop-AzResourceGroupDeployment](#stop-azresourcegroupdeployment)
    - [Test-AzResourceGroupDeployment](#test-azresourcegroupdeployment)
    - [Get-AzManagementGroupDeploymentWhatIfResult](#get-azmanagementgroupdeploymentwhatifresult)
    - [Get-AzTenantDeploymentWhatIfResult](#get-aztenantdeploymentwhatifresult)
  - [Az.Sql](#azsql)
    - [Set-AzSqlServerActiveDirectoryAdministrator](#set-azsqlserveractivedirectoryadministrator)
  - [Az.Synapse](#azsynapse)
    - [New-AzSynapseSqlPool](#new-azsynapsesqlpool)
    - [Update-AzSynapseSqlPool](#update-azsynapsesqlpool)
  - [Az.Network](#aznetwork)
    - [Approve-AzPrivateEndpointConnection](#approve-azprivateendpointconnection)
    - [Deny-AzPrivateEndpointConnection](#deny-azprivateendpointconnection)
    - [Get-AzPrivateEndpointConnection](#get-azprivateendpointconnection)
    - [Remove-AzPrivateEndpointConnection](#remove-azprivateendpointconnection)
    - [Set-AzPrivateEndpointConnection](#set-azprivateendpointconnection)
    - [New-AzNetworkWatcherConnectionMonitorEndpointObject](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a>Az.Aks

### <a name="new-azakscluster"></a>New-AzAksCluster

- Non supporta più il parametro `NodeOsType` e non è stato trovato alcun alias per il nome del parametro originale. Sarà sempre `Linux`.
- Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.
- Il valore predefinito di `NodeVmSetType` è cambiato da `AvailabilitySet` a `VirtualMachineScaleSets`.
- Il valore predefinito di `NetworkPlugin` è cambiato da `none` a `azure`.

#### <a name="before"></a>Prima

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a>Dopo

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a>Set-AzAksCluster

Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.

#### <a name="before"></a>Prima

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a>Dopo

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a>Az.ContainerRegistry

### <a name="new-azcontainerregistry"></a>New-AzContainerRegistry

Non supporta più il parametro `StorageAccountName` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a>Dopo

`Classic` è stato deprecato e `StorageAccountName` è stato rimosso perché funziona solo con la versione classica di Registro Container.

## <a name="azfunctions"></a>Az.Functions

### <a name="get-azfunctionapp"></a>Get-AzFunctionApp

Il parametro opzionale `IncludeSlot` è stato rimosso da tutti i set di parametri di `Get-AzFunctionApp` tranne uno. Il cmdlet supporta ora il recupero degli slot di distribuzione nei risultati quando si specifica `-IncludeSlot`.
Questa funzionalità non veniva eseguita correttamente nella versione precedente del cmdlet. Tuttavia, ora è stata corretta.

### <a name="new-azfunctionapp"></a>New-AzFunctionApp

- Il parametro `-DisableApplicationInsights` di `New-AzFunctionApp` è stato corretto per cui quando questa opzione viene specificata non vengono creati progetti di Application Insights.
- Il supporto per creare app per le funzioni di PowerShell 6.2 è stato rimosso dopo la data EOL di Poiché PowerShell 6.2. L'indicazione corrente per i clienti è di creare invece app per le funzioni di PowerShell 7.0.
- La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 6.2 a 7.0 nelle app per le funzioni di Windows per PowerShell quando il parametro `RuntimeVersion` non viene specificato.
- La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 10 a 12 nelle app per le funzioni di Windows e Linux per Node quando il parametro `RuntimeVersion` non viene specificato. Tuttavia, gli utenti possono comunque creare app per le funzioni di Node 10 specificando `-Runtime Node` e `-RuntimeVersion 10`. La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 3.7 a 3.8 nelle app per le funzioni di Linux per Python quando il parametro `RuntimeVersion` non viene specificato. Tuttavia, gli utenti possono comunque creare app per le funzioni di Python 3.7 specificando `-Runtime Python` e `-RuntimeVersion 3.7`.

#### <a name="before"></a>Prima

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a>Dopo

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a>Az.KeyVault

### <a name="new-azkeyvault"></a>New-AzKeyVault

Non supporta più il parametro `DisableSoftDelete` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a>Dopo

La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0. Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="update-azkeyvault"></a>Update-AzKeyVault

Non supporta più i parametri `EnableSoftDelete`, `SoftDeleteRetentionInDays` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a>Dopo

La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0. Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change

### <a name="get-azkeyvaultsecret"></a>Get-AzKeyVaultSecret

La proprietà `SecretValueText` di tipo `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` è stata rimossa. La proprietà `SecretValueText` è stata sostituita con `SecretValue`.

#### <a name="before"></a>Prima

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a>Dopo

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a>Az.ManagedServices

### <a name="get-azmanagedservicesdefinition"></a>Get-AzManagedServicesDefinition

Non supporta più il parametro `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Dopo

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a>New-AzManagedServicesAssignment

Non supporta più i parametri `RegistrationDefinitionName`, `RegistrationDefinitionResourceId` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a>Dopo

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a>Remove-AzManagedServicesAssignment

Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a>Dopo

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a>Remove-AzManagedServicesDefinition

Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a>Dopo

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a>Az.ResourceManager

### <a name="get-azmanagementgroupdeployment"></a>Get-AzManagementGroupDeployment

Non supporta più il parametro `ApiVersion` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a>Dopo

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a>Get-AzManagementGroupDeploymentOperation

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azdeployment"></a>Get-AzDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentoperation"></a>Get-AzDeploymentOperation

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azdeploymentwhatifresult"></a>Get-AzDeploymentWhatIfResult

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeployment"></a>Get-AzTenantDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentoperation"></a>Get-AzTenantDeploymentOperation

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="new-azmanagementgroupdeployment"></a>New-AzManagementGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="new-azdeployment"></a>New-AzDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="new-aztenantdeployment"></a>New-AzTenantDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="remove-azmanagementgroupdeployment"></a>Remove-AzManagementGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="remove-azdeployment"></a>Remove-AzDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="remove-aztenantdeployment"></a>Remove-AzTenantDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="save-azmanagementgroupdeploymenttemplate"></a>Save-AzManagementGroupDeploymentTemplate

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="save-azdeploymenttemplate"></a>Save-AzDeploymentTemplate

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="save-aztenantdeploymenttemplate"></a>Save-AzTenantDeploymentTemplate

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="stop-azmanagementgroupdeployment"></a>Stop-AzManagementGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="stop-azdeployment"></a>Stop-AzDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="stop-aztenantdeployment"></a>Stop-AzTenantDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="test-azmanagementgroupdeployment"></a>Test-AzManagementGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="test-azdeployment"></a>Test-AzDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="test-aztenantdeployment"></a>Test-AzTenantDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeployment"></a>Get-AzResourceGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentoperation"></a>Get-AzResourceGroupDeploymentOperation

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azresourcegroupdeploymentwhatifresult"></a>Get-AzResourceGroupDeploymentWhatIfResult

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="new-azresourcegroupdeployment"></a>New-AzResourceGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="remove-azresourcegroupdeployment"></a>Remove-AzResourceGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="save-azresourcegroupdeploymenttemplate"></a>Save-AzResourceGroupDeploymentTemplate

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="stop-azresourcegroupdeployment"></a>Stop-AzResourceGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="test-azresourcegroupdeployment"></a>Test-AzResourceGroupDeployment

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a>Get-AzManagementGroupDeploymentWhatIfResult

Uguale a `Get-AzManagementGroupDeployment`.

### <a name="get-aztenantdeploymentwhatifresult"></a>Get-AzTenantDeploymentWhatIfResult

Uguale a `Get-AzManagementGroupDeployment`.

## <a name="azsql"></a>Az.Sql

### <a name="set-azsqlserveractivedirectoryadministrator"></a>Set-AzSqlServerActiveDirectoryAdministrator

Non supporta più il parametro `IsAzureADOnlyAuthentication` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a>Dopo

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a>Az.Synapse

### <a name="new-azsynapsesqlpool"></a>New-AzSynapseSqlPool

Non supporta più i parametri `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a>Dopo

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a>Update-AzSynapseSqlPool

Non supporta più i parametri `Suspend`, `Resume` e non è stato trovato alcun alias per il nome del parametro originale.

## <a name="aznetwork"></a>Az.Network

### <a name="approve-azprivateendpointconnection"></a>Approve-AzPrivateEndpointConnection

Non supporta più il parametro `PrivateLinkResourceType` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a>Dopo

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a>Deny-AzPrivateEndpointConnection

Uguale a `Approve-AzPrivateEndpointConnection`.

### <a name="get-azprivateendpointconnection"></a>Get-AzPrivateEndpointConnection

Uguale a `Approve-AzPrivateEndpointConnection`.

### <a name="remove-azprivateendpointconnection"></a>Remove-AzPrivateEndpointConnection

Uguale a `Approve-AzPrivateEndpointConnection`.

### <a name="set-azprivateendpointconnection"></a>Set-AzPrivateEndpointConnection

Uguale a `Approve-AzPrivateEndpointConnection`.

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a>New-AzNetworkWatcherConnectionMonitorEndpointObject

Non supporta più i parametri `FilterType`, `FilterItem` e non è stato trovato alcun alias per il nome del parametro originale.

#### <a name="before"></a>Prima

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a>After

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
