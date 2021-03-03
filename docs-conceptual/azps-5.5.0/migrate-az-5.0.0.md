---
title: Guida alla migrazione per Az 5.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 5.0.0 di Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684927"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="0156a-103">Guida alla migrazione per Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="0156a-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="0156a-104">Questo documento descrive le modifiche apportate tra le versioni 4.0.0 e 5.0.0 del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="0156a-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="0156a-105">Guida alla migrazione per Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="0156a-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="0156a-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0156a-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="0156a-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0156a-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="0156a-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0156a-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="0156a-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0156a-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="0156a-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0156a-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="0156a-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="0156a-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="0156a-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0156a-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="0156a-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0156a-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="0156a-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="0156a-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="0156a-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="0156a-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0156a-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="0156a-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0156a-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="0156a-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0156a-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="0156a-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0156a-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="0156a-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0156a-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="0156a-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0156a-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="0156a-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="0156a-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="0156a-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="0156a-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="0156a-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="0156a-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="0156a-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="0156a-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="0156a-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="0156a-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="0156a-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="0156a-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="0156a-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="0156a-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="0156a-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="0156a-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="0156a-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="0156a-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="0156a-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="0156a-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="0156a-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="0156a-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="0156a-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="0156a-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="0156a-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="0156a-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="0156a-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="0156a-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="0156a-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="0156a-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="0156a-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="0156a-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="0156a-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="0156a-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="0156a-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0156a-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="0156a-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0156a-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="0156a-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="0156a-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="0156a-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0156a-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="0156a-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0156a-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="0156a-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0156a-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="0156a-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="0156a-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="0156a-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="0156a-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="0156a-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="0156a-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0156a-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="0156a-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0156a-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="0156a-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0156a-169">New-AzAksCluster</span></span>

- <span data-ttu-id="0156a-170">Non supporta più il parametro `NodeOsType` e non è stato trovato alcun alias per il nome del parametro originale. Sarà sempre `Linux`.</span><span class="sxs-lookup"><span data-stu-id="0156a-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="0156a-171">Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="0156a-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="0156a-172">Il valore predefinito di `NodeVmSetType` è cambiato da `AvailabilitySet` a `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="0156a-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="0156a-173">Il valore predefinito di `NetworkPlugin` è cambiato da `none` a `azure`.</span><span class="sxs-lookup"><span data-stu-id="0156a-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-174">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-175">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="0156a-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="0156a-176">Set-AzAksCluster</span></span>

<span data-ttu-id="0156a-177">Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="0156a-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-178">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-179">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="0156a-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0156a-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="0156a-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0156a-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="0156a-182">Non supporta più il parametro `StorageAccountName` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-183">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="0156a-184">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-184">After</span></span>

<span data-ttu-id="0156a-185">`Classic` è stato deprecato e `StorageAccountName` è stato rimosso perché funziona solo con la versione classica di Registro Container.</span><span class="sxs-lookup"><span data-stu-id="0156a-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="0156a-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="0156a-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="0156a-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0156a-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="0156a-188">Il parametro opzionale `IncludeSlot` è stato rimosso da tutti i set di parametri di `Get-AzFunctionApp` tranne uno.</span><span class="sxs-lookup"><span data-stu-id="0156a-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="0156a-189">Il cmdlet supporta ora il recupero degli slot di distribuzione nei risultati quando si specifica `-IncludeSlot`.</span><span class="sxs-lookup"><span data-stu-id="0156a-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="0156a-190">Questa funzionalità non veniva eseguita correttamente nella versione precedente del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0156a-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="0156a-191">Tuttavia, ora è stata corretta.</span><span class="sxs-lookup"><span data-stu-id="0156a-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="0156a-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="0156a-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="0156a-193">Il parametro `-DisableApplicationInsights` di `New-AzFunctionApp` è stato corretto per cui quando questa opzione viene specificata non vengono creati progetti di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="0156a-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="0156a-194">Il supporto per creare app per le funzioni di PowerShell 6.2 è stato rimosso dopo la data EOL di Poiché PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="0156a-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="0156a-195">L'indicazione corrente per i clienti è di creare invece app per le funzioni di PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="0156a-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="0156a-196">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 6.2 a 7.0 nelle app per le funzioni di Windows per PowerShell quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="0156a-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="0156a-197">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 10 a 12 nelle app per le funzioni di Windows e Linux per Node quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="0156a-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="0156a-198">Tuttavia, gli utenti possono comunque creare app per le funzioni di Node 10 specificando `-Runtime Node` e `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="0156a-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="0156a-199">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 3.7 a 3.8 nelle app per le funzioni di Linux per Python quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="0156a-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="0156a-200">Tuttavia, gli utenti possono comunque creare app per le funzioni di Python 3.7 specificando `-Runtime Python` e `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="0156a-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-201">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="0156a-202">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="0156a-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="0156a-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-204">New-AzKeyVault</span></span>

<span data-ttu-id="0156a-205">Non supporta più il parametro `DisableSoftDelete` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-206">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="0156a-207">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-207">After</span></span>

<span data-ttu-id="0156a-208">La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="0156a-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="0156a-209">Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="0156a-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="0156a-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0156a-210">Update-AzKeyVault</span></span>

<span data-ttu-id="0156a-211">Non supporta più i parametri `EnableSoftDelete`, `SoftDeleteRetentionInDays` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-212">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="0156a-213">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-213">After</span></span>

<span data-ttu-id="0156a-214">La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="0156a-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="0156a-215">Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="0156a-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="0156a-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0156a-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="0156a-217">La proprietà `SecretValueText` di tipo `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0156a-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="0156a-218">Applicare un oggetto `-AsPlainText` alla chiamata per ottenere il segreto del testo normale o usare il `$secret.SecretValue` tipo `SecureString` nello script.</span><span class="sxs-lookup"><span data-stu-id="0156a-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-219">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="0156a-220">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="0156a-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0156a-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="0156a-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0156a-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="0156a-223">Non supporta più il parametro `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-224">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-225">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="0156a-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0156a-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="0156a-227">Non supporta più i parametri `RegistrationDefinitionName`, `RegistrationDefinitionResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-228">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-229">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="0156a-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="0156a-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="0156a-231">Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-232">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-233">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="0156a-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="0156a-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="0156a-235">Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-236">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-237">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="0156a-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="0156a-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="0156a-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0156a-240">Non supporta più il parametro `ApiVersion` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-241">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-242">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="0156a-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="0156a-244">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="0156a-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-245">Get-AzDeployment</span></span>

<span data-ttu-id="0156a-246">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="0156a-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="0156a-248">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="0156a-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="0156a-250">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="0156a-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="0156a-252">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="0156a-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="0156a-254">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="0156a-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0156a-256">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="0156a-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-257">New-AzDeployment</span></span>

<span data-ttu-id="0156a-258">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="0156a-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="0156a-260">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="0156a-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0156a-262">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="0156a-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-263">Remove-AzDeployment</span></span>

<span data-ttu-id="0156a-264">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="0156a-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="0156a-266">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="0156a-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="0156a-268">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="0156a-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="0156a-270">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="0156a-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="0156a-272">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="0156a-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0156a-274">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="0156a-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-275">Stop-AzDeployment</span></span>

<span data-ttu-id="0156a-276">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="0156a-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="0156a-278">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="0156a-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="0156a-280">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="0156a-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-281">Test-AzDeployment</span></span>

<span data-ttu-id="0156a-282">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="0156a-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="0156a-284">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="0156a-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0156a-286">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="0156a-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="0156a-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="0156a-288">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="0156a-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="0156a-290">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="0156a-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0156a-292">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="0156a-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0156a-294">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="0156a-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="0156a-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="0156a-296">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="0156a-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0156a-298">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="0156a-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0156a-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="0156a-300">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="0156a-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="0156a-302">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="0156a-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="0156a-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="0156a-304">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="0156a-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="0156a-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0156a-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="0156a-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="0156a-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="0156a-307">Non supporta più il parametro `IsAzureADOnlyAuthentication` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-308">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="0156a-309">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="0156a-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="0156a-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="0156a-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0156a-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="0156a-312">Non supporta più i parametri `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-313">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="0156a-314">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="0156a-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="0156a-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="0156a-316">Non supporta più i parametri `Suspend`, `Resume` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="0156a-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0156a-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="0156a-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0156a-319">Non supporta più il parametro `PrivateLinkResourceType` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-320">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="0156a-321">Dopo</span><span class="sxs-lookup"><span data-stu-id="0156a-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="0156a-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0156a-323">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0156a-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="0156a-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0156a-325">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0156a-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="0156a-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0156a-327">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0156a-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="0156a-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0156a-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="0156a-329">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="0156a-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="0156a-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0156a-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="0156a-331">Non supporta più i parametri `FilterType`, `FilterItem` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0156a-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="0156a-332">Prima</span><span class="sxs-lookup"><span data-stu-id="0156a-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="0156a-333">After</span><span class="sxs-lookup"><span data-stu-id="0156a-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
