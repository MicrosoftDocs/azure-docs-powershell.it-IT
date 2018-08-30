---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 2a6e20137f12ae9317c7eeed330a2433774e1ea9
ms.sourcegitcommit: f648ac92fafb16cc0e9ca6bc85d00fa327baf396
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/28/2018
ms.locfileid: "43019040"
---
# <a name="release-notes"></a><span data-ttu-id="222d1-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="222d1-103">Release notes</span></span>

<span data-ttu-id="222d1-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="222d1-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="670---august-2018"></a><span data-ttu-id="222d1-105">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-105">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="222d1-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-106">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-107">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-107">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="222d1-108">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="222d1-108">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="222d1-109">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="222d1-109">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="222d1-110">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="222d1-110">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="222d1-111">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-111">Azure.Storage</span></span>
* <span data-ttu-id="222d1-112">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="222d1-112">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="222d1-113">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="222d1-113">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="222d1-114">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="222d1-114">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="222d1-115">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-115">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="222d1-116">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="222d1-116">Azure.AnalysisServices</span></span>
* <span data-ttu-id="222d1-117">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-117">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="222d1-118">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="222d1-118">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="222d1-119">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-119">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="222d1-120">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="222d1-120">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="222d1-121">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-121">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="222d1-122">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="222d1-122">AzureRM.Automation</span></span>
* <span data-ttu-id="222d1-123">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-123">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="222d1-124">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="222d1-124">AzureRM.Backup</span></span>
* <span data-ttu-id="222d1-125">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-125">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="222d1-126">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="222d1-126">AzureRM.Batch</span></span>
* <span data-ttu-id="222d1-127">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-127">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="222d1-128">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="222d1-128">AzureRM.Billing</span></span>
* <span data-ttu-id="222d1-129">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-129">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="222d1-130">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="222d1-130">AzureRM.Cdn</span></span>
* <span data-ttu-id="222d1-131">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-131">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="222d1-132">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="222d1-132">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="222d1-133">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-133">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-134">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-134">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-135">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-135">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="222d1-136">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-136">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="222d1-137">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="222d1-137">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="222d1-138">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="222d1-138">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="222d1-139">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="222d1-139">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="222d1-140">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="222d1-140">AzureRM.Consumption</span></span>
* <span data-ttu-id="222d1-141">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-141">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="222d1-142">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="222d1-142">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="222d1-143">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-143">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="222d1-144">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="222d1-144">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="222d1-145">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-145">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="222d1-146">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="222d1-146">AzureRM.DataFactories</span></span>
* <span data-ttu-id="222d1-147">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-147">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="222d1-148">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="222d1-148">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="222d1-149">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-149">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="222d1-150">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="222d1-150">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="222d1-151">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-151">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="222d1-152">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="222d1-152">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="222d1-153">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="222d1-153">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="222d1-154">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="222d1-154">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="222d1-155">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-155">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="222d1-156">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-156">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="222d1-157">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="222d1-157">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="222d1-158">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="222d1-159">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="222d1-159">AzureRM.Dns</span></span>
* <span data-ttu-id="222d1-160">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="222d1-161">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="222d1-161">AzureRM.EventGrid</span></span>
* <span data-ttu-id="222d1-162">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="222d1-163">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="222d1-163">AzureRM.EventHub</span></span>
* <span data-ttu-id="222d1-164">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-164">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="222d1-165">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="222d1-165">AzureRM.HDInsight</span></span>
* <span data-ttu-id="222d1-166">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-166">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="222d1-167">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="222d1-167">AzureRM.Insights</span></span>
* <span data-ttu-id="222d1-168">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-168">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="222d1-169">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="222d1-169">AzureRM.IotHub</span></span>
* <span data-ttu-id="222d1-170">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-171">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-171">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-172">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="222d1-173">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="222d1-173">AzureRM.LogicApp</span></span>
* <span data-ttu-id="222d1-174">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="222d1-175">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="222d1-175">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="222d1-176">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="222d1-177">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="222d1-177">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="222d1-178">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="222d1-179">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="222d1-179">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="222d1-180">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="222d1-181">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="222d1-181">AzureRM.Media</span></span>
* <span data-ttu-id="222d1-182">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-182">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="222d1-183">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-183">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-184">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="222d1-184">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="222d1-185">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="222d1-185">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="222d1-186">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="222d1-186">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="222d1-187">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="222d1-187">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="222d1-188">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="222d1-188">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="222d1-189">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="222d1-189">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="222d1-190">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="222d1-190">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="222d1-191">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="222d1-191">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="222d1-192">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="222d1-192">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="222d1-193">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="222d1-194">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="222d1-194">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="222d1-195">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="222d1-196">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="222d1-196">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="222d1-197">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="222d1-198">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="222d1-198">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="222d1-199">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="222d1-200">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="222d1-200">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="222d1-201">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="222d1-202">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="222d1-202">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="222d1-203">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="222d1-203">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="222d1-204">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="222d1-204">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="222d1-205">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="222d1-205">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="222d1-206">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-206">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="222d1-207">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="222d1-207">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="222d1-208">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="222d1-208">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="222d1-209">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="222d1-209">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="222d1-210">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="222d1-210">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="222d1-211">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="222d1-212">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="222d1-212">AzureRM.RedisCache</span></span>
* <span data-ttu-id="222d1-213">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="222d1-214">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="222d1-214">AzureRM.Relay</span></span>
* <span data-ttu-id="222d1-215">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="222d1-216">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="222d1-216">AzureRM.Resources</span></span>
* <span data-ttu-id="222d1-217">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="222d1-217">Support template deployment at subscription scope.</span></span> <span data-ttu-id="222d1-218">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="222d1-218">Add new Cmdlets:</span></span>
    - <span data-ttu-id="222d1-219">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-219">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="222d1-220">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-220">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="222d1-221">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-221">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="222d1-222">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-222">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="222d1-223">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-223">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="222d1-224">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="222d1-224">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="222d1-225">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="222d1-225">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="222d1-226">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="222d1-226">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="222d1-227">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-227">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="222d1-228">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="222d1-229">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="222d1-229">AzureRM.Scheduler</span></span>
* <span data-ttu-id="222d1-230">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="222d1-231">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="222d1-231">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="222d1-232">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="222d1-233">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="222d1-233">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="222d1-234">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="222d1-235">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-235">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-236">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="222d1-237">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-237">AzureRM.Storage</span></span>
* <span data-ttu-id="222d1-238">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="222d1-239">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="222d1-239">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="222d1-240">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="222d1-241">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="222d1-241">AzureRM.Tags</span></span>
* <span data-ttu-id="222d1-242">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="222d1-243">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="222d1-243">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="222d1-244">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="222d1-245">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="222d1-245">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="222d1-246">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="222d1-247">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="222d1-247">AzureRM.Websites</span></span>
* <span data-ttu-id="222d1-248">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="222d1-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="222d1-249">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-249">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="222d1-250">Generale</span><span class="sxs-lookup"><span data-stu-id="222d1-250">General</span></span>
* <span data-ttu-id="222d1-251">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="222d1-251">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="222d1-252">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-252">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-253">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="222d1-253">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="222d1-254">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-254">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="222d1-255">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-255">Azure.Storage</span></span>
* <span data-ttu-id="222d1-256">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="222d1-256">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="222d1-257">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="222d1-257">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="222d1-258">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="222d1-258">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="222d1-259">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="222d1-259">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="222d1-260">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="222d1-260">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="222d1-261">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="222d1-261">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="222d1-262">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="222d1-262">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="222d1-263">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="222d1-263">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="222d1-264">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="222d1-264">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-265">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-265">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-266">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="222d1-266">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="222d1-267">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="222d1-267">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="222d1-268">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="222d1-268">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="222d1-269">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="222d1-269">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="222d1-270">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="222d1-270">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="222d1-271">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="222d1-271">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="222d1-272">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="222d1-272">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="222d1-273">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="222d1-273">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="222d1-274">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="222d1-274">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="222d1-275">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="222d1-275">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="222d1-276">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="222d1-276">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="222d1-277">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="222d1-277">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="222d1-278">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="222d1-278">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="222d1-279">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="222d1-279">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="222d1-280">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="222d1-280">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="222d1-281">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="222d1-281">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="222d1-282">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="222d1-282">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="222d1-283">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="222d1-283">AzureRM.EventHub</span></span>
* <span data-ttu-id="222d1-284">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="222d1-284">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="222d1-285">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="222d1-285">AzureRM.Insights</span></span>
* <span data-ttu-id="222d1-286">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="222d1-286">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="222d1-287">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="222d1-287">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-288">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-288">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-289">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="222d1-289">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="222d1-290">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-290">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-291">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="222d1-291">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="222d1-292">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="222d1-292">AzureRM.Resources</span></span>
* <span data-ttu-id="222d1-293">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="222d1-293">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="222d1-294">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="222d1-294">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="222d1-295">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="222d1-295">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="222d1-296">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="222d1-296">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="222d1-297">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="222d1-297">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="222d1-298">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-298">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-299">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="222d1-299">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="222d1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="222d1-300">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="222d1-301">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="222d1-301">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="222d1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="222d1-302">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="222d1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="222d1-303">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="222d1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="222d1-304">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="222d1-305">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="222d1-305">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="222d1-306">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="222d1-306">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="222d1-307">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-307">AzureRM.Storage</span></span>
* <span data-ttu-id="222d1-308">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="222d1-308">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="222d1-309">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="222d1-309">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="222d1-310">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="222d1-310">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="222d1-311">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="222d1-311">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="222d1-312">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="222d1-312">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="222d1-313">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="222d1-313">AzureRM.Tags</span></span>
* <span data-ttu-id="222d1-314">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="222d1-314">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="222d1-315">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-315">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="222d1-316">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-316">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-317">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="222d1-317">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="222d1-318">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-318">Azure.Storage</span></span>
* <span data-ttu-id="222d1-319">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="222d1-319">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="222d1-320">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="222d1-320">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="222d1-321">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="222d1-321">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="222d1-322">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="222d1-322">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="222d1-323">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="222d1-323">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="222d1-324">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="222d1-324">AzureRM.Automation</span></span>
* <span data-ttu-id="222d1-325">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="222d1-325">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-326">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-326">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-327">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="222d1-327">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="222d1-328">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="222d1-328">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="222d1-329">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="222d1-329">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="222d1-330">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="222d1-330">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="222d1-331">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="222d1-331">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="222d1-332">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="222d1-332">AzureRM.EventHub</span></span>
* <span data-ttu-id="222d1-333">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="222d1-333">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-334">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-334">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-335">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="222d1-335">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="222d1-336">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="222d1-336">AzureRM.LogicApp</span></span>
* <span data-ttu-id="222d1-337">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="222d1-337">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="222d1-338">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-338">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-339">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="222d1-339">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="222d1-340">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="222d1-340">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="222d1-341">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="222d1-341">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="222d1-342">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="222d1-342">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="222d1-343">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="222d1-343">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="222d1-344">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="222d1-344">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="222d1-345">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="222d1-345">AzureRM.Relay</span></span>
* <span data-ttu-id="222d1-346">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="222d1-346">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="222d1-347">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="222d1-347">AzureRM.Resources</span></span>
* <span data-ttu-id="222d1-348">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="222d1-348">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="222d1-349">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="222d1-349">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="222d1-350">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="222d1-350">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="222d1-351">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="222d1-351">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="222d1-352">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="222d1-352">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="222d1-353">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="222d1-353">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="222d1-354">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="222d1-354">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="222d1-355">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="222d1-355">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="222d1-356">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="222d1-356">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="222d1-357">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="222d1-357">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="222d1-358">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="222d1-358">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="222d1-359">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="222d1-359">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="222d1-360">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="222d1-360">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="222d1-361">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="222d1-361">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="222d1-362">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="222d1-362">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="222d1-363">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="222d1-363">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="222d1-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-364">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-365">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="222d1-365">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="222d1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="222d1-366">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="222d1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="222d1-367">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="222d1-368">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="222d1-368">AzureRM.Websites</span></span>
* <span data-ttu-id="222d1-369">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="222d1-369">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="222d1-370">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="222d1-370">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="222d1-371">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="222d1-371">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="222d1-372">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-372">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="222d1-373">Generale</span><span class="sxs-lookup"><span data-stu-id="222d1-373">General</span></span>
* <span data-ttu-id="222d1-374">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="222d1-374">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="222d1-375">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-375">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-376">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="222d1-376">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-377">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-377">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-378">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="222d1-378">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="222d1-379">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="222d1-379">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="222d1-380">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-380">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="222d1-381">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="222d1-381">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="222d1-382">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-382">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="222d1-383">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="222d1-383">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="222d1-384">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-384">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="222d1-385">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="222d1-385">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="222d1-386">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="222d1-386">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="222d1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-387">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="222d1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-388">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="222d1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-389">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="222d1-390">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="222d1-390">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="222d1-391">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="222d1-391">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="222d1-392">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="222d1-392">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="222d1-393">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="222d1-393">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="222d1-394">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="222d1-394">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="222d1-395">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="222d1-395">AzureRM.EventHub</span></span>
* <span data-ttu-id="222d1-396">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="222d1-396">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="222d1-397">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="222d1-397">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="222d1-398">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="222d1-398">Provided Default Parameter set.</span></span>
* <span data-ttu-id="222d1-399">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="222d1-399">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-401">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="222d1-401">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="222d1-402">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-402">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-403">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="222d1-403">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="222d1-404">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="222d1-404">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="222d1-405">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="222d1-405">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="222d1-406">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="222d1-406">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="222d1-407">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="222d1-407">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="222d1-408">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="222d1-408">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="222d1-409">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="222d1-409">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="222d1-410">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="222d1-410">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="222d1-411">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="222d1-411">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="222d1-412">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="222d1-412">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="222d1-413">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="222d1-413">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="222d1-414">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="222d1-414">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="222d1-415">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="222d1-415">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="222d1-416">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="222d1-416">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="222d1-417">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="222d1-417">AzureRM.Resources</span></span>
* <span data-ttu-id="222d1-418">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="222d1-418">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="222d1-419">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="222d1-419">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="222d1-420">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="222d1-420">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="222d1-421">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="222d1-421">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="222d1-422">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="222d1-422">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="222d1-423">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="222d1-423">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="222d1-424">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="222d1-424">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="222d1-425">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="222d1-425">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="222d1-426">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="222d1-426">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="222d1-427">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="222d1-427">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="222d1-428">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="222d1-428">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="222d1-429">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="222d1-429">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="222d1-430">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="222d1-430">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="222d1-431">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="222d1-431">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="222d1-432">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="222d1-432">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="222d1-433">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-433">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-434">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="222d1-434">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="222d1-435">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="222d1-435">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="222d1-436">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-436">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="222d1-437">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-437">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-438">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="222d1-438">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="222d1-439">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="222d1-439">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="222d1-440">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="222d1-440">Azure.Storage</span></span>
* <span data-ttu-id="222d1-441">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="222d1-441">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-442">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-442">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-443">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="222d1-443">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="222d1-444">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="222d1-444">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="222d1-445">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="222d1-445">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="222d1-446">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="222d1-446">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="222d1-447">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="222d1-447">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="222d1-448">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="222d1-448">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="222d1-449">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="222d1-449">Start-AzureRmVM</span></span>
    - <span data-ttu-id="222d1-450">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="222d1-450">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="222d1-451">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="222d1-451">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="222d1-452">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="222d1-452">Set-AzureRmVM</span></span>
    - <span data-ttu-id="222d1-453">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="222d1-453">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="222d1-454">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-454">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="222d1-455">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="222d1-455">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="222d1-456">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="222d1-456">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="222d1-457">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-457">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="222d1-458">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-458">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="222d1-459">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-459">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="222d1-460">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="222d1-460">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="222d1-461">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="222d1-461">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="222d1-462">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="222d1-462">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="222d1-463">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="222d1-463">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="222d1-464">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="222d1-464">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="222d1-465">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="222d1-465">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="222d1-466">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="222d1-466">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="222d1-467">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="222d1-467">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="222d1-468">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="222d1-468">AzureRM.EventGrid</span></span>
* <span data-ttu-id="222d1-469">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="222d1-469">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-470">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-470">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-471">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="222d1-471">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="222d1-472">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="222d1-472">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="222d1-473">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="222d1-473">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="222d1-474">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="222d1-474">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="222d1-475">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="222d1-475">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="222d1-476">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="222d1-476">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="222d1-477">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="222d1-477">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="222d1-478">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="222d1-478">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="222d1-479">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-479">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-480">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="222d1-480">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="222d1-481">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="222d1-481">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="222d1-482">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-482">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="222d1-483">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="222d1-483">AzureRM.Websites</span></span>
* <span data-ttu-id="222d1-484">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="222d1-484">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="222d1-485">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="222d1-485">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="222d1-486">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-486">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="222d1-487">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="222d1-487">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="222d1-488">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="222d1-488">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="222d1-489">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-489">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="222d1-490">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-490">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-491">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="222d1-491">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="222d1-492">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="222d1-492">AzureRM.Compute</span></span>
* <span data-ttu-id="222d1-493">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="222d1-493">VMSS VM Update feature</span></span>
    - <span data-ttu-id="222d1-494">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="222d1-494">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="222d1-495">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="222d1-495">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="222d1-496">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="222d1-496">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="222d1-497">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="222d1-497">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="222d1-498">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="222d1-498">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="222d1-499">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="222d1-499">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="222d1-500">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="222d1-500">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="222d1-501">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="222d1-501">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="222d1-502">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="222d1-502">AzureRM.KeyVault</span></span>
* <span data-ttu-id="222d1-503">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="222d1-503">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="222d1-504">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-504">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-505">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="222d1-505">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="222d1-506">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="222d1-506">AzureRM.Resources</span></span>
* <span data-ttu-id="222d1-507">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="222d1-507">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="222d1-508">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="222d1-508">AzureRM.Scheduler</span></span>
* <span data-ttu-id="222d1-509">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="222d1-509">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="222d1-510">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-510">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-511">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="222d1-511">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="222d1-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="222d1-512">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="222d1-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="222d1-513">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="222d1-514">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="222d1-514">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="222d1-515">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="222d1-515">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="222d1-516">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="222d1-516">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="222d1-517">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="222d1-517">AzureRM.Websites</span></span>
* <span data-ttu-id="222d1-518">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="222d1-518">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="222d1-519">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="222d1-519">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="222d1-520">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="222d1-520">AzureRM.Profile</span></span>
* <span data-ttu-id="222d1-521">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="222d1-521">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="222d1-522">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="222d1-522">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="222d1-523">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="222d1-523">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="222d1-524">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="222d1-524">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="222d1-525">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="222d1-525">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="222d1-526">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="222d1-526">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="222d1-527">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="222d1-527">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="222d1-528">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="222d1-528">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="222d1-529">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="222d1-529">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="222d1-530">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="222d1-530">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="222d1-531">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="222d1-531">Added support for MSI identity</span></span>
* <span data-ttu-id="222d1-532">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="222d1-532">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="222d1-533">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="222d1-533">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="222d1-534">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="222d1-534">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="222d1-535">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="222d1-535">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="222d1-536">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="222d1-536">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="222d1-537">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="222d1-537">AzureRM.Batch</span></span>
* <span data-ttu-id="222d1-538">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="222d1-538">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="222d1-539">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="222d1-539">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="222d1-540">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="222d1-540">AzureRM.Consumption</span></span>
* <span data-ttu-id="222d1-541">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="222d1-541">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="222d1-542">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="222d1-542">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="222d1-543">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="222d1-543">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="222d1-544">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-544">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="222d1-545">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="222d1-545">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="222d1-546">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="222d1-546">AzureRM.Network</span></span>
* <span data-ttu-id="222d1-547">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="222d1-547">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="222d1-548">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="222d1-548">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="222d1-549">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="222d1-549">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="222d1-550">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="222d1-550">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="222d1-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-551">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="222d1-552">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="222d1-552">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="222d1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-553">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="222d1-554">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="222d1-554">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="222d1-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="222d1-555">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="222d1-556">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="222d1-556">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="222d1-557">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="222d1-557">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="222d1-558">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="222d1-558">AzureRM.Sql</span></span>
* <span data-ttu-id="222d1-559">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="222d1-559">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="222d1-560">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="222d1-560">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="222d1-561">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="222d1-561">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="222d1-562">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="222d1-562">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="222d1-563">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="222d1-563">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="222d1-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="222d1-564">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="222d1-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="222d1-565">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="222d1-566">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="222d1-566">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="222d1-567">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="222d1-567">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="222d1-568">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="222d1-568">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="222d1-569">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="222d1-569">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="222d1-570">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="222d1-570">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
