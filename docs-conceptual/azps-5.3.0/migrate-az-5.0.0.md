---
title: Guida alla migrazione per Az 5.0.0
description: Questa guida alla migrazione contiene un elenco di modifiche di rilievo apportate ad Azure PowerShell nella versione 5.0.0 di Az.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "97893701"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="a3368-103">Guida alla migrazione per Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="a3368-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="a3368-104">Questo documento descrive le modifiche apportate tra le versioni 4.0.0 e 5.0.0 del modulo Az.</span><span class="sxs-lookup"><span data-stu-id="a3368-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="a3368-105">Guida alla migrazione per Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="a3368-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="a3368-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a3368-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="a3368-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a3368-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="a3368-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a3368-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="a3368-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a3368-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="a3368-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a3368-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="a3368-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a3368-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="a3368-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a3368-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="a3368-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a3368-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="a3368-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="a3368-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="a3368-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="a3368-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a3368-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="a3368-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a3368-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="a3368-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a3368-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="a3368-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="a3368-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="a3368-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="a3368-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="a3368-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a3368-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="a3368-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="a3368-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="a3368-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="a3368-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="a3368-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="a3368-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="a3368-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="a3368-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="a3368-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="a3368-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="a3368-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="a3368-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="a3368-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="a3368-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="a3368-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="a3368-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="a3368-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="a3368-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="a3368-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="a3368-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="a3368-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="a3368-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="a3368-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="a3368-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="a3368-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="a3368-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="a3368-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="a3368-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="a3368-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="a3368-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="a3368-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="a3368-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="a3368-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="a3368-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="a3368-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a3368-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="a3368-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a3368-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="a3368-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="a3368-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="a3368-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a3368-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="a3368-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a3368-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="a3368-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a3368-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="a3368-162">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="a3368-163">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="a3368-164">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="a3368-165">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="a3368-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="a3368-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a3368-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="a3368-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a3368-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="a3368-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a3368-169">New-AzAksCluster</span></span>

- <span data-ttu-id="a3368-170">Non supporta più il parametro `NodeOsType` e non è stato trovato alcun alias per il nome del parametro originale. Sarà sempre `Linux`.</span><span class="sxs-lookup"><span data-stu-id="a3368-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="a3368-171">Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="a3368-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="a3368-172">Il valore predefinito di `NodeVmSetType` è cambiato da `AvailabilitySet` a `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="a3368-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="a3368-173">Il valore predefinito di `NetworkPlugin` è cambiato da `none` a `azure`.</span><span class="sxs-lookup"><span data-stu-id="a3368-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-174">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-175">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="a3368-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a3368-176">Set-AzAksCluster</span></span>

<span data-ttu-id="a3368-177">Non supporta più l'alias `ClientIdAndSecret` per il parametro `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="a3368-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-178">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-179">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="a3368-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a3368-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="a3368-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a3368-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="a3368-182">Non supporta più il parametro `StorageAccountName` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-183">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="a3368-184">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-184">After</span></span>

<span data-ttu-id="a3368-185">`Classic` è stato deprecato e `StorageAccountName` è stato rimosso perché funziona solo con la versione classica di Registro Container.</span><span class="sxs-lookup"><span data-stu-id="a3368-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="a3368-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="a3368-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="a3368-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a3368-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="a3368-188">Il parametro opzionale `IncludeSlot` è stato rimosso da tutti i set di parametri di `Get-AzFunctionApp` tranne uno.</span><span class="sxs-lookup"><span data-stu-id="a3368-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="a3368-189">Il cmdlet supporta ora il recupero degli slot di distribuzione nei risultati quando si specifica `-IncludeSlot`.</span><span class="sxs-lookup"><span data-stu-id="a3368-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="a3368-190">Questa funzionalità non veniva eseguita correttamente nella versione precedente del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3368-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="a3368-191">Tuttavia, ora è stata corretta.</span><span class="sxs-lookup"><span data-stu-id="a3368-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="a3368-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="a3368-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="a3368-193">Il parametro `-DisableApplicationInsights` di `New-AzFunctionApp` è stato corretto per cui quando questa opzione viene specificata non vengono creati progetti di Application Insights.</span><span class="sxs-lookup"><span data-stu-id="a3368-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="a3368-194">Il supporto per creare app per le funzioni di PowerShell 6.2 è stato rimosso dopo la data EOL di Poiché PowerShell 6.2.</span><span class="sxs-lookup"><span data-stu-id="a3368-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="a3368-195">L'indicazione corrente per i clienti è di creare invece app per le funzioni di PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="a3368-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="a3368-196">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 6.2 a 7.0 nelle app per le funzioni di Windows per PowerShell quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="a3368-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="a3368-197">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 10 a 12 nelle app per le funzioni di Windows e Linux per Node quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="a3368-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="a3368-198">Tuttavia, gli utenti possono comunque creare app per le funzioni di Node 10 specificando `-Runtime Node` e `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="a3368-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="a3368-199">La versione di runtime predefinita di Funzioni versione 3 è stata cambiata da 3.7 a 3.8 nelle app per le funzioni di Linux per Python quando il parametro `RuntimeVersion` non viene specificato.</span><span class="sxs-lookup"><span data-stu-id="a3368-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="a3368-200">Tuttavia, gli utenti possono comunque creare app per le funzioni di Python 3.7 specificando `-Runtime Python` e `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="a3368-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-201">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="a3368-202">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="a3368-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="a3368-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-204">New-AzKeyVault</span></span>

<span data-ttu-id="a3368-205">Non supporta più il parametro `DisableSoftDelete` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-206">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="a3368-207">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-207">After</span></span>

<span data-ttu-id="a3368-208">La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="a3368-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="a3368-209">Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="a3368-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="a3368-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a3368-210">Update-AzKeyVault</span></span>

<span data-ttu-id="a3368-211">Non supporta più i parametri `EnableSoftDelete`, `SoftDeleteRetentionInDays` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-212">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="a3368-213">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-213">After</span></span>

<span data-ttu-id="a3368-214">La possibilità di aggiornare l'impostazione dell'eliminazione temporanea è deprecata in Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="a3368-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="a3368-215">Per altre informazioni, vedere https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span><span class="sxs-lookup"><span data-stu-id="a3368-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="a3368-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a3368-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="a3368-217">La proprietà `SecretValueText` di tipo `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="a3368-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="a3368-218">La proprietà `SecretValueText` è stata sostituita con `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="a3368-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-219">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="a3368-220">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="a3368-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="a3368-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="a3368-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a3368-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="a3368-223">Non supporta più il parametro `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-224">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-225">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="a3368-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="a3368-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="a3368-227">Non supporta più i parametri `RegistrationDefinitionName`, `RegistrationDefinitionResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-228">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-229">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="a3368-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="a3368-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="a3368-231">Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-232">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-233">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="a3368-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a3368-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="a3368-235">Non supporta più i parametri `Id`, `ResourceId` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-236">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-237">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="a3368-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="a3368-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="a3368-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="a3368-240">Non supporta più il parametro `ApiVersion` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-241">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-242">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="a3368-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="a3368-244">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="a3368-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-245">Get-AzDeployment</span></span>

<span data-ttu-id="a3368-246">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="a3368-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="a3368-248">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="a3368-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="a3368-250">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="a3368-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="a3368-252">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="a3368-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="a3368-254">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="a3368-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="a3368-256">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="a3368-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-257">New-AzDeployment</span></span>

<span data-ttu-id="a3368-258">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="a3368-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="a3368-260">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="a3368-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="a3368-262">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="a3368-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-263">Remove-AzDeployment</span></span>

<span data-ttu-id="a3368-264">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="a3368-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="a3368-266">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="a3368-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="a3368-268">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="a3368-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="a3368-270">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="a3368-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="a3368-272">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="a3368-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="a3368-274">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="a3368-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-275">Stop-AzDeployment</span></span>

<span data-ttu-id="a3368-276">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="a3368-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="a3368-278">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="a3368-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="a3368-280">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="a3368-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-281">Test-AzDeployment</span></span>

<span data-ttu-id="a3368-282">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="a3368-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="a3368-284">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="a3368-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="a3368-286">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="a3368-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="a3368-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="a3368-288">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="a3368-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="a3368-290">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="a3368-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="a3368-292">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="a3368-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="a3368-294">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="a3368-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a3368-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="a3368-296">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="a3368-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="a3368-298">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="a3368-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="a3368-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="a3368-300">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="a3368-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="a3368-302">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="a3368-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="a3368-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="a3368-304">Uguale a `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="a3368-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="a3368-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a3368-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="a3368-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="a3368-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="a3368-307">Non supporta più il parametro `IsAzureADOnlyAuthentication` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-308">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="a3368-309">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="a3368-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="a3368-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="a3368-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a3368-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="a3368-312">Non supporta più i parametri `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-313">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="a3368-314">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="a3368-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a3368-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="a3368-316">Non supporta più i parametri `Suspend`, `Resume` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="a3368-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a3368-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="a3368-318">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="a3368-319">Non supporta più il parametro `PrivateLinkResourceType` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-320">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="a3368-321">Dopo</span><span class="sxs-lookup"><span data-stu-id="a3368-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="a3368-322">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="a3368-323">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="a3368-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="a3368-324">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="a3368-325">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="a3368-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="a3368-326">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="a3368-327">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="a3368-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="a3368-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3368-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="a3368-329">Uguale a `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="a3368-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="a3368-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="a3368-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="a3368-331">Non supporta più i parametri `FilterType`, `FilterItem` e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="a3368-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="a3368-332">Prima</span><span class="sxs-lookup"><span data-stu-id="a3368-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="a3368-333">After</span><span class="sxs-lookup"><span data-stu-id="a3368-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
