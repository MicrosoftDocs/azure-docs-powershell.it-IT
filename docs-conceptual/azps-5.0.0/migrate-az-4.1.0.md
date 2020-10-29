---
title: Guida alla migrazione per Az 4.1.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 4.1.0 di Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: c64541beb5eb0d3db38932fb3915de865919641b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753619"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="6b776-103">Guida alla migrazione per Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6b776-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="6b776-104">Questo documento descrive le modifiche apportate tra le versioni 3.0.0 e 4.1.0 del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="6b776-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="6b776-105">Guida alla migrazione per Az 4.1.0</span><span class="sxs-lookup"><span data-stu-id="6b776-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="6b776-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b776-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="6b776-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6b776-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="6b776-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="6b776-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="6b776-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="6b776-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="6b776-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="6b776-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="6b776-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6b776-111">Az.Compute</span></span>](#azcompute)
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
  - [<span data-ttu-id="6b776-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b776-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="6b776-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6b776-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="6b776-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6b776-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="6b776-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6b776-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
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
  - [<span data-ttu-id="6b776-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6b776-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="6b776-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6b776-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="6b776-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="6b776-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="6b776-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="6b776-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="6b776-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="6b776-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="6b776-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="6b776-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="6b776-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="6b776-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="6b776-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6b776-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="6b776-124">Il tipo della proprietà `Type` di tipo `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` è stato modificato da `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` a `System.String`.</span><span class="sxs-lookup"><span data-stu-id="6b776-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="6b776-125">Il cmdlet `New-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-126">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzApiManagement` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="6b776-127">Il cmdlet `Set-AzApiManagement` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-128">Il set di parametri `__AllParameterSets` per il cmdlet `Set-AzApiManagement` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="6b776-129">Il cmdlet `Get-AzApiManagementProperty` è stato sostituito da `Get-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="6b776-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="6b776-130">Il cmdlet `New-AzApiManagementProperty` è stato sostituito da `New-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="6b776-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="6b776-131">Il cmdlet `Remove-AzApiManagementProperty` è stato sostituito da `Remove-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="6b776-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="6b776-132">Il cmdlet `Set-AzApiManagementProperty` è stato sostituito da `Set-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="6b776-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="6b776-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="6b776-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="6b776-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="6b776-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="6b776-135">La proprietà `ApplicationPackages` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplication` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="6b776-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="6b776-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="6b776-137">La proprietà `PublicIPs` di tipo `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` è stata rimossa</span><span class="sxs-lookup"><span data-stu-id="6b776-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="6b776-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="6b776-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="6b776-139">Il tipo della proprietà `StorageUrlExpiry` di tipo `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` è stato modificato da `System.DateTime` a `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="6b776-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="6b776-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="6b776-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="6b776-141">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="6b776-142">Il cmdlet `Get-AzVMImage` non supporta più il parametro `FilterExpression` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-143">Il set di parametri `ListVMImage` per il cmdlet `Get-AzVMImage` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="6b776-144">Il cmdlet `New-AzVMConfig` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-145">Il set di parametri `AssignIdentityParameterSet` per il cmdlet `New-AzVMConfig` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="6b776-146">Il cmdlet `Update-AzVM` non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-147">Il set di parametri `AssignIdentityParameterSet` per il cmdlet `Update-AzVM` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="6b776-148">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6b776-149">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-150">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-150">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="6b776-151">After</span><span class="sxs-lookup"><span data-stu-id="6b776-151">After</span></span>

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

- <span data-ttu-id="6b776-152">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6b776-153">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-154">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-154">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="6b776-155">After</span><span class="sxs-lookup"><span data-stu-id="6b776-155">After</span></span>

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

- <span data-ttu-id="6b776-156">Il tipo generico per la proprietà `VirtualMachines`, `VirtualMachineScaleSets` e `AvailabilitySets` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="6b776-157">La proprietà `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus` e `AvailabilitySetsColocationStatus` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-158">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-158">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="6b776-159">After</span><span class="sxs-lookup"><span data-stu-id="6b776-159">After</span></span>

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

<span data-ttu-id="6b776-160">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="6b776-161">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="6b776-162">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="6b776-163">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="6b776-164">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="6b776-165">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="6b776-166">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="6b776-167">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="6b776-168">Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-169">Non supporta più il parametro `AssignIdentity` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-170">Il set di parametri `__AllParameterSets` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="6b776-171">Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="6b776-172">Il set di parametri `AssignIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="6b776-173">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="6b776-174">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="6b776-175">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="6b776-176">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="6b776-177">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="6b776-178">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="6b776-179">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="6b776-180">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="6b776-181">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="6b776-182">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="6b776-183">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="6b776-184">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="6b776-185">Non supporta più il parametro `AutomaticRepairMaxInstanceRepairsPercent` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-186">Il set di parametri `__AllParameterSets` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="6b776-187">Il set di parametri `ExplicitIdentityParameterSet` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="6b776-188">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="6b776-189">Il tipo della proprietà `AutomaticRepairsPolicy` di tipo `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` è stato modificato da `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` a `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="6b776-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="6b776-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="6b776-191">L'alias `New-AzKeyVaultCertificateOrganizationDetails` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="6b776-192">Usare `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="6b776-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-193">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="6b776-194">After</span><span class="sxs-lookup"><span data-stu-id="6b776-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="6b776-195">L'alias `New-AzKeyVaultCertificateAdministratorDetails` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="6b776-196">Usare `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="6b776-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-197">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="6b776-198">After</span><span class="sxs-lookup"><span data-stu-id="6b776-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="6b776-199">`-EnableSoftDelete` è stato rimosso, perché l'eliminazione temporanea è abilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6b776-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="6b776-200">Usare `-DisableSoftDelete` se non si vuole questo comportamento.</span><span class="sxs-lookup"><span data-stu-id="6b776-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-201">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="6b776-202">After</span><span class="sxs-lookup"><span data-stu-id="6b776-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="6b776-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="6b776-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="6b776-204">Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="6b776-205">Il tipo della proprietà `RetentionPolicy` di tipo `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` è stato modificato da `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` a `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="6b776-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="6b776-206">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzMetricAlertRuleV2Criteria` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="6b776-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="6b776-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="6b776-208">Il tipo generico per la proprietà `RoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="6b776-209">Il tipo generico per il parametro `SuccessThresholdRoundTripTimeMs` è stato modificato da `System.Nullable1[System.Int32]` a `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="6b776-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="6b776-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="6b776-211">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="6b776-212">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="6b776-213">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="6b776-214">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="6b776-215">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="6b776-216">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="6b776-217">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="6b776-218">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="6b776-219">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="6b776-220">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="6b776-221">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="6b776-222">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="6b776-223">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="6b776-224">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="6b776-225">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="6b776-226">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="6b776-227">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="6b776-228">La proprietà `Metadata` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="6b776-229">Il cmdlet `Get-AzOperationalInsightsSavedSearchResult` non è più supportato dall'SDK ed è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="6b776-230">Il cmdlet `Get-AzOperationalInsightsSearchResult` non è più supportato dall'SDK ed è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6b776-231">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6b776-232">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6b776-233">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="6b776-234">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="6b776-235">Il cmdlet `Get-AzOperationalInsightsLinkTarget` non è più supportato dall'SDK ed è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="6b776-236">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="6b776-237">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="6b776-238">Il cmdlet `New-AzOperationalInsightsWorkspace` non supporta più il parametro `CustomerId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="6b776-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="6b776-239">Il set di parametri `__AllParameterSets` per il cmdlet `New-AzOperationalInsightsWorkspace` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="6b776-240">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="6b776-241">La proprietà `PortalUrl` di tipo `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="6b776-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="6b776-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="6b776-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="6b776-243">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="6b776-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="6b776-244">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="6b776-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="6b776-245">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="6b776-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="6b776-246">Il parametro `TenantLevel` è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="6b776-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="6b776-247">Il tipo generico per la proprietà `Aliases` è stato modificato da `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` a `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="6b776-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="6b776-248">Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="6b776-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="6b776-249">Il cmdlet `New-AzPolicyAssignment` non supporta più il tipo `System.Management.Automation.PSObject` per il parametro `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="6b776-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="6b776-250">Il tipo della proprietà `Status` di tipo `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` è stato modificato da `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` a `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="6b776-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="6b776-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="6b776-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="6b776-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="6b776-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="6b776-253">Modifica del valore NetWorkRule DefaultAction da: Allow = 1, Deny = 0, a: Allow = 0, Deny = 1.</span><span class="sxs-lookup"><span data-stu-id="6b776-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="6b776-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="6b776-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="6b776-255">Rimozione di 2 proprietà dall'oggetto di output AzureStorageTable.CloudTable.ServiceClient: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="6b776-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="6b776-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="6b776-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="6b776-257">Modifica del tipo di output da CloudFile ad AzureStorageFile. L'output originale diventerà la proprietà figlio "CloudFile" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="6b776-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-258">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="6b776-259">After</span><span class="sxs-lookup"><span data-stu-id="6b776-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="6b776-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="6b776-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="6b776-261">Modifica del tipo di output da CloudFileDirectory ad AzureStorageFileDirectory. L'output originale diventerà la proprietà figlio "CloudFileDirectory" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="6b776-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-262">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="6b776-263">After</span><span class="sxs-lookup"><span data-stu-id="6b776-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="6b776-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="6b776-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="6b776-265">Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la proprietà figlio "CloudFileShare" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="6b776-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-266">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="6b776-267">After</span><span class="sxs-lookup"><span data-stu-id="6b776-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="6b776-268">Modifica del tipo di output da FileShareProperties ad AzureStorageFileShare. L'output originale diventerà la sottoproprietà figlio "CloudFileShare.Properties" del nuovo output</span><span class="sxs-lookup"><span data-stu-id="6b776-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-269">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="6b776-270">After</span><span class="sxs-lookup"><span data-stu-id="6b776-270">After</span></span>

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

<span data-ttu-id="6b776-271">Quando si rimuovono le sottodirectory di file con l'oggetto directory padre e -Path, non è più possibile immettere -Path dalla pipeline con il tipo (stringa) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="6b776-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="6b776-272">Prima</span><span class="sxs-lookup"><span data-stu-id="6b776-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="6b776-273">After</span><span class="sxs-lookup"><span data-stu-id="6b776-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
