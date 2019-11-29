---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: 2280b594ee9f525b2fa3175c917f6365cea354ba
ms.sourcegitcommit: 45e1823aa1a792840aa4829831b5f67a9d5d24a0
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "74537114"
---
## <a name="310---november-2019"></a><span data-ttu-id="10032-103">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="10032-103">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10032-104">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="10032-104">Highlights since the last major release</span></span>
* <span data-ttu-id="10032-105">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-105">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="10032-106">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-106">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-107">Az.Compute</span></span>
* <span data-ttu-id="10032-108">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-108">VM Reapply feature</span></span>
    - <span data-ttu-id="10032-109">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="10032-109">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="10032-110">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="10032-110">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="10032-111">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-111">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="10032-112">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10032-112">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="10032-113">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-113">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="10032-114">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="10032-114">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="10032-115">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="10032-115">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="10032-116">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="10032-116">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="10032-117">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="10032-117">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="10032-118">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-118">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="10032-119">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="10032-119">Az.DataBoxEdge</span></span>
* <span data-ttu-id="10032-120">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="10032-120">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10032-121">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="10032-121">Get the Order</span></span>
* <span data-ttu-id="10032-122">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="10032-122">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10032-123">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="10032-123">Create new Order</span></span>
* <span data-ttu-id="10032-124">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="10032-124">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="10032-125">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="10032-125">Remove the Order</span></span>
* <span data-ttu-id="10032-126">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="10032-126">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="10032-127">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="10032-127">Now creates Local Share</span></span>
* <span data-ttu-id="10032-128">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="10032-128">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="10032-129">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="10032-129">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="10032-130">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="10032-130">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="10032-131">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="10032-131">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="10032-132">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="10032-132">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10032-133">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="10032-133">Gets the information about Triggers</span></span>
* <span data-ttu-id="10032-134">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="10032-134">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10032-135">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="10032-135">Create new Triggers</span></span>
* <span data-ttu-id="10032-136">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="10032-136">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="10032-137">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="10032-137">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-138">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-138">Az.DataFactory</span></span>
* <span data-ttu-id="10032-139">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="10032-139">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="10032-140">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="10032-140">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-141">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-141">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-142">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="10032-142">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-143">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-143">Az.EventHub</span></span>
* <span data-ttu-id="10032-144">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="10032-144">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10032-145">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10032-145">Az.FrontDoor</span></span>
* <span data-ttu-id="10032-146">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="10032-146">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="10032-147">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="10032-147">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="10032-148">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="10032-148">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="10032-149">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="10032-149">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-150">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-150">Az.Network</span></span>
* <span data-ttu-id="10032-151">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="10032-151">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="10032-152">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="10032-152">Az.PrivateDns</span></span>
* <span data-ttu-id="10032-153">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-153">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-154">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-154">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-155">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="10032-155">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="10032-156">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="10032-156">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="10032-157">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-157">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10032-158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10032-158">Az.RedisCache</span></span>
* <span data-ttu-id="10032-159">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="10032-159">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="10032-160">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="10032-160">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="10032-161">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="10032-161">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-162">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-162">Az.Resources</span></span>
- <span data-ttu-id="10032-163">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="10032-163">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="10032-164">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="10032-164">Updated create policy definition help example</span></span>
- <span data-ttu-id="10032-165">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="10032-165">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="10032-166">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="10032-166">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="10032-167">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="10032-167">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-168">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-168">Az.Sql</span></span>
* <span data-ttu-id="10032-169">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="10032-169">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="10032-170">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="10032-170">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="10032-171">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="10032-171">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="10032-172">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-172">General</span></span>
* <span data-ttu-id="10032-173">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-173">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10032-174">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-174">Az.Accounts</span></span>
* <span data-ttu-id="10032-175">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="10032-175">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="10032-176">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10032-176">Az.Advisor</span></span>
* <span data-ttu-id="10032-177">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="10032-177">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10032-178">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10032-178">Az.Batch</span></span>
* <span data-ttu-id="10032-179">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="10032-179">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="10032-180">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="10032-180">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="10032-181">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="10032-181">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="10032-182">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="10032-182">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="10032-183">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="10032-183">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="10032-184">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="10032-184">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="10032-185">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="10032-185">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="10032-186">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="10032-186">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="10032-187">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="10032-187">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="10032-188">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="10032-188">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="10032-189">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="10032-189">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="10032-190">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="10032-190">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="10032-191">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="10032-191">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="10032-192">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="10032-192">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="10032-193">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="10032-193">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="10032-194">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="10032-194">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="10032-195">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="10032-195">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="10032-196">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10032-196">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="10032-197">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="10032-197">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="10032-198">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="10032-198">This operation is no longer supported.</span></span>
* <span data-ttu-id="10032-199">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10032-199">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="10032-200">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="10032-200">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="10032-201">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="10032-201">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="10032-202">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="10032-202">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="10032-203">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="10032-203">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="10032-204">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="10032-204">New non-verified images are also now returned.</span></span> <span data-ttu-id="10032-205">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="10032-205">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="10032-206">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="10032-206">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="10032-207">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="10032-207">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="10032-208">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="10032-208">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="10032-209">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="10032-209">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="10032-210">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="10032-210">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="10032-211">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="10032-211">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="10032-212">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="10032-212">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="10032-213">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="10032-213">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="10032-214">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="10032-214">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10032-215">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-215">Az.Cdn</span></span>
* <span data-ttu-id="10032-216">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="10032-216">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="10032-217">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="10032-217">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-218">Az.Compute</span></span>
* <span data-ttu-id="10032-219">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="10032-219">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="10032-220">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="10032-220">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="10032-221">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="10032-221">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="10032-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="10032-222">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="10032-223">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10032-223">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10032-224">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="10032-224">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="10032-225">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="10032-225">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="10032-226">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-226">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="10032-227">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="10032-227">Breaking changes</span></span>
    - <span data-ttu-id="10032-228">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="10032-228">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="10032-229">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="10032-229">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-230">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-230">Az.DataFactory</span></span>
* <span data-ttu-id="10032-231">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="10032-231">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-232">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-232">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-233">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="10032-233">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="10032-234">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="10032-234">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="10032-235">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="10032-235">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="10032-236">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="10032-236">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="10032-237">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="10032-237">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="10032-238">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="10032-238">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10032-239">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10032-239">Az.FrontDoor</span></span>
* <span data-ttu-id="10032-240">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="10032-240">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10032-241">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10032-241">Az.HDInsight</span></span>
* <span data-ttu-id="10032-242">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="10032-242">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="10032-243">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="10032-243">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="10032-244">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="10032-244">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="10032-245">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-245">Removed five cmdlets:</span></span>
    - <span data-ttu-id="10032-246">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10032-246">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10032-247">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10032-247">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10032-248">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="10032-248">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="10032-249">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10032-249">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="10032-250">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10032-250">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="10032-251">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-251">Added three cmdlets:</span></span>
    - <span data-ttu-id="10032-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10032-252">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="10032-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10032-253">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="10032-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="10032-254">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="10032-255">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="10032-255">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="10032-256">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="10032-256">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="10032-257">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="10032-257">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="10032-258">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="10032-258">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="10032-259">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="10032-259">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="10032-260">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="10032-260">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="10032-261">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="10032-261">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="10032-262">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="10032-262">Added some scenario test cases.</span></span>
* <span data-ttu-id="10032-263">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="10032-263">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-264">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-264">Az.IotHub</span></span>
* <span data-ttu-id="10032-265">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="10032-265">Breaking changes:</span></span>
    - <span data-ttu-id="10032-266">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="10032-266">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10032-267">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="10032-267">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10032-268">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="10032-268">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10032-269">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="10032-269">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10032-270">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="10032-270">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="10032-271">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="10032-271">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="10032-272">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="10032-272">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="10032-273">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="10032-273">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="10032-274">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="10032-274">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10032-275">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="10032-275">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="10032-276">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="10032-276">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="10032-277">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="10032-277">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-278">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-278">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-279">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-279">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="10032-280">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-280">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="10032-281">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-281">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="10032-282">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-282">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="10032-283">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-283">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="10032-284">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-284">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="10032-285">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-285">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="10032-286">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-286">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="10032-287">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="10032-287">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-288">Az.Resources</span></span>
* <span data-ttu-id="10032-289">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="10032-289">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-290">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-290">Az.Network</span></span>
* <span data-ttu-id="10032-291">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="10032-291">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="10032-292">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="10032-292">Updated cmdlet:</span></span>
        - <span data-ttu-id="10032-293">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-293">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-294">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-294">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-295">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-295">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-296">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-296">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-297">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-297">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="10032-298">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="10032-298">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="10032-299">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-299">New cmdlet:</span></span>
        - <span data-ttu-id="10032-300">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="10032-300">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="10032-301">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="10032-301">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="10032-302">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-302">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="10032-303">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-303">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="10032-304">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="10032-304">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="10032-305">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="10032-305">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="10032-306">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-306">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="10032-307">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="10032-307">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="10032-308">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-308">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-309">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="10032-309">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="10032-310">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-310">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10032-311">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-311">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10032-312">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-312">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="10032-313">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="10032-313">Set-AzVirtualHub</span></span>
* <span data-ttu-id="10032-314">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="10032-314">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="10032-315">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="10032-315">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10032-316">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="10032-316">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="10032-317">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="10032-317">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="10032-318">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="10032-318">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="10032-319">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="10032-319">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="10032-320">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="10032-320">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="10032-321">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-321">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-322">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="10032-322">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="10032-323">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="10032-323">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10032-324">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="10032-324">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10032-325">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="10032-325">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10032-326">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="10032-326">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10032-327">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="10032-327">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="10032-328">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="10032-328">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="10032-329">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="10032-329">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="10032-330">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-330">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-331">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="10032-331">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="10032-332">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="10032-332">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="10032-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="10032-333">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="10032-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="10032-334">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="10032-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="10032-335">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="10032-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-336">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="10032-337">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="10032-337">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10032-338">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="10032-338">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="10032-339">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="10032-339">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="10032-340">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="10032-340">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="10032-341">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="10032-341">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="10032-342">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="10032-342">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="10032-343">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="10032-343">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="10032-344">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="10032-344">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="10032-345">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="10032-345">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="10032-346">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-346">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="10032-347">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="10032-347">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="10032-348">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-348">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-349">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10032-349">New-AzIpGroup</span></span>
        - <span data-ttu-id="10032-350">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10032-350">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="10032-351">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10032-351">Get-AzIpGroup</span></span>
        - <span data-ttu-id="10032-352">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="10032-352">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-353">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-353">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-354">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="10032-354">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-355">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-355">Az.Sql</span></span>
* <span data-ttu-id="10032-356">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="10032-356">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="10032-357">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="10032-357">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="10032-358">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="10032-358">Removed deprecated aliases:</span></span>
* <span data-ttu-id="10032-359">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="10032-359">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="10032-360">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="10032-360">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="10032-361">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-361">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="10032-362">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="10032-362">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="10032-363">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="10032-363">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="10032-364">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="10032-364">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-365">Az.Storage</span></span>
* <span data-ttu-id="10032-366">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10032-366">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="10032-367">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-367">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="10032-368">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-368">Set-AzStorageAccount</span></span>
* <span data-ttu-id="10032-369">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="10032-369">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="10032-370">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10032-370">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="10032-371">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10032-371">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="10032-372">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="10032-372">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="10032-373">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-373">General</span></span>
* <span data-ttu-id="10032-374">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-374">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10032-375">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-375">Az.Accounts</span></span>
* <span data-ttu-id="10032-376">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="10032-376">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10032-377">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-377">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-378">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="10032-378">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="10032-379">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="10032-379">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-380">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-380">Az.Automation</span></span>
* <span data-ttu-id="10032-381">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="10032-381">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="10032-382">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10032-382">Az.Batch</span></span>
* <span data-ttu-id="10032-383">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="10032-383">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-384">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-384">Az.Compute</span></span>
* <span data-ttu-id="10032-385">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-385">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="10032-386">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="10032-386">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="10032-387">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="10032-387">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="10032-388">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="10032-388">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-389">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-389">Az.DataFactory</span></span>
* <span data-ttu-id="10032-390">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="10032-390">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="10032-391">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="10032-391">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="10032-392">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="10032-392">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-393">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-393">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-394">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="10032-394">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="10032-395">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="10032-395">Az.HealthcareApis</span></span>
* <span data-ttu-id="10032-396">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-396">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="10032-397">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="10032-397">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="10032-398">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="10032-398">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="10032-399">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="10032-399">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-400">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-400">Az.IotHub</span></span>
* <span data-ttu-id="10032-401">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="10032-401">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="10032-402">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="10032-402">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="10032-403">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-403">Az.Monitor</span></span>
* <span data-ttu-id="10032-404">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="10032-404">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="10032-405">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="10032-405">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="10032-406">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="10032-406">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="10032-407">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="10032-407">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-408">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-408">Az.Network</span></span>
* <span data-ttu-id="10032-409">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="10032-409">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="10032-410">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-410">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="10032-411">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-411">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-412">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-412">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="10032-413">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10032-413">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10032-414">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="10032-414">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="10032-415">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-415">Updated cmdlets:</span></span>
        - <span data-ttu-id="10032-416">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-416">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10032-417">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-417">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10032-418">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-418">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="10032-419">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="10032-419">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="10032-420">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="10032-420">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="10032-421">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="10032-421">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="10032-422">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="10032-422">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10032-423">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10032-423">Az.RedisCache</span></span>
* <span data-ttu-id="10032-424">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="10032-424">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-425">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-425">Az.Sql</span></span>
* <span data-ttu-id="10032-426">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="10032-426">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-427">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-427">Az.Storage</span></span>
* <span data-ttu-id="10032-428">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="10032-428">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="10032-429">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="10032-429">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="10032-430">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="10032-430">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="10032-431">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="10032-431">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="10032-432">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-432">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10032-433">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10032-433">Az.StorageSync</span></span>
* <span data-ttu-id="10032-434">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="10032-434">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-435">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-435">Az.Websites</span></span>
* <span data-ttu-id="10032-436">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="10032-436">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="10032-437">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="10032-437">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="10032-438">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-438">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-439">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="10032-439">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="10032-440">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="10032-440">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="10032-441">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="10032-441">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-442">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-442">Az.Automation</span></span>
* <span data-ttu-id="10032-443">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="10032-443">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="10032-444">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="10032-444">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="10032-445">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="10032-445">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-446">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-446">Az.Compute</span></span>
* <span data-ttu-id="10032-447">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="10032-447">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="10032-448">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10032-448">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10032-449">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="10032-449">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="10032-450">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="10032-450">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="10032-451">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="10032-451">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="10032-452">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="10032-452">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="10032-453">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="10032-453">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="10032-454">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="10032-454">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="10032-455">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="10032-455">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-456">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-456">Az.DataFactory</span></span>
* <span data-ttu-id="10032-457">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="10032-457">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="10032-458">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="10032-458">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="10032-459">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10032-459">Az.HDInsight</span></span>
* <span data-ttu-id="10032-460">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="10032-460">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-461">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-461">Az.IotHub</span></span>
* <span data-ttu-id="10032-462">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="10032-462">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="10032-463">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="10032-463">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="10032-464">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="10032-464">New cmdlets are:</span></span>
    - <span data-ttu-id="10032-465">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10032-465">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10032-466">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10032-466">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10032-467">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10032-467">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="10032-468">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10032-468">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-469">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-469">Az.Monitor</span></span>
* <span data-ttu-id="10032-470">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="10032-470">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="10032-471">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="10032-471">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="10032-472">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="10032-472">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="10032-473">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="10032-473">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="10032-474">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="10032-474">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="10032-475">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="10032-475">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="10032-476">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10032-476">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="10032-477">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="10032-477">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="10032-478">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="10032-478">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="10032-479">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="10032-479">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="10032-480">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="10032-480">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="10032-481">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="10032-481">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="10032-482">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="10032-482">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="10032-483">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="10032-483">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="10032-484">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="10032-484">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="10032-485">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="10032-485">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="10032-486">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="10032-486">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="10032-487">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-487">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="10032-488">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="10032-488">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="10032-489">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-489">Overall improved help files</span></span>
* <span data-ttu-id="10032-490">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="10032-490">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-491">Az.Network</span></span>
* <span data-ttu-id="10032-492">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="10032-492">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="10032-493">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="10032-493">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="10032-494">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="10032-494">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="10032-495">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="10032-495">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="10032-496">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="10032-496">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="10032-497">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="10032-497">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="10032-498">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="10032-498">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="10032-499">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="10032-499">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="10032-500">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-500">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="10032-501">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="10032-501">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="10032-502">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-502">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="10032-503">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-503">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="10032-504">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-504">New cmdlets</span></span>
        - <span data-ttu-id="10032-505">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="10032-505">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="10032-506">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="10032-506">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="10032-507">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="10032-507">Updated cmdlet:</span></span>
        - <span data-ttu-id="10032-508">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="10032-508">New-VpnSite</span></span>
        - <span data-ttu-id="10032-509">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="10032-509">Update-VpnSite</span></span>
        - <span data-ttu-id="10032-510">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10032-510">New-VpnConnection</span></span>
        - <span data-ttu-id="10032-511">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10032-511">Update-VpnConnection</span></span>
* <span data-ttu-id="10032-512">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="10032-512">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-513">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-513">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-514">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="10032-514">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="10032-515">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="10032-515">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-516">Az.Resources</span></span>
* <span data-ttu-id="10032-517">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="10032-517">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-518">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-518">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-519">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="10032-519">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="10032-520">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="10032-520">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="10032-521">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10032-521">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10032-522">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10032-522">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10032-523">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10032-523">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10032-524">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="10032-524">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="10032-525">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10032-525">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10032-526">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10032-526">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10032-527">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10032-527">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10032-528">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10032-528">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10032-529">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="10032-529">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="10032-530">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="10032-530">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="10032-531">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="10032-531">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="10032-532">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="10032-532">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="10032-533">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="10032-533">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="10032-534">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="10032-534">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10032-535">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10032-535">Az.SignalR</span></span>
* <span data-ttu-id="10032-536">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="10032-536">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-537">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-537">Az.Sql</span></span>
* <span data-ttu-id="10032-538">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="10032-538">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="10032-539">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="10032-539">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="10032-540">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-540">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="10032-541">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="10032-541">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="10032-542">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="10032-542">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-543">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-543">Az.Storage</span></span>
* <span data-ttu-id="10032-544">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="10032-544">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="10032-545">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="10032-545">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="10032-546">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10032-546">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="10032-547">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10032-547">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="10032-548">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="10032-548">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="10032-549">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10032-549">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="10032-550">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="10032-550">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="10032-551">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10032-551">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10032-552">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10032-552">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10032-553">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10032-553">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="10032-554">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="10032-554">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-555">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-555">Az.Websites</span></span>
* <span data-ttu-id="10032-556">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="10032-556">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="10032-557">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="10032-557">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="10032-558">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="10032-558">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="10032-559">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="10032-559">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="10032-560">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-560">General</span></span>
* <span data-ttu-id="10032-561">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="10032-561">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10032-562">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-562">Az.Accounts</span></span>
* <span data-ttu-id="10032-563">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="10032-563">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="10032-564">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10032-564">Az.Aks</span></span>
* <span data-ttu-id="10032-565">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="10032-565">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="10032-566">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="10032-566">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10032-567">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-567">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-568">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="10032-568">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="10032-569">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="10032-569">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="10032-570">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="10032-570">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="10032-571">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="10032-571">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="10032-572">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="10032-572">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10032-573">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10032-573">Az.Batch</span></span>
* <span data-ttu-id="10032-574">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="10032-574">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10032-575">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-575">Az.Cdn</span></span>
* <span data-ttu-id="10032-576">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="10032-576">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-577">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-577">Az.Compute</span></span>
* <span data-ttu-id="10032-578">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="10032-578">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="10032-579">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-579">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="10032-580">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-580">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="10032-581">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="10032-581">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="10032-582">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="10032-582">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="10032-583">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10032-583">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="10032-584">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="10032-584">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="10032-585">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="10032-585">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-586">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-586">Az.DataFactory</span></span>
* <span data-ttu-id="10032-587">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="10032-587">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="10032-588">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="10032-588">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="10032-589">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="10032-589">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="10032-590">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="10032-590">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-591">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-591">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-592">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="10032-592">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-593">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-593">Az.EventHub</span></span>
* <span data-ttu-id="10032-594">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-594">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="10032-595">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="10032-595">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="10032-596">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="10032-596">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="10032-597">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="10032-597">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="10032-598">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10032-598">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10032-599">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="10032-599">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-600">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-600">Az.Monitor</span></span>
* <span data-ttu-id="10032-601">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-601">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-602">Az.Network</span></span>
* <span data-ttu-id="10032-603">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-603">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="10032-604">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="10032-604">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="10032-605">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="10032-605">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="10032-606">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="10032-606">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="10032-607">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="10032-607">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="10032-608">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="10032-608">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="10032-609">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="10032-609">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-610">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-610">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-611">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="10032-611">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="10032-612">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="10032-612">Added example</span></span>
    - <span data-ttu-id="10032-613">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="10032-613">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="10032-614">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10032-614">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="10032-615">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="10032-615">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-616">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-616">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-617">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="10032-617">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-618">Az.Resources</span></span>
* <span data-ttu-id="10032-619">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="10032-619">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="10032-620">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="10032-620">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="10032-621">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="10032-621">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="10032-622">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-622">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-623">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-623">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-624">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-624">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="10032-625">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="10032-625">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="10032-626">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="10032-626">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="10032-627">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-627">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-628">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="10032-628">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="10032-629">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="10032-629">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="10032-630">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="10032-630">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="10032-631">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="10032-631">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="10032-632">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="10032-632">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="10032-633">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="10032-633">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-634">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-634">Az.Sql</span></span>
* <span data-ttu-id="10032-635">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="10032-635">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-636">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-636">Az.Storage</span></span>
* <span data-ttu-id="10032-637">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="10032-637">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="10032-638">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="10032-638">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="10032-639">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10032-639">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="10032-640">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10032-640">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="10032-641">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="10032-641">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="10032-642">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10032-642">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-643">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-643">Az.Websites</span></span>
* <span data-ttu-id="10032-644">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10032-644">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="10032-645">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-645">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-646">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-646">Az.Accounts</span></span>
* <span data-ttu-id="10032-647">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10032-647">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="10032-648">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="10032-648">Az.ApplicationInsights</span></span>
* <span data-ttu-id="10032-649">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="10032-649">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="10032-650">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-650">Az.Automation</span></span>
* <span data-ttu-id="10032-651">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="10032-651">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-652">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-653">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="10032-653">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-654">Az.Compute</span></span>
* <span data-ttu-id="10032-655">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="10032-655">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10032-656">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10032-656">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10032-657">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="10032-657">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="10032-658">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="10032-658">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-659">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-659">Az.DataFactory</span></span>
* <span data-ttu-id="10032-660">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="10032-660">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="10032-661">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="10032-661">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-662">Az.EventHub</span></span>
* <span data-ttu-id="10032-663">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10032-663">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10032-664">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="10032-664">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10032-665">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-665">Az.KeyVault</span></span>
* <span data-ttu-id="10032-666">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="10032-666">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10032-667">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10032-667">Az.LogicApp</span></span>
* <span data-ttu-id="10032-668">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="10032-668">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="10032-669">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="10032-669">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="10032-670">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="10032-670">Az.ManagedServices</span></span>
* <span data-ttu-id="10032-671">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="10032-671">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-672">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-672">Az.Network</span></span>
* <span data-ttu-id="10032-673">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="10032-673">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="10032-674">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-674">New cmdlets</span></span>
        - <span data-ttu-id="10032-675">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10032-675">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10032-676">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-676">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10032-677">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-677">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-678">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-678">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-679">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-679">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-680">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-680">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="10032-681">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="10032-681">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="10032-682">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-682">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="10032-683">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="10032-683">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="10032-684">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="10032-684">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="10032-685">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="10032-685">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="10032-686">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="10032-686">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="10032-687">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="10032-687">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="10032-688">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="10032-688">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="10032-689">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-689">Updated cmdlets</span></span>
        - <span data-ttu-id="10032-690">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-690">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10032-691">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-691">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="10032-692">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-692">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="10032-693">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="10032-693">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="10032-694">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-694">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="10032-695">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="10032-695">Updated cmdlet:</span></span>
        - <span data-ttu-id="10032-696">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-696">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10032-697">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-697">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="10032-698">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-698">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="10032-699">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="10032-699">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="10032-700">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="10032-700">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="10032-701">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="10032-701">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-702">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-702">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-703">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="10032-703">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="10032-704">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="10032-704">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-705">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-705">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-706">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="10032-706">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10032-707">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="10032-707">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="10032-708">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="10032-708">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="10032-709">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="10032-709">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="10032-710">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="10032-710">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="10032-711">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="10032-711">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10032-712">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="10032-712">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="10032-713">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="10032-713">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="10032-714">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-714">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="10032-715">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="10032-715">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-716">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-716">Az.Resources</span></span>
- <span data-ttu-id="10032-717">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="10032-717">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="10032-718">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10032-718">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-719">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-719">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-720">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="10032-720">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="10032-721">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="10032-721">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-722">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-722">Az.Sql</span></span>
* <span data-ttu-id="10032-723">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="10032-723">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="10032-724">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="10032-724">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="10032-725">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="10032-725">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-726">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-726">Az.Storage</span></span>
* <span data-ttu-id="10032-727">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="10032-727">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10032-728">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10032-728">Az.StorageSync</span></span>
* <span data-ttu-id="10032-729">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="10032-729">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="10032-730">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="10032-730">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-731">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-731">Az.Websites</span></span>
* <span data-ttu-id="10032-732">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10032-732">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="10032-733">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="10032-733">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="10032-734">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="10032-734">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="10032-735">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-735">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-736">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-736">Az.Accounts</span></span>
* <span data-ttu-id="10032-737">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="10032-737">Add support for profile cmdlets</span></span>
* <span data-ttu-id="10032-738">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="10032-738">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="10032-739">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="10032-739">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="10032-740">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10032-740">Az.Advisor</span></span>
* <span data-ttu-id="10032-741">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="10032-741">GA release of Az.Advisor</span></span>
* <span data-ttu-id="10032-742">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="10032-742">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="10032-743">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-743">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-744">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="10032-744">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="10032-745">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10032-745">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="10032-746">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="10032-746">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="10032-747">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="10032-747">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="10032-748">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="10032-748">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="10032-749">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10032-749">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="10032-750">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="10032-750">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-751">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-751">Az.Automation</span></span>
* <span data-ttu-id="10032-752">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="10032-752">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-753">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-753">Az.Compute</span></span>
* <span data-ttu-id="10032-754">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="10032-754">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-755">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-755">Az.DataFactory</span></span>
* <span data-ttu-id="10032-756">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="10032-756">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10032-757">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10032-757">Az.EventGrid</span></span>
* <span data-ttu-id="10032-758">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="10032-758">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-759">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-759">Az.IotHub</span></span>
* <span data-ttu-id="10032-760">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="10032-760">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-761">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-761">Az.Network</span></span>
* <span data-ttu-id="10032-762">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="10032-762">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="10032-763">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="10032-763">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10032-764">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10032-764">Az.PolicyInsights</span></span>
* <span data-ttu-id="10032-765">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="10032-765">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="10032-766">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="10032-766">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-767">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-768">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="10032-768">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-769">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-769">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-770">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="10032-770">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-771">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-771">Az.Resources</span></span>
    - <span data-ttu-id="10032-772">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="10032-772">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="10032-773">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="10032-773">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="10032-774">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="10032-774">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="10032-775">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="10032-775">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-776">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-776">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-777">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="10032-777">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-778">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-778">Az.Sql</span></span>
* <span data-ttu-id="10032-779">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="10032-779">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="10032-780">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-780">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="10032-781">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10032-781">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10032-782">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10032-782">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10032-783">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="10032-783">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="10032-784">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10032-784">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10032-785">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10032-785">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="10032-786">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="10032-786">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="10032-787">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="10032-787">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-788">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-788">Az.Storage</span></span>
* <span data-ttu-id="10032-789">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-789">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="10032-790">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10032-790">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="10032-791">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="10032-791">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="10032-792">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="10032-792">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="10032-793">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-793">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="10032-794">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-794">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="10032-795">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-795">Set-AzStorageAccount</span></span>
* <span data-ttu-id="10032-796">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="10032-796">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="10032-797">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10032-797">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="10032-798">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="10032-798">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="10032-799">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="10032-799">Az.StorageSync</span></span>
* <span data-ttu-id="10032-800">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="10032-800">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="10032-801">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="10032-801">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-802">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-802">Az.Accounts</span></span>
* <span data-ttu-id="10032-803">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="10032-803">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="10032-804">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="10032-804">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="10032-805">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="10032-805">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="10032-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="10032-806">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="10032-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="10032-807">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-808">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-808">Az.Compute</span></span>
* <span data-ttu-id="10032-809">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="10032-809">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="10032-810">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="10032-810">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="10032-811">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10032-811">Az.Dns</span></span>
* <span data-ttu-id="10032-812">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="10032-812">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10032-813">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10032-813">Az.EventGrid</span></span>
* <span data-ttu-id="10032-814">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="10032-814">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="10032-815">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-815">New cmdlets:</span></span>
    - <span data-ttu-id="10032-816">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10032-816">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10032-817">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-817">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10032-818">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10032-818">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10032-819">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-819">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="10032-820">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="10032-820">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="10032-821">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-821">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10032-822">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10032-822">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10032-823">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-823">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="10032-824">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="10032-824">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="10032-825">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="10032-825">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="10032-826">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="10032-826">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10032-827">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-827">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="10032-828">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="10032-828">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="10032-829">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-829">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="10032-830">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="10032-830">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="10032-831">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="10032-831">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="10032-832">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-832">Updated cmdlets:</span></span>
    - <span data-ttu-id="10032-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="10032-833">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="10032-834">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="10032-834">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10032-835">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="10032-835">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="10032-836">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="10032-836">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="10032-837">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="10032-837">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="10032-838">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="10032-838">Event subscription expiration date,</span></span>
            - <span data-ttu-id="10032-839">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="10032-839">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="10032-840">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="10032-840">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="10032-841">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="10032-841">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="10032-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="10032-842">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="10032-843">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="10032-843">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="10032-844">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="10032-844">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="10032-845">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="10032-845">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="10032-846">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="10032-846">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10032-847">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10032-847">Az.FrontDoor</span></span>
* <span data-ttu-id="10032-848">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="10032-848">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="10032-849">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="10032-849">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="10032-850">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="10032-850">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="10032-851">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="10032-851">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-852">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-852">Az.Network</span></span>
* <span data-ttu-id="10032-853">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-853">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="10032-854">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-854">New cmdlets</span></span>
        - <span data-ttu-id="10032-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="10032-855">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="10032-856">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10032-856">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="10032-857">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-857">New cmdlets</span></span> 
        - <span data-ttu-id="10032-858">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="10032-858">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="10032-859">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-859">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="10032-860">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-860">New cmdlets</span></span> 
        - <span data-ttu-id="10032-861">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-861">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="10032-862">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-862">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10032-863">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="10032-863">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="10032-864">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-864">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="10032-865">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="10032-865">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="10032-866">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10032-866">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="10032-867">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-867">New cmdlets</span></span>
        - <span data-ttu-id="10032-868">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10032-868">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10032-869">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10032-869">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10032-870">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="10032-870">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="10032-871">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="10032-871">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="10032-872">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="10032-872">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="10032-873">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="10032-873">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="10032-874">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="10032-874">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="10032-875">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10032-875">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="10032-876">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="10032-876">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="10032-877">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="10032-877">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="10032-878">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-878">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="10032-879">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="10032-879">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="10032-880">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-880">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="10032-881">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="10032-881">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="10032-882">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="10032-882">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="10032-883">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="10032-883">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="10032-884">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="10032-884">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="10032-885">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-885">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="10032-886">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="10032-886">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="10032-887">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="10032-887">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="10032-888">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-888">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="10032-889">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="10032-889">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="10032-890">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="10032-890">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="10032-891">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="10032-891">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="10032-892">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-892">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10032-893">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-893">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="10032-894">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-894">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-895">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-895">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-896">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="10032-896">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-897">Az.Resources</span></span>
* <span data-ttu-id="10032-898">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="10032-898">Support for additional Template Export options</span></span>
    - <span data-ttu-id="10032-899">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10032-899">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10032-900">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10032-900">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="10032-901">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="10032-901">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-902">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-902">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-903">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="10032-903">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-904">Az.Sql</span></span>
* <span data-ttu-id="10032-905">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="10032-905">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="10032-906">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="10032-906">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="10032-907">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="10032-907">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="10032-908">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10032-908">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10032-909">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10032-909">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10032-910">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="10032-910">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="10032-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10032-911">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="10032-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="10032-912">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-913">Az.Storage</span></span>
* <span data-ttu-id="10032-914">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10032-914">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="10032-915">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-915">New-AzStorageAccount</span></span>
* <span data-ttu-id="10032-916">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="10032-916">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="10032-917">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-917">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-918">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-918">Az.Websites</span></span>
* <span data-ttu-id="10032-919">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="10032-919">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="10032-920">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="10032-920">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="10032-921">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="10032-921">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="10032-922">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-922">Az.Cdn</span></span>
* <span data-ttu-id="10032-923">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="10032-923">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-924">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-924">Az.Compute</span></span>
* <span data-ttu-id="10032-925">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="10032-925">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="10032-926">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="10032-926">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-927">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-927">Az.EventHub</span></span>
* <span data-ttu-id="10032-928">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="10032-928">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="10032-929">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10032-929">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-930">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-930">Az.Network</span></span>
* <span data-ttu-id="10032-931">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="10032-931">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="10032-932">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="10032-932">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10032-933">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10032-933">Az.PolicyInsights</span></span>
* <span data-ttu-id="10032-934">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="10032-934">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-935">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-935">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-936">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="10032-936">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-937">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-937">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-938">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10032-938">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-939">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-939">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-940">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="10032-940">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="10032-941">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="10032-941">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-942">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-942">Az.Sql</span></span>
* <span data-ttu-id="10032-943">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="10032-943">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="10032-944">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-944">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="10032-945">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="10032-945">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="10032-946">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="10032-946">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-947">Az.Websites</span></span>
* <span data-ttu-id="10032-948">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="10032-948">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="10032-949">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-949">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="10032-950">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-950">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-951">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="10032-951">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="10032-952">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="10032-952">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="10032-953">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="10032-953">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="10032-954">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="10032-954">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="10032-955">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-955">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="10032-956">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="10032-956">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="10032-957">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="10032-957">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="10032-958">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="10032-958">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="10032-959">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-959">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="10032-960">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="10032-960">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="10032-961">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-961">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="10032-962">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="10032-962">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="10032-963">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="10032-963">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="10032-964">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="10032-964">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="10032-965">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="10032-965">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="10032-966">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="10032-966">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="10032-967">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="10032-967">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="10032-968">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="10032-968">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="10032-969">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="10032-969">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="10032-970">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="10032-970">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="10032-971">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="10032-971">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="10032-972">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="10032-972">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="10032-973">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="10032-973">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="10032-974">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-974">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="10032-975">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="10032-975">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="10032-976">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="10032-976">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="10032-977">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="10032-977">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="10032-978">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="10032-978">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="10032-979">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="10032-979">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="10032-980">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="10032-980">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="10032-981">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="10032-981">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="10032-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="10032-982">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="10032-983">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="10032-983">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="10032-984">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10032-984">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10032-985">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="10032-985">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="10032-986">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="10032-986">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="10032-987">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="10032-987">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="10032-988">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="10032-988">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="10032-989">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="10032-989">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="10032-990">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10032-990">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="10032-991">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="10032-991">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10032-992">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10032-992">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="10032-993">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="10032-993">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="10032-994">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="10032-994">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10032-995">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="10032-995">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="10032-996">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="10032-996">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="10032-997">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10032-997">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="10032-998">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="10032-998">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="10032-999">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="10032-999">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="10032-1000">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="10032-1000">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="10032-1001">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="10032-1001">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="10032-1002">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="10032-1002">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="10032-1003">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="10032-1003">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="10032-1004">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="10032-1004">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="10032-1005">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="10032-1005">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="10032-1006">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="10032-1006">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="10032-1007">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10032-1007">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10032-1008">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10032-1008">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10032-1009">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10032-1009">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10032-1010">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="10032-1010">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10032-1011">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="10032-1011">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="10032-1012">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10032-1012">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="10032-1013">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="10032-1013">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="10032-1014">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="10032-1014">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="10032-1015">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="10032-1015">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="10032-1016">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="10032-1016">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="10032-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="10032-1017">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="10032-1018">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="10032-1018">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="10032-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="10032-1019">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="10032-1020">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10032-1020">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="10032-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="10032-1021">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="10032-1022">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="10032-1022">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="10032-1023">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="10032-1023">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="10032-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="10032-1024">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="10032-1025">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="10032-1025">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="10032-1026">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="10032-1026">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="10032-1027">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="10032-1027">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1028">Az.Automation</span></span>
* <span data-ttu-id="10032-1029">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="10032-1029">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="10032-1030">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="10032-1030">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="10032-1031">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="10032-1031">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="10032-1032">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="10032-1032">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="10032-1033">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="10032-1033">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="10032-1034">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="10032-1034">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="10032-1035">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="10032-1035">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1036">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1036">Az.Compute</span></span>
* <span data-ttu-id="10032-1037">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="10032-1037">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="10032-1038">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="10032-1038">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1039">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1039">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1040">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1040">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-1041">Az.Monitor</span></span>
* <span data-ttu-id="10032-1042">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-1042">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1043">Az.Network</span></span>
* <span data-ttu-id="10032-1044">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="10032-1044">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="10032-1045">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="10032-1045">Updated cmdlet:</span></span>
        - <span data-ttu-id="10032-1046">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-1046">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="10032-1047">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="10032-1047">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1048">Az.Resources</span></span>
* <span data-ttu-id="10032-1049">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="10032-1049">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1050">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1050">Az.Sql</span></span>
* <span data-ttu-id="10032-1051">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="10032-1051">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="10032-1052">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1052">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1053">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1053">Az.Accounts</span></span>
* <span data-ttu-id="10032-1054">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="10032-1054">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-1055">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-1055">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-1056">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="10032-1056">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="10032-1057">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="10032-1057">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1058">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1058">Az.Compute</span></span>
* <span data-ttu-id="10032-1059">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="10032-1059">Proximity placement group feature.</span></span>
    - <span data-ttu-id="10032-1060">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="10032-1060">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="10032-1061">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1061">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="10032-1062">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="10032-1062">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="10032-1063">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="10032-1063">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="10032-1064">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-1064">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="10032-1065">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="10032-1065">Breaking changes</span></span>
    - <span data-ttu-id="10032-1066">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="10032-1066">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="10032-1067">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="10032-1067">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="10032-1068">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="10032-1068">Az.DeploymentManager</span></span>
* <span data-ttu-id="10032-1069">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="10032-1069">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="10032-1070">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="10032-1070">Az.Dns</span></span>
* <span data-ttu-id="10032-1071">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="10032-1071">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="10032-1072">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="10032-1072">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="10032-1073">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="10032-1073">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="10032-1074">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10032-1074">Az.FrontDoor</span></span>
* <span data-ttu-id="10032-1075">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1075">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="10032-1076">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="10032-1076">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="10032-1077">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10032-1077">Az.HDInsight</span></span>
* <span data-ttu-id="10032-1078">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-1078">Removed two cmdlets:</span></span>
    - <span data-ttu-id="10032-1079">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10032-1079">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="10032-1080">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10032-1080">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10032-1081">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="10032-1081">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="10032-1082">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="10032-1082">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="10032-1083">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="10032-1083">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="10032-1084">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="10032-1084">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-1085">Az.Monitor</span></span>
* <span data-ttu-id="10032-1086">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="10032-1086">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="10032-1087">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="10032-1087">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="10032-1088">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="10032-1088">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="10032-1089">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="10032-1089">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="10032-1090">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="10032-1090">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="10032-1091">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="10032-1091">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="10032-1092">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="10032-1092">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="10032-1093">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10032-1093">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10032-1094">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10032-1094">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10032-1095">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10032-1095">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10032-1096">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10032-1096">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10032-1097">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="10032-1097">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="10032-1098">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="10032-1098">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="10032-1099">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="10032-1099">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1100">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1100">Az.Network</span></span>
* <span data-ttu-id="10032-1101">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="10032-1101">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="10032-1102">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-1102">New cmdlets</span></span>
        - <span data-ttu-id="10032-1103">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10032-1103">New-AzNatGateway</span></span>
        - <span data-ttu-id="10032-1104">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10032-1104">Get-AzNatGateway</span></span>
        - <span data-ttu-id="10032-1105">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10032-1105">Set-AzNatGateway</span></span>
        - <span data-ttu-id="10032-1106">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="10032-1106">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="10032-1107">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="10032-1107">Updated cmdlets</span></span>
        - <span data-ttu-id="10032-1108">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10032-1108">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="10032-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="10032-1109">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="10032-1110">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-1110">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="10032-1111">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-1111">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="10032-1112">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="10032-1112">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10032-1113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10032-1113">Az.PolicyInsights</span></span>
* <span data-ttu-id="10032-1114">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="10032-1114">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="10032-1115">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="10032-1115">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="10032-1116">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="10032-1116">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1117">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1117">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-1118">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="10032-1118">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="10032-1119">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10032-1119">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="10032-1120">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="10032-1120">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="10032-1121">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-1121">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="10032-1122">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="10032-1122">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="10032-1123">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="10032-1123">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="10032-1124">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10032-1124">Az.Relay</span></span>
* <span data-ttu-id="10032-1125">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="10032-1125">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-1126">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-1126">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-1127">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10032-1127">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1128">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1128">Az.Storage</span></span>
* <span data-ttu-id="10032-1129">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="10032-1129">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="10032-1130">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="10032-1130">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="10032-1131">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="10032-1131">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="10032-1132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1132">New-AzStorageAccount</span></span>
* <span data-ttu-id="10032-1133">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="10032-1133">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="10032-1134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1134">New-AzStorageAccount</span></span>
    - <span data-ttu-id="10032-1135">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1135">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="10032-1136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1136">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1137">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1137">Az.Websites</span></span>
* <span data-ttu-id="10032-1138">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="10032-1138">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="10032-1139">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="10032-1139">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="10032-1140">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1140">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10032-1141">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="10032-1141">Highlights since the last major release</span></span>
* <span data-ttu-id="10032-1142">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10032-1142">General availability of `Az` module</span></span>
* <span data-ttu-id="10032-1143">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10032-1143">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10032-1144">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10032-1144">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10032-1145">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1145">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10032-1146">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10032-1146">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10032-1147">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1147">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10032-1148">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="10032-1148">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10032-1149">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1149">Az.Accounts</span></span>
* <span data-ttu-id="10032-1150">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="10032-1150">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="10032-1151">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10032-1151">Az.Batch</span></span>
* <span data-ttu-id="10032-1152">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1152">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10032-1153">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-1153">Az.Cdn</span></span>
* <span data-ttu-id="10032-1154">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1154">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-1155">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-1155">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-1156">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1156">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1157">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1157">Az.Compute</span></span>
* <span data-ttu-id="10032-1158">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="10032-1158">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="10032-1159">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1159">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1160">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="10032-1160">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-1161">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-1161">Az.DataFactory</span></span>
* <span data-ttu-id="10032-1162">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="10032-1162">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1163">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1163">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1164">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1164">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10032-1165">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10032-1165">Az.EventGrid</span></span>
* <span data-ttu-id="10032-1166">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="10032-1166">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-1167">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-1167">Az.EventHub</span></span>
* <span data-ttu-id="10032-1168">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="10032-1168">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="10032-1169">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="10032-1169">Az.HDInsight</span></span>
* <span data-ttu-id="10032-1170">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1170">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-1171">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-1171">Az.IotHub</span></span>
* <span data-ttu-id="10032-1172">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1172">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10032-1173">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1173">Az.KeyVault</span></span>
* <span data-ttu-id="10032-1174">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1174">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1175">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="10032-1175">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="10032-1176">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10032-1176">Az.MachineLearning</span></span>
* <span data-ttu-id="10032-1177">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1177">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="10032-1178">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10032-1178">Az.Media</span></span>
* <span data-ttu-id="10032-1179">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1179">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-1180">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-1180">Az.Monitor</span></span>
  * <span data-ttu-id="10032-1181">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="10032-1181">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="10032-1182">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="10032-1182">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="10032-1183">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="10032-1183">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="10032-1184">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10032-1184">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10032-1185">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10032-1185">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="10032-1186">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="10032-1186">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="10032-1187">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="10032-1187">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1188">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1188">Az.Network</span></span>
* <span data-ttu-id="10032-1189">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1189">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1190">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="10032-1190">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="10032-1191">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="10032-1191">Az.NotificationHubs</span></span>
* <span data-ttu-id="10032-1192">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1192">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-1193">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-1193">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-1194">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1194">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="10032-1195">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="10032-1195">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="10032-1196">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1197">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1197">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-1198">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1199">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1199">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="10032-1200">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="10032-1200">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="10032-1201">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="10032-1201">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10032-1202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10032-1202">Az.RedisCache</span></span>
* <span data-ttu-id="10032-1203">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1204">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1204">Az.Resources</span></span>
* <span data-ttu-id="10032-1205">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="10032-1205">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1206">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1206">Az.Sql</span></span>
* <span data-ttu-id="10032-1207">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="10032-1207">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="10032-1208">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1209">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="10032-1209">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="10032-1210">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="10032-1210">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="10032-1211">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="10032-1211">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="10032-1212">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="10032-1212">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="10032-1213">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="10032-1213">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1214">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1214">Az.Websites</span></span>
* <span data-ttu-id="10032-1215">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="10032-1215">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="10032-1216">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="10032-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="10032-1217">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="10032-1217">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="10032-1218">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="10032-1218">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="10032-1219">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1219">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10032-1220">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="10032-1220">Highlights since the last major release</span></span>
* <span data-ttu-id="10032-1221">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10032-1221">General availability of `Az` module</span></span>
* <span data-ttu-id="10032-1222">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10032-1222">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10032-1223">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10032-1223">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10032-1224">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1224">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10032-1225">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10032-1225">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10032-1226">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1226">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10032-1227">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="10032-1227">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="10032-1228">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1228">Az.Accounts</span></span>
* <span data-ttu-id="10032-1229">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="10032-1229">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10032-1230">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10032-1230">Az.AnalysisServices</span></span>
* <span data-ttu-id="10032-1231">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="10032-1231">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="10032-1232">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="10032-1232">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1233">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1233">Az.Automation</span></span>
* <span data-ttu-id="10032-1234">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="10032-1234">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="10032-1235">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="10032-1235">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="10032-1236">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1236">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1237">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1237">Az.Compute</span></span>
* <span data-ttu-id="10032-1238">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1238">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="10032-1239">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="10032-1239">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="10032-1240">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1240">Az.ContainerInstance</span></span>
* <span data-ttu-id="10032-1241">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="10032-1241">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-1242">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-1242">Az.DataFactory</span></span>
* <span data-ttu-id="10032-1243">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="10032-1243">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="10032-1244">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="10032-1244">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1245">Az.Resources</span></span>
* <span data-ttu-id="10032-1246">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="10032-1246">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="10032-1247">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="10032-1247">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="10032-1248">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="10032-1248">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="10032-1249">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10032-1249">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="10032-1250">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="10032-1250">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="10032-1251">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="10032-1251">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1252">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1252">Az.Sql</span></span>
* <span data-ttu-id="10032-1253">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="10032-1253">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1254">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1254">Az.Storage</span></span>
* <span data-ttu-id="10032-1255">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="10032-1255">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="10032-1256">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10032-1256">New-AzStorageContext</span></span>
* <span data-ttu-id="10032-1257">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="10032-1257">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="10032-1258">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10032-1258">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10032-1259">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="10032-1259">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="10032-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1260">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="10032-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1261">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="10032-1262">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="10032-1262">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="10032-1263">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10032-1263">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10032-1264">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="10032-1264">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="10032-1265">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10032-1265">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="10032-1266">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="10032-1266">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="10032-1267">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1267">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="10032-1268">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="10032-1268">Highlights since the last major release</span></span>
* <span data-ttu-id="10032-1269">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="10032-1269">General availability of `Az` module</span></span>
* <span data-ttu-id="10032-1270">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="10032-1270">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="10032-1271">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="10032-1271">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="10032-1272">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1272">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="10032-1273">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10032-1273">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10032-1274">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1274">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="10032-1275">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="10032-1275">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1276">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1276">Az.Automation</span></span>
* <span data-ttu-id="10032-1277">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="10032-1277">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="10032-1278">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="10032-1278">Dynamic grouping</span></span>
    * <span data-ttu-id="10032-1279">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="10032-1279">Pre-Post script</span></span>
    * <span data-ttu-id="10032-1280">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="10032-1280">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1281">Az.Compute</span></span>
* <span data-ttu-id="10032-1282">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="10032-1282">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="10032-1283">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="10032-1283">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10032-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1284">Az.KeyVault</span></span>
* <span data-ttu-id="10032-1285">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1285">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1286">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1286">Az.Network</span></span>
* <span data-ttu-id="10032-1287">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1287">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="10032-1288">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="10032-1288">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1289">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1289">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-1290">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="10032-1290">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="10032-1291">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="10032-1291">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1292">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1292">Az.Resources</span></span>
* <span data-ttu-id="10032-1293">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="10032-1293">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="10032-1294">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="10032-1294">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1295">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1295">Az.Sql</span></span>
* <span data-ttu-id="10032-1296">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="10032-1296">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1297">Az.Storage</span></span>
* <span data-ttu-id="10032-1298">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10032-1298">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="10032-1299">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1299">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10032-1300">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1300">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10032-1301">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1301">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="10032-1302">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="10032-1302">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="10032-1303">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="10032-1303">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="10032-1304">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="10032-1304">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1305">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1305">Az.Websites</span></span>
* <span data-ttu-id="10032-1306">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="10032-1306">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="10032-1307">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1307">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1308">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1308">Az.Accounts</span></span>
* <span data-ttu-id="10032-1309">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="10032-1309">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="10032-1310">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1310">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1311">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1311">Az.Automation</span></span>
* <span data-ttu-id="10032-1312">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1312">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="10032-1313">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="10032-1313">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="10032-1314">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="10032-1314">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10032-1315">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-1315">Az.Cdn</span></span>
* <span data-ttu-id="10032-1316">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="10032-1316">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1317">Az.Compute</span></span>
* <span data-ttu-id="10032-1318">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="10032-1318">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-1319">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-1319">Az.DataFactory</span></span>
* <span data-ttu-id="10032-1320">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="10032-1320">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10032-1321">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10032-1321">Az.LogicApp</span></span>
* <span data-ttu-id="10032-1322">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="10032-1322">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1323">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1323">Az.Network</span></span>
* <span data-ttu-id="10032-1324">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="10032-1324">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1325">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1325">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-1326">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1326">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="10032-1327">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="10032-1327">SDK Update</span></span>
* <span data-ttu-id="10032-1328">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10032-1328">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="10032-1329">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10032-1329">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1330">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1330">Az.Resources</span></span>
* <span data-ttu-id="10032-1331">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="10032-1331">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="10032-1332">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="10032-1332">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="10032-1333">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="10032-1333">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="10032-1334">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="10032-1334">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="10032-1335">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="10032-1335">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="10032-1336">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="10032-1336">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1337">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1337">Az.Sql</span></span>
* <span data-ttu-id="10032-1338">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="10032-1338">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="10032-1339">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="10032-1339">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1340">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1340">Az.Storage</span></span>
* <span data-ttu-id="10032-1341">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1341">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="10032-1342">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1342">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="10032-1343">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10032-1343">Az.AnalysisServices</span></span>
* <span data-ttu-id="10032-1344">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="10032-1344">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1345">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1345">Az.Automation</span></span>
* <span data-ttu-id="10032-1346">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1346">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="10032-1347">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1347">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="10032-1348">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1348">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-1349">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-1349">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-1350">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="10032-1350">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1351">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1351">Az.Compute</span></span>
* <span data-ttu-id="10032-1352">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="10032-1352">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="10032-1353">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="10032-1353">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="10032-1354">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10032-1354">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="10032-1355">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="10032-1355">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1356">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1356">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1357">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="10032-1357">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="10032-1358">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="10032-1358">Az.EventHub</span></span>
* <span data-ttu-id="10032-1359">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="10032-1359">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="10032-1360">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1360">Az.KeyVault</span></span>
* <span data-ttu-id="10032-1361">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="10032-1361">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10032-1362">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10032-1362">Az.LogicApp</span></span>
* <span data-ttu-id="10032-1363">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="10032-1363">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="10032-1364">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="10032-1364">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="10032-1365">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="10032-1365">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="10032-1366">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10032-1366">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10032-1367">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10032-1367">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10032-1368">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10032-1368">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="10032-1369">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="10032-1369">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="10032-1370">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="10032-1370">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="10032-1371">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1371">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10032-1372">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1372">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10032-1373">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1373">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="10032-1374">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1374">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="10032-1375">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="10032-1375">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="10032-1376">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-1376">Az.Monitor</span></span>
* <span data-ttu-id="10032-1377">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="10032-1377">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1378">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1378">Az.Network</span></span>
* <span data-ttu-id="10032-1379">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="10032-1379">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="10032-1380">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-1380">Az.OperationalInsights</span></span>
* <span data-ttu-id="10032-1381">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="10032-1381">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="10032-1382">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="10032-1382">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="10032-1383">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="10032-1383">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="10032-1384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1384">Az.Resources</span></span>
* <span data-ttu-id="10032-1385">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10032-1385">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10032-1386">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10032-1386">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="10032-1387">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="10032-1387">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="10032-1388">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="10032-1388">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1389">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1389">Az.Sql</span></span>
* <span data-ttu-id="10032-1390">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="10032-1390">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="10032-1391">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="10032-1391">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1392">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1392">Az.Websites</span></span>
* <span data-ttu-id="10032-1393">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="10032-1393">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="10032-1394">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1394">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1395">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1395">Az.Accounts</span></span>
* <span data-ttu-id="10032-1396">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10032-1396">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10032-1397">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10032-1397">Az.AnalysisServices</span></span>
<span data-ttu-id="10032-1398">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="10032-1398">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1399">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1399">Az.Compute</span></span>
* <span data-ttu-id="10032-1400">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="10032-1400">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="10032-1401">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="10032-1401">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="10032-1402">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="10032-1402">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1403">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1403">Az.RecoveryServices</span></span>
<span data-ttu-id="10032-1404">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="10032-1404">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1405">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1405">Az.Resources</span></span>
* <span data-ttu-id="10032-1406">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="10032-1406">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="10032-1407">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="10032-1407">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="10032-1408">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="10032-1408">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="10032-1409">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="10032-1409">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1410">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1410">Az.Sql</span></span>
* <span data-ttu-id="10032-1411">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="10032-1411">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="10032-1412">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="10032-1412">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="10032-1413">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="10032-1413">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="10032-1414">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1414">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1415">Az.Accounts</span></span>
* <span data-ttu-id="10032-1416">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="10032-1416">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="10032-1417">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="10032-1417">Az.AnalysisServices</span></span>
* <span data-ttu-id="10032-1418">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="10032-1418">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1419">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1419">Az.RecoveryServices</span></span>
* <span data-ttu-id="10032-1420">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="10032-1420">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="10032-1421">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1421">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1422">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1422">Az.Accounts</span></span>
* <span data-ttu-id="10032-1423">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="10032-1423">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="10032-1424">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1424">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10032-1425">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="10032-1425">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="10032-1426">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="10032-1426">Az.Aks</span></span>
* <span data-ttu-id="10032-1427">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1427">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="10032-1428">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1428">Az.Automation</span></span>
* <span data-ttu-id="10032-1429">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="10032-1429">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="10032-1430">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1430">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="10032-1431">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="10032-1431">Az.Cdn</span></span>
* <span data-ttu-id="10032-1432">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1432">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1433">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1433">Az.Compute</span></span>
* <span data-ttu-id="10032-1434">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="10032-1434">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="10032-1435">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="10032-1435">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="10032-1436">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="10032-1436">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="10032-1437">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="10032-1437">Az.ContainerRegistry</span></span>
* <span data-ttu-id="10032-1438">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1438">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="10032-1439">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="10032-1439">Az.DataFactory</span></span>
* <span data-ttu-id="10032-1440">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="10032-1440">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1441">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1441">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1442">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="10032-1442">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="10032-1443">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="10032-1443">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="10032-1444">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1444">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-1445">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-1445">Az.IotHub</span></span>
* <span data-ttu-id="10032-1446">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10032-1446">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="10032-1447">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1447">Az.KeyVault</span></span>
* <span data-ttu-id="10032-1448">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1448">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1449">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1449">Az.Network</span></span>
* <span data-ttu-id="10032-1450">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1450">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1451">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1451">Az.Resources</span></span>
* <span data-ttu-id="10032-1452">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="10032-1452">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="10032-1453">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="10032-1453">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="10032-1454">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="10032-1454">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="10032-1455">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="10032-1455">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="10032-1456">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="10032-1456">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="10032-1457">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="10032-1457">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="10032-1458">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="10032-1458">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-1459">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-1459">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-1460">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="10032-1460">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="10032-1461">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="10032-1461">Fix some error messages.</span></span>
* <span data-ttu-id="10032-1462">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="10032-1462">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="10032-1463">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="10032-1463">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10032-1464">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10032-1464">Az.SignalR</span></span>
* <span data-ttu-id="10032-1465">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1465">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1466">Az.Sql</span></span>
* <span data-ttu-id="10032-1467">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1467">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10032-1468">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="10032-1468">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="10032-1469">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="10032-1469">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="10032-1470">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="10032-1470">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1471">Az.Storage</span></span>
* <span data-ttu-id="10032-1472">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1472">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10032-1473">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="10032-1473">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="10032-1474">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="10032-1474">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="10032-1475">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="10032-1475">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="10032-1476">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="10032-1476">Az.TrafficManager</span></span>
* <span data-ttu-id="10032-1477">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1477">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1478">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1478">Az.Websites</span></span>
* <span data-ttu-id="10032-1479">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="10032-1479">Update incorrect online help URLs</span></span>
* <span data-ttu-id="10032-1480">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-1480">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="10032-1481">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="10032-1481">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="10032-1482">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="10032-1482">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="10032-1483">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1483">Az.Accounts</span></span>
* <span data-ttu-id="10032-1484">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="10032-1484">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1485">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1485">Az.Compute</span></span>
* <span data-ttu-id="10032-1486">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="10032-1486">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="10032-1487">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="10032-1487">Updated the description of ID in help files</span></span>
* <span data-ttu-id="10032-1488">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1488">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1489">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1489">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1490">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="10032-1490">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="10032-1491">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="10032-1491">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="10032-1492">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="10032-1492">Az.EventGrid</span></span>
* <span data-ttu-id="10032-1493">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="10032-1493">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="10032-1494">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="10032-1494">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="10032-1495">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="10032-1495">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10032-1496">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="10032-1496">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10032-1497">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="10032-1497">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10032-1498">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="10032-1498">Dead letter endpoint.</span></span>
    - <span data-ttu-id="10032-1499">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="10032-1499">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="10032-1500">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="10032-1500">Event Time-To-Live,</span></span>
        - <span data-ttu-id="10032-1501">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="10032-1501">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="10032-1502">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="10032-1502">Dead letter endpoint.</span></span>
* <span data-ttu-id="10032-1503">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="10032-1503">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="10032-1504">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="10032-1504">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="10032-1505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-1505">Az.IotHub</span></span>
* <span data-ttu-id="10032-1506">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="10032-1506">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="10032-1507">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="10032-1507">Az.LogicApp</span></span>
* <span data-ttu-id="10032-1508">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="10032-1508">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1509">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1509">Az.Resources</span></span>
* <span data-ttu-id="10032-1510">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="10032-1510">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="10032-1511">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="10032-1511">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="10032-1512">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10032-1512">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10032-1513">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="10032-1513">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="10032-1514">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="10032-1514">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="10032-1515">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="10032-1515">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="10032-1516">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="10032-1516">Az.SignalR</span></span>
* <span data-ttu-id="10032-1517">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1517">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1518">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1518">Az.Sql</span></span>
* <span data-ttu-id="10032-1519">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="10032-1519">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="10032-1520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1520">Az.Storage</span></span>
* <span data-ttu-id="10032-1521">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="10032-1521">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="10032-1522">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="10032-1522">New-AzStorageContext</span></span>
* <span data-ttu-id="10032-1523">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="10032-1523">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="10032-1524">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="10032-1524">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1525">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1525">Az.Websites</span></span>
* <span data-ttu-id="10032-1526">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="10032-1526">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="10032-1527">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1527">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="10032-1528">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1528">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="10032-1529">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-1529">General</span></span>

- <span data-ttu-id="10032-1530">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="10032-1530">General Availability of Az Module</span></span>
- <span data-ttu-id="10032-1531">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="10032-1531">Online help for each module</span></span>
- <span data-ttu-id="10032-1532">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="10032-1532">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="10032-1533">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="10032-1533">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="10032-1534">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1534">Az.Accounts</span></span>
- <span data-ttu-id="10032-1535">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10032-1535">Changed from Az.Profile</span></span>
- <span data-ttu-id="10032-1536">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="10032-1536">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10032-1537">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-1537">Az.ApiManagement</span></span>
- <span data-ttu-id="10032-1538">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="10032-1538">Fixes for #7002</span></span>
- <span data-ttu-id="10032-1539">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="10032-1540">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="10032-1540">Az.Batch</span></span>
- <span data-ttu-id="10032-1541">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="10032-1541">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="10032-1542">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="10032-1542">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="10032-1543">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1543">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="10032-1544">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="10032-1544">Az.Billing</span></span>
- <span data-ttu-id="10032-1545">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1545">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="10032-1546">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="10032-1546">Az.CognitivServices</span></span>
- <span data-ttu-id="10032-1547">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1547">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="10032-1548">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="10032-1548">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10032-1549">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1549">Az.ContainerInstance</span></span>
- <span data-ttu-id="10032-1550">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="10032-1550">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="10032-1551">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="10032-1551">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="10032-1552">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1552">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10032-1553">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1553">Az.DataLakeStore</span></span>
- <span data-ttu-id="10032-1554">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1554">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="10032-1555">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="10032-1555">Az.Monitor</span></span>
- <span data-ttu-id="10032-1556">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1556">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="10032-1557">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="10032-1557">Az.KeyVault</span></span>
- <span data-ttu-id="10032-1558">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="10032-1558">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="10032-1559">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="10032-1559">Az.MachineLearning</span></span>
- <span data-ttu-id="10032-1560">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="10032-1560">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="10032-1561">Az.Media</span><span class="sxs-lookup"><span data-stu-id="10032-1561">Az.Media</span></span>
- <span data-ttu-id="10032-1562">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="10032-1562">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10032-1563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1563">Az.Network</span></span>
<span data-ttu-id="10032-1564">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="10032-1564">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="10032-1565">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="10032-1565">New cmdlets added:</span></span>
        - <span data-ttu-id="10032-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1566">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1567">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1568">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1569">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1570">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1571">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="10032-1571">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="10032-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="10032-1572">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="10032-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="10032-1573">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="10032-1574">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="10032-1574">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="10032-1575">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="10032-1575">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="10032-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10032-1576">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10032-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="10032-1577">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="10032-1578">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1578">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="10032-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1579">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="10032-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="10032-1580">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="10032-1581">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="10032-1581">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="10032-1582">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10032-1582">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10032-1583">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10032-1583">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="10032-1584">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="10032-1584">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="10032-1585">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="10032-1585">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="10032-1586">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1586">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="10032-1587">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="10032-1587">Az.OperationalInsights</span></span>
- <span data-ttu-id="10032-1588">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1588">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="10032-1589">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10032-1589">Az.Profile</span></span>
- <span data-ttu-id="10032-1590">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="10032-1590">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1591">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1591">Az.RecoveryServices</span></span>
- <span data-ttu-id="10032-1592">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1592">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="10032-1593">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1593">Az.Resources</span></span>
- <span data-ttu-id="10032-1594">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1594">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10032-1595">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-1595">Az.ServiceFabric</span></span>
- <span data-ttu-id="10032-1596">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="10032-1596">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="10032-1597">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1597">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="10032-1598">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10032-1598">Az.SIgnalR</span></span>
- <span data-ttu-id="10032-1599">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="10032-1599">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="10032-1600">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1600">Az.Sql</span></span>
- <span data-ttu-id="10032-1601">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="10032-1601">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="10032-1602">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1602">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="10032-1603">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1603">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="10032-1604">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1604">Az.Storage</span></span>
- <span data-ttu-id="10032-1605">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1605">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10032-1606">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1606">Az.Websites</span></span>
- <span data-ttu-id="10032-1607">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="10032-1607">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="10032-1608">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1608">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="10032-1609">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-1609">General</span></span>

* <span data-ttu-id="10032-1610">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="10032-1610">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="10032-1611">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1611">Az.Compute</span></span>

* <span data-ttu-id="10032-1612">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="10032-1612">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="10032-1613">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1613">Az.DataLakeStore</span></span>

* <span data-ttu-id="10032-1614">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="10032-1614">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="10032-1615">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="10032-1615">Az.FrontDoor</span></span>

* <span data-ttu-id="10032-1616">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="10032-1616">Fixed some broken links</span></span>
    - <span data-ttu-id="10032-1617">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="10032-1617">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="10032-1618">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="10032-1618">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="10032-1619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="10032-1619">Az.RecoveryServices</span></span>

* <span data-ttu-id="10032-1620">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-1620">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="10032-1621">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="10032-1621">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="10032-1622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1622">Az.Resources</span></span>

* <span data-ttu-id="10032-1623">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="10032-1623">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="10032-1624">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="10032-1624">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="10032-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1625">Az.Sql</span></span>

* <span data-ttu-id="10032-1626">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="10032-1626">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="10032-1627">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="10032-1627">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="10032-1628">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="10032-1628">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="10032-1629">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1629">Az.Storage</span></span>

* <span data-ttu-id="10032-1630">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1630">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="10032-1631">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="10032-1631">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="10032-1632">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10032-1632">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10032-1633">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="10032-1633">Support Static Website configuration</span></span>
    - <span data-ttu-id="10032-1634">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10032-1634">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="10032-1635">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="10032-1635">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="10032-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1636">Az.Websites</span></span>

* <span data-ttu-id="10032-1637">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="10032-1637">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="10032-1638">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="10032-1638">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="10032-1639">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="10032-1639">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="10032-1640">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1640">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="10032-1641">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="10032-1641">Az.ApiManagement</span></span>
* <span data-ttu-id="10032-1642">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="10032-1642">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="10032-1643">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="10032-1643">Az.Automation</span></span>
* <span data-ttu-id="10032-1644">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="10032-1644">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="10032-1645">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="10032-1645">Added Update Management cmdlets</span></span>
* <span data-ttu-id="10032-1646">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="10032-1646">Added Source Control cmdlets</span></span>
* <span data-ttu-id="10032-1647">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="10032-1647">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="10032-1648">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="10032-1648">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="10032-1649">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1649">Az.Compute</span></span>
* <span data-ttu-id="10032-1650">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="10032-1650">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="10032-1651">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="10032-1651">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="10032-1652">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1652">Az.ContainerInstance</span></span>
* <span data-ttu-id="10032-1653">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="10032-1653">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="10032-1654">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="10032-1654">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="10032-1655">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="10032-1655">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="10032-1656">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1656">Az.Network</span></span>
* <span data-ttu-id="10032-1657">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="10032-1657">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="10032-1658">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="10032-1658">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="10032-1659">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="10032-1659">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="10032-1660">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="10032-1660">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="10032-1661">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="10032-1661">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="10032-1662">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="10032-1662">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="10032-1663">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="10032-1663">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="10032-1664">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="10032-1664">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="10032-1665">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="10032-1665">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="10032-1666">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="10032-1666">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="10032-1667">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="10032-1667">Az.Relay</span></span>
* <span data-ttu-id="10032-1668">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="10032-1668">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="10032-1669">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1669">Az.Resources</span></span>
* <span data-ttu-id="10032-1670">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="10032-1670">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="10032-1671">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="10032-1671">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="10032-1672">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="10032-1672">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="10032-1673">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-1673">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-1674">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="10032-1674">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="10032-1675">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1675">Az.Sql</span></span>
* <span data-ttu-id="10032-1676">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="10032-1676">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="10032-1677">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1677">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10032-1678">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1678">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10032-1679">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1679">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10032-1680">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="10032-1680">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="10032-1681">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10032-1681">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10032-1682">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10032-1682">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10032-1683">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10032-1683">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="10032-1684">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="10032-1684">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="10032-1685">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="10032-1685">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="10032-1686">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="10032-1686">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="10032-1687">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="10032-1687">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="10032-1688">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10032-1688">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10032-1689">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="10032-1689">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="10032-1690">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="10032-1690">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="10032-1691">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="10032-1691">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="10032-1692">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="10032-1692">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="10032-1693">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1693">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="10032-1694">Generale</span><span class="sxs-lookup"><span data-stu-id="10032-1694">General</span></span>
* <span data-ttu-id="10032-1695">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="10032-1695">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="10032-1696">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10032-1696">Az.Profile</span></span>
* <span data-ttu-id="10032-1697">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10032-1697">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="10032-1698">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="10032-1698">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="10032-1699">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="10032-1699">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="10032-1700">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="10032-1700">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="10032-1701">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="10032-1701">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="10032-1702">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="10032-1702">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="10032-1703">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="10032-1703">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-1704">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-1704">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-1705">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="10032-1705">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1706">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1706">Az.Compute</span></span>
* <span data-ttu-id="10032-1707">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="10032-1707">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="10032-1708">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="10032-1708">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="10032-1709">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="10032-1709">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1710">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1710">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1711">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="10032-1711">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="10032-1712">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="10032-1712">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="10032-1713">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="10032-1713">Az.Insights</span></span>
* <span data-ttu-id="10032-1714">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="10032-1714">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="10032-1715">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="10032-1715">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="10032-1716">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="10032-1716">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="10032-1717">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="10032-1717">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1718">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1718">Az.Network</span></span>
* <span data-ttu-id="10032-1719">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="10032-1719">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="10032-1720">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-1720">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="10032-1721">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="10032-1721">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="10032-1722">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10032-1722">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="10032-1723">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="10032-1723">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="10032-1724">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="10032-1724">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="10032-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="10032-1725">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="10032-1726">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="10032-1726">Az.PolicyInsights</span></span>
* <span data-ttu-id="10032-1727">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="10032-1727">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1728">Az.Resources</span></span>
* <span data-ttu-id="10032-1729">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="10032-1729">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="10032-1730">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="10032-1730">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="10032-1731">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="10032-1731">Az.ServiceBus</span></span>
* <span data-ttu-id="10032-1732">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="10032-1732">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="10032-1733">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="10032-1733">Az.ServiceFabric</span></span>
* <span data-ttu-id="10032-1734">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="10032-1734">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="10032-1735">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="10032-1735">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="10032-1736">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="10032-1736">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="10032-1737">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="10032-1737">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="10032-1738">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="10032-1738">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="10032-1739">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1739">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="10032-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="10032-1740">Az.Profile</span></span>
* <span data-ttu-id="10032-1741">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="10032-1741">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="10032-1742">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="10032-1742">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1743">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1743">Az.Compute</span></span>
* <span data-ttu-id="10032-1744">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="10032-1744">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="10032-1745">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10032-1745">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="10032-1746">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="10032-1746">Az.DataLakeStore</span></span>
* <span data-ttu-id="10032-1747">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="10032-1747">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="10032-1748">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10032-1748">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="10032-1749">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="10032-1749">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10032-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="10032-1750">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="10032-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10032-1751">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1752">Az.Network</span></span>
* <span data-ttu-id="10032-1753">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="10032-1753">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="10032-1754">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10032-1754">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1755">Az.Resources</span></span>
* <span data-ttu-id="10032-1756">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="10032-1756">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="10032-1757">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="10032-1757">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="10032-1758">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1758">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="10032-1759">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="10032-1759">Azure.Storage</span></span>
* <span data-ttu-id="10032-1760">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="10032-1760">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="10032-1761">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10032-1761">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="10032-1762">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="10032-1762">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="10032-1763">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="10032-1763">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="10032-1764">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="10032-1764">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="10032-1765">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="10032-1765">Az.CognitiveServices</span></span>
* <span data-ttu-id="10032-1766">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="10032-1766">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="10032-1767">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="10032-1767">Az.Compute</span></span>
* <span data-ttu-id="10032-1768">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="10032-1768">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="10032-1769">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="10032-1769">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="10032-1770">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="10032-1770">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="10032-1771">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="10032-1771">Az.DataFactoryV2</span></span>
* <span data-ttu-id="10032-1772">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="10032-1772">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="10032-1773">Az.Network</span><span class="sxs-lookup"><span data-stu-id="10032-1773">Az.Network</span></span>
* <span data-ttu-id="10032-1774">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10032-1774">Added NetworkProfile functionality.</span></span> <span data-ttu-id="10032-1775">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="10032-1775">new cmdlets added</span></span>
    - <span data-ttu-id="10032-1776">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10032-1776">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="10032-1777">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10032-1777">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="10032-1778">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10032-1778">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="10032-1779">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="10032-1779">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="10032-1780">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1780">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="10032-1781">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1781">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="10032-1782">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="10032-1782">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="10032-1783">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="10032-1783">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="10032-1784">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="10032-1784">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="10032-1785">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="10032-1785">Az.RedisCache</span></span>
* <span data-ttu-id="10032-1786">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="10032-1786">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="10032-1787">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="10032-1787">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="10032-1788">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="10032-1788">Az.Resources</span></span>
* <span data-ttu-id="10032-1789">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="10032-1789">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="10032-1790">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="10032-1790">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="10032-1791">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="10032-1791">Az.Sql</span></span>
* <span data-ttu-id="10032-1792">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="10032-1792">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="10032-1793">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="10032-1793">Az.Websites</span></span>
* <span data-ttu-id="10032-1794">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="10032-1794">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="10032-1795">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="10032-1795">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="10032-1796">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="10032-1796">0.2.0 - September 2018</span></span>
 <span data-ttu-id="10032-1797">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="10032-1797">Initial Release</span></span>
