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
ms.openlocfilehash: 6043d17df1b5e91521bad31e65372c10ee6a5c6a
ms.sourcegitcommit: dca906e73e943aac207cee23b79915773419c673
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/30/2018
ms.locfileid: "43250062"
---
# <a name="release-notes"></a><span data-ttu-id="48b61-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="48b61-103">Release notes</span></span>

<span data-ttu-id="48b61-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="48b61-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="680---august-2018"></a><span data-ttu-id="48b61-105">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-105">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="48b61-106">Generale</span><span class="sxs-lookup"><span data-stu-id="48b61-106">General</span></span>
* <span data-ttu-id="48b61-107">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="48b61-107">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="48b61-108">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-108">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-109">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="48b61-109">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-110">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-110">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-111">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="48b61-111">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="48b61-112">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="48b61-112">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="48b61-113">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="48b61-113">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="48b61-114">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="48b61-114">AzureRM.IotHub</span></span>
* <span data-ttu-id="48b61-115">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="48b61-115">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-116">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-116">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-117">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="48b61-117">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="48b61-118">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="48b61-118">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="48b61-119">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="48b61-119">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-120">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-120">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-121">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="48b61-121">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="48b61-122">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48b61-122">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="48b61-123">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="48b61-123">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="48b61-124">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48b61-124">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="48b61-125">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="48b61-125">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="48b61-126">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="48b61-126">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="48b61-127">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="48b61-127">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="48b61-128">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="48b61-128">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="48b61-129">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="48b61-129">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="48b61-130">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="48b61-130">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="48b61-131">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="48b61-131">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="48b61-132">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="48b61-132">AzureRM.Websites</span></span>
* <span data-ttu-id="48b61-133">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="48b61-133">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="48b61-134">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-134">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="48b61-135">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-135">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-136">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-136">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="48b61-137">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="48b61-137">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="48b61-138">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="48b61-138">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="48b61-139">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="48b61-139">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="48b61-140">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-140">Azure.Storage</span></span>
* <span data-ttu-id="48b61-141">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="48b61-141">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="48b61-142">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="48b61-142">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="48b61-143">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48b61-143">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="48b61-144">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-144">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="48b61-145">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48b61-145">Azure.AnalysisServices</span></span>
* <span data-ttu-id="48b61-146">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-146">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="48b61-147">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48b61-147">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="48b61-148">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-148">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="48b61-149">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="48b61-149">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="48b61-150">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-150">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="48b61-151">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="48b61-151">AzureRM.Automation</span></span>
* <span data-ttu-id="48b61-152">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-152">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="48b61-153">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="48b61-153">AzureRM.Backup</span></span>
* <span data-ttu-id="48b61-154">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-154">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="48b61-155">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="48b61-155">AzureRM.Batch</span></span>
* <span data-ttu-id="48b61-156">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-156">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="48b61-157">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="48b61-157">AzureRM.Billing</span></span>
* <span data-ttu-id="48b61-158">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-158">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="48b61-159">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="48b61-159">AzureRM.Cdn</span></span>
* <span data-ttu-id="48b61-160">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-160">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="48b61-161">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="48b61-161">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="48b61-162">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-162">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-163">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-163">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-164">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-164">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="48b61-165">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-165">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="48b61-166">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="48b61-166">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="48b61-167">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="48b61-167">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="48b61-168">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="48b61-168">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="48b61-169">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="48b61-169">AzureRM.Consumption</span></span>
* <span data-ttu-id="48b61-170">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-170">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="48b61-171">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="48b61-171">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="48b61-172">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-172">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="48b61-173">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="48b61-173">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="48b61-174">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-174">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="48b61-175">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="48b61-175">AzureRM.DataFactories</span></span>
* <span data-ttu-id="48b61-176">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-176">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="48b61-177">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="48b61-177">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="48b61-178">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-178">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="48b61-179">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="48b61-179">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="48b61-180">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-180">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="48b61-181">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48b61-181">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="48b61-182">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="48b61-182">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="48b61-183">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="48b61-183">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="48b61-184">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-184">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="48b61-185">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-185">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="48b61-186">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="48b61-186">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="48b61-187">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="48b61-188">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="48b61-188">AzureRM.Dns</span></span>
* <span data-ttu-id="48b61-189">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="48b61-190">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48b61-190">AzureRM.EventGrid</span></span>
* <span data-ttu-id="48b61-191">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="48b61-192">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="48b61-192">AzureRM.EventHub</span></span>
* <span data-ttu-id="48b61-193">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="48b61-194">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="48b61-194">AzureRM.HDInsight</span></span>
* <span data-ttu-id="48b61-195">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="48b61-196">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="48b61-196">AzureRM.Insights</span></span>
* <span data-ttu-id="48b61-197">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="48b61-198">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="48b61-198">AzureRM.IotHub</span></span>
* <span data-ttu-id="48b61-199">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-200">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-200">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-201">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-201">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="48b61-202">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48b61-202">AzureRM.LogicApp</span></span>
* <span data-ttu-id="48b61-203">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-203">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="48b61-204">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="48b61-204">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="48b61-205">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-205">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="48b61-206">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="48b61-206">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="48b61-207">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="48b61-208">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="48b61-208">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="48b61-209">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="48b61-210">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="48b61-210">AzureRM.Media</span></span>
* <span data-ttu-id="48b61-211">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-212">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-212">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-213">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="48b61-213">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="48b61-214">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="48b61-214">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="48b61-215">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="48b61-215">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="48b61-216">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="48b61-216">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="48b61-217">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="48b61-217">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="48b61-218">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="48b61-218">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="48b61-219">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="48b61-219">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="48b61-220">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="48b61-220">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="48b61-221">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="48b61-221">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="48b61-222">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-222">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="48b61-223">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48b61-223">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="48b61-224">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="48b61-225">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48b61-225">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="48b61-226">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="48b61-227">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="48b61-227">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="48b61-228">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="48b61-229">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="48b61-229">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="48b61-230">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="48b61-231">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="48b61-231">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="48b61-232">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="48b61-232">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="48b61-233">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="48b61-233">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="48b61-234">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="48b61-234">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="48b61-235">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-235">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="48b61-236">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="48b61-236">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="48b61-237">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="48b61-237">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="48b61-238">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="48b61-238">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="48b61-239">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="48b61-239">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="48b61-240">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="48b61-241">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="48b61-241">AzureRM.RedisCache</span></span>
* <span data-ttu-id="48b61-242">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="48b61-243">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="48b61-243">AzureRM.Relay</span></span>
* <span data-ttu-id="48b61-244">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-245">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-245">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-246">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="48b61-246">Support template deployment at subscription scope.</span></span> <span data-ttu-id="48b61-247">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="48b61-247">Add new Cmdlets:</span></span>
    - <span data-ttu-id="48b61-248">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-248">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="48b61-249">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-249">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="48b61-250">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-250">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="48b61-251">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-251">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="48b61-252">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-252">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="48b61-253">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="48b61-253">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="48b61-254">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="48b61-254">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="48b61-255">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="48b61-255">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="48b61-256">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-256">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="48b61-257">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-257">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="48b61-258">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="48b61-258">AzureRM.Scheduler</span></span>
* <span data-ttu-id="48b61-259">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="48b61-260">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48b61-260">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="48b61-261">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="48b61-262">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48b61-262">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="48b61-263">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="48b61-264">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-264">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-265">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="48b61-266">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-266">AzureRM.Storage</span></span>
* <span data-ttu-id="48b61-267">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="48b61-268">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="48b61-268">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="48b61-269">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-269">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="48b61-270">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="48b61-270">AzureRM.Tags</span></span>
* <span data-ttu-id="48b61-271">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-271">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="48b61-272">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48b61-272">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="48b61-273">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-273">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="48b61-274">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="48b61-274">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="48b61-275">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-275">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="48b61-276">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="48b61-276">AzureRM.Websites</span></span>
* <span data-ttu-id="48b61-277">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="48b61-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="48b61-278">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-278">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="48b61-279">Generale</span><span class="sxs-lookup"><span data-stu-id="48b61-279">General</span></span>
* <span data-ttu-id="48b61-280">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="48b61-280">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="48b61-281">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-281">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-282">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="48b61-282">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="48b61-283">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-283">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="48b61-284">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-284">Azure.Storage</span></span>
* <span data-ttu-id="48b61-285">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b61-285">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="48b61-286">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b61-286">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="48b61-287">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48b61-287">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="48b61-288">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="48b61-288">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="48b61-289">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="48b61-289">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="48b61-290">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="48b61-290">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="48b61-291">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="48b61-291">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="48b61-292">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="48b61-292">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="48b61-293">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="48b61-293">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-294">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-294">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-295">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="48b61-295">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="48b61-296">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="48b61-296">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="48b61-297">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="48b61-297">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="48b61-298">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="48b61-298">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="48b61-299">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="48b61-299">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="48b61-300">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="48b61-300">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="48b61-301">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="48b61-301">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="48b61-302">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="48b61-302">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="48b61-303">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="48b61-303">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="48b61-304">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="48b61-304">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="48b61-305">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="48b61-305">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="48b61-306">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="48b61-306">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="48b61-307">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="48b61-307">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="48b61-308">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="48b61-308">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="48b61-309">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="48b61-309">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="48b61-310">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48b61-310">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="48b61-311">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="48b61-311">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="48b61-312">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="48b61-312">AzureRM.EventHub</span></span>
* <span data-ttu-id="48b61-313">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="48b61-313">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="48b61-314">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="48b61-314">AzureRM.Insights</span></span>
* <span data-ttu-id="48b61-315">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="48b61-315">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="48b61-316">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="48b61-316">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-317">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-317">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-318">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48b61-318">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-319">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-319">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-320">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="48b61-320">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-321">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-321">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-322">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="48b61-322">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="48b61-323">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="48b61-323">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="48b61-324">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48b61-324">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="48b61-325">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="48b61-325">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="48b61-326">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="48b61-326">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="48b61-327">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-327">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-328">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="48b61-328">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="48b61-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="48b61-329">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="48b61-330">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="48b61-330">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="48b61-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="48b61-331">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="48b61-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="48b61-332">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="48b61-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="48b61-333">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="48b61-334">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="48b61-334">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="48b61-335">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="48b61-335">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="48b61-336">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-336">AzureRM.Storage</span></span>
* <span data-ttu-id="48b61-337">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="48b61-337">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="48b61-338">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="48b61-338">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="48b61-339">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48b61-339">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="48b61-340">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48b61-340">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="48b61-341">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48b61-341">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="48b61-342">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="48b61-342">AzureRM.Tags</span></span>
* <span data-ttu-id="48b61-343">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="48b61-343">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="48b61-344">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-344">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="48b61-345">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-345">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-346">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="48b61-346">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="48b61-347">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-347">Azure.Storage</span></span>
* <span data-ttu-id="48b61-348">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="48b61-348">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="48b61-349">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="48b61-349">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="48b61-350">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="48b61-350">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="48b61-351">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48b61-351">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="48b61-352">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="48b61-352">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="48b61-353">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="48b61-353">AzureRM.Automation</span></span>
* <span data-ttu-id="48b61-354">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="48b61-354">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-355">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-355">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-356">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48b61-356">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="48b61-357">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="48b61-357">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="48b61-358">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="48b61-358">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="48b61-359">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="48b61-359">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="48b61-360">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="48b61-360">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="48b61-361">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="48b61-361">AzureRM.EventHub</span></span>
* <span data-ttu-id="48b61-362">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="48b61-362">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-363">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-363">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-364">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="48b61-364">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="48b61-365">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="48b61-365">AzureRM.LogicApp</span></span>
* <span data-ttu-id="48b61-366">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="48b61-366">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-367">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-367">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-368">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="48b61-368">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="48b61-369">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="48b61-369">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="48b61-370">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="48b61-370">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="48b61-371">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="48b61-371">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="48b61-372">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="48b61-372">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="48b61-373">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="48b61-373">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="48b61-374">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="48b61-374">AzureRM.Relay</span></span>
* <span data-ttu-id="48b61-375">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="48b61-375">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-376">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-376">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-377">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="48b61-377">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="48b61-378">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="48b61-378">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="48b61-379">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="48b61-379">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="48b61-380">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="48b61-380">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="48b61-381">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="48b61-381">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="48b61-382">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48b61-382">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="48b61-383">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="48b61-383">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="48b61-384">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="48b61-384">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="48b61-385">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="48b61-385">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="48b61-386">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="48b61-386">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="48b61-387">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="48b61-387">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="48b61-388">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="48b61-388">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="48b61-389">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="48b61-389">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="48b61-390">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="48b61-390">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="48b61-391">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48b61-391">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="48b61-392">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="48b61-392">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="48b61-393">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-393">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-394">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="48b61-394">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="48b61-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="48b61-395">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="48b61-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="48b61-396">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="48b61-397">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="48b61-397">AzureRM.Websites</span></span>
* <span data-ttu-id="48b61-398">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="48b61-398">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="48b61-399">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="48b61-399">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="48b61-400">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="48b61-400">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="48b61-401">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-401">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="48b61-402">Generale</span><span class="sxs-lookup"><span data-stu-id="48b61-402">General</span></span>
* <span data-ttu-id="48b61-403">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="48b61-403">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="48b61-404">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-404">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-405">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="48b61-405">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-406">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-406">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-407">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="48b61-407">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="48b61-408">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="48b61-408">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="48b61-409">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-409">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="48b61-410">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="48b61-410">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="48b61-411">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-411">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="48b61-412">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="48b61-412">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="48b61-413">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-413">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="48b61-414">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="48b61-414">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="48b61-415">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="48b61-415">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="48b61-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-416">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="48b61-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-417">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="48b61-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-418">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="48b61-419">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48b61-419">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="48b61-420">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="48b61-420">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="48b61-421">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="48b61-421">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="48b61-422">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="48b61-422">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="48b61-423">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="48b61-423">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="48b61-424">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="48b61-424">AzureRM.EventHub</span></span>
* <span data-ttu-id="48b61-425">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="48b61-425">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="48b61-426">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="48b61-426">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="48b61-427">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="48b61-427">Provided Default Parameter set.</span></span>
* <span data-ttu-id="48b61-428">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="48b61-428">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-429">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-429">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-430">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="48b61-430">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-431">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-431">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-432">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="48b61-432">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="48b61-433">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="48b61-433">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="48b61-434">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="48b61-434">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="48b61-435">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="48b61-435">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="48b61-436">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="48b61-436">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="48b61-437">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="48b61-437">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="48b61-438">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="48b61-438">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="48b61-439">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="48b61-439">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="48b61-440">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="48b61-440">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="48b61-441">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="48b61-441">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="48b61-442">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="48b61-442">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="48b61-443">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="48b61-443">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="48b61-444">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="48b61-444">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="48b61-445">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="48b61-445">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-446">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-446">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-447">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="48b61-447">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="48b61-448">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="48b61-448">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="48b61-449">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="48b61-449">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="48b61-450">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="48b61-450">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="48b61-451">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="48b61-451">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="48b61-452">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="48b61-452">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="48b61-453">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="48b61-453">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="48b61-454">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="48b61-454">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="48b61-455">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="48b61-455">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="48b61-456">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="48b61-456">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="48b61-457">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="48b61-457">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="48b61-458">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="48b61-458">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="48b61-459">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="48b61-459">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="48b61-460">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="48b61-460">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="48b61-461">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="48b61-461">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="48b61-462">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-462">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-463">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="48b61-463">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="48b61-464">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="48b61-464">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="48b61-465">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-465">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="48b61-466">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-466">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-467">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="48b61-467">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="48b61-468">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="48b61-468">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="48b61-469">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="48b61-469">Azure.Storage</span></span>
* <span data-ttu-id="48b61-470">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="48b61-470">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-471">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-471">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-472">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="48b61-472">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="48b61-473">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="48b61-473">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="48b61-474">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="48b61-474">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="48b61-475">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="48b61-475">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="48b61-476">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="48b61-476">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="48b61-477">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="48b61-477">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="48b61-478">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b61-478">Start-AzureRmVM</span></span>
    - <span data-ttu-id="48b61-479">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b61-479">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="48b61-480">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b61-480">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="48b61-481">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="48b61-481">Set-AzureRmVM</span></span>
    - <span data-ttu-id="48b61-482">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="48b61-482">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="48b61-483">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-483">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="48b61-484">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="48b61-484">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="48b61-485">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="48b61-485">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="48b61-486">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-486">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="48b61-487">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-487">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="48b61-488">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-488">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="48b61-489">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="48b61-489">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="48b61-490">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="48b61-490">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="48b61-491">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="48b61-491">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="48b61-492">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="48b61-492">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="48b61-493">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="48b61-493">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="48b61-494">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="48b61-494">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="48b61-495">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="48b61-495">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="48b61-496">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="48b61-496">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="48b61-497">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="48b61-497">AzureRM.EventGrid</span></span>
* <span data-ttu-id="48b61-498">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="48b61-498">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-499">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-499">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-500">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="48b61-500">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="48b61-501">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="48b61-501">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="48b61-502">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="48b61-502">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="48b61-503">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="48b61-503">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="48b61-504">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="48b61-504">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="48b61-505">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="48b61-505">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="48b61-506">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="48b61-506">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="48b61-507">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="48b61-507">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="48b61-508">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-508">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-509">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="48b61-509">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="48b61-510">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48b61-510">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="48b61-511">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-511">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="48b61-512">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="48b61-512">AzureRM.Websites</span></span>
* <span data-ttu-id="48b61-513">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="48b61-513">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="48b61-514">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="48b61-514">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="48b61-515">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-515">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="48b61-516">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="48b61-516">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="48b61-517">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="48b61-517">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="48b61-518">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-518">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="48b61-519">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-519">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-520">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="48b61-520">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="48b61-521">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="48b61-521">AzureRM.Compute</span></span>
* <span data-ttu-id="48b61-522">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="48b61-522">VMSS VM Update feature</span></span>
    - <span data-ttu-id="48b61-523">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="48b61-523">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="48b61-524">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="48b61-524">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="48b61-525">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="48b61-525">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="48b61-526">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="48b61-526">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="48b61-527">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="48b61-527">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="48b61-528">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="48b61-528">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="48b61-529">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="48b61-529">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="48b61-530">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="48b61-530">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="48b61-531">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="48b61-531">AzureRM.KeyVault</span></span>
* <span data-ttu-id="48b61-532">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="48b61-532">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="48b61-533">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-533">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-534">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="48b61-534">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="48b61-535">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="48b61-535">AzureRM.Resources</span></span>
* <span data-ttu-id="48b61-536">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="48b61-536">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="48b61-537">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="48b61-537">AzureRM.Scheduler</span></span>
* <span data-ttu-id="48b61-538">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="48b61-538">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="48b61-539">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-539">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-540">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="48b61-540">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="48b61-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48b61-541">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="48b61-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="48b61-542">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="48b61-543">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="48b61-543">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="48b61-544">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="48b61-544">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="48b61-545">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48b61-545">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="48b61-546">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="48b61-546">AzureRM.Websites</span></span>
* <span data-ttu-id="48b61-547">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="48b61-547">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="48b61-548">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="48b61-548">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="48b61-549">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="48b61-549">AzureRM.Profile</span></span>
* <span data-ttu-id="48b61-550">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="48b61-550">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="48b61-551">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="48b61-551">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="48b61-552">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="48b61-552">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="48b61-553">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="48b61-553">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="48b61-554">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="48b61-554">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="48b61-555">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="48b61-555">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="48b61-556">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="48b61-556">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="48b61-557">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="48b61-557">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="48b61-558">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="48b61-558">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="48b61-559">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="48b61-559">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="48b61-560">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="48b61-560">Added support for MSI identity</span></span>
* <span data-ttu-id="48b61-561">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="48b61-561">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="48b61-562">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="48b61-562">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="48b61-563">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b61-563">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="48b61-564">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="48b61-564">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="48b61-565">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="48b61-565">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="48b61-566">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="48b61-566">AzureRM.Batch</span></span>
* <span data-ttu-id="48b61-567">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="48b61-567">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="48b61-568">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="48b61-568">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="48b61-569">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="48b61-569">AzureRM.Consumption</span></span>
* <span data-ttu-id="48b61-570">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="48b61-570">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="48b61-571">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="48b61-571">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="48b61-572">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="48b61-572">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="48b61-573">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-573">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="48b61-574">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="48b61-574">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="48b61-575">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="48b61-575">AzureRM.Network</span></span>
* <span data-ttu-id="48b61-576">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="48b61-576">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="48b61-577">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="48b61-577">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="48b61-578">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="48b61-578">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="48b61-579">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="48b61-579">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="48b61-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-580">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="48b61-581">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="48b61-581">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="48b61-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-582">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="48b61-583">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="48b61-583">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="48b61-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="48b61-584">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="48b61-585">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="48b61-585">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="48b61-586">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="48b61-586">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="48b61-587">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="48b61-587">AzureRM.Sql</span></span>
* <span data-ttu-id="48b61-588">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="48b61-588">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="48b61-589">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="48b61-589">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="48b61-590">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="48b61-590">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="48b61-591">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="48b61-591">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="48b61-592">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="48b61-592">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="48b61-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48b61-593">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="48b61-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="48b61-594">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="48b61-595">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="48b61-595">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="48b61-596">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="48b61-596">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="48b61-597">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="48b61-597">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="48b61-598">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="48b61-598">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="48b61-599">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="48b61-599">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
