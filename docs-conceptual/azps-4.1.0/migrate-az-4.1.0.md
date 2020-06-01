---
ms.openlocfilehash: 636fd0432d421f74fa74f3275abbc31ec5dc0b5c
ms.sourcegitcommit: 31f4facf815c2e25dc44e2fde0e1d2bd690bfc54
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/20/2020
ms.locfileid: "83688527"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="ef59a-101">Guida alla migrazione per Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ef59a-101">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="ef59a-102">Questo documento descrive le modifiche apportate tra le versioni 3.0.0 e 4.1.0 del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="ef59a-102">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="ef59a-103">Guida alla migrazione per Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="ef59a-103">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="ef59a-104">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef59a-104">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="ef59a-105">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ef59a-105">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="ef59a-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="ef59a-106">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="ef59a-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="ef59a-107">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="ef59a-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="ef59a-108">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="ef59a-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ef59a-109">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="ef59a-110">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ef59a-110">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="ef59a-111">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ef59a-111">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="ef59a-112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ef59a-112">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="ef59a-113">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ef59a-113">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="ef59a-114">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ef59a-114">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="ef59a-115">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ef59a-115">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="ef59a-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="ef59a-116">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="ef59a-117">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="ef59a-117">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="ef59a-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="ef59a-118">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="ef59a-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="ef59a-119">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="ef59a-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="ef59a-120">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="ef59a-121">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef59a-121">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="ef59a-122">Il tipo della proprietà `Type` di tipo `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` è stato modificato da `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` a `System.String`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-122">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="ef59a-123">Il cmdlet `New-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-123">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-124">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzApiManagement` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-124">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="ef59a-125">Il cmdlet `Set-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-125">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-126">Il set di parametri `__AllParameterSets` per il cmdlet `Set-AzApiManagement` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-126">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="ef59a-127">Il cmdlet `Get-AzApiManagementProperty` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-127">The cmdlet `Get-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="ef59a-128">Il cmdlet `New-AzApiManagementProperty` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-128">The cmdlet `New-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="ef59a-129">Il cmdlet `Remove-AzApiManagementProperty` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-129">The cmdlet `Remove-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="ef59a-130">Il cmdlet `Set-AzApiManagementProperty` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-130">The cmdlet `Set-AzApiManagementProperty` has been removed and no alias was found for the original cmdlet name.</span></span>

## <a name="azbatch"></a><span data-ttu-id="ef59a-131">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="ef59a-131">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="ef59a-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="ef59a-132">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="ef59a-133">La proprietà `ApplicationPackages` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplication` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-133">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="ef59a-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="ef59a-134">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="ef59a-135">La proprietà `PublicIPs` di tipo `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="ef59a-135">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="ef59a-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="ef59a-136">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="ef59a-137">Il tipo della proprietà `StorageUrlExpiry` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` è stato modificato da `System.DateTime` a `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-137">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="ef59a-138">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="ef59a-138">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="ef59a-139">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-139">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="ef59a-140">Il cmdlet `Get-AzVMImage` non supporta più il parametro `FilterExpression` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-140">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-141">Il set di parametri `ListVMImage` per il cmdlet `Get-AzVMImage` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-141">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="ef59a-142">Il cmdlet `New-AzVMConfig` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-142">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-143">Il set di parametri `AssignIdentityParameterSet` per il cmdlet `New-AzVMConfig` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-143">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="ef59a-144">Il cmdlet `Update-AzVM` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-144">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-145">Il set di parametri `AssignIdentityParameterSet` per il cmdlet `Update-AzVM` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-145">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="ef59a-146">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-146">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="ef59a-147">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-147">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-148">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-148">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="ef59a-149">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-149">After</span></span>

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

- <span data-ttu-id="ef59a-150">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-150">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="ef59a-151">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-151">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-152">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-152">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="ef59a-153">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-153">After</span></span>

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

- <span data-ttu-id="ef59a-154">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-154">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="ef59a-155">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-155">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-156">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-156">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="ef59a-157">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-157">After</span></span>

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

<span data-ttu-id="ef59a-158">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-158">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="ef59a-159">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-159">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="ef59a-160">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="ef59a-161">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="ef59a-162">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="ef59a-163">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="ef59a-164">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="ef59a-165">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="ef59a-166">Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-166">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-167">Non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-167">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-168">Il set di parametri `__AllParameterSets` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-168">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="ef59a-169">Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-169">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="ef59a-170">Il set di parametri `AssignIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-170">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="ef59a-171">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-171">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="ef59a-172">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-172">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="ef59a-173">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="ef59a-174">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="ef59a-175">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="ef59a-176">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="ef59a-177">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="ef59a-178">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="ef59a-179">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="ef59a-180">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="ef59a-181">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="ef59a-182">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="ef59a-183">Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-183">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-184">Il set di parametri `__AllParameterSets` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-184">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="ef59a-185">Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-185">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="ef59a-186">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-186">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="ef59a-187">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-187">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="ef59a-188">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="ef59a-188">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="ef59a-189">L'alias `New-AzKeyVaultCertificateOrganizationDetails` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-189">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="ef59a-190">Usare `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-190">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-191">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-191">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="ef59a-192">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-192">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="ef59a-193">L'alias `New-AzKeyVaultCertificateAdministratorDetails` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-193">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="ef59a-194">Usare `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-194">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-195">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-195">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="ef59a-196">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-196">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="ef59a-197">`-EnableSoftDelete` è stato rimosso, perché l'eliminazione temporanea è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ef59a-197">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="ef59a-198">Usare `-DisableSoftDelete` se non si vuole questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="ef59a-198">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-199">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-199">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="ef59a-200">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-200">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="ef59a-201">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="ef59a-201">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="ef59a-202">Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-202">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="ef59a-203">Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-203">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="ef59a-204">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzMetricAlertRuleV2Criteria` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-204">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="ef59a-205">Az.Network</span><span class="sxs-lookup"><span data-stu-id="ef59a-205">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="ef59a-206">Il tipo generico per la proprietà `RoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-206">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="ef59a-207">Il tipo generico per il parametro `SuccessThresholdRoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-207">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="ef59a-208">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="ef59a-208">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="ef59a-209">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-209">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="ef59a-210">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-210">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="ef59a-211">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="ef59a-212">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="ef59a-213">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="ef59a-214">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="ef59a-215">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="ef59a-216">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="ef59a-217">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="ef59a-218">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="ef59a-219">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="ef59a-220">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="ef59a-221">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="ef59a-222">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="ef59a-223">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="ef59a-224">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="ef59a-225">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="ef59a-226">La proprietà `Metadata` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-226">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="ef59a-227">Il cmdlet `Get-AzOperationalInsightsSavedSearchResult` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-227">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="ef59a-228">Il cmdlet `Get-AzOperationalInsightsSearchResult` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-228">The cmdlet `Get-AzOperationalInsightsSearchResult` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="ef59a-229">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-229">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="ef59a-230">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-230">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="ef59a-231">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="ef59a-232">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="ef59a-233">Il cmdlet `Get-AzOperationalInsightsLinkTarget` è stato rimosso e non è stato trovato alcun alias per il nome del cmdlet originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-233">The cmdlet `Get-AzOperationalInsightsLinkTarget` has been removed and no alias was found for the original cmdlet name.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="ef59a-234">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="ef59a-235">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-235">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="ef59a-236">Il cmdlet `New-AzOperationalInsightsWorkspace` non supporta più il parametro `CustomerId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="ef59a-236">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="ef59a-237">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzOperationalInsightsWorkspace` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-237">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="ef59a-238">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-238">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="ef59a-239">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="ef59a-239">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="ef59a-240">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="ef59a-240">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="ef59a-241">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-241">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="ef59a-242">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-242">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="ef59a-243">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="ef59a-244">Il parametro `TenantLevel` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="ef59a-244">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="ef59a-245">Il tipo generico per la proprietà `Aliases` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-245">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="ef59a-246">Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-246">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="ef59a-247">Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-247">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="ef59a-248">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="ef59a-248">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="ef59a-249">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="ef59a-249">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="ef59a-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="ef59a-250">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="ef59a-251">Modifica del valore NetWorkRule DefaultAction da: Allow = 1, Deny = 0, a: Allow = 0, Deny = 1.</span><span class="sxs-lookup"><span data-stu-id="ef59a-251">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="ef59a-252">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="ef59a-252">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="ef59a-253">Rimozione di 2 proprietà dall'oggetto di output AzureStorageTable.CloudTable.ServiceClient: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="ef59a-253">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="ef59a-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="ef59a-254">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="ef59a-255">Modifica del tipo di output da CloudFile ad AzureStorageFile. L'output originale diventerà la proprietà figlio "CloudFile" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="ef59a-255">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-256">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-256">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="ef59a-257">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-257">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="ef59a-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="ef59a-258">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="ef59a-259">Modifica del tipo di output da CloudFileDirectory ad AzureStorageFileDirectory. L'output originale diventerà la proprietà figlio "CloudFileDirectory" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="ef59a-259">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-260">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-260">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="ef59a-261">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-261">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="ef59a-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="ef59a-262">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="ef59a-263">Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la proprietà figlio "CloudFileShare" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="ef59a-263">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-264">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-264">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="ef59a-265">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-265">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="ef59a-266">Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la sottoproprietà figlio "CloudFileShare.Properties" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="ef59a-266">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-267">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-267">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="ef59a-268">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-268">After</span></span>

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

<span data-ttu-id="ef59a-269">Quando si rimuovono le sottodirectory di file con l'oggetto directory padre e -Path, non è più possibile immettere -Path dalla pipeline con il tipo (stringa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ef59a-269">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="ef59a-270">Prima</span><span class="sxs-lookup"><span data-stu-id="ef59a-270">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="ef59a-271">After</span><span class="sxs-lookup"><span data-stu-id="ef59a-271">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
