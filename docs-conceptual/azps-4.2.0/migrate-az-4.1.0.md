---
title: Guida alla migrazione per Az 4.1.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 4.1.0 di Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.openlocfilehash: e3a4563acf4b0820b61a2ac5da244b26490c8174
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "85363466"
---
# <a name="migration-guide-for-az-410"></a>Guida alla migrazione per Az 4.1.0

Questo documento descrive le modifiche apportate tra le versioni 3.0.0 e 4.1.0 del modulo Az.

- [Guida alla migrazione per Az 4.1.0](#migration-guide-for-az-410)
  - [Az.ApiManagement](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [Az.Batch](#azbatch)
    - [`Get-AzBatchApplication`, `New-AzBatchApplication`](#get-azbatchapplication-new-azbatchapplication)
    - [`Get-AzBatchComputeNode`, `New-AzBatchPool`](#get-azbatchcomputenode-new-azbatchpool)
    - [`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [Az.Compute](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [Az.KeyVault](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [Az.Monitor](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [Az.Network](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [Az.OperationalInsights](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [Az.Resources](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [Az.Storage](#azstorage)
    - [`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [`New-AzStorageTable`, `Get-AzStorageTable`](#new-azstoragetable-get-azstoragetable)
    - [`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a>Az.ApiManagement

### `Add-AzApiManagementRegion`

Il tipo della proprietà `Type` di tipo `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` è stato modificato da `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` a `System.String`.

### `New-AzApiManagement`

- Il cmdlet `New-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `__AllParameterSets` per il cmdlet `New-AzApiManagement` è stato rimosso.

### `Set-AzApiManagement`

- Il cmdlet `Set-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `__AllParameterSets` per il cmdlet `Set-AzApiManagement` è stato rimosso.

### `Get-AzApiManagementProperty`

Il cmdlet `Get-AzApiManagementProperty` è stato sostituito da `Get-AzureApiManagementNamedValue`.

### `New-AzApiManagementProperty`

Il cmdlet `New-AzApiManagementProperty` è stato sostituito da `New-AzureApiManagementNamedValue`.

### `Remove-AzApiManagementProperty`

Il cmdlet `Remove-AzApiManagementProperty` è stato sostituito da `Remove-AzureApiManagementNamedValue`.

### `Set-AzApiManagementProperty`

Il cmdlet `Set-AzApiManagementProperty` è stato sostituito da `Set-AzureApiManagementNamedValue`.

## <a name="azbatch"></a>Az.Batch

### <a name="get-azbatchapplication-new-azbatchapplication"></a>`Get-AzBatchApplication`, `New-AzBatchApplication`

La proprietà `ApplicationPackages` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplication` è stata rimossa.

### <a name="get-azbatchcomputenode-new-azbatchpool"></a>`Get-AzBatchComputeNode`, `New-AzBatchPool`

La proprietà `PublicIPs` di tipo `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` è stata rimossa

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a>`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`

Il tipo della proprietà `StorageUrlExpiry` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` è stato modificato da `System.DateTime` a `System.DateTime?`.

## <a name="azcompute"></a>Az.Compute

### `Remove-AzVmssDiagnosticsExtension`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVMImage`

- Il cmdlet `Get-AzVMImage` non supporta più il parametro `FilterExpression` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `ListVMImage` per il cmdlet `Get-AzVMImage` è stato rimosso.

### `New-AzVMConfig`

- Il cmdlet `New-AzVMConfig` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `AssignIdentityParameterSet` per il cmdlet `New-AzVMConfig` è stato rimosso.

### `Update-AzVM`

- Il cmdlet `Update-AzVM` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `AssignIdentityParameterSet` per il cmdlet `Update-AzVM` è stato rimosso.

### `New-AzProximityPlacementGroup`

- Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.

#### <a name="before"></a>Prima

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.

#### <a name="before"></a>Prima

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.
- La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.

#### <a name="before"></a>Prima

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a>After

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssDataDisk`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssExtension`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssNetworkInterfaceConfiguration`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSecret`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssSshPublicKey`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Add-AzVmssWinRMListener`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmssConfig`

- Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.
- Non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `__AllParameterSets` è stato rimosso.
- Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.
- Il set di parametri `AssignIdentityParameterSet` è stato rimosso.

### `Remove-AzVmssDataDisk`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssExtension`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Remove-AzVmssNetworkInterfaceConfiguration`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssBootDiagnostic`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOsProfile`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssRollingUpgradePolicy`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssStorageProfile`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `New-AzVmss`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Repair-AzVmssServiceFabricUpdateDomain`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Get-AzVmss`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Set-AzVmssOrchestrationServiceState`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Update-AzVmss`

- Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.
- Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `__AllParameterSets` è stato rimosso.
- Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.

### `Add-AzVmssDiagnosticsExtension`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

### `Disable-AzVmssDiskEncryption`

Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.

## <a name="azkeyvault"></a>Az.KeyVault

### `New-AzKeyVaultCertificateOrganizationDetail`

L'alias `New-AzKeyVaultCertificateOrganizationDetails` è stato rimosso. Usare `New-AzKeyVaultCertificateOrganizationDetail`.

#### <a name="before"></a>Prima

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a>After

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

L'alias `New-AzKeyVaultCertificateAdministratorDetails` è stato rimosso. Usare `New-AzKeyVaultCertificateAdministratorDetail`.

#### <a name="before"></a>Prima

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a>After

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

`-EnableSoftDelete` è stato rimosso, perché l'eliminazione temporanea è abilitata per impostazione predefinita. Usare `-DisableSoftDelete` se non si vuole questo comportamento.

#### <a name="before"></a>Prima

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a>After

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a>Az.Monitor

### `Add-AzLogProfile`

Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `Get-AzLogProfile`

Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.

### `New-AzMetricAlertRuleV2Criteria`

Il set di parametri `__AllParameterSets` per il cmdlet `New-AzMetricAlertRuleV2Criteria` è stato rimosso.

## <a name="aznetwork"></a>Az.Network

### `Get-AzNetworkWatcherConnectionMonitor`

Il tipo generico per la proprietà `RoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

Il tipo generico per il parametro `SuccessThresholdRoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.

## <a name="azoperationalinsights"></a>Az.OperationalInsights

### `Get-AzOperationalInsightsDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsApplicationInsightsDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsAzureActivityLogDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsCustomLogDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsLinuxSyslogDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsWindowsEventDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Remove-AzOperationalInsightsDataSource`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Disable-AzOperationalInsightsIISLogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Enable-AzOperationalInsightsIISLogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Get-AzOperationalInsightsSavedSearch`

La proprietà `Metadata` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` è stata rimossa.

### `Get-AzOperationalInsightsSavedSearchResult`

Il cmdlet `Get-AzOperationalInsightsSavedSearchResult` non è più supportato dall'SDK ed è stato rimosso.

### `Get-AzOperationalInsightsSearchResult`

Il cmdlet `Get-AzOperationalInsightsSearchResult` non è più supportato dall'SDK ed è stato rimosso.

### `Get-AzOperationalInsightsStorageInsight`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsStorageInsight`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Remove-AzOperationalInsightsStorageInsight`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Set-AzOperationalInsightsStorageInsight`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Get-AzOperationalInsightsLinkTarget`

Il cmdlet `Get-AzOperationalInsightsLinkTarget` non è più supportato dall'SDK ed è stato rimosso.

### `Get-AzOperationalInsightsWorkspace`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `New-AzOperationalInsightsWorkspace`

- La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.
- Il cmdlet `New-AzOperationalInsightsWorkspace` non supporta più il parametro `CustomerId` e non è stato trovato alcun alias per il nome del parametro originale.
- Il set di parametri `__AllParameterSets` per il cmdlet `New-AzOperationalInsightsWorkspace` è stato rimosso.

### `Set-AzOperationalInsightsWorkspace`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

### `Invoke-AzOperationalInsightsQuery`

La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.

## <a name="azresources"></a>Az.Resources

### `Get-AzDeploymentScript`

Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzDeploymentScriptLog`

Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Save-AzDeploymentScriptLog`

Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

Il parametro `TenantLevel` è stato rimosso.

### `Get-AzPolicyAlias`

Il tipo generico per la proprietà `Aliases` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.

### `New-AzPolicyAssignment`

- Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicyDefinition`.
- Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicySetDefinition`.

### `Remove-AzDeploymentScript`

Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.

## <a name="azstorage"></a>Az.Storage

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a>`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`

Modifica del valore NetWorkRule DefaultAction da: Allow = 1, Deny = 0, a: Allow = 0, Deny = 1.

### <a name="new-azstoragetable-get-azstoragetable"></a>`New-AzStorageTable`, `Get-AzStorageTable`

Rimozione di 2 proprietà dall'oggetto di output AzureStorageTable.CloudTable.ServiceClient: ConnectionPolicy, ConsistencyLevel.

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a>`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`

Modifica del tipo di output da CloudFile ad AzureStorageFile. L'output originale diventerà la proprietà figlio "CloudFile" del nuovo output

#### <a name="before"></a>Prima

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a>After

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a>`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`

Modifica del tipo di output da CloudFileDirectory ad AzureStorageFileDirectory. L'output originale diventerà la proprietà figlio "CloudFileDirectory" del nuovo output

#### <a name="before"></a>Prima

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a>`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`

Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la proprietà figlio "CloudFileShare" del nuovo output

#### <a name="before"></a>Prima

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a>After

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la sottoproprietà figlio "CloudFileShare.Properties" del nuovo output

#### <a name="before"></a>Prima

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a>After

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

Quando si rimuovono le sottodirectory di file con l'oggetto directory padre e -Path, non è più possibile immettere -Path dalla pipeline con il tipo (stringa) corrispondente.

#### <a name="before"></a>Prima

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a>After

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
