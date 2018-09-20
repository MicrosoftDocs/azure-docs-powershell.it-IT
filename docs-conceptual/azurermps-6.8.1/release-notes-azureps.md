---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 08/28/2018
ms.openlocfilehash: f4f3141998be14f0b5b223aed1af283534bf061d
ms.sourcegitcommit: bc88e64c494337821274d6a66c1edad656c119c5
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/20/2018
ms.locfileid: "46300834"
---
# <a name="release-notes"></a><span data-ttu-id="2d2da-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="2d2da-103">Release notes</span></span>

<span data-ttu-id="2d2da-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="681---august-2018"></a><span data-ttu-id="2d2da-105">6.8.1 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-105">6.8.1 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d2da-106">Generale</span><span class="sxs-lookup"><span data-stu-id="2d2da-106">General</span></span>
* <span data-ttu-id="2d2da-107">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-107">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2d2da-108">Assembly di runtime comuni aggiornati</span><span class="sxs-lookup"><span data-stu-id="2d2da-108">Updated common runtime assemblies</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d2da-109">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d2da-109">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d2da-110">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-110">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2d2da-111">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6603</span><span class="sxs-lookup"><span data-stu-id="2d2da-111">Fixed issue https://github.com/Azure/azure-powershell/issues/6603</span></span>
    - <span data-ttu-id="2d2da-112">I cmdlet Import-AzureRmApiManagementApi e \*-AzureRmApiManagementCertificate gestiscono ora i percorsi relativi</span><span class="sxs-lookup"><span data-stu-id="2d2da-112">Import-AzureRmApiManagementApi and \*-AzureRmApiManagementCertificate cmdlets now handle relative Paths</span></span>
* <span data-ttu-id="2d2da-113">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6879</span><span class="sxs-lookup"><span data-stu-id="2d2da-113">Fixed issue https://github.com/Azure/azure-powershell/issues/6879</span></span>
    - <span data-ttu-id="2d2da-114">CertificateInformation è una proprietà impostabile che consente il corretto funzionamento del cmdlet Set-AzureRmApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2d2da-114">The CertificateInformation is a settable property allowing for Set-AzureRmApiManagement cmdlet to work property.</span></span> <span data-ttu-id="2d2da-115">Risoluzione del problema tramite l'aggiornamento a NuGet 4.0.4-preview</span><span class="sxs-lookup"><span data-stu-id="2d2da-115">Fixed by upgrading to 4.0.4-preview nuget</span></span>
* <span data-ttu-id="2d2da-116">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6853</span><span class="sxs-lookup"><span data-stu-id="2d2da-116">Fixed issue https://github.com/Azure/azure-powershell/issues/6853</span></span>
    - <span data-ttu-id="2d2da-117">Correzione del filtro Odata per la ricerca del prodotto in base al nome</span><span class="sxs-lookup"><span data-stu-id="2d2da-117">Fixed the Odata filter for Search by Name on Product</span></span>
* <span data-ttu-id="2d2da-118">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6814</span><span class="sxs-lookup"><span data-stu-id="2d2da-118">Fixed issue https://github.com/Azure/azure-powershell/issues/6814</span></span>
    - <span data-ttu-id="2d2da-119">Correzione del filtro Odata per la ricerca dell'API in base al nome</span><span class="sxs-lookup"><span data-stu-id="2d2da-119">Fixed the Odata filter for Search by Name on Api</span></span>
* <span data-ttu-id="2d2da-120">Aggiunta del supporto per logger AzureMonitor</span><span class="sxs-lookup"><span data-stu-id="2d2da-120">Added support for AzureMonitor logger</span></span>


#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-121">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-121">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-122">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2d2da-122">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="2d2da-123">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="2d2da-123">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="2d2da-124">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-124">Fixed issue with default resource groups not being set.</span></span>
* <span data-ttu-id="2d2da-125">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="2d2da-125">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-126">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-126">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-127">Modifica in visualizzazione tabella della presentazione predefinita dell'output del cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d2da-127">Changed default cmdlet output presentation to table view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2d2da-128">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d2da-128">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d2da-129">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="2d2da-129">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>


#### <a name="azurermresources"></a><span data-ttu-id="2d2da-130">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-130">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-131">Risoluzione del problema relativo alla creazione di applicazioni gestite dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2d2da-131">Fixed issue with creating managed applications from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-132">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-132">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-133">Problemi risolti</span><span class="sxs-lookup"><span data-stu-id="2d2da-133">Fixed issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d2da-134">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d2da-134">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d2da-135">Aggiunta del supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2d2da-135">Added Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="2d2da-136">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2d2da-136">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="2d2da-137">Aggiunta del supporto per il metodo di routing Subnet</span><span class="sxs-lookup"><span data-stu-id="2d2da-137">Added Support for the Subnet routing method</span></span>
    - <span data-ttu-id="2d2da-138">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2d2da-138">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="2d2da-139">Aggiunta del supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="2d2da-139">Added Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="2d2da-140">Aggiunta del supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="2d2da-140">Added Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="2d2da-141">Aggiunta del supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2d2da-141">Added Support for Custom Headers in endpoints</span></span>

## <a name="680---august-2018"></a><span data-ttu-id="2d2da-142">6.8.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-142">6.8.0 - August 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d2da-143">Generale</span><span class="sxs-lookup"><span data-stu-id="2d2da-143">General</span></span>
* <span data-ttu-id="2d2da-144">Risoluzione del problema relativo alla mancata configurazione dei gruppi di risorse predefiniti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-144">Fixed issue with default resource groups not being set.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-145">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-145">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-146">Aggiunta della proprietà di scadenza ai token restituiti durante Connect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="2d2da-146">Added expiration property to tokens returned during Connect-AzureRmAccount</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-147">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-147">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-148">Risoluzione del problema relativo alla mancanza della destinazione nell'output dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2d2da-148">Fixed the issue that target is missing in error output.</span></span>
* <span data-ttu-id="2d2da-149">Risoluzione del problema relativo al tipo di account di archiviazione per una VM con disco gestito</span><span class="sxs-lookup"><span data-stu-id="2d2da-149">Fixed issue with storage account type for VM with managed disk</span></span>
* <span data-ttu-id="2d2da-150">Correzione dei cmdlet dell'estensione AEM per altri ambienti, ad esempio Azure Cina</span><span class="sxs-lookup"><span data-stu-id="2d2da-150">Fix AEM Extension cmdlets for other environments, for example Azure China</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="2d2da-151">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-151">AzureRM.IotHub</span></span>
* <span data-ttu-id="2d2da-152">Correzione degli esempi per New-AzureRmIotHubExportDevices e New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="2d2da-152">Fix examples for New-AzureRmIotHubExportDevices and New-AzureRmIotHubImportDevices</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-153">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-153">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-154">Modifica della rappresentazione predefinita dei modelli in visualizzazione tabella</span><span class="sxs-lookup"><span data-stu-id="2d2da-154">Changed default models representation to table-view</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2d2da-155">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d2da-155">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d2da-156">Correzione dell'errore in Update-AzureRmPowerBIEmbeddedCapacity durante il tentativo di ridimensionamento della capacità in sospeso</span><span class="sxs-lookup"><span data-stu-id="2d2da-156">Fix failure in Update-AzureRmPowerBIEmbeddedCapacity when trying to scale paused capacity</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-157">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-157">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-158">Risoluzione del problema relativo alla creazione di un'applicazione gestita dal Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2d2da-158">Fixed issue with creating managed application from the MarketPlace.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-159">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-159">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-160">Risoluzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="2d2da-160">Fix for issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/5058
    - https://github.com/Azure/azure-powershell/issues/5055
    - https://github.com/Azure/azure-powershell/issues/6891

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d2da-161">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d2da-161">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d2da-162">Supporto per il metodo di routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2d2da-162">Support for the MultiValue routing method</span></span>
    - <span data-ttu-id="2d2da-163">Nuovo parametro 'MaxReturn' per il routing MultiValue</span><span class="sxs-lookup"><span data-stu-id="2d2da-163">New parameter 'MaxReturn' for MultiValue routing</span></span>
* <span data-ttu-id="2d2da-164">Supporto per il metodo di routing della subnet</span><span class="sxs-lookup"><span data-stu-id="2d2da-164">Support for the Subnet routing method</span></span>
    - <span data-ttu-id="2d2da-165">Supporto per gli intervalli di indirizzi IP (subnet) negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2d2da-165">Support for IP address ranges (subnets) in endpoints</span></span>
* <span data-ttu-id="2d2da-166">Supporto per le intestazioni personalizzate nei profili</span><span class="sxs-lookup"><span data-stu-id="2d2da-166">Support for Custom Headers in profiles</span></span>
* <span data-ttu-id="2d2da-167">Supporto per gli intervalli di codici di stato previsti nei profili</span><span class="sxs-lookup"><span data-stu-id="2d2da-167">Support for Expected status code ranges in profiles</span></span>
* <span data-ttu-id="2d2da-168">Supporto per le intestazioni personalizzate negli endpoint</span><span class="sxs-lookup"><span data-stu-id="2d2da-168">Support for Custom Headers in endpoints</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d2da-169">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d2da-169">AzureRM.Websites</span></span>
* <span data-ttu-id="2d2da-170">Risoluzione del problema relativo alla configurazione non corretta del gruppo di risorse predefinito.</span><span class="sxs-lookup"><span data-stu-id="2d2da-170">Fixed issue with default resource group being set incorrectly.</span></span>

## <a name="670---august-2018"></a><span data-ttu-id="2d2da-171">6.7.0 - Agosto 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-171">6.7.0 - August 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-172">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-172">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-173">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-173">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2d2da-174">Aggiunta dell'ID utente al nome di contesto predefinito per evitare conflitti di contesto</span><span class="sxs-lookup"><span data-stu-id="2d2da-174">Add user id to default context name to avoid context clashing</span></span>
    - https://github.com/Azure/azure-powershell/issues/6489
* <span data-ttu-id="2d2da-175">Risoluzione dei problemi relativi a Clear-AzureRmContext che provocavano errori con la selezione di un contesto #6398</span><span class="sxs-lookup"><span data-stu-id="2d2da-175">Fix issues with Clear-AzureRmContext that caused issues with selecting a context #6398</span></span>
* <span data-ttu-id="2d2da-176">È possibile passare il dominio del tenant al parametro "-TenantId" per "Connect-AzureRmAccount"</span><span class="sxs-lookup"><span data-stu-id="2d2da-176">Enable tenant domain to be passed to '-TenantId' parameter for 'Connect-AzureRmAccount'</span></span>
    - https://github.com/Azure/azure-powershell/issues/3974
    - https://github.com/Azure/azure-powershell/issues/6709

#### <a name="azurestorage"></a><span data-ttu-id="2d2da-177">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-177">Azure.Storage</span></span>
* <span data-ttu-id="2d2da-178">Rimozione della limitazione di 5 TB per la quota di Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="2d2da-178">Remove the 5TB limitation for Azure File Share quota</span></span>
- <span data-ttu-id="2d2da-179">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2d2da-179">Set-AzureStorageShareQuota</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2d2da-180">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-180">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2d2da-181">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-181">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azureanalysisservices"></a><span data-ttu-id="2d2da-182">Azure.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-182">Azure.AnalysisServices</span></span>
* <span data-ttu-id="2d2da-183">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-183">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d2da-184">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d2da-184">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d2da-185">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-185">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermapplicationinsights"></a><span data-ttu-id="2d2da-186">AzureRM.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2d2da-186">AzureRM.ApplicationInsights</span></span>
* <span data-ttu-id="2d2da-187">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-187">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2d2da-188">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2d2da-188">AzureRM.Automation</span></span>
* <span data-ttu-id="2d2da-189">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-189">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbackup"></a><span data-ttu-id="2d2da-190">AzureRM.Backup</span><span class="sxs-lookup"><span data-stu-id="2d2da-190">AzureRM.Backup</span></span>
* <span data-ttu-id="2d2da-191">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-191">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2d2da-192">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2d2da-192">AzureRM.Batch</span></span>
* <span data-ttu-id="2d2da-193">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-193">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermbilling"></a><span data-ttu-id="2d2da-194">AzureRM.Billing</span><span class="sxs-lookup"><span data-stu-id="2d2da-194">AzureRM.Billing</span></span>
* <span data-ttu-id="2d2da-195">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-195">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcdn"></a><span data-ttu-id="2d2da-196">AzureRM.Cdn</span><span class="sxs-lookup"><span data-stu-id="2d2da-196">AzureRM.Cdn</span></span>
* <span data-ttu-id="2d2da-197">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-197">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcognitiveservices"></a><span data-ttu-id="2d2da-198">AzureRM.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-198">AzureRM.CognitiveServices</span></span>
* <span data-ttu-id="2d2da-199">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-199">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-200">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-200">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-201">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-201">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2d2da-202">Aggiunta del parametro EvictionPolicy a New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-202">Add EvictionPolicy parameter to New-AzureRmVmssConfig</span></span>
* <span data-ttu-id="2d2da-203">Uso della posizione predefinita in DiskFileParameterSet di New-AzureRmVm se non è specificata alcuna posizione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-203">Use default location in the DiskFileParameterSet of New-AzureRmVm if no Location is specified.</span></span>
* <span data-ttu-id="2d2da-204">Correzione della descrizione del parametro in Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2d2da-204">Fix parameter description in Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2d2da-205">Correzione del cmdlet Get-AzureRmVMDiskEncryptionStatus per alcuni scenari correlati a singlepass</span><span class="sxs-lookup"><span data-stu-id="2d2da-205">Fix Get-AzureRmVMDiskEncryptionStatus cmdlet for certain singlepass related scenarios</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2d2da-206">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2d2da-206">AzureRM.Consumption</span></span>
* <span data-ttu-id="2d2da-207">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-207">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerinstance"></a><span data-ttu-id="2d2da-208">AzureRM.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2d2da-208">AzureRM.ContainerInstance</span></span>
* <span data-ttu-id="2d2da-209">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-209">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermcontainerregistry"></a><span data-ttu-id="2d2da-210">AzureRM.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2d2da-210">AzureRM.ContainerRegistry</span></span>
* <span data-ttu-id="2d2da-211">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-211">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactories"></a><span data-ttu-id="2d2da-212">AzureRM.DataFactories</span><span class="sxs-lookup"><span data-stu-id="2d2da-212">AzureRM.DataFactories</span></span>
* <span data-ttu-id="2d2da-213">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-213">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2d2da-214">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d2da-214">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2d2da-215">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-215">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2d2da-216">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d2da-216">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2d2da-217">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-217">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d2da-218">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d2da-218">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d2da-219">Correzione del debug quando DebugPreference è impostato dalla riga di comando di PowerShell</span><span class="sxs-lookup"><span data-stu-id="2d2da-219">Fix debugging when DebugPreference is set from powershell command line</span></span>
* <span data-ttu-id="2d2da-220">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2d2da-220">Update example for Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2d2da-221">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-221">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2d2da-222">Esempio di aggiornamento per Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-222">Update example for Set-AzureRmDataLakeStoreItemAclEntry</span></span>

#### <a name="azurermdevtestlabs"></a><span data-ttu-id="2d2da-223">AzureRM.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2d2da-223">AzureRM.DevTestLabs</span></span>
* <span data-ttu-id="2d2da-224">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-224">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermdns"></a><span data-ttu-id="2d2da-225">AzureRM.Dns</span><span class="sxs-lookup"><span data-stu-id="2d2da-225">AzureRM.Dns</span></span>
* <span data-ttu-id="2d2da-226">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-226">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2d2da-227">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d2da-227">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2d2da-228">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-228">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d2da-229">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-229">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d2da-230">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-230">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermhdinsight"></a><span data-ttu-id="2d2da-231">AzureRM.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d2da-231">AzureRM.HDInsight</span></span>
* <span data-ttu-id="2d2da-232">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-232">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2d2da-233">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2d2da-233">AzureRM.Insights</span></span>
* <span data-ttu-id="2d2da-234">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-234">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermiothub"></a><span data-ttu-id="2d2da-235">AzureRM.IotHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-235">AzureRM.IotHub</span></span>
* <span data-ttu-id="2d2da-236">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-236">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-237">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-237">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-238">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-238">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2d2da-239">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d2da-239">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2d2da-240">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-240">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearning"></a><span data-ttu-id="2d2da-241">AzureRM.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2d2da-241">AzureRM.MachineLearning</span></span>
* <span data-ttu-id="2d2da-242">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-242">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmachinelearningcompute"></a><span data-ttu-id="2d2da-243">AzureRM.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2d2da-243">AzureRM.MachineLearningCompute</span></span>
* <span data-ttu-id="2d2da-244">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-244">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmarketplaceordering"></a><span data-ttu-id="2d2da-245">AzureRM.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2d2da-245">AzureRM.MarketplaceOrdering</span></span>
* <span data-ttu-id="2d2da-246">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-246">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermmedia"></a><span data-ttu-id="2d2da-247">AzureRM.Media</span><span class="sxs-lookup"><span data-stu-id="2d2da-247">AzureRM.Media</span></span>
* <span data-ttu-id="2d2da-248">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-248">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-249">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-249">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-250">Aggiunta dell'esempio per Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d2da-250">Added example for Set-AzureRmLocalNetworkGateway</span></span>
* <span data-ttu-id="2d2da-251">Aggiunta di esempi e descrizioni per Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey e New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d2da-251">Added examples and descriptions for Add-AzureRmVirtualNetworkGatewayIpConfig, Get-AzureRmVirtualNetworkGatewayConnectionSharedKey and New-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d2da-252">Aggiunta di esempi per Remove-AzureRmVirtualNetworkGatewayIpConfig e Reset-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2d2da-252">Added examples for Remove-AzureRmVirtualNetworkGatewayIpConfig and Reset-AzureRmVirtualNetworkGateway</span></span>
* <span data-ttu-id="2d2da-253">Aggiunta di un esempio per Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2d2da-253">Added example for Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="2d2da-254">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2d2da-254">Added example for Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>
* <span data-ttu-id="2d2da-255">Aggiunta di un esempio per Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2d2da-255">Added example for Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2d2da-256">Rigenerazione dei cmdlet per ApplicationSecurityGroup, RouteTable e Usage con il generatore di codice più recente</span><span class="sxs-lookup"><span data-stu-id="2d2da-256">Re-generated cmdlets for ApplicationSecurityGroup, RouteTable and Usage using latest code generator</span></span>
* <span data-ttu-id="2d2da-257">Chiarimento del messaggio di errore per Get-AzureRmVirtualNetworkSubnetConfig durante il tentativo di ottenere una subnet che non esegue exitc</span><span class="sxs-lookup"><span data-stu-id="2d2da-257">Clarified error message for Get-AzureRmVirtualNetworkSubnetConfig when attempting to get a subnet that does not exitc</span></span>

#### <a name="azurermnotificationhubs"></a><span data-ttu-id="2d2da-258">AzureRM.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2d2da-258">AzureRM.NotificationHubs</span></span>
* <span data-ttu-id="2d2da-259">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-259">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermoperationalinsights"></a><span data-ttu-id="2d2da-260">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d2da-260">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2d2da-261">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-261">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2d2da-262">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d2da-262">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2d2da-263">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-263">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermpowerbiembedded"></a><span data-ttu-id="2d2da-264">AzureRM.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2d2da-264">AzureRM.PowerBIEmbedded</span></span>
* <span data-ttu-id="2d2da-265">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-265">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservices"></a><span data-ttu-id="2d2da-266">AzureRM.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-266">AzureRM.RecoveryServices</span></span>
* <span data-ttu-id="2d2da-267">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-267">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2d2da-268">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d2da-268">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d2da-269">Aggiunta di un filtro di criteri al cmdlet Get-AzureRmRecoveryServicesBackItem.</span><span class="sxs-lookup"><span data-stu-id="2d2da-269">Added policy filter to Get-AzureRmRecoveryServicesBackItem cmdlet.</span></span> <span data-ttu-id="2d2da-270">Il comando restituisce l'elenco degli elementi di backup protetti dall'ID criterio.</span><span class="sxs-lookup"><span data-stu-id="2d2da-270">The command returns the list of backup items protected by the given policy id.</span></span>
* <span data-ttu-id="2d2da-271">Aggiornamento di Microsoft.Azure.Management.RecoveryServices.Backup alla versione 3.0.0-preview.</span><span class="sxs-lookup"><span data-stu-id="2d2da-271">Updated Microsoft.Azure.Management.RecoveryServices.Backup to version 3.0.0-preview.</span></span>
* <span data-ttu-id="2d2da-272">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-272">Updated to the latest version of the Azure ClientRuntime.</span></span>
* <span data-ttu-id="2d2da-273">Aggiunta del parametro TargetResourceGroupName a Restore-AzureRmRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="2d2da-273">Added TargetResourceGroupName parameter to Restore-AzureRmRecoveryServicesBackupItem.</span></span> <span data-ttu-id="2d2da-274">Il gruppo di risorse in cui vengono ripristinati i dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-274">The resource group to which the managed disks are restored.</span></span> <span data-ttu-id="2d2da-275">Applicabile al backup di macchine virtuali con dischi gestiti.</span><span class="sxs-lookup"><span data-stu-id="2d2da-275">Applicable to backup of VM with managed disks.</span></span>

#### <a name="azurermrecoveryservicessiterecovery"></a><span data-ttu-id="2d2da-276">AzureRM.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2d2da-276">AzureRM.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2d2da-277">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-277">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrediscache"></a><span data-ttu-id="2d2da-278">AzureRM.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2d2da-278">AzureRM.RedisCache</span></span>
* <span data-ttu-id="2d2da-279">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-279">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2d2da-280">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2d2da-280">AzureRM.Relay</span></span>
* <span data-ttu-id="2d2da-281">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-281">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-282">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-282">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-283">Supporto di distribuzione di modelli a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-283">Support template deployment at subscription scope.</span></span> <span data-ttu-id="2d2da-284">Aggiunta di nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2d2da-284">Add new Cmdlets:</span></span>
    - <span data-ttu-id="2d2da-285">New-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-285">New-AzureRmDeployment</span></span>
    - <span data-ttu-id="2d2da-286">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-286">Get-AzureRmDeployment</span></span>
    - <span data-ttu-id="2d2da-287">Test-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-287">Test-AzureRmDeployment</span></span>
    - <span data-ttu-id="2d2da-288">Remove-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-288">Remove-AzureRmDeployment</span></span>
    - <span data-ttu-id="2d2da-289">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-289">Stop-AzureRmDeployment</span></span>
    - <span data-ttu-id="2d2da-290">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="2d2da-290">Save-AzureRmDeploymentTemplate</span></span>
    - <span data-ttu-id="2d2da-291">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="2d2da-291">Get-AzureRmDeploymentOperation</span></span>
* <span data-ttu-id="2d2da-292">Risoluzione del problema per il quale veniva generato un errore quando si passava un contesto a Set-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="2d2da-292">Fix issue where error is thrown when passing a context to Set-AzureRmResource</span></span>
    - https://github.com/Azure/azure-powershell/issues/5705
* <span data-ttu-id="2d2da-293">Correzione dell'esempio in New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-293">Fix example in New-AzureRmResourceGroupDeployment</span></span>
* <span data-ttu-id="2d2da-294">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-294">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2d2da-295">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2d2da-295">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2d2da-296">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-296">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-297">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-297">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-298">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-298">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2d2da-299">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d2da-299">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2d2da-300">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-300">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-301">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-301">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-302">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-302">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2d2da-303">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-303">AzureRM.Storage</span></span>
* <span data-ttu-id="2d2da-304">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-304">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermstreamanalytics"></a><span data-ttu-id="2d2da-305">AzureRM.StreamAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d2da-305">AzureRM.StreamAnalytics</span></span>
* <span data-ttu-id="2d2da-306">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-306">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2d2da-307">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2d2da-307">AzureRM.Tags</span></span>
* <span data-ttu-id="2d2da-308">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-308">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d2da-309">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d2da-309">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d2da-310">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-310">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermusageaggregates"></a><span data-ttu-id="2d2da-311">AzureRM.UsageAggregates</span><span class="sxs-lookup"><span data-stu-id="2d2da-311">AzureRM.UsageAggregates</span></span>
* <span data-ttu-id="2d2da-312">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-312">Updated to the latest version of the Azure ClientRuntime.</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d2da-313">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d2da-313">AzureRM.Websites</span></span>
* <span data-ttu-id="2d2da-314">Aggiornamento alla versione più recente del runtime del client di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2da-314">Updated to the latest version of the Azure ClientRuntime.</span></span>

## <a name="660---july-2018"></a><span data-ttu-id="2d2da-315">6.6.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-315">6.6.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d2da-316">Generale</span><span class="sxs-lookup"><span data-stu-id="2d2da-316">General</span></span>
* <span data-ttu-id="2d2da-317">Aggiornamento di tutti i file della Guida in modo da includere tipi di parametri completi e correggere i tipi di input/output.</span><span class="sxs-lookup"><span data-stu-id="2d2da-317">Updated all help files to include full parameter types and correct input/output types.</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-318">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-318">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-319">Aggiornamento della libreria Common.Strategy per consentire di confermare che il file di configurazione corrente per una risorsa è compatibile con la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-319">Updated Common.Strategy library to be able to validate that the current config for a resource is compatible with the target resource.</span></span>
* <span data-ttu-id="2d2da-320">Aggiunta dei tipi ps1xml a Common.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-320">Added ps1xml types to Common.Storage</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d2da-321">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-321">Azure.Storage</span></span>
* <span data-ttu-id="2d2da-322">Aggiunta del supporto per l'ottenimento del contesto di archiviazione da DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2da-322">Added support for getting Storage Context from DefaultProfile</span></span>
* <span data-ttu-id="2d2da-323">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d2da-323">Added Ps1XmlAttribute to cmdlets output types properties.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d2da-324">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d2da-324">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d2da-325">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6370</span><span class="sxs-lookup"><span data-stu-id="2d2da-325">Fixed issue https://github.com/Azure/azure-powershell/issues/6370</span></span>
    - <span data-ttu-id="2d2da-326">Correzione del bug in Automapper per la conversione di PsApiManagementApi in ApiContract</span><span class="sxs-lookup"><span data-stu-id="2d2da-326">Fixed bug in Automapper to translate PsApiManagementApi to ApiContract</span></span>
* <span data-ttu-id="2d2da-327">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6515</span><span class="sxs-lookup"><span data-stu-id="2d2da-327">Fixed issue https://github.com/Azure/azure-powershell/issues/6515</span></span>
    - <span data-ttu-id="2d2da-328">Correzione del bug in File.Save per evitare l'overload con il tipo di codifica</span><span class="sxs-lookup"><span data-stu-id="2d2da-328">Fixed bug in File.Save to not overload with Encoding Type</span></span>
* <span data-ttu-id="2d2da-329">Risoluzione del problema https://github.com/Azure/azure-powershell/issues/6560</span><span class="sxs-lookup"><span data-stu-id="2d2da-329">Fixed issue https://github.com/Azure/azure-powershell/issues/6560</span></span>
    - <span data-ttu-id="2d2da-330">Aggiornamento alla versione 4.0.3 di Nuget per correggere l'eccezione del criterio in apiId</span><span class="sxs-lookup"><span data-stu-id="2d2da-330">Upgraded to 4.0.3 Nuget version which fixes the pattern exception on apiId</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-331">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-331">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-332">Correzione del problema relativo all'impossibilità di creare una VM con DiskFileParameterSet in New-AzureRmVm a causa della ridenominazione del tipo di account di archiviazione PremiumLRS.</span><span class="sxs-lookup"><span data-stu-id="2d2da-332">Fix issue with creating a vm using DiskFileParameterSet in New-AzureRmVm failing because of PremiumLRS storage account type renaming.</span></span>
* <span data-ttu-id="2d2da-333">Correzione del cmdlet Invoke-AzureRmVMRunCommand</span><span class="sxs-lookup"><span data-stu-id="2d2da-333">Fix Invoke-AzureRmVMRunCommand cmdlet</span></span>
* <span data-ttu-id="2d2da-334">Aggiornamento di Get-AzureRmAvailabilitySet per abilitare l'elenco di tutti i set di disponibilità in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-334">Update Get-AzureRmAvailabilitySet to enable list all availability sets in a subscription.</span></span>  <span data-ttu-id="2d2da-335">Il parametro ResouceGroupName è ora facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2d2da-335">(ResouceGroupName parameter is now optional.)</span></span>
* <span data-ttu-id="2d2da-336">Aggiornamento di SimpleParameterSet di 'New-AzureRmVm' per abilitare la rete accelerata nelle VM idonee.</span><span class="sxs-lookup"><span data-stu-id="2d2da-336">Update SimpleParameterSet of 'New-AzureRmVm' to enable Accelerated Network on qualifying vms.</span></span>
* <span data-ttu-id="2d2da-337">Aggiornamento del semplice set di parametri New-AzureRmVmss in modo da generare un errore di creazione del set di scalabilità di macchine virtuali quando il bilanciamento del carico specificato da un utente esiste già.</span><span class="sxs-lookup"><span data-stu-id="2d2da-337">Update New-AzureRmVmss simple parameter set to fail creating the vmss when a user specified LB already exists.</span></span>
* <span data-ttu-id="2d2da-338">Aggiornamento dell'esempio per New-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2d2da-338">Update example for New-AzureRmDisk</span></span>
* <span data-ttu-id="2d2da-339">Aggiunta dell'esempio per 'New-AzureRmVM'</span><span class="sxs-lookup"><span data-stu-id="2d2da-339">Add example for 'New-AzureRmVM'</span></span>
* <span data-ttu-id="2d2da-340">Aggiornamento della descrizione per Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="2d2da-340">Update description for Set-AzureRmVMOSDisk</span></span>
* <span data-ttu-id="2d2da-341">Aggiornamento dell'esempio 1 per Set-AzureRmVMBginfoExtension in modo da correggere l'ortografia e il prefisso.</span><span class="sxs-lookup"><span data-stu-id="2d2da-341">Update Example 1 for Set-AzureRmVMBginfoExtension to correct spelling and prefix.</span></span> 

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2d2da-342">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d2da-342">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2d2da-343">Aggiornamento della versione di ADF .Net SDK a 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="2d2da-343">Updated the ADF .Net SDK version to 1.1.0.</span></span>
* <span data-ttu-id="2d2da-344">Supporto per la condivisione del runtime di integrazione self-hosted tra data factory.</span><span class="sxs-lookup"><span data-stu-id="2d2da-344">Support self-hosted integration runtime sharing across data factories.</span></span>
     - <span data-ttu-id="2d2da-345">Aggiunta del nuovo parametro -SharedIntegrationRuntimeResourceId al cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d2da-345">Add new parameter -SharedIntegrationRuntimeResourceId to Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>
     - <span data-ttu-id="2d2da-346">Aggiunta del nuovo parametro facoltativo -LinkedDataFactoryName al cmdlet Remove-AzureRmDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="2d2da-346">Add new optional parameter -LinkedDataFactoryName to Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet.</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d2da-347">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d2da-347">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d2da-348">Aggiornamento della versione di DataPlane SDK (Microsoft.Azure.DataLake.Store) a 1.1.9</span><span class="sxs-lookup"><span data-stu-id="2d2da-348">Updated the DataPlane SDK (Microsoft.Azure.DataLake.Store) version to 1.1.9</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d2da-349">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-349">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d2da-350">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="2d2da-350">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>

#### <a name="azurerminsights"></a><span data-ttu-id="2d2da-351">AzureRM.Insights</span><span class="sxs-lookup"><span data-stu-id="2d2da-351">AzureRM.Insights</span></span>
* <span data-ttu-id="2d2da-352">Correzione della formattazione di OutputType nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2d2da-352">Fixed formatting of OutputType in help files</span></span>
* <span data-ttu-id="2d2da-353">Uso della versione di anteprima di Microsoft.Azure.Management.Monitor SDK 0.19.1</span><span class="sxs-lookup"><span data-stu-id="2d2da-353">Using Microsoft.Azure.Management.Monitor SDK 0.19.1-preview</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-354">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-354">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-355">Correzione del problema di piping in Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d2da-355">Fix piping issue in Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-356">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-356">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-357">Aggiunta di esempi per i cmdlet LoadBalancerInboundNatPoolConfig.</span><span class="sxs-lookup"><span data-stu-id="2d2da-357">Added examples for LoadBalancerInboundNatPoolConfig cmdlets.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-358">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-358">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-359">Correzione del problema relativo alla presenza di nome di tag e valore per 'Get-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="2d2da-359">Fix issue when providing both tag name and value for 'Get-AzureRmResource'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6765
* <span data-ttu-id="2d2da-360">Correzione dello scenario di piping con 'Set-AzureRmResource'</span><span class="sxs-lookup"><span data-stu-id="2d2da-360">Fix piping scenario with 'Set-AzureRmResource'</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-361">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-361">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-362">Aggiornamento del piping per InputObject e ResourceId nei cmdlet di rimozione</span><span class="sxs-lookup"><span data-stu-id="2d2da-362">Updated piping for InputObject and ResourceId in remove cmdlets</span></span>
* <span data-ttu-id="2d2da-363">Correzione di alcuni problemi</span><span class="sxs-lookup"><span data-stu-id="2d2da-363">fixed few issues</span></span>
    - https://github.com/Azure/azure-powershell/issues/3780
    - https://github.com/Azure/azure-powershell/issues/4340

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-364">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-364">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-365">Aggiunta del supporto per Advanced Threat Protection per il server con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d2da-365">Adding Server Advanced Threat Protection support with the following cmdlets:</span></span>
    - <span data-ttu-id="2d2da-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2d2da-366">Enable-AzureRmSqlServerAdvancedThreatProtection; Disable-AzureRmSqlServerAdvancedThreatProtection; Get-AzureRmSqlServerAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2d2da-367">Aggiunta del supporto per la valutazione della vulnerabilità con i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d2da-367">Adding Vulnerability Assessment support with the following cmdlets:</span></span>
    - <span data-ttu-id="2d2da-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span><span class="sxs-lookup"><span data-stu-id="2d2da-368">Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Get-AzureRmSqlDatabaseVulnerabilityAssessmentSettings; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentSettings</span></span>
    - <span data-ttu-id="2d2da-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span><span class="sxs-lookup"><span data-stu-id="2d2da-369">Set-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Get-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline; Clear-AzureRmSqlDatabaseVulnerabilityAssessmentRuleBaseline</span></span>
    - <span data-ttu-id="2d2da-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span><span class="sxs-lookup"><span data-stu-id="2d2da-370">Convert-AzureRmSqlDatabaseVulnerabilityAssessmentScan; Get-AzureRmSqlDatabaseVulnerabilityAssessmentScanRecord; Start-AzureRmSqlDatabaseVulnerabilityAssessmentScan</span></span>
* <span data-ttu-id="2d2da-371">Correzione dell'esempio in Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2d2da-371">Fixed example in Remove-AzureRmSqlServerFirewallRule</span></span>
* <span data-ttu-id="2d2da-372">Correzione della gestione non corretta di data e ora per impostazioni cultura non degli Stati Uniti in Get-AzureSqlSyncGroupLog</span><span class="sxs-lookup"><span data-stu-id="2d2da-372">Fix datetime handling incorrectly for non-us base culture in Get-AzureSqlSyncGroupLog</span></span>

#### <a name="azurermstorage"></a><span data-ttu-id="2d2da-373">AzureRM.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-373">AzureRM.Storage</span></span>
* <span data-ttu-id="2d2da-374">Aggiunta di Ps1XmlAttribute alle proprietà dei tipi di output dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d2da-374">Add Ps1XmlAttribute to cmdlets output types properties</span></span>
* <span data-ttu-id="2d2da-375">Visualizzazione dell'output del cmdlet StorageAccount nella vista tabella</span><span class="sxs-lookup"><span data-stu-id="2d2da-375">Show StorageAccount cmdlet output in table view</span></span>
    - <span data-ttu-id="2d2da-376">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d2da-376">Get-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2d2da-377">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d2da-377">New-AzureRmStorageAccount</span></span>
    - <span data-ttu-id="2d2da-378">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2d2da-378">Set-AzureRmStorageAccount</span></span>

#### <a name="azurermtags"></a><span data-ttu-id="2d2da-379">AzureRM.Tags</span><span class="sxs-lookup"><span data-stu-id="2d2da-379">AzureRM.Tags</span></span>
* <span data-ttu-id="2d2da-380">Rimozione dell'istruzione non corretta dalla Guida del cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="2d2da-380">Remove incorrect statement from Tag cmdlet help</span></span>
    - https://github.com/Azure/azure-powershell/issues/3878

## <a name="650---july-2018"></a><span data-ttu-id="2d2da-381">6.5.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-381">6.5.0 - July 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-382">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-382">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-383">Aggiornamento della Guida per 'Get-AzureRmContextAutosaveSetting'</span><span class="sxs-lookup"><span data-stu-id="2d2da-383">Updated help for 'Get-AzureRmContextAutosaveSetting'</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d2da-384">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-384">Azure.Storage</span></span>
* <span data-ttu-id="2d2da-385">Supporto del caricamento di BLOB o file con token di firma di accesso condiviso a sola scrittura</span><span class="sxs-lookup"><span data-stu-id="2d2da-385">Support Upload Blob or File with write only Sas token</span></span>
- <span data-ttu-id="2d2da-386">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2d2da-386">Set-AzureStorageBlobContent</span></span>
- <span data-ttu-id="2d2da-387">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2d2da-387">Set-AzureStorageFileContent</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2d2da-388">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-388">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2d2da-389">Aggiunta della proprietà obbligatoria ResourceGroupName ad AS.</span><span class="sxs-lookup"><span data-stu-id="2d2da-389">Add required property ResourceGroupName to AS.</span></span>

#### <a name="azurermautomation"></a><span data-ttu-id="2d2da-390">AzureRM.Automation</span><span class="sxs-lookup"><span data-stu-id="2d2da-390">AzureRM.Automation</span></span>
* <span data-ttu-id="2d2da-391">Aggiornamento della Guida e aggiunta di un esempio per 'New-AzureRMAutomationSchedule'</span><span class="sxs-lookup"><span data-stu-id="2d2da-391">Update help and add example for 'New-AzureRMAutomationSchedule'</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-392">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-392">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-393">Aggiunta del parametro -Tag a Update/New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d2da-393">Add -Tag parameter to Update/New-AzureRmAvailabilitySet</span></span>
* <span data-ttu-id="2d2da-394">Aggiunta di un esempio per 'Add-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="2d2da-394">Add example for 'Add-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2d2da-395">Aggiunta di esempi per 'Remove-AzureRmVmssExtension'</span><span class="sxs-lookup"><span data-stu-id="2d2da-395">Add examples for 'Remove-AzureRmVmssExtension'</span></span>
* <span data-ttu-id="2d2da-396">Aggiornamento della Guida per 'Set-AzureRmVMAccessExtension'</span><span class="sxs-lookup"><span data-stu-id="2d2da-396">Update help for 'Set-AzureRmVMAccessExtension'</span></span>
* <span data-ttu-id="2d2da-397">Aggiornamento di SimpleParameterSet per New-AzureRmVmmss per l'impostazione di SinglePlacementGroup su false per impostazione predefinita e aggiunta del parametro opzionale 'SinglePlacementGroup' che consente all'utente di creare il set di scalabilità di macchine virtuali in un singolo gruppo di selezione host.</span><span class="sxs-lookup"><span data-stu-id="2d2da-397">Update SimpleParameterSet for New-AzureRmVmss to set SinglePlacementGroup to false by default and add switch parameter 'SinglePlacementGroup' that enables the user to create the VMSS in a single placement group.</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d2da-398">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-398">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d2da-399">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSEventHubDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="2d2da-399">Added a readonly property 'PendingReplicationOperationsCount' to PSEventHubDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-400">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-400">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-401">Aggiornamento del messaggio di errore per Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2d2da-401">Update error message for Set-AzureRmKeyVaultAccessPolicy</span></span>

#### <a name="azurermlogicapp"></a><span data-ttu-id="2d2da-402">AzureRM.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2d2da-402">AzureRM.LogicApp</span></span>
* <span data-ttu-id="2d2da-403">Correzione dell'errore "Impossibile risolvere set di parametri" in New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="2d2da-403">Fixed "parameter set could not be resolved" error in New-AzureRmLogicApp</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-404">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-404">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-405">Abilitazione del peering di reti virtuali in più tenant per Set/Add-AzureRmVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2d2da-405">Enable peering across Virtual Networks in multiple Tenants for Set/Add-AzureRmVirtualNetworkPeering</span></span>
* <span data-ttu-id="2d2da-406">Aggiornamento dei cmdlet seguenti per il gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2d2da-406">Updated below cmdlets for Application Gateway</span></span>
    - <span data-ttu-id="2d2da-407">New-AzureRmApplicationGateway: aggiunta del flag EnableFIPS e del supporto delle zone</span><span class="sxs-lookup"><span data-stu-id="2d2da-407">New-AzureRmApplicationGateway : Added EnableFIPS flag and Zones support</span></span>
    - <span data-ttu-id="2d2da-408">New-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2d2da-408">New-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
    - <span data-ttu-id="2d2da-409">Set-AzureRmApplicationGatewaySku: aggiunta dei nuovi SKU Standard_v2 e WAF_v2</span><span class="sxs-lookup"><span data-stu-id="2d2da-409">Set-AzureRmApplicationGatewaySku : Added new skus Standard_v2 and WAF_v2</span></span>
* <span data-ttu-id="2d2da-410">Rigenerazione del cmdlet RouteTable con la versione più recente del generatore</span><span class="sxs-lookup"><span data-stu-id="2d2da-410">Regenerated RouteTable cmdlets with the latest generator version</span></span>

#### <a name="azurermrelay"></a><span data-ttu-id="2d2da-411">AzureRM.Relay</span><span class="sxs-lookup"><span data-stu-id="2d2da-411">AzureRM.Relay</span></span>
* <span data-ttu-id="2d2da-412">Aggiornamento dei file markdown, correzione del problema relativo al nome del parametro nell'esempio</span><span class="sxs-lookup"><span data-stu-id="2d2da-412">Updated markdown files, fix for the parameter name issue in example</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-413">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-413">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-414">Aggiornamento dei cmdlet roleassignment e roledefinition:</span><span class="sxs-lookup"><span data-stu-id="2d2da-414">Update Roleassignment and roledefinition cmdlets:</span></span>
    - <span data-ttu-id="2d2da-415">Rimozione delle chiamate roledefinition aggiuntive eseguite nell'ambito del paging.</span><span class="sxs-lookup"><span data-stu-id="2d2da-415">Remove extra roledefinition calls done as part of paging.</span></span>
* <span data-ttu-id="2d2da-416">Correzione del cmdlet Get-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="2d2da-416">Fix Get-AzureRmRoleAssignment cmdlet</span></span>
    - <span data-ttu-id="2d2da-417">Correzione della funzionalità dei parametri del comando -ExpandPrincipalGroups</span><span class="sxs-lookup"><span data-stu-id="2d2da-417">Fix -ExpandPrincipalGroups command parameter functionality</span></span>
* <span data-ttu-id="2d2da-418">Correzione del problema con 'Get-AzureRmResource', in cui il parametro '-ResourceType' faceva distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="2d2da-418">Fix issue with 'Get-AzureRmResource' where '-ResourceType' parameter was case sensitive</span></span>

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-419">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-419">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-420">Aggiunta del parametro top e skip ai cmdlet list</span><span class="sxs-lookup"><span data-stu-id="2d2da-420">Added top and skip parameter to list cmdlets</span></span>
* <span data-ttu-id="2d2da-421">Aggiunta di cmdlet di migrazione dello spazio dei nomi da Standard a Premium:</span><span class="sxs-lookup"><span data-stu-id="2d2da-421">Added Standard to Premium NameSpace migration cmdlets :</span></span>
    - <span data-ttu-id="2d2da-422">Start-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d2da-422">Start-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d2da-423">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d2da-423">Get-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d2da-424">Complete-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d2da-424">Complete-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d2da-425">Stop-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d2da-425">Stop-AzureRmServiceBusMigration</span></span>
    - <span data-ttu-id="2d2da-426">Remove-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="2d2da-426">Remove-AzureRmServiceBusMigration</span></span>
* <span data-ttu-id="2d2da-427">Aggiunta di una proprietà 'PendingReplicationOperationsCount' di sola lettura alla classe PSServiceBusDRConfigurationAttributes, che fornisce il conteggio delle operazioni di replica in sospeso mentre la replica è in corso</span><span class="sxs-lookup"><span data-stu-id="2d2da-427">Added a readonly property 'PendingReplicationOperationsCount' to PSServiceBusDRConfigurationAttributes class, which gives the pending replication operations count while replication is in progress</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2d2da-428">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d2da-428">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2d2da-429">Aggiornamento dell'esempio per 'New-AzureRmServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="2d2da-429">Update example for 'New-AzureRmServiceFabricCluster'</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-430">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-430">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-431">Aggiunta di nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere il certificato TDE all'istanza di SQL Server o a un'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="2d2da-431">Adding new Cmdlets for Management.Sql to allow customers to add TDE Certificate to Sql Server instance or a Managed Instance</span></span>
    - <span data-ttu-id="2d2da-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2d2da-432">Add-AzureRmSqlServerTransparentDataEncryptionCertificate</span></span>
    - <span data-ttu-id="2d2da-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span><span class="sxs-lookup"><span data-stu-id="2d2da-433">Add-AzureRmSqlManagedInstanceTransparentDataEncryptionCertificate</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d2da-434">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d2da-434">AzureRM.Websites</span></span>
* <span data-ttu-id="2d2da-435">Se impostati su false, `Set-AzureRmWebApp -AssignIdentity` e `Set-AzureRmWebAppSlot -AssignIdentity` rimuovono ora la proprietà Identity anche dal tag di anteprima object.Removing del sito.</span><span class="sxs-lookup"><span data-stu-id="2d2da-435">`Set-AzureRmWebApp -AssignIdentity` and  `Set-AzureRmWebAppSlot -AssignIdentity` when set to false will now remove the Identity property from the site object.Removing preview tag as well.</span></span>
* <span data-ttu-id="2d2da-436">Aggiornamento dell'esempio `Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics`</span><span class="sxs-lookup"><span data-stu-id="2d2da-436">`Get-AzureRmWebAppMetrics`,`Get-AzureRmAppServicePlanMetrics` example updated</span></span>
* <span data-ttu-id="2d2da-437">`Set-AzureRmWebApp -PhpVersion` supporta off come versione php valida</span><span class="sxs-lookup"><span data-stu-id="2d2da-437">`Set-AzureRmWebApp -PhpVersion` supports off as a valid php version</span></span>

## <a name="640---july-2018"></a><span data-ttu-id="2d2da-438">6.4.0 - Luglio 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-438">6.4.0 - July 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2d2da-439">Generale</span><span class="sxs-lookup"><span data-stu-id="2d2da-439">General</span></span>
* <span data-ttu-id="2d2da-440">Correzione della formattazione di OutputType nei file della Guida per la maggior parte dei moduli</span><span class="sxs-lookup"><span data-stu-id="2d2da-440">Fixed formatting of OutputType in help files for most modules</span></span>

#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-441">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-441">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-442">Aggiunta dell'attributo Ps1Xml ai tipi di output di base</span><span class="sxs-lookup"><span data-stu-id="2d2da-442">Ps1Xml attribute added to the basic output types</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-443">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-443">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-444">Funzionalità tag IP per VMSS</span><span class="sxs-lookup"><span data-stu-id="2d2da-444">IP Tag feature for VMSS</span></span>
    - <span data-ttu-id="2d2da-445">Aggiunta del cmdlet 'New-AzureRmVmssIpTagConfig'</span><span class="sxs-lookup"><span data-stu-id="2d2da-445">'New-AzureRmVmssIpTagConfig' cmdlet is added</span></span>
    - <span data-ttu-id="2d2da-446">Aggiunta del parametro IpTag a New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-446">IpTag parameter is added to New-AzureRmVmssIpConfig</span></span>
* <span data-ttu-id="2d2da-447">Funzionalità di ripristino dello stato precedente automatico del sistema operativo per VMSS</span><span class="sxs-lookup"><span data-stu-id="2d2da-447">Auto OS Rollback feature for VMSS</span></span>
    - <span data-ttu-id="2d2da-448">Aggiunta dei parametri DisableAutoRollback a New-AzureRmVmssConfig e Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-448">DisableAutoRollback parameters are added to New-AzureRmVmssConfig and Update-AzureRmVmss</span></span>
* <span data-ttu-id="2d2da-449">Funzionalità Cronologia degli aggiornamenti del sistema operativo per Vmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-449">OS Upgrade History feature for Vmss</span></span>
    - <span data-ttu-id="2d2da-450">Aggiunta del parametro opzionale OSUpgradeHistory a Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-450">OSUpgradeHistory switch parameter is added to Get-AzureRmVmss</span></span>

#### <a name="azurermdatalakeanalytics"></a><span data-ttu-id="2d2da-451">AzureRM.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2d2da-451">AzureRM.DataLakeAnalytics</span></span>
* <span data-ttu-id="2d2da-452">Aggiunta del supporto per gli elenchi di controllo di accesso del catalogo tramite i comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d2da-452">Add support for Catalog ACLs through the following commands:</span></span>
    - <span data-ttu-id="2d2da-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-453">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2d2da-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-454">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>
    - <span data-ttu-id="2d2da-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-455">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d2da-456">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d2da-456">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d2da-457">Aggiunta del supporto per l'annullamento e della verifica dello stato per Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="2d2da-457">Add cancellation support and progress tracking for Set-AzureRmDataLakeStoreItemAclEntry, Remove-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl</span></span>
* <span data-ttu-id="2d2da-458">Aggiunta del supporto per l'annullamento per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="2d2da-458">Add cancellation support for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2d2da-459">Correzione dello scaricamento dei messaggi di debug per i cmdlet che eseguono operazioni ricorsive</span><span class="sxs-lookup"><span data-stu-id="2d2da-459">Fix flushing of debug messages for cmdlets that does recursive operations</span></span>
* <span data-ttu-id="2d2da-460">Correzione della posizione del test dei cmdlet di DataLake</span><span class="sxs-lookup"><span data-stu-id="2d2da-460">Fix location of test of DataLake cmdlets</span></span>

#### <a name="azurermeventhub"></a><span data-ttu-id="2d2da-461">AzureRM.EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2da-461">AzureRM.EventHub</span></span>
* <span data-ttu-id="2d2da-462">Aggiunta del parametro facoltativo MaxCount al cmdlet per le operazioni dell'elenco Get-AzureRmEventHub e Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="2d2da-462">Added Optional MaxCount parameter to List Operations cmdlet Get-AzureRmEventHub and Get-AzureRmEventHubConsumerGroup</span></span>
* <span data-ttu-id="2d2da-463">Risoluzione del problema nel cmdlet New-AzureRmEventHub che richiede almeno un parametro durante la creazione di un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="2d2da-463">Fixed issue in New-AzureRmEventHub cmdlet where at least one parameter needed while creating New EventHub.</span></span> <span data-ttu-id="2d2da-464">Aggiunta di un set di parametri predefinito.</span><span class="sxs-lookup"><span data-stu-id="2d2da-464">Provided Default Parameter set.</span></span>
* <span data-ttu-id="2d2da-465">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmEventHubKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2d2da-465">Added optional Parameter -KeyValue to New-AzureRmEventHubKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-466">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-466">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-467">Correzione di un problema relativo alla restituzione di tutte le risorse da parte di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="2d2da-467">Fix issue where all resources were being returned by Get-AzureRmKeyVault -Tag</span></span>

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-468">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-468">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-469">Esposizione di nuovi SKU per VirtualNetworkGateways con ridondanza della zona</span><span class="sxs-lookup"><span data-stu-id="2d2da-469">Expose new Skus for Zone-Redundant VirtualNetworkGateways</span></span>
* <span data-ttu-id="2d2da-470">Aggiunta di nuovi comandi per la funzionalità delle API partner di ExpressRoute tramite ARM</span><span class="sxs-lookup"><span data-stu-id="2d2da-470">Added new commands for feature: ExpressRoute Partner APIs via ARM</span></span>
    - <span data-ttu-id="2d2da-471">Aggiunta di Get-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2d2da-471">Added Get-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2d2da-472">Aggiunta di Set-AzureRmExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="2d2da-472">Added Set-AzureRmExpressRouteCrossConnection</span></span>
    - <span data-ttu-id="2d2da-473">Aggiunta di Add-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d2da-473">Added Add-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d2da-474">Aggiunta di Get-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d2da-474">Added Get-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d2da-475">Aggiunta di Remove-AzureRmExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="2d2da-475">Added Remove-AzureRmExpressRouteCrossConnectionPeering</span></span>
    - <span data-ttu-id="2d2da-476">Aggiunta di Get-AzureRMExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2d2da-476">Added Get-AzureRMExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2d2da-477">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2d2da-477">Added Get-AzureRMExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2d2da-478">Aggiunta di Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2d2da-478">Added Get-AzureRMExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2d2da-479">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d2da-479">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d2da-480">Aggiunta del cmdlet Get-AzureRmRecoveryServicesBackupStatus.</span><span class="sxs-lookup"><span data-stu-id="2d2da-480">Added Get-AzureRmRecoveryServicesBackupStatus cmdlet.</span></span> <span data-ttu-id="2d2da-481">Questo cmdlet accetta un ID di macchina virtuale e verifica se la VM è protetta da un insieme di credenziali nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2d2da-481">This cmdlet takes a VM ID and checks if the VM is protected by some vault in the subscription.</span></span> <span data-ttu-id="2d2da-482">Se tale insieme di credenziali esiste, il cmdlet restituisce i dettagli dell'insieme di credenziali.</span><span class="sxs-lookup"><span data-stu-id="2d2da-482">If there exists such a vault, the cmdlet outputs the vault details.</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-483">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-483">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-484">Aggiornamento dei cmdlet Get-AzureRmPolicyAssignment:</span><span class="sxs-lookup"><span data-stu-id="2d2da-484">Update Get-AzureRmPolicyAssignment cmdlets:</span></span>
    - <span data-ttu-id="2d2da-485">Aggiunta del supporto per elencare i valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2d2da-485">Add support for listing -Scope values at management group level</span></span>
    - <span data-ttu-id="2d2da-486">Aggiunta del supporto per il recupero di singole assegnazioni con valori -Scope a livello di gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="2d2da-486">Add support for retrieving individual assignments with -Scope values at management group level</span></span>
    - <span data-ttu-id="2d2da-487">Aggiunta delle opzioni -Effective e -All al parametro di controllo</span><span class="sxs-lookup"><span data-stu-id="2d2da-487">Add -Effective and -All switches to control  parameter</span></span>
* <span data-ttu-id="2d2da-488">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2d2da-488">Update Get/New/Remove/Set-AzureRmPolicyDefinition cmdlets</span></span>
    - <span data-ttu-id="2d2da-489">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="2d2da-489">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2d2da-490">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="2d2da-490">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2d2da-491">Aggiornamento dei cmdlet Get/New/Remove/Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="2d2da-491">Update Get/New/Remove/Set-AzureRmPolicySetDefinition cmdlets</span></span>
    - <span data-ttu-id="2d2da-492">Aggiunta del parametro -ManagementGroupName per l'applicazione di operazioni a un gruppo di gestione specifico</span><span class="sxs-lookup"><span data-stu-id="2d2da-492">Add -ManagementGroupName parameter to apply operations to a given management group</span></span>
    - <span data-ttu-id="2d2da-493">Aggiunta del parametro -SubscriptionId per l'applicazione di operazioni a una sottoscrizione specifica</span><span class="sxs-lookup"><span data-stu-id="2d2da-493">Add -SubscriptionId parameter to apply operations to a given subscription</span></span>
* <span data-ttu-id="2d2da-494">Aggiunta del supporto per i riferimenti segreti di KeyVault nei parametri quando si usa 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2d2da-494">Add KeyVault secret reference support in parameters when using 'TemplateParameterObject' in 'New-AzureRmResourceGroupDeployment'</span></span>
* <span data-ttu-id="2d2da-495">Risoluzione del problema a causa del quale il parametro '-EndDate' viene ignorato per 'New-AzureRmADAppCredential'</span><span class="sxs-lookup"><span data-stu-id="2d2da-495">Fix issue where '-EndDate' parameter was ignored for 'New-AzureRmADAppCredential'</span></span>
    - https://github.com/Azure/azure-powershell/issues/6505
* <span data-ttu-id="2d2da-496">Risoluzione del problema relativo all'uso di un URL non corretto da parte di 'Add-AzureRmADGroupMember' per l'effettuazione di una richiesta</span><span class="sxs-lookup"><span data-stu-id="2d2da-496">Fix issue where 'Add-AzureRmADGroupMember' used incorrect URL to make request</span></span>
    - https://github.com/Azure/azure-powershell/issues/6485

#### <a name="azurermservicebus"></a><span data-ttu-id="2d2da-497">AzureRM.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2d2da-497">AzureRM.ServiceBus</span></span>
* <span data-ttu-id="2d2da-498">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmServiceBusKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2d2da-498">Added optional Parameter -KeyValue to New-AzureRmServiceBusKey cmdlet, which enables user to provide KeyValue.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-499">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-499">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-500">Chiarimento dei punti di ripristino definiti dall'utente per SQLDW nella Guida di New-AzureRmSqlDatabaseRestorePoint</span><span class="sxs-lookup"><span data-stu-id="2d2da-500">Clarified User-Defined Restore Points for SQLDW in New-AzureRmSqlDatabaseRestorePoint help</span></span>
* <span data-ttu-id="2d2da-501">Aggiornamento della documentazione del parametro -ComputeGeneration in alcuni cmdlet</span><span class="sxs-lookup"><span data-stu-id="2d2da-501">Updated documentation of -ComputeGeneration parameter in several cmdlets</span></span>

## <a name="630---june-2018"></a><span data-ttu-id="2d2da-502">6.3.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-502">6.3.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-503">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-503">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-504">Aggiornamento dei messaggi di errore per Enable-AzureRmContextAutoSave</span><span class="sxs-lookup"><span data-stu-id="2d2da-504">Updated error messages for Enable-AzureRmContextAutoSave</span></span>
* <span data-ttu-id="2d2da-505">Creare un contesto per ogni sottoscrizione quando si esegue 'Connect-AzureRmAccount' senza contesto precedente</span><span class="sxs-lookup"><span data-stu-id="2d2da-505">Create a context for each subscription when running 'Connect-AzureRmAccount' with no previous context</span></span>

#### <a name="azurestorage"></a><span data-ttu-id="2d2da-506">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2d2da-506">Azure.Storage</span></span>
* <span data-ttu-id="2d2da-507">Aggiunta di altre informazioni sul parametro -Permissions nei file della Guida.</span><span class="sxs-lookup"><span data-stu-id="2d2da-507">Added additional information about -Permissions parameter in help files.</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-508">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-508">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-509">'Get-AzureRmVmDiskEncryptionStatus' risolve un problema riscontrato per le VM senza dischi dati</span><span class="sxs-lookup"><span data-stu-id="2d2da-509">'Get-AzureRmVmDiskEncryptionStatus' fixes an issue observed for VMs with no data disks</span></span> 
* <span data-ttu-id="2d2da-510">Aggiornamento della versione della libreria del client di calcolo per la correzione dei cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="2d2da-510">Update Compute client library version to fix following cmdlets</span></span>
    - <span data-ttu-id="2d2da-511">Grant-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2d2da-511">Grant-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2d2da-512">Grant-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2d2da-512">Grant-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2d2da-513">Save-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="2d2da-513">Save-AzureRmVMImage</span></span>
* <span data-ttu-id="2d2da-514">Correzione dei cmdlet seguenti per la corretta visualizzazione di 'operation ID' e 'operation status':</span><span class="sxs-lookup"><span data-stu-id="2d2da-514">Fixed following cmdlets to show 'operation ID' and 'operation status' correctly:</span></span>
    - <span data-ttu-id="2d2da-515">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d2da-515">Start-AzureRmVM</span></span>
    - <span data-ttu-id="2d2da-516">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d2da-516">Stop-AzureRmVM</span></span>
    - <span data-ttu-id="2d2da-517">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d2da-517">Restart-AzureRmVM</span></span>
    - <span data-ttu-id="2d2da-518">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d2da-518">Set-AzureRmVM</span></span>
    - <span data-ttu-id="2d2da-519">Remove-AzuerRmVM</span><span class="sxs-lookup"><span data-stu-id="2d2da-519">Remove-AzuerRmVM</span></span>
    - <span data-ttu-id="2d2da-520">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-520">Set-AzureRmVmss</span></span>
    - <span data-ttu-id="2d2da-521">Start-AzureRmVmssRollingOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2d2da-521">Start-AzureRmVmssRollingOSUpgrade</span></span>
    - <span data-ttu-id="2d2da-522">Stop-AzureRmVmssRollingUpgrade</span><span class="sxs-lookup"><span data-stu-id="2d2da-522">Stop-AzureRmVmssRollingUpgrade</span></span>
    - <span data-ttu-id="2d2da-523">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-523">Start-AzureRmVmss</span></span>
    - <span data-ttu-id="2d2da-524">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-524">Restart-AzureRmVmss</span></span>
    - <span data-ttu-id="2d2da-525">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-525">Stop-AzureRmVmss</span></span>
    - <span data-ttu-id="2d2da-526">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="2d2da-526">Remove-AzureRmVmss</span></span>
    - <span data-ttu-id="2d2da-527">ConvertTo-AzureRmVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="2d2da-527">ConvertTo-AzureRmVMManagedDisk</span></span>
    - <span data-ttu-id="2d2da-528">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="2d2da-528">Revoke-AzureRmSnapshotAccess</span></span>
    - <span data-ttu-id="2d2da-529">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="2d2da-529">Remove-AzureRmSnapshot</span></span>
    - <span data-ttu-id="2d2da-530">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="2d2da-530">Revoke-AzureRmDiskAccess</span></span>
    - <span data-ttu-id="2d2da-531">Remove-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2d2da-531">Remove-AzureRmDisk</span></span>
    - <span data-ttu-id="2d2da-532">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="2d2da-532">Remove-AzureRmContainerService</span></span>
    - <span data-ttu-id="2d2da-533">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2d2da-533">Remove-AzureRmAvailabilitySet</span></span>

#### <a name="azurermeventgrid"></a><span data-ttu-id="2d2da-534">AzureRM.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2d2da-534">AzureRM.EventGrid</span></span>
* <span data-ttu-id="2d2da-535">Rimozione delle condizioni di convalida ValidateNotNullOrEmpty per SubjectBeginsWith/SubjectEndsWith nel cmdlet Update-AzureRmEventGridSubscription per consentire la modifica di questi parametri in una stringa vuota, se necessario.</span><span class="sxs-lookup"><span data-stu-id="2d2da-535">Remove ValidateNotNullOrEmpty validation conditions for SubjectBeginsWith/SubjectEndsWith in Update-AzureRmEventGridSubscription cmdlet to allow changing these parameters to empty string if needed.</span></span>

#### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-536">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-536">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-537">Correzione del problema per il quale non venivano restituiti tag con l'esecuzione di Get-AzureRmKeyVault -Tag</span><span class="sxs-lookup"><span data-stu-id="2d2da-537">Fix issue where no Tags are being returned when Get-AzureRmKeyVault -Tag is run</span></span>

#### <a name="azurermpolicyinsights"></a><span data-ttu-id="2d2da-538">AzureRM.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2d2da-538">AzureRM.PolicyInsights</span></span>
* <span data-ttu-id="2d2da-539">Versione pubblica dei cmdlet di Policy Insights</span><span class="sxs-lookup"><span data-stu-id="2d2da-539">Public release of Policy Insights cmdlets</span></span>
    - <span data-ttu-id="2d2da-540">Uso della versione API 2018-04-04</span><span class="sxs-lookup"><span data-stu-id="2d2da-540">Use API version 2018-04-04</span></span>
    - <span data-ttu-id="2d2da-541">Aggiunta di PolicyDefinitionReferenceId ai risultati di Get-AzureRmPolicyStateSummary</span><span class="sxs-lookup"><span data-stu-id="2d2da-541">Add PolicyDefinitionReferenceId to the results of Get-AzureRmPolicyStateSummary</span></span>

#### <a name="azurermrecoveryservicesbackup"></a><span data-ttu-id="2d2da-542">AzureRM.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2d2da-542">AzureRM.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2d2da-543">Aggiunta del parametro -Vault ai cmdlet RecoveryServices.Backup.</span><span class="sxs-lookup"><span data-stu-id="2d2da-543">Added -Vault parameter to RecoveryServices.Backup cmdlets.</span></span> <span data-ttu-id="2d2da-544">Quando viene passato, sostituisce il cmdlet Set-AzureRmRecoveryServicesContext.</span><span class="sxs-lookup"><span data-stu-id="2d2da-544">When passed, this will override the Set-AzureRmRecoveryServicesContext cmdlet.</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-545">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-545">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-546">Aggiornamento dell'esempio nel file della Guida per Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="2d2da-546">Updated example in the help file for Get-AzureRmSqlDatabaseExpanded</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d2da-547">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d2da-547">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d2da-548">Aggiornamento del file della Guida per Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-548">Updated the help file for Add-AzureRmTrafficManagerEndpointConfig</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d2da-549">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d2da-549">AzureRM.Websites</span></span>
* <span data-ttu-id="2d2da-550">'Set-AzureRmWebApp' è stato aggiornato in modo da non sovrascrive AppSettings quando si usa -AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2d2da-550">'Set-AzureRmWebApp' is updated to not overwrite the AppSettings when using -AssignIdentity</span></span>
* <span data-ttu-id="2d2da-551">'New-AzureRmWebAppSlot' è stato aggiornato per tenere conto di AppServicePlan come parametro facoltativo</span><span class="sxs-lookup"><span data-stu-id="2d2da-551">'New-AzureRmWebAppSlot' is updated to honor AppServicePlan as an optional parameter</span></span>

## <a name="621---june-2018"></a><span data-ttu-id="2d2da-552">6.2.1 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-552">6.2.1 - June 2018</span></span>
### <a name="azurermoperationalinsights"></a><span data-ttu-id="2d2da-553">AzureRM.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2d2da-553">AzureRM.OperationalInsights</span></span>
* <span data-ttu-id="2d2da-554">Aggiornamento del modello PSWorkspace per consentire alla rete di usare il tipo come parametro</span><span class="sxs-lookup"><span data-stu-id="2d2da-554">Updated PSWorkspace model to allow Network to use type as a parameter</span></span>

## <a name="620---june-2018"></a><span data-ttu-id="2d2da-555">6.2.0 - Giugno 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-555">6.2.0 - June 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-556">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-556">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-557">Risoluzione del problema relativo al mancato caricamento della versione 10.0.3 di Newtonsoft.Json durante l'importazione del modulo</span><span class="sxs-lookup"><span data-stu-id="2d2da-557">Fix issue where version 10.0.3 of Newtonsoft.Json wasn't being loaded on module import</span></span>

#### <a name="azurermcompute"></a><span data-ttu-id="2d2da-558">AzureRM.Compute</span><span class="sxs-lookup"><span data-stu-id="2d2da-558">AzureRM.Compute</span></span>
* <span data-ttu-id="2d2da-559">Funzionalità di aggiornamento delle VM di set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="2d2da-559">VMSS VM Update feature</span></span>
    - <span data-ttu-id="2d2da-560">Aggiunta dei cmdlet "Update-AzureRmVmssVM" e "New-AzureRmVMDataDisk"</span><span class="sxs-lookup"><span data-stu-id="2d2da-560">Added 'Update-AzureRmVmssVM' and 'New-AzureRmVMDataDisk' cmdlets</span></span>
    - <span data-ttu-id="2d2da-561">Aggiunta del parametro VirtualMachineScaleSetVM al cmdlet "Add-AzureRmVMDataDisk" per supportare l'aggiunta di un disco dati a una VM di un set di scalabilità di macchine virtuali</span><span class="sxs-lookup"><span data-stu-id="2d2da-561">Add VirtualMachineScaleSetVM parameter to 'Add-AzureRmVMDataDisk' cmdlet to support adding a data disk to Vmss VM.</span></span>

#### <a name="azurermdatafactoryv2"></a><span data-ttu-id="2d2da-562">AzureRM.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2d2da-562">AzureRM.DataFactoryV2</span></span>
* <span data-ttu-id="2d2da-563">Aggiornamento di ADF .Net SDK alla versione 0.8.0-preview contenente le modifiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="2d2da-563">Updated the ADF .Net SDK version to 0.8.0-preview containing following changes:</span></span>
    - <span data-ttu-id="2d2da-564">Aggiunta dell'operazione di configurazione del repository della factory</span><span class="sxs-lookup"><span data-stu-id="2d2da-564">Added Configure factory repository operation</span></span>
    - <span data-ttu-id="2d2da-565">Aggiornamento del servizio collegato QuickBooks per l'esposizione delle proprietà consumerKey e consumerSecret</span><span class="sxs-lookup"><span data-stu-id="2d2da-565">Updated QuickBooks LinkedService to expose consumerKey and consumerSecret properties</span></span>
    - <span data-ttu-id="2d2da-566">Aggiornamento di diversi tipi di modello da SecretBase a Object</span><span class="sxs-lookup"><span data-stu-id="2d2da-566">Updated Several model types from SecretBase to Object</span></span>
    - <span data-ttu-id="2d2da-567">Aggiunta del trigger di eventi BLOB</span><span class="sxs-lookup"><span data-stu-id="2d2da-567">Added Blob Events trigger</span></span>

### <a name="azurermkeyvault"></a><span data-ttu-id="2d2da-568">AzureRM.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2d2da-568">AzureRM.KeyVault</span></span>
* <span data-ttu-id="2d2da-569">Aggiornamento della documentazione con output di esempio</span><span class="sxs-lookup"><span data-stu-id="2d2da-569">Update documentation with example output</span></span>

### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-570">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-570">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-571">Abilitazione dei parametri di Analisi del traffico nei cmdlet di Network Watcher</span><span class="sxs-lookup"><span data-stu-id="2d2da-571">Enable Traffic Analytics parameters on Network Watcher cmdlets</span></span>

#### <a name="azurermresources"></a><span data-ttu-id="2d2da-572">AzureRM.Resources</span><span class="sxs-lookup"><span data-stu-id="2d2da-572">AzureRM.Resources</span></span>
* <span data-ttu-id="2d2da-573">Risoluzione del problema relativo alla proprietà "Properties" degli oggetti "PSResource" restituiti da "Get-AzureRmResource"</span><span class="sxs-lookup"><span data-stu-id="2d2da-573">Fix issue with 'Properties' property of 'PSResource' object(s) returned from 'Get-AzureRmResource'</span></span>

#### <a name="azurermscheduler"></a><span data-ttu-id="2d2da-574">AzureRM.Scheduler</span><span class="sxs-lookup"><span data-stu-id="2d2da-574">AzureRM.Scheduler</span></span>
* <span data-ttu-id="2d2da-575">Risoluzione del problema relativo alla mancata impostazione dei nuovi valori di autenticazione con l'aggiornamento di ServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="2d2da-575">Fix issue with update ServiceBusQueueJob not setting new Auth values</span></span>

### <a name="azurermsql"></a><span data-ttu-id="2d2da-576">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-576">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-577">Aggiornamento dei cmdlet seguenti con il parametro LicenseType facoltativo</span><span class="sxs-lookup"><span data-stu-id="2d2da-577">Updated the following cmdlets with optional LicenseType parameter</span></span>
    - <span data-ttu-id="2d2da-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d2da-578">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2d2da-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2d2da-579">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2d2da-580">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2d2da-580">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2d2da-581">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d2da-581">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2d2da-582">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d2da-582">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermwebsites"></a><span data-ttu-id="2d2da-583">AzureRM.Websites</span><span class="sxs-lookup"><span data-stu-id="2d2da-583">AzureRM.Websites</span></span>
* <span data-ttu-id="2d2da-584">Aggiornamento di "New-AzureRMWebApp" per l'uso di algoritmi comuni della libreria Strategy</span><span class="sxs-lookup"><span data-stu-id="2d2da-584">'New-AzureRMWebApp' is updated to use common algorithms from the Strategy library.</span></span>

## <a name="610---may-2018"></a><span data-ttu-id="2d2da-585">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="2d2da-585">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="2d2da-586">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="2d2da-586">AzureRM.Profile</span></span>
* <span data-ttu-id="2d2da-587">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="2d2da-587">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="2d2da-588">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2d2da-588">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="2d2da-589">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="2d2da-589">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="2d2da-590">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d2da-590">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="2d2da-591">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="2d2da-591">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="2d2da-592">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2d2da-592">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="2d2da-593">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="2d2da-593">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="2d2da-594">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="2d2da-594">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="2d2da-595">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="2d2da-595">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="2d2da-596">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="2d2da-596">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="2d2da-597">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="2d2da-597">Added support for MSI identity</span></span>
* <span data-ttu-id="2d2da-598">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="2d2da-598">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="2d2da-599">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="2d2da-599">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="2d2da-600">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d2da-600">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="2d2da-601">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="2d2da-601">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="2d2da-602">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2d2da-602">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="2d2da-603">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="2d2da-603">AzureRM.Batch</span></span>
* <span data-ttu-id="2d2da-604">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="2d2da-604">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="2d2da-605">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="2d2da-605">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="2d2da-606">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="2d2da-606">AzureRM.Consumption</span></span>
* <span data-ttu-id="2d2da-607">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="2d2da-607">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="2d2da-608">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2d2da-608">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="2d2da-609">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="2d2da-609">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="2d2da-610">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-610">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="2d2da-611">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="2d2da-611">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="2d2da-612">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="2d2da-612">AzureRM.Network</span></span>
* <span data-ttu-id="2d2da-613">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="2d2da-613">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="2d2da-614">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="2d2da-614">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="2d2da-615">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d2da-615">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="2d2da-616">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="2d2da-616">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="2d2da-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-617">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2d2da-618">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="2d2da-618">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="2d2da-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-619">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="2d2da-620">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="2d2da-620">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="2d2da-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="2d2da-621">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="2d2da-622">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2d2da-622">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="2d2da-623">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="2d2da-623">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="2d2da-624">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="2d2da-624">AzureRM.Sql</span></span>
* <span data-ttu-id="2d2da-625">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="2d2da-625">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="2d2da-626">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="2d2da-626">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="2d2da-627">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="2d2da-627">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="2d2da-628">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="2d2da-628">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="2d2da-629">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="2d2da-629">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="2d2da-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d2da-630">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="2d2da-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="2d2da-631">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="2d2da-632">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="2d2da-632">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="2d2da-633">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2d2da-633">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="2d2da-634">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="2d2da-634">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="2d2da-635">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2d2da-635">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="2d2da-636">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="2d2da-636">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>
