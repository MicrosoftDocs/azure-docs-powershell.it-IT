---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: ee3f54e6bc15dbbaeb97cad7463cb1d2e5795e3e
ms.sourcegitcommit: 05431341858d10eb9c345213275c3ccc24c83c9b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/13/2019
ms.locfileid: "74062140"
---
## <a name="300---november-2019"></a><span data-ttu-id="30865-103">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="30865-103">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="30865-104">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-104">General</span></span>
* <span data-ttu-id="30865-105">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30865-105">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30865-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-106">Az.Accounts</span></span>
* <span data-ttu-id="30865-107">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="30865-107">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="30865-108">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="30865-108">Az.Advisor</span></span>
* <span data-ttu-id="30865-109">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="30865-109">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30865-110">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30865-110">Az.Batch</span></span>
* <span data-ttu-id="30865-111">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="30865-111">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="30865-112">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="30865-112">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="30865-113">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="30865-113">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="30865-114">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="30865-114">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="30865-115">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30865-115">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="30865-116">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30865-116">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="30865-117">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="30865-117">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="30865-118">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="30865-118">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="30865-119">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="30865-119">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="30865-120">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="30865-120">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="30865-121">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="30865-121">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="30865-122">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="30865-122">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="30865-123">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="30865-123">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="30865-124">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="30865-124">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="30865-125">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="30865-125">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="30865-126">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="30865-126">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="30865-127">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="30865-127">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="30865-128">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30865-128">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="30865-129">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="30865-129">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="30865-130">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="30865-130">This operation is no longer supported.</span></span>
* <span data-ttu-id="30865-131">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30865-131">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="30865-132">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="30865-132">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="30865-133">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="30865-133">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="30865-134">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="30865-134">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="30865-135">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="30865-135">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="30865-136">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="30865-136">New non-verified images are also now returned.</span></span> <span data-ttu-id="30865-137">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="30865-137">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="30865-138">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="30865-138">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="30865-139">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="30865-139">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="30865-140">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="30865-140">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="30865-141">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="30865-141">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="30865-142">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="30865-142">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="30865-143">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="30865-143">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="30865-144">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="30865-144">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="30865-145">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="30865-145">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="30865-146">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="30865-146">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30865-147">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-147">Az.Cdn</span></span>
* <span data-ttu-id="30865-148">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="30865-148">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="30865-149">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="30865-149">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-150">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-150">Az.Compute</span></span>
* <span data-ttu-id="30865-151">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="30865-151">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="30865-152">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="30865-152">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="30865-153">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="30865-153">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="30865-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="30865-154">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="30865-155">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30865-155">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30865-156">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="30865-156">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="30865-157">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="30865-157">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="30865-158">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30865-158">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="30865-159">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="30865-159">Breaking changes</span></span>
    - <span data-ttu-id="30865-160">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="30865-160">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="30865-161">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="30865-161">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-162">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-162">Az.DataFactory</span></span>
* <span data-ttu-id="30865-163">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="30865-163">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-164">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-164">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-165">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="30865-165">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="30865-166">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="30865-166">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="30865-167">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="30865-167">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="30865-168">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="30865-168">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="30865-169">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="30865-169">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="30865-170">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="30865-170">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30865-171">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30865-171">Az.FrontDoor</span></span>
* <span data-ttu-id="30865-172">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="30865-172">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30865-173">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30865-173">Az.HDInsight</span></span>
* <span data-ttu-id="30865-174">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="30865-174">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="30865-175">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="30865-175">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="30865-176">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="30865-176">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="30865-177">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-177">Removed five cmdlets:</span></span>
    - <span data-ttu-id="30865-178">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30865-178">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30865-179">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30865-179">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30865-180">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="30865-180">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="30865-181">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30865-181">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="30865-182">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30865-182">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="30865-183">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-183">Added three cmdlets:</span></span>
    - <span data-ttu-id="30865-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30865-184">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="30865-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30865-185">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="30865-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="30865-186">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="30865-187">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="30865-187">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="30865-188">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="30865-188">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="30865-189">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="30865-189">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="30865-190">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="30865-190">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="30865-191">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="30865-191">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="30865-192">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="30865-192">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="30865-193">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="30865-193">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="30865-194">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="30865-194">Added some scenario test cases.</span></span>
* <span data-ttu-id="30865-195">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="30865-195">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-196">Az.IotHub</span></span>
* <span data-ttu-id="30865-197">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="30865-197">Breaking changes:</span></span>
    - <span data-ttu-id="30865-198">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="30865-198">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30865-199">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="30865-199">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30865-200">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="30865-200">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30865-201">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="30865-201">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30865-202">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="30865-202">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="30865-203">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="30865-203">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="30865-204">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="30865-204">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="30865-205">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="30865-205">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="30865-206">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="30865-206">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30865-207">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="30865-207">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="30865-208">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="30865-208">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="30865-209">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="30865-209">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-210">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-210">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-211">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-211">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="30865-212">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-212">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="30865-213">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-213">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="30865-214">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-214">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="30865-215">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-215">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="30865-216">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-216">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="30865-217">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-217">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="30865-218">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-218">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="30865-219">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="30865-219">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-220">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-220">Az.Resources</span></span>
* <span data-ttu-id="30865-221">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="30865-221">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-222">Az.Network</span></span>
* <span data-ttu-id="30865-223">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="30865-223">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="30865-224">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="30865-224">Updated cmdlet:</span></span>
        - <span data-ttu-id="30865-225">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-225">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-226">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-226">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-227">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-227">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-228">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-228">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-229">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-229">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="30865-230">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="30865-230">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="30865-231">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-231">New cmdlet:</span></span>
        - <span data-ttu-id="30865-232">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="30865-232">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="30865-233">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="30865-233">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="30865-234">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-234">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="30865-235">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-235">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="30865-236">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="30865-236">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="30865-237">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="30865-237">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="30865-238">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-238">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="30865-239">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="30865-239">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="30865-240">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-240">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-241">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="30865-241">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="30865-242">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-242">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30865-243">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-243">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30865-244">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-244">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="30865-245">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="30865-245">Set-AzVirtualHub</span></span>
* <span data-ttu-id="30865-246">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="30865-246">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="30865-247">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="30865-247">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30865-248">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="30865-248">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="30865-249">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="30865-249">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="30865-250">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="30865-250">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="30865-251">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="30865-251">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="30865-252">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="30865-252">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="30865-253">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-253">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-254">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="30865-254">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="30865-255">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="30865-255">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30865-256">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30865-256">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30865-257">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30865-257">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30865-258">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30865-258">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30865-259">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30865-259">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="30865-260">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="30865-260">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="30865-261">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="30865-261">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="30865-262">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-262">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-263">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="30865-263">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="30865-264">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="30865-264">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="30865-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="30865-265">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="30865-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="30865-266">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="30865-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="30865-267">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="30865-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-268">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="30865-269">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="30865-269">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30865-270">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="30865-270">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="30865-271">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="30865-271">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="30865-272">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="30865-272">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="30865-273">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="30865-273">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="30865-274">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="30865-274">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="30865-275">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30865-275">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="30865-276">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="30865-276">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="30865-277">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="30865-277">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="30865-278">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-278">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="30865-279">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="30865-279">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="30865-280">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-280">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-281">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30865-281">New-AzIpGroup</span></span>
        - <span data-ttu-id="30865-282">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30865-282">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="30865-283">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30865-283">Get-AzIpGroup</span></span>
        - <span data-ttu-id="30865-284">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="30865-284">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-285">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-285">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-286">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="30865-286">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-287">Az.Sql</span></span>
* <span data-ttu-id="30865-288">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="30865-288">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="30865-289">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="30865-289">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="30865-290">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="30865-290">Removed deprecated aliases:</span></span>
* <span data-ttu-id="30865-291">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="30865-291">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="30865-292">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="30865-292">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="30865-293">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-293">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="30865-294">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="30865-294">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="30865-295">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="30865-295">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="30865-296">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="30865-296">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-297">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-297">Az.Storage</span></span>
* <span data-ttu-id="30865-298">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30865-298">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="30865-299">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-299">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="30865-300">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-300">Set-AzStorageAccount</span></span>
* <span data-ttu-id="30865-301">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="30865-301">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="30865-302">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30865-302">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="30865-303">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30865-303">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="30865-304">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="30865-304">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="30865-305">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-305">General</span></span>
* <span data-ttu-id="30865-306">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30865-306">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30865-307">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-307">Az.Accounts</span></span>
* <span data-ttu-id="30865-308">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="30865-308">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30865-309">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-309">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-310">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="30865-310">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="30865-311">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="30865-311">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-312">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-312">Az.Automation</span></span>
* <span data-ttu-id="30865-313">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="30865-313">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="30865-314">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30865-314">Az.Batch</span></span>
* <span data-ttu-id="30865-315">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="30865-315">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-316">Az.Compute</span></span>
* <span data-ttu-id="30865-317">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30865-317">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="30865-318">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="30865-318">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="30865-319">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="30865-319">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="30865-320">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="30865-320">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-321">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-321">Az.DataFactory</span></span>
* <span data-ttu-id="30865-322">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="30865-322">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="30865-323">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="30865-323">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="30865-324">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="30865-324">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-325">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-325">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-326">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="30865-326">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="30865-327">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="30865-327">Az.HealthcareApis</span></span>
* <span data-ttu-id="30865-328">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="30865-328">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="30865-329">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="30865-329">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="30865-330">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="30865-330">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="30865-331">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="30865-331">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-332">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-332">Az.IotHub</span></span>
* <span data-ttu-id="30865-333">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="30865-333">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="30865-334">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="30865-334">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="30865-335">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-335">Az.Monitor</span></span>
* <span data-ttu-id="30865-336">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="30865-336">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="30865-337">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="30865-337">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="30865-338">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="30865-338">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="30865-339">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="30865-339">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-340">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-340">Az.Network</span></span>
* <span data-ttu-id="30865-341">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="30865-341">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="30865-342">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-342">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="30865-343">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-343">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-344">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-344">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="30865-345">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="30865-345">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="30865-346">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="30865-346">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="30865-347">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-347">Updated cmdlets:</span></span>
        - <span data-ttu-id="30865-348">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-348">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30865-349">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-349">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30865-350">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-350">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="30865-351">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="30865-351">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="30865-352">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="30865-352">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="30865-353">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="30865-353">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="30865-354">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="30865-354">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30865-355">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30865-355">Az.RedisCache</span></span>
* <span data-ttu-id="30865-356">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="30865-356">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-357">Az.Sql</span></span>
* <span data-ttu-id="30865-358">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="30865-358">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-359">Az.Storage</span></span>
* <span data-ttu-id="30865-360">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="30865-360">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="30865-361">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="30865-361">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="30865-362">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="30865-362">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="30865-363">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="30865-363">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="30865-364">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-364">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30865-365">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30865-365">Az.StorageSync</span></span>
* <span data-ttu-id="30865-366">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="30865-366">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-367">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-367">Az.Websites</span></span>
* <span data-ttu-id="30865-368">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="30865-368">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="30865-369">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="30865-369">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="30865-370">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-370">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-371">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="30865-371">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="30865-372">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="30865-372">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="30865-373">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="30865-373">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-374">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-374">Az.Automation</span></span>
* <span data-ttu-id="30865-375">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="30865-375">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="30865-376">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="30865-376">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="30865-377">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="30865-377">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-378">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-378">Az.Compute</span></span>
* <span data-ttu-id="30865-379">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="30865-379">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="30865-380">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30865-380">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30865-381">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="30865-381">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="30865-382">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="30865-382">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="30865-383">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30865-383">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="30865-384">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="30865-384">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="30865-385">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="30865-385">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="30865-386">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="30865-386">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="30865-387">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="30865-387">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-388">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-388">Az.DataFactory</span></span>
* <span data-ttu-id="30865-389">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="30865-389">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="30865-390">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="30865-390">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="30865-391">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30865-391">Az.HDInsight</span></span>
* <span data-ttu-id="30865-392">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="30865-392">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-393">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-393">Az.IotHub</span></span>
* <span data-ttu-id="30865-394">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="30865-394">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="30865-395">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="30865-395">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="30865-396">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="30865-396">New cmdlets are:</span></span>
    - <span data-ttu-id="30865-397">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="30865-397">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30865-398">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="30865-398">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30865-399">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="30865-399">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="30865-400">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="30865-400">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-401">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-401">Az.Monitor</span></span>
* <span data-ttu-id="30865-402">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="30865-402">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="30865-403">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="30865-403">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="30865-404">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="30865-404">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="30865-405">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="30865-405">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="30865-406">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="30865-406">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="30865-407">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="30865-407">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="30865-408">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30865-408">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="30865-409">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="30865-409">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="30865-410">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="30865-410">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="30865-411">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="30865-411">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="30865-412">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="30865-412">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="30865-413">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="30865-413">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="30865-414">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="30865-414">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="30865-415">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="30865-415">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="30865-416">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="30865-416">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="30865-417">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="30865-417">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="30865-418">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="30865-418">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="30865-419">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-419">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="30865-420">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="30865-420">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="30865-421">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-421">Overall improved help files</span></span>
* <span data-ttu-id="30865-422">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="30865-422">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-423">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-423">Az.Network</span></span>
* <span data-ttu-id="30865-424">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="30865-424">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="30865-425">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="30865-425">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="30865-426">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30865-426">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="30865-427">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="30865-427">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="30865-428">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="30865-428">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="30865-429">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="30865-429">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="30865-430">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="30865-430">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="30865-431">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30865-431">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="30865-432">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-432">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="30865-433">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="30865-433">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="30865-434">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-434">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="30865-435">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-435">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="30865-436">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-436">New cmdlets</span></span>
        - <span data-ttu-id="30865-437">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="30865-437">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="30865-438">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="30865-438">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="30865-439">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="30865-439">Updated cmdlet:</span></span>
        - <span data-ttu-id="30865-440">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="30865-440">New-VpnSite</span></span>
        - <span data-ttu-id="30865-441">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="30865-441">Update-VpnSite</span></span>
        - <span data-ttu-id="30865-442">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="30865-442">New-VpnConnection</span></span>
        - <span data-ttu-id="30865-443">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="30865-443">Update-VpnConnection</span></span>
* <span data-ttu-id="30865-444">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="30865-444">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-445">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-445">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-446">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="30865-446">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="30865-447">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="30865-447">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-448">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-448">Az.Resources</span></span>
* <span data-ttu-id="30865-449">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="30865-449">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-450">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-450">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-451">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="30865-451">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="30865-452">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="30865-452">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="30865-453">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="30865-453">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30865-454">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="30865-454">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30865-455">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="30865-455">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30865-456">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="30865-456">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="30865-457">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="30865-457">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30865-458">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="30865-458">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30865-459">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="30865-459">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30865-460">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="30865-460">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30865-461">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="30865-461">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="30865-462">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="30865-462">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="30865-463">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="30865-463">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="30865-464">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="30865-464">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="30865-465">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="30865-465">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="30865-466">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30865-466">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30865-467">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30865-467">Az.SignalR</span></span>
* <span data-ttu-id="30865-468">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="30865-468">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-469">Az.Sql</span></span>
* <span data-ttu-id="30865-470">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="30865-470">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="30865-471">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="30865-471">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="30865-472">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-472">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="30865-473">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="30865-473">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="30865-474">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="30865-474">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-475">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-475">Az.Storage</span></span>
* <span data-ttu-id="30865-476">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="30865-476">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="30865-477">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="30865-477">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="30865-478">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30865-478">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="30865-479">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30865-479">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="30865-480">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="30865-480">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="30865-481">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30865-481">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="30865-482">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="30865-482">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="30865-483">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="30865-483">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30865-484">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="30865-484">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30865-485">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="30865-485">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="30865-486">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="30865-486">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-487">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-487">Az.Websites</span></span>
* <span data-ttu-id="30865-488">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="30865-488">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="30865-489">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="30865-489">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="30865-490">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="30865-490">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="30865-491">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="30865-491">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="30865-492">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-492">General</span></span>
* <span data-ttu-id="30865-493">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="30865-493">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30865-494">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-494">Az.Accounts</span></span>
* <span data-ttu-id="30865-495">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="30865-495">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="30865-496">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30865-496">Az.Aks</span></span>
* <span data-ttu-id="30865-497">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="30865-497">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="30865-498">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="30865-498">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30865-499">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-499">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-500">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="30865-500">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="30865-501">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="30865-501">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="30865-502">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="30865-502">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="30865-503">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="30865-503">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="30865-504">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="30865-504">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30865-505">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30865-505">Az.Batch</span></span>
* <span data-ttu-id="30865-506">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="30865-506">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30865-507">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-507">Az.Cdn</span></span>
* <span data-ttu-id="30865-508">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="30865-508">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-509">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-509">Az.Compute</span></span>
* <span data-ttu-id="30865-510">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="30865-510">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="30865-511">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30865-511">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="30865-512">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-512">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="30865-513">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="30865-513">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="30865-514">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="30865-514">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="30865-515">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="30865-515">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="30865-516">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="30865-516">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="30865-517">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="30865-517">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-518">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-518">Az.DataFactory</span></span>
* <span data-ttu-id="30865-519">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="30865-519">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="30865-520">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="30865-520">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="30865-521">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="30865-521">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="30865-522">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="30865-522">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-523">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-523">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-524">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="30865-524">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30865-525">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30865-525">Az.EventHub</span></span>
* <span data-ttu-id="30865-526">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-526">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="30865-527">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="30865-527">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="30865-528">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="30865-528">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="30865-529">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="30865-529">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="30865-530">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="30865-530">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="30865-531">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="30865-531">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-532">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-532">Az.Monitor</span></span>
* <span data-ttu-id="30865-533">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-533">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-534">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-534">Az.Network</span></span>
* <span data-ttu-id="30865-535">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-535">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="30865-536">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="30865-536">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="30865-537">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="30865-537">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="30865-538">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="30865-538">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="30865-539">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="30865-539">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="30865-540">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="30865-540">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="30865-541">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="30865-541">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-542">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-542">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-543">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="30865-543">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="30865-544">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="30865-544">Added example</span></span>
    - <span data-ttu-id="30865-545">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="30865-545">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="30865-546">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="30865-546">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="30865-547">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="30865-547">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-548">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-548">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-549">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="30865-549">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-550">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-550">Az.Resources</span></span>
* <span data-ttu-id="30865-551">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="30865-551">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="30865-552">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="30865-552">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="30865-553">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="30865-553">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="30865-554">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-554">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-555">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-555">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-556">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-556">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="30865-557">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="30865-557">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="30865-558">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="30865-558">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="30865-559">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-559">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-560">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="30865-560">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="30865-561">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="30865-561">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="30865-562">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="30865-562">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="30865-563">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="30865-563">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="30865-564">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="30865-564">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="30865-565">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="30865-565">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-566">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-566">Az.Sql</span></span>
* <span data-ttu-id="30865-567">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="30865-567">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-568">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-568">Az.Storage</span></span>
* <span data-ttu-id="30865-569">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="30865-569">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="30865-570">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="30865-570">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="30865-571">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30865-571">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="30865-572">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30865-572">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="30865-573">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="30865-573">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="30865-574">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30865-574">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-575">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-575">Az.Websites</span></span>
* <span data-ttu-id="30865-576">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30865-576">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="30865-577">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-577">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-578">Az.Accounts</span></span>
* <span data-ttu-id="30865-579">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="30865-579">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="30865-580">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="30865-580">Az.ApplicationInsights</span></span>
* <span data-ttu-id="30865-581">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="30865-581">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="30865-582">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-582">Az.Automation</span></span>
* <span data-ttu-id="30865-583">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="30865-583">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-584">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-584">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-585">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="30865-585">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-586">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-586">Az.Compute</span></span>
* <span data-ttu-id="30865-587">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="30865-587">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="30865-588">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30865-588">Az.ContainerRegistry</span></span>
* <span data-ttu-id="30865-589">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="30865-589">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="30865-590">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="30865-590">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-591">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-591">Az.DataFactory</span></span>
* <span data-ttu-id="30865-592">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="30865-592">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="30865-593">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="30865-593">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30865-594">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30865-594">Az.EventHub</span></span>
* <span data-ttu-id="30865-595">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="30865-595">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="30865-596">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="30865-596">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30865-597">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-597">Az.KeyVault</span></span>
* <span data-ttu-id="30865-598">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="30865-598">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30865-599">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30865-599">Az.LogicApp</span></span>
* <span data-ttu-id="30865-600">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="30865-600">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="30865-601">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="30865-601">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="30865-602">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="30865-602">Az.ManagedServices</span></span>
* <span data-ttu-id="30865-603">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="30865-603">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-604">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-604">Az.Network</span></span>
* <span data-ttu-id="30865-605">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="30865-605">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="30865-606">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-606">New cmdlets</span></span>
        - <span data-ttu-id="30865-607">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30865-607">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30865-608">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-608">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30865-609">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-609">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-610">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-610">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-611">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-611">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-612">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-612">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="30865-613">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="30865-613">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="30865-614">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-614">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="30865-615">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="30865-615">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="30865-616">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="30865-616">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="30865-617">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="30865-617">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="30865-618">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="30865-618">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="30865-619">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="30865-619">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="30865-620">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="30865-620">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="30865-621">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-621">Updated cmdlets</span></span>
        - <span data-ttu-id="30865-622">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-622">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30865-623">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-623">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="30865-624">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-624">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="30865-625">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="30865-625">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="30865-626">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-626">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="30865-627">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="30865-627">Updated cmdlet:</span></span>
        - <span data-ttu-id="30865-628">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-628">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="30865-629">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-629">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="30865-630">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-630">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="30865-631">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="30865-631">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="30865-632">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="30865-632">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="30865-633">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="30865-633">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-634">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-634">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-635">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="30865-635">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="30865-636">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="30865-636">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-637">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-637">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-638">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="30865-638">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="30865-639">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="30865-639">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="30865-640">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="30865-640">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="30865-641">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="30865-641">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="30865-642">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="30865-642">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="30865-643">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="30865-643">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="30865-644">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="30865-644">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="30865-645">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="30865-645">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="30865-646">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-646">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="30865-647">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="30865-647">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-648">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-648">Az.Resources</span></span>
- <span data-ttu-id="30865-649">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="30865-649">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="30865-650">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="30865-650">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-651">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-651">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-652">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="30865-652">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="30865-653">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="30865-653">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-654">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-654">Az.Sql</span></span>
* <span data-ttu-id="30865-655">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="30865-655">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="30865-656">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="30865-656">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="30865-657">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="30865-657">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-658">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-658">Az.Storage</span></span>
* <span data-ttu-id="30865-659">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="30865-659">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30865-660">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30865-660">Az.StorageSync</span></span>
* <span data-ttu-id="30865-661">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="30865-661">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="30865-662">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="30865-662">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-663">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-663">Az.Websites</span></span>
* <span data-ttu-id="30865-664">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="30865-664">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="30865-665">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="30865-665">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="30865-666">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="30865-666">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="30865-667">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-667">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-668">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-668">Az.Accounts</span></span>
* <span data-ttu-id="30865-669">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="30865-669">Add support for profile cmdlets</span></span>
* <span data-ttu-id="30865-670">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="30865-670">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="30865-671">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30865-671">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="30865-672">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="30865-672">Az.Advisor</span></span>
* <span data-ttu-id="30865-673">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="30865-673">GA release of Az.Advisor</span></span>
* <span data-ttu-id="30865-674">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="30865-674">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="30865-675">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-675">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-676">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="30865-676">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="30865-677">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="30865-677">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="30865-678">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="30865-678">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="30865-679">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="30865-679">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="30865-680">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="30865-680">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="30865-681">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="30865-681">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="30865-682">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="30865-682">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-683">Az.Automation</span></span>
* <span data-ttu-id="30865-684">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="30865-684">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-685">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-685">Az.Compute</span></span>
* <span data-ttu-id="30865-686">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="30865-686">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-687">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-687">Az.DataFactory</span></span>
* <span data-ttu-id="30865-688">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="30865-688">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30865-689">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30865-689">Az.EventGrid</span></span>
* <span data-ttu-id="30865-690">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="30865-690">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-691">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-691">Az.IotHub</span></span>
* <span data-ttu-id="30865-692">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="30865-692">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-693">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-693">Az.Network</span></span>
* <span data-ttu-id="30865-694">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="30865-694">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="30865-695">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="30865-695">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30865-696">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30865-696">Az.PolicyInsights</span></span>
* <span data-ttu-id="30865-697">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="30865-697">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="30865-698">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="30865-698">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-699">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-699">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-700">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="30865-700">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-701">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-701">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-702">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="30865-702">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-703">Az.Resources</span></span>
    - <span data-ttu-id="30865-704">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="30865-704">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="30865-705">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="30865-705">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="30865-706">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="30865-706">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="30865-707">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="30865-707">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-708">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-708">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-709">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="30865-709">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-710">Az.Sql</span></span>
* <span data-ttu-id="30865-711">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="30865-711">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="30865-712">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-712">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="30865-713">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30865-713">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30865-714">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30865-714">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30865-715">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="30865-715">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="30865-716">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30865-716">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="30865-717">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30865-717">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="30865-718">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="30865-718">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="30865-719">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="30865-719">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-720">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-720">Az.Storage</span></span>
* <span data-ttu-id="30865-721">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-721">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="30865-722">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30865-722">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="30865-723">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="30865-723">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="30865-724">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="30865-724">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="30865-725">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-725">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="30865-726">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-726">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="30865-727">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-727">Set-AzStorageAccount</span></span>
* <span data-ttu-id="30865-728">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="30865-728">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="30865-729">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30865-729">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="30865-730">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="30865-730">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="30865-731">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="30865-731">Az.StorageSync</span></span>
* <span data-ttu-id="30865-732">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="30865-732">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="30865-733">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="30865-733">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-734">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-734">Az.Accounts</span></span>
* <span data-ttu-id="30865-735">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="30865-735">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="30865-736">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="30865-736">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="30865-737">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="30865-737">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="30865-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="30865-738">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="30865-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="30865-739">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-740">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-740">Az.Compute</span></span>
* <span data-ttu-id="30865-741">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="30865-741">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="30865-742">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="30865-742">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="30865-743">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="30865-743">Az.Dns</span></span>
* <span data-ttu-id="30865-744">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="30865-744">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30865-745">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30865-745">Az.EventGrid</span></span>
* <span data-ttu-id="30865-746">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="30865-746">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="30865-747">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-747">New cmdlets:</span></span>
    - <span data-ttu-id="30865-748">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30865-748">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30865-749">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-749">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30865-750">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30865-750">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30865-751">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-751">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="30865-752">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="30865-752">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="30865-753">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-753">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30865-754">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="30865-754">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="30865-755">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-755">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="30865-756">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="30865-756">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="30865-757">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="30865-757">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="30865-758">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="30865-758">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="30865-759">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-759">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="30865-760">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30865-760">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="30865-761">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-761">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="30865-762">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="30865-762">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="30865-763">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="30865-763">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="30865-764">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-764">Updated cmdlets:</span></span>
    - <span data-ttu-id="30865-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30865-765">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="30865-766">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="30865-766">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="30865-767">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="30865-767">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="30865-768">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="30865-768">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="30865-769">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="30865-769">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="30865-770">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="30865-770">Event subscription expiration date,</span></span>
            - <span data-ttu-id="30865-771">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="30865-771">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="30865-772">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="30865-772">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="30865-773">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="30865-773">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="30865-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30865-774">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="30865-775">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="30865-775">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="30865-776">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="30865-776">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="30865-777">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="30865-777">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="30865-778">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="30865-778">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30865-779">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30865-779">Az.FrontDoor</span></span>
* <span data-ttu-id="30865-780">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="30865-780">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="30865-781">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="30865-781">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="30865-782">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="30865-782">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="30865-783">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="30865-783">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-784">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-784">Az.Network</span></span>
* <span data-ttu-id="30865-785">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-785">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="30865-786">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-786">New cmdlets</span></span>
        - <span data-ttu-id="30865-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="30865-787">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="30865-788">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="30865-788">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="30865-789">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-789">New cmdlets</span></span> 
        - <span data-ttu-id="30865-790">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="30865-790">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="30865-791">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-791">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="30865-792">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-792">New cmdlets</span></span> 
        - <span data-ttu-id="30865-793">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-793">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="30865-794">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-794">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30865-795">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="30865-795">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="30865-796">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-796">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="30865-797">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="30865-797">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="30865-798">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30865-798">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="30865-799">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-799">New cmdlets</span></span>
        - <span data-ttu-id="30865-800">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30865-800">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30865-801">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30865-801">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30865-802">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="30865-802">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="30865-803">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="30865-803">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="30865-804">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="30865-804">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="30865-805">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="30865-805">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="30865-806">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="30865-806">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="30865-807">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="30865-807">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="30865-808">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="30865-808">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="30865-809">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="30865-809">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="30865-810">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-810">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="30865-811">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="30865-811">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="30865-812">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-812">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="30865-813">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="30865-813">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="30865-814">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="30865-814">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="30865-815">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="30865-815">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="30865-816">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="30865-816">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="30865-817">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-817">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="30865-818">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="30865-818">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="30865-819">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="30865-819">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="30865-820">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-820">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="30865-821">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="30865-821">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="30865-822">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="30865-822">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="30865-823">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="30865-823">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="30865-824">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-824">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="30865-825">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-825">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="30865-826">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-826">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-827">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-827">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-828">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="30865-828">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-829">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-829">Az.Resources</span></span>
* <span data-ttu-id="30865-830">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="30865-830">Support for additional Template Export options</span></span>
    - <span data-ttu-id="30865-831">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30865-831">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="30865-832">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30865-832">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="30865-833">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="30865-833">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-834">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-834">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-835">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="30865-835">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-836">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-836">Az.Sql</span></span>
* <span data-ttu-id="30865-837">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="30865-837">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="30865-838">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="30865-838">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="30865-839">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="30865-839">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="30865-840">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30865-840">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30865-841">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30865-841">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30865-842">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="30865-842">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="30865-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="30865-843">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="30865-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="30865-844">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-845">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-845">Az.Storage</span></span>
* <span data-ttu-id="30865-846">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30865-846">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="30865-847">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-847">New-AzStorageAccount</span></span>
* <span data-ttu-id="30865-848">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="30865-848">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="30865-849">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-849">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-850">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-850">Az.Websites</span></span>
* <span data-ttu-id="30865-851">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="30865-851">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="30865-852">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="30865-852">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="30865-853">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="30865-853">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="30865-854">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-854">Az.Cdn</span></span>
* <span data-ttu-id="30865-855">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="30865-855">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-856">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-856">Az.Compute</span></span>
* <span data-ttu-id="30865-857">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="30865-857">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="30865-858">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="30865-858">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30865-859">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30865-859">Az.EventHub</span></span>
* <span data-ttu-id="30865-860">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="30865-860">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="30865-861">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30865-861">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-862">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-862">Az.Network</span></span>
* <span data-ttu-id="30865-863">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="30865-863">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="30865-864">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="30865-864">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30865-865">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30865-865">Az.PolicyInsights</span></span>
* <span data-ttu-id="30865-866">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="30865-866">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-867">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-867">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-868">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="30865-868">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-869">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-869">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-870">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30865-870">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-871">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-871">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-872">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="30865-872">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="30865-873">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="30865-873">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-874">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-874">Az.Sql</span></span>
* <span data-ttu-id="30865-875">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="30865-875">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="30865-876">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-876">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="30865-877">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="30865-877">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="30865-878">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="30865-878">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-879">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-879">Az.Websites</span></span>
* <span data-ttu-id="30865-880">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="30865-880">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="30865-881">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-881">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="30865-882">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-882">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-883">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="30865-883">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="30865-884">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="30865-884">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="30865-885">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="30865-885">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="30865-886">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="30865-886">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="30865-887">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-887">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="30865-888">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="30865-888">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="30865-889">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="30865-889">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="30865-890">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="30865-890">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="30865-891">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-891">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="30865-892">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="30865-892">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="30865-893">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-893">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="30865-894">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="30865-894">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="30865-895">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="30865-895">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="30865-896">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="30865-896">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="30865-897">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="30865-897">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="30865-898">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="30865-898">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="30865-899">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="30865-899">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="30865-900">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="30865-900">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="30865-901">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="30865-901">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="30865-902">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="30865-902">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="30865-903">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="30865-903">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="30865-904">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30865-904">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="30865-905">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="30865-905">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="30865-906">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-906">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="30865-907">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="30865-907">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="30865-908">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="30865-908">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="30865-909">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="30865-909">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="30865-910">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30865-910">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="30865-911">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="30865-911">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="30865-912">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="30865-912">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="30865-913">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="30865-913">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="30865-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="30865-914">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="30865-915">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="30865-915">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="30865-916">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="30865-916">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="30865-917">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="30865-917">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="30865-918">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="30865-918">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="30865-919">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="30865-919">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="30865-920">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="30865-920">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="30865-921">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="30865-921">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="30865-922">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="30865-922">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="30865-923">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="30865-923">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="30865-924">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="30865-924">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="30865-925">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="30865-925">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="30865-926">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="30865-926">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="30865-927">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="30865-927">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="30865-928">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="30865-928">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="30865-929">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="30865-929">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="30865-930">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="30865-930">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="30865-931">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="30865-931">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="30865-932">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="30865-932">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="30865-933">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="30865-933">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="30865-934">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="30865-934">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="30865-935">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="30865-935">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="30865-936">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="30865-936">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="30865-937">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="30865-937">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="30865-938">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="30865-938">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="30865-939">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="30865-939">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="30865-940">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="30865-940">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="30865-941">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="30865-941">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="30865-942">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="30865-942">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="30865-943">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="30865-943">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="30865-944">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="30865-944">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="30865-945">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="30865-945">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="30865-946">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="30865-946">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="30865-947">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="30865-947">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="30865-948">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="30865-948">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="30865-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="30865-949">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="30865-950">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="30865-950">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="30865-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="30865-951">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="30865-952">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="30865-952">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="30865-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="30865-953">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="30865-954">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="30865-954">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="30865-955">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="30865-955">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="30865-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="30865-956">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="30865-957">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="30865-957">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="30865-958">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="30865-958">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="30865-959">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="30865-959">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-960">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-960">Az.Automation</span></span>
* <span data-ttu-id="30865-961">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="30865-961">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="30865-962">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="30865-962">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="30865-963">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="30865-963">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="30865-964">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="30865-964">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="30865-965">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="30865-965">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="30865-966">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="30865-966">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="30865-967">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="30865-967">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-968">Az.Compute</span></span>
* <span data-ttu-id="30865-969">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="30865-969">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="30865-970">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="30865-970">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-971">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-971">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-972">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-972">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-973">Az.Monitor</span></span>
* <span data-ttu-id="30865-974">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-974">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-975">Az.Network</span></span>
* <span data-ttu-id="30865-976">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="30865-976">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="30865-977">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="30865-977">Updated cmdlet:</span></span>
        - <span data-ttu-id="30865-978">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-978">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="30865-979">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="30865-979">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-980">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-980">Az.Resources</span></span>
* <span data-ttu-id="30865-981">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="30865-981">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-982">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-982">Az.Sql</span></span>
* <span data-ttu-id="30865-983">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="30865-983">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="30865-984">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-984">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-985">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-985">Az.Accounts</span></span>
* <span data-ttu-id="30865-986">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="30865-986">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-987">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-987">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-988">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="30865-988">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="30865-989">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="30865-989">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-990">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-990">Az.Compute</span></span>
* <span data-ttu-id="30865-991">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="30865-991">Proximity placement group feature.</span></span>
    - <span data-ttu-id="30865-992">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="30865-992">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="30865-993">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="30865-993">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="30865-994">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="30865-994">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="30865-995">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="30865-995">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="30865-996">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30865-996">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="30865-997">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="30865-997">Breaking changes</span></span>
    - <span data-ttu-id="30865-998">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="30865-998">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="30865-999">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="30865-999">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="30865-1000">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="30865-1000">Az.DeploymentManager</span></span>
* <span data-ttu-id="30865-1001">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="30865-1001">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="30865-1002">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="30865-1002">Az.Dns</span></span>
* <span data-ttu-id="30865-1003">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="30865-1003">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="30865-1004">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="30865-1004">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="30865-1005">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="30865-1005">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="30865-1006">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30865-1006">Az.FrontDoor</span></span>
* <span data-ttu-id="30865-1007">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1007">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="30865-1008">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="30865-1008">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="30865-1009">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30865-1009">Az.HDInsight</span></span>
* <span data-ttu-id="30865-1010">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-1010">Removed two cmdlets:</span></span>
    - <span data-ttu-id="30865-1011">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30865-1011">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="30865-1012">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30865-1012">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="30865-1013">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="30865-1013">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="30865-1014">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="30865-1014">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="30865-1015">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="30865-1015">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="30865-1016">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="30865-1016">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-1017">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-1017">Az.Monitor</span></span>
* <span data-ttu-id="30865-1018">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="30865-1018">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="30865-1019">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="30865-1019">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="30865-1020">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="30865-1020">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="30865-1021">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="30865-1021">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="30865-1022">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="30865-1022">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="30865-1023">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="30865-1023">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="30865-1024">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="30865-1024">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="30865-1025">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30865-1025">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30865-1026">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30865-1026">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30865-1027">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30865-1027">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30865-1028">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30865-1028">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30865-1029">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="30865-1029">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="30865-1030">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="30865-1030">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="30865-1031">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="30865-1031">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1032">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1032">Az.Network</span></span>
* <span data-ttu-id="30865-1033">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="30865-1033">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="30865-1034">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-1034">New cmdlets</span></span>
        - <span data-ttu-id="30865-1035">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30865-1035">New-AzNatGateway</span></span>
        - <span data-ttu-id="30865-1036">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30865-1036">Get-AzNatGateway</span></span>
        - <span data-ttu-id="30865-1037">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30865-1037">Set-AzNatGateway</span></span>
        - <span data-ttu-id="30865-1038">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="30865-1038">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="30865-1039">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="30865-1039">Updated cmdlets</span></span>
        - <span data-ttu-id="30865-1040">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="30865-1040">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="30865-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="30865-1041">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="30865-1042">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-1042">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="30865-1043">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-1043">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="30865-1044">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="30865-1044">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30865-1045">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30865-1045">Az.PolicyInsights</span></span>
* <span data-ttu-id="30865-1046">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="30865-1046">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="30865-1047">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="30865-1047">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="30865-1048">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="30865-1048">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1049">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1049">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-1050">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="30865-1050">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="30865-1051">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30865-1051">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="30865-1052">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="30865-1052">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="30865-1053">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-1053">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="30865-1054">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="30865-1054">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="30865-1055">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="30865-1055">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="30865-1056">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="30865-1056">Az.Relay</span></span>
* <span data-ttu-id="30865-1057">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="30865-1057">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-1058">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-1058">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-1059">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30865-1059">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1060">Az.Storage</span></span>
* <span data-ttu-id="30865-1061">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="30865-1061">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="30865-1062">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="30865-1062">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="30865-1063">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="30865-1063">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="30865-1064">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1064">New-AzStorageAccount</span></span>
* <span data-ttu-id="30865-1065">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="30865-1065">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="30865-1066">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1066">New-AzStorageAccount</span></span>
    - <span data-ttu-id="30865-1067">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1067">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="30865-1068">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1068">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1069">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1069">Az.Websites</span></span>
* <span data-ttu-id="30865-1070">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="30865-1070">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="30865-1071">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="30865-1071">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="30865-1072">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1072">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30865-1073">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="30865-1073">Highlights since the last major release</span></span>
* <span data-ttu-id="30865-1074">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="30865-1074">General availability of `Az` module</span></span>
* <span data-ttu-id="30865-1075">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30865-1075">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30865-1076">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30865-1076">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30865-1077">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1077">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30865-1078">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="30865-1078">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30865-1079">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1079">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30865-1080">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="30865-1080">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30865-1081">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1081">Az.Accounts</span></span>
* <span data-ttu-id="30865-1082">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="30865-1082">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="30865-1083">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30865-1083">Az.Batch</span></span>
* <span data-ttu-id="30865-1084">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1084">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30865-1085">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-1085">Az.Cdn</span></span>
* <span data-ttu-id="30865-1086">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1086">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-1087">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-1087">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-1088">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1088">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1089">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1089">Az.Compute</span></span>
* <span data-ttu-id="30865-1090">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="30865-1090">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="30865-1091">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1091">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1092">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="30865-1092">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-1093">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-1093">Az.DataFactory</span></span>
* <span data-ttu-id="30865-1094">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="30865-1094">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1095">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1095">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1096">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1096">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30865-1097">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30865-1097">Az.EventGrid</span></span>
* <span data-ttu-id="30865-1098">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="30865-1098">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30865-1099">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30865-1099">Az.EventHub</span></span>
* <span data-ttu-id="30865-1100">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="30865-1100">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="30865-1101">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="30865-1101">Az.HDInsight</span></span>
* <span data-ttu-id="30865-1102">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1102">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-1103">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-1103">Az.IotHub</span></span>
* <span data-ttu-id="30865-1104">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1104">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30865-1105">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1105">Az.KeyVault</span></span>
* <span data-ttu-id="30865-1106">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1106">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1107">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="30865-1107">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="30865-1108">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="30865-1108">Az.MachineLearning</span></span>
* <span data-ttu-id="30865-1109">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1109">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="30865-1110">Az.Media</span><span class="sxs-lookup"><span data-stu-id="30865-1110">Az.Media</span></span>
* <span data-ttu-id="30865-1111">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1111">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-1112">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-1112">Az.Monitor</span></span>
  * <span data-ttu-id="30865-1113">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="30865-1113">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="30865-1114">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="30865-1114">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="30865-1115">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="30865-1115">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="30865-1116">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30865-1116">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="30865-1117">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30865-1117">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="30865-1118">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="30865-1118">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="30865-1119">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="30865-1119">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1120">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1120">Az.Network</span></span>
* <span data-ttu-id="30865-1121">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1121">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1122">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="30865-1122">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="30865-1123">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="30865-1123">Az.NotificationHubs</span></span>
* <span data-ttu-id="30865-1124">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1124">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-1125">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-1125">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-1126">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1126">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="30865-1127">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="30865-1127">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="30865-1128">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1128">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1129">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1129">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-1130">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1130">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1131">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1131">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="30865-1132">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="30865-1132">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="30865-1133">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="30865-1133">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30865-1134">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30865-1134">Az.RedisCache</span></span>
* <span data-ttu-id="30865-1135">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1135">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1136">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1136">Az.Resources</span></span>
* <span data-ttu-id="30865-1137">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="30865-1137">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1138">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1138">Az.Sql</span></span>
* <span data-ttu-id="30865-1139">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="30865-1139">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="30865-1140">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1140">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1141">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="30865-1141">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="30865-1142">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="30865-1142">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="30865-1143">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="30865-1143">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="30865-1144">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="30865-1144">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="30865-1145">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="30865-1145">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1146">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1146">Az.Websites</span></span>
* <span data-ttu-id="30865-1147">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="30865-1147">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="30865-1148">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="30865-1148">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="30865-1149">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="30865-1149">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="30865-1150">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="30865-1150">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="30865-1151">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1151">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30865-1152">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="30865-1152">Highlights since the last major release</span></span>
* <span data-ttu-id="30865-1153">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="30865-1153">General availability of `Az` module</span></span>
* <span data-ttu-id="30865-1154">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30865-1154">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30865-1155">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30865-1155">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30865-1156">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1156">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30865-1157">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="30865-1157">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30865-1158">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1158">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30865-1159">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="30865-1159">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="30865-1160">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1160">Az.Accounts</span></span>
* <span data-ttu-id="30865-1161">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="30865-1161">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30865-1162">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30865-1162">Az.AnalysisServices</span></span>
* <span data-ttu-id="30865-1163">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="30865-1163">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="30865-1164">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="30865-1164">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-1165">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1165">Az.Automation</span></span>
* <span data-ttu-id="30865-1166">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="30865-1166">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="30865-1167">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="30865-1167">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="30865-1168">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1168">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1169">Az.Compute</span></span>
* <span data-ttu-id="30865-1170">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1170">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="30865-1171">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="30865-1171">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="30865-1172">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1172">Az.ContainerInstance</span></span>
* <span data-ttu-id="30865-1173">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="30865-1173">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-1174">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-1174">Az.DataFactory</span></span>
* <span data-ttu-id="30865-1175">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="30865-1175">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="30865-1176">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="30865-1176">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1177">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1177">Az.Resources</span></span>
* <span data-ttu-id="30865-1178">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="30865-1178">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="30865-1179">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="30865-1179">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="30865-1180">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="30865-1180">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="30865-1181">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="30865-1181">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="30865-1182">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="30865-1182">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="30865-1183">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="30865-1183">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1184">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1184">Az.Sql</span></span>
* <span data-ttu-id="30865-1185">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="30865-1185">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1186">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1186">Az.Storage</span></span>
* <span data-ttu-id="30865-1187">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="30865-1187">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="30865-1188">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30865-1188">New-AzStorageContext</span></span>
* <span data-ttu-id="30865-1189">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="30865-1189">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="30865-1190">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30865-1190">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="30865-1191">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="30865-1191">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="30865-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1192">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="30865-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1193">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="30865-1194">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="30865-1194">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="30865-1195">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30865-1195">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="30865-1196">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="30865-1196">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="30865-1197">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30865-1197">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="30865-1198">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="30865-1198">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="30865-1199">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1199">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="30865-1200">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="30865-1200">Highlights since the last major release</span></span>
* <span data-ttu-id="30865-1201">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="30865-1201">General availability of `Az` module</span></span>
* <span data-ttu-id="30865-1202">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="30865-1202">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="30865-1203">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="30865-1203">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="30865-1204">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1204">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="30865-1205">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="30865-1205">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30865-1206">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1206">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="30865-1207">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="30865-1207">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-1208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1208">Az.Automation</span></span>
* <span data-ttu-id="30865-1209">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="30865-1209">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="30865-1210">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="30865-1210">Dynamic grouping</span></span>
    * <span data-ttu-id="30865-1211">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="30865-1211">Pre-Post script</span></span>
    * <span data-ttu-id="30865-1212">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="30865-1212">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1213">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1213">Az.Compute</span></span>
* <span data-ttu-id="30865-1214">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="30865-1214">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="30865-1215">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="30865-1215">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30865-1216">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1216">Az.KeyVault</span></span>
* <span data-ttu-id="30865-1217">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1217">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1218">Az.Network</span></span>
* <span data-ttu-id="30865-1219">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1219">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="30865-1220">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="30865-1220">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1221">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1221">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-1222">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="30865-1222">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="30865-1223">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="30865-1223">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1224">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1224">Az.Resources</span></span>
* <span data-ttu-id="30865-1225">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="30865-1225">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="30865-1226">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="30865-1226">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1227">Az.Sql</span></span>
* <span data-ttu-id="30865-1228">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="30865-1228">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1229">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1229">Az.Storage</span></span>
* <span data-ttu-id="30865-1230">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30865-1230">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="30865-1231">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1231">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30865-1232">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1232">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30865-1233">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1233">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="30865-1234">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="30865-1234">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="30865-1235">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="30865-1235">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="30865-1236">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="30865-1236">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1237">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1237">Az.Websites</span></span>
* <span data-ttu-id="30865-1238">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="30865-1238">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="30865-1239">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1239">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-1240">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1240">Az.Accounts</span></span>
* <span data-ttu-id="30865-1241">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="30865-1241">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="30865-1242">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1242">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-1243">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1243">Az.Automation</span></span>
* <span data-ttu-id="30865-1244">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1244">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="30865-1245">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="30865-1245">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="30865-1246">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="30865-1246">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30865-1247">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-1247">Az.Cdn</span></span>
* <span data-ttu-id="30865-1248">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="30865-1248">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1249">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1249">Az.Compute</span></span>
* <span data-ttu-id="30865-1250">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="30865-1250">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-1251">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-1251">Az.DataFactory</span></span>
* <span data-ttu-id="30865-1252">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="30865-1252">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30865-1253">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30865-1253">Az.LogicApp</span></span>
* <span data-ttu-id="30865-1254">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="30865-1254">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1255">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1255">Az.Network</span></span>
* <span data-ttu-id="30865-1256">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="30865-1256">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1257">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1257">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-1258">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1258">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="30865-1259">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="30865-1259">SDK Update</span></span>
* <span data-ttu-id="30865-1260">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="30865-1260">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="30865-1261">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="30865-1261">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1262">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1262">Az.Resources</span></span>
* <span data-ttu-id="30865-1263">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="30865-1263">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="30865-1264">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="30865-1264">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="30865-1265">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="30865-1265">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="30865-1266">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="30865-1266">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="30865-1267">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="30865-1267">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="30865-1268">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="30865-1268">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1269">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1269">Az.Sql</span></span>
* <span data-ttu-id="30865-1270">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="30865-1270">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="30865-1271">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="30865-1271">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1272">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1272">Az.Storage</span></span>
* <span data-ttu-id="30865-1273">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1273">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="30865-1274">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1274">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="30865-1275">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30865-1275">Az.AnalysisServices</span></span>
* <span data-ttu-id="30865-1276">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="30865-1276">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1277">Az.Automation</span></span>
* <span data-ttu-id="30865-1278">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1278">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="30865-1279">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1279">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="30865-1280">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1280">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-1281">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-1281">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-1282">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="30865-1282">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1283">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1283">Az.Compute</span></span>
* <span data-ttu-id="30865-1284">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="30865-1284">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="30865-1285">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="30865-1285">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="30865-1286">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="30865-1286">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="30865-1287">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="30865-1287">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1288">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1288">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1289">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="30865-1289">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="30865-1290">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="30865-1290">Az.EventHub</span></span>
* <span data-ttu-id="30865-1291">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="30865-1291">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="30865-1292">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1292">Az.KeyVault</span></span>
* <span data-ttu-id="30865-1293">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="30865-1293">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30865-1294">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30865-1294">Az.LogicApp</span></span>
* <span data-ttu-id="30865-1295">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="30865-1295">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="30865-1296">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="30865-1296">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="30865-1297">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="30865-1297">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="30865-1298">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30865-1298">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30865-1299">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30865-1299">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30865-1300">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30865-1300">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="30865-1301">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="30865-1301">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="30865-1302">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="30865-1302">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="30865-1303">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1303">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30865-1304">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1304">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30865-1305">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1305">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="30865-1306">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1306">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="30865-1307">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="30865-1307">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="30865-1308">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-1308">Az.Monitor</span></span>
* <span data-ttu-id="30865-1309">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="30865-1309">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1310">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1310">Az.Network</span></span>
* <span data-ttu-id="30865-1311">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="30865-1311">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="30865-1312">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-1312">Az.OperationalInsights</span></span>
* <span data-ttu-id="30865-1313">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="30865-1313">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="30865-1314">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="30865-1314">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="30865-1315">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="30865-1315">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="30865-1316">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1316">Az.Resources</span></span>
* <span data-ttu-id="30865-1317">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="30865-1317">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="30865-1318">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="30865-1318">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="30865-1319">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="30865-1319">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="30865-1320">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="30865-1320">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1321">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1321">Az.Sql</span></span>
* <span data-ttu-id="30865-1322">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="30865-1322">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="30865-1323">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="30865-1323">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1324">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1324">Az.Websites</span></span>
* <span data-ttu-id="30865-1325">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="30865-1325">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="30865-1326">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1326">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-1327">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1327">Az.Accounts</span></span>
* <span data-ttu-id="30865-1328">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="30865-1328">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30865-1329">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30865-1329">Az.AnalysisServices</span></span>
<span data-ttu-id="30865-1330">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="30865-1330">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1331">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1331">Az.Compute</span></span>
* <span data-ttu-id="30865-1332">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="30865-1332">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="30865-1333">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="30865-1333">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="30865-1334">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="30865-1334">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1335">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1335">Az.RecoveryServices</span></span>
<span data-ttu-id="30865-1336">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="30865-1336">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1337">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1337">Az.Resources</span></span>
* <span data-ttu-id="30865-1338">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="30865-1338">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="30865-1339">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="30865-1339">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="30865-1340">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="30865-1340">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="30865-1341">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="30865-1341">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1342">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1342">Az.Sql</span></span>
* <span data-ttu-id="30865-1343">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="30865-1343">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="30865-1344">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="30865-1344">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="30865-1345">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="30865-1345">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="30865-1346">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1346">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-1347">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1347">Az.Accounts</span></span>
* <span data-ttu-id="30865-1348">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="30865-1348">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="30865-1349">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="30865-1349">Az.AnalysisServices</span></span>
* <span data-ttu-id="30865-1350">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="30865-1350">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1351">Az.RecoveryServices</span></span>
* <span data-ttu-id="30865-1352">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="30865-1352">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="30865-1353">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1353">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-1354">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1354">Az.Accounts</span></span>
* <span data-ttu-id="30865-1355">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="30865-1355">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="30865-1356">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1356">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30865-1357">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="30865-1357">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="30865-1358">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="30865-1358">Az.Aks</span></span>
* <span data-ttu-id="30865-1359">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1359">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="30865-1360">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1360">Az.Automation</span></span>
* <span data-ttu-id="30865-1361">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="30865-1361">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="30865-1362">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1362">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="30865-1363">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="30865-1363">Az.Cdn</span></span>
* <span data-ttu-id="30865-1364">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1364">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1365">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1365">Az.Compute</span></span>
* <span data-ttu-id="30865-1366">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="30865-1366">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="30865-1367">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="30865-1367">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="30865-1368">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="30865-1368">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="30865-1369">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30865-1369">Az.ContainerRegistry</span></span>
* <span data-ttu-id="30865-1370">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1370">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="30865-1371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="30865-1371">Az.DataFactory</span></span>
* <span data-ttu-id="30865-1372">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="30865-1372">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1373">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1373">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1374">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="30865-1374">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="30865-1375">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="30865-1375">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="30865-1376">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1376">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-1377">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-1377">Az.IotHub</span></span>
* <span data-ttu-id="30865-1378">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="30865-1378">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="30865-1379">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1379">Az.KeyVault</span></span>
* <span data-ttu-id="30865-1380">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1380">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1381">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1381">Az.Network</span></span>
* <span data-ttu-id="30865-1382">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1382">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1383">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1383">Az.Resources</span></span>
* <span data-ttu-id="30865-1384">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="30865-1384">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="30865-1385">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="30865-1385">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="30865-1386">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="30865-1386">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="30865-1387">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="30865-1387">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="30865-1388">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="30865-1388">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="30865-1389">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="30865-1389">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="30865-1390">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="30865-1390">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-1391">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-1391">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-1392">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="30865-1392">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="30865-1393">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="30865-1393">Fix some error messages.</span></span>
* <span data-ttu-id="30865-1394">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="30865-1394">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="30865-1395">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="30865-1395">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30865-1396">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30865-1396">Az.SignalR</span></span>
* <span data-ttu-id="30865-1397">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1397">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1398">Az.Sql</span></span>
* <span data-ttu-id="30865-1399">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1399">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30865-1400">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="30865-1400">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="30865-1401">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="30865-1401">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="30865-1402">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="30865-1402">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1403">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1403">Az.Storage</span></span>
* <span data-ttu-id="30865-1404">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1404">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30865-1405">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="30865-1405">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="30865-1406">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="30865-1406">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="30865-1407">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="30865-1407">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="30865-1408">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="30865-1408">Az.TrafficManager</span></span>
* <span data-ttu-id="30865-1409">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1409">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1410">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1410">Az.Websites</span></span>
* <span data-ttu-id="30865-1411">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="30865-1411">Update incorrect online help URLs</span></span>
* <span data-ttu-id="30865-1412">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-1412">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="30865-1413">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="30865-1413">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="30865-1414">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="30865-1414">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="30865-1415">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1415">Az.Accounts</span></span>
* <span data-ttu-id="30865-1416">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="30865-1416">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1417">Az.Compute</span></span>
* <span data-ttu-id="30865-1418">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="30865-1418">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="30865-1419">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="30865-1419">Updated the description of ID in help files</span></span>
* <span data-ttu-id="30865-1420">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1420">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1421">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1421">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1422">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="30865-1422">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="30865-1423">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="30865-1423">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="30865-1424">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="30865-1424">Az.EventGrid</span></span>
* <span data-ttu-id="30865-1425">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="30865-1425">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="30865-1426">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="30865-1426">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="30865-1427">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="30865-1427">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="30865-1428">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="30865-1428">Event Time-To-Live,</span></span>
        - <span data-ttu-id="30865-1429">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="30865-1429">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="30865-1430">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="30865-1430">Dead letter endpoint.</span></span>
    - <span data-ttu-id="30865-1431">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="30865-1431">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="30865-1432">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="30865-1432">Event Time-To-Live,</span></span>
        - <span data-ttu-id="30865-1433">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="30865-1433">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="30865-1434">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="30865-1434">Dead letter endpoint.</span></span>
* <span data-ttu-id="30865-1435">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="30865-1435">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="30865-1436">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="30865-1436">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="30865-1437">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-1437">Az.IotHub</span></span>
* <span data-ttu-id="30865-1438">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="30865-1438">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="30865-1439">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="30865-1439">Az.LogicApp</span></span>
* <span data-ttu-id="30865-1440">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="30865-1440">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1441">Az.Resources</span></span>
* <span data-ttu-id="30865-1442">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="30865-1442">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="30865-1443">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="30865-1443">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="30865-1444">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30865-1444">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="30865-1445">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="30865-1445">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="30865-1446">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="30865-1446">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="30865-1447">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="30865-1447">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="30865-1448">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="30865-1448">Az.SignalR</span></span>
* <span data-ttu-id="30865-1449">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1449">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1450">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1450">Az.Sql</span></span>
* <span data-ttu-id="30865-1451">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="30865-1451">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="30865-1452">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1452">Az.Storage</span></span>
* <span data-ttu-id="30865-1453">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="30865-1453">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="30865-1454">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="30865-1454">New-AzStorageContext</span></span>
* <span data-ttu-id="30865-1455">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="30865-1455">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="30865-1456">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="30865-1456">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1457">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1457">Az.Websites</span></span>
* <span data-ttu-id="30865-1458">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="30865-1458">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="30865-1459">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1459">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="30865-1460">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1460">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="30865-1461">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-1461">General</span></span>

- <span data-ttu-id="30865-1462">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="30865-1462">General Availability of Az Module</span></span>
- <span data-ttu-id="30865-1463">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="30865-1463">Online help for each module</span></span>
- <span data-ttu-id="30865-1464">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="30865-1464">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="30865-1465">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="30865-1465">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="30865-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1466">Az.Accounts</span></span>
- <span data-ttu-id="30865-1467">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30865-1467">Changed from Az.Profile</span></span>
- <span data-ttu-id="30865-1468">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="30865-1468">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="30865-1469">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-1469">Az.ApiManagement</span></span>
- <span data-ttu-id="30865-1470">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="30865-1470">Fixes for #7002</span></span>
- <span data-ttu-id="30865-1471">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1471">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="30865-1472">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="30865-1472">Az.Batch</span></span>
- <span data-ttu-id="30865-1473">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="30865-1473">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="30865-1474">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="30865-1474">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="30865-1475">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1475">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="30865-1476">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="30865-1476">Az.Billing</span></span>
- <span data-ttu-id="30865-1477">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1477">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="30865-1478">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="30865-1478">Az.CognitivServices</span></span>
- <span data-ttu-id="30865-1479">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1479">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="30865-1480">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="30865-1480">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="30865-1481">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1481">Az.ContainerInstance</span></span>
- <span data-ttu-id="30865-1482">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="30865-1482">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="30865-1483">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="30865-1483">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="30865-1484">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1484">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="30865-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1485">Az.DataLakeStore</span></span>
- <span data-ttu-id="30865-1486">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1486">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="30865-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="30865-1487">Az.Monitor</span></span>
- <span data-ttu-id="30865-1488">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1488">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="30865-1489">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="30865-1489">Az.KeyVault</span></span>
- <span data-ttu-id="30865-1490">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="30865-1490">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="30865-1491">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="30865-1491">Az.MachineLearning</span></span>
- <span data-ttu-id="30865-1492">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="30865-1492">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="30865-1493">Az.Media</span><span class="sxs-lookup"><span data-stu-id="30865-1493">Az.Media</span></span>
- <span data-ttu-id="30865-1494">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="30865-1494">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="30865-1495">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1495">Az.Network</span></span>
<span data-ttu-id="30865-1496">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="30865-1496">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="30865-1497">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="30865-1497">New cmdlets added:</span></span>
        - <span data-ttu-id="30865-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1498">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1499">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1500">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1501">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1502">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1503">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="30865-1503">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="30865-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="30865-1504">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="30865-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="30865-1505">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="30865-1506">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="30865-1506">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="30865-1507">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30865-1507">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="30865-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="30865-1508">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="30865-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="30865-1509">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="30865-1510">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1510">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="30865-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1511">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="30865-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="30865-1512">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="30865-1513">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="30865-1513">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="30865-1514">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30865-1514">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="30865-1515">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30865-1515">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="30865-1516">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30865-1516">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="30865-1517">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="30865-1517">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="30865-1518">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1518">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="30865-1519">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="30865-1519">Az.OperationalInsights</span></span>
- <span data-ttu-id="30865-1520">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1520">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="30865-1521">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30865-1521">Az.Profile</span></span>
- <span data-ttu-id="30865-1522">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="30865-1522">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1523">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1523">Az.RecoveryServices</span></span>
- <span data-ttu-id="30865-1524">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1524">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="30865-1525">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1525">Az.Resources</span></span>
- <span data-ttu-id="30865-1526">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1526">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="30865-1527">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-1527">Az.ServiceFabric</span></span>
- <span data-ttu-id="30865-1528">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="30865-1528">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="30865-1529">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1529">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="30865-1530">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="30865-1530">Az.SIgnalR</span></span>
- <span data-ttu-id="30865-1531">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="30865-1531">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="30865-1532">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1532">Az.Sql</span></span>
- <span data-ttu-id="30865-1533">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="30865-1533">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="30865-1534">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1534">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="30865-1535">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1535">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="30865-1536">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1536">Az.Storage</span></span>
- <span data-ttu-id="30865-1537">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1537">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="30865-1538">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1538">Az.Websites</span></span>
- <span data-ttu-id="30865-1539">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="30865-1539">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="30865-1540">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1540">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="30865-1541">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-1541">General</span></span>

* <span data-ttu-id="30865-1542">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="30865-1542">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="30865-1543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1543">Az.Compute</span></span>

* <span data-ttu-id="30865-1544">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="30865-1544">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="30865-1545">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1545">Az.DataLakeStore</span></span>

* <span data-ttu-id="30865-1546">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="30865-1546">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="30865-1547">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="30865-1547">Az.FrontDoor</span></span>

* <span data-ttu-id="30865-1548">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="30865-1548">Fixed some broken links</span></span>
    - <span data-ttu-id="30865-1549">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="30865-1549">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="30865-1550">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="30865-1550">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="30865-1551">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="30865-1551">Az.RecoveryServices</span></span>

* <span data-ttu-id="30865-1552">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-1552">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="30865-1553">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="30865-1553">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="30865-1554">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1554">Az.Resources</span></span>

* <span data-ttu-id="30865-1555">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="30865-1555">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="30865-1556">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="30865-1556">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="30865-1557">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1557">Az.Sql</span></span>

* <span data-ttu-id="30865-1558">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="30865-1558">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="30865-1559">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="30865-1559">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="30865-1560">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="30865-1560">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="30865-1561">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1561">Az.Storage</span></span>

* <span data-ttu-id="30865-1562">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1562">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="30865-1563">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="30865-1563">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="30865-1564">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="30865-1564">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="30865-1565">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="30865-1565">Support Static Website configuration</span></span>
    - <span data-ttu-id="30865-1566">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30865-1566">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="30865-1567">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="30865-1567">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="30865-1568">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1568">Az.Websites</span></span>

* <span data-ttu-id="30865-1569">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="30865-1569">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="30865-1570">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="30865-1570">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="30865-1571">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="30865-1571">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="30865-1572">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1572">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="30865-1573">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="30865-1573">Az.ApiManagement</span></span>
* <span data-ttu-id="30865-1574">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="30865-1574">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="30865-1575">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="30865-1575">Az.Automation</span></span>
* <span data-ttu-id="30865-1576">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="30865-1576">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="30865-1577">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="30865-1577">Added Update Management cmdlets</span></span>
* <span data-ttu-id="30865-1578">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="30865-1578">Added Source Control cmdlets</span></span>
* <span data-ttu-id="30865-1579">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="30865-1579">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="30865-1580">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="30865-1580">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="30865-1581">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1581">Az.Compute</span></span>
* <span data-ttu-id="30865-1582">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="30865-1582">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="30865-1583">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="30865-1583">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="30865-1584">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1584">Az.ContainerInstance</span></span>
* <span data-ttu-id="30865-1585">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="30865-1585">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="30865-1586">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="30865-1586">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="30865-1587">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="30865-1587">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="30865-1588">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1588">Az.Network</span></span>
* <span data-ttu-id="30865-1589">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="30865-1589">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="30865-1590">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="30865-1590">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="30865-1591">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="30865-1591">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="30865-1592">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="30865-1592">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="30865-1593">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="30865-1593">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="30865-1594">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="30865-1594">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="30865-1595">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="30865-1595">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="30865-1596">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="30865-1596">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="30865-1597">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="30865-1597">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="30865-1598">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="30865-1598">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="30865-1599">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="30865-1599">Az.Relay</span></span>
* <span data-ttu-id="30865-1600">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="30865-1600">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="30865-1601">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1601">Az.Resources</span></span>
* <span data-ttu-id="30865-1602">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="30865-1602">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="30865-1603">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="30865-1603">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="30865-1604">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="30865-1604">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="30865-1605">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-1605">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-1606">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="30865-1606">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="30865-1607">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1607">Az.Sql</span></span>
* <span data-ttu-id="30865-1608">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="30865-1608">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="30865-1609">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1609">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30865-1610">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1610">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30865-1611">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1611">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30865-1612">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="30865-1612">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="30865-1613">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="30865-1613">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30865-1614">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="30865-1614">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30865-1615">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="30865-1615">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="30865-1616">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="30865-1616">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="30865-1617">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="30865-1617">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="30865-1618">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="30865-1618">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="30865-1619">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="30865-1619">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="30865-1620">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="30865-1620">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="30865-1621">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="30865-1621">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="30865-1622">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="30865-1622">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="30865-1623">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="30865-1623">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="30865-1624">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="30865-1624">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="30865-1625">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1625">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="30865-1626">Generale</span><span class="sxs-lookup"><span data-stu-id="30865-1626">General</span></span>
* <span data-ttu-id="30865-1627">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="30865-1627">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="30865-1628">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30865-1628">Az.Profile</span></span>
* <span data-ttu-id="30865-1629">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="30865-1629">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="30865-1630">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="30865-1630">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="30865-1631">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="30865-1631">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="30865-1632">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="30865-1632">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="30865-1633">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="30865-1633">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="30865-1634">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="30865-1634">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="30865-1635">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="30865-1635">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-1636">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-1636">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-1637">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="30865-1637">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1638">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1638">Az.Compute</span></span>
* <span data-ttu-id="30865-1639">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="30865-1639">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="30865-1640">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="30865-1640">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="30865-1641">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="30865-1641">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1642">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1642">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1643">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="30865-1643">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="30865-1644">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="30865-1644">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="30865-1645">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="30865-1645">Az.Insights</span></span>
* <span data-ttu-id="30865-1646">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="30865-1646">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="30865-1647">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="30865-1647">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="30865-1648">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="30865-1648">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="30865-1649">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="30865-1649">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1650">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1650">Az.Network</span></span>
* <span data-ttu-id="30865-1651">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="30865-1651">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="30865-1652">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-1652">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="30865-1653">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="30865-1653">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="30865-1654">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="30865-1654">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="30865-1655">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="30865-1655">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="30865-1656">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="30865-1656">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="30865-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="30865-1657">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="30865-1658">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="30865-1658">Az.PolicyInsights</span></span>
* <span data-ttu-id="30865-1659">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="30865-1659">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1660">Az.Resources</span></span>
* <span data-ttu-id="30865-1661">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="30865-1661">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="30865-1662">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="30865-1662">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="30865-1663">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="30865-1663">Az.ServiceBus</span></span>
* <span data-ttu-id="30865-1664">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="30865-1664">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="30865-1665">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="30865-1665">Az.ServiceFabric</span></span>
* <span data-ttu-id="30865-1666">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="30865-1666">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="30865-1667">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="30865-1667">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="30865-1668">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="30865-1668">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="30865-1669">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="30865-1669">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="30865-1670">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="30865-1670">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="30865-1671">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1671">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="30865-1672">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="30865-1672">Az.Profile</span></span>
* <span data-ttu-id="30865-1673">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="30865-1673">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="30865-1674">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="30865-1674">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1675">Az.Compute</span></span>
* <span data-ttu-id="30865-1676">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="30865-1676">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="30865-1677">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30865-1677">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="30865-1678">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="30865-1678">Az.DataLakeStore</span></span>
* <span data-ttu-id="30865-1679">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="30865-1679">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="30865-1680">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30865-1680">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="30865-1681">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="30865-1681">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="30865-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="30865-1682">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="30865-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="30865-1683">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1684">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1684">Az.Network</span></span>
* <span data-ttu-id="30865-1685">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="30865-1685">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="30865-1686">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30865-1686">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1687">Az.Resources</span></span>
* <span data-ttu-id="30865-1688">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="30865-1688">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="30865-1689">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="30865-1689">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="30865-1690">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1690">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="30865-1691">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="30865-1691">Azure.Storage</span></span>
* <span data-ttu-id="30865-1692">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="30865-1692">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="30865-1693">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="30865-1693">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="30865-1694">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="30865-1694">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="30865-1695">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="30865-1695">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="30865-1696">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="30865-1696">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="30865-1697">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="30865-1697">Az.CognitiveServices</span></span>
* <span data-ttu-id="30865-1698">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="30865-1698">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="30865-1699">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="30865-1699">Az.Compute</span></span>
* <span data-ttu-id="30865-1700">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="30865-1700">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="30865-1701">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="30865-1701">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="30865-1702">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="30865-1702">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="30865-1703">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="30865-1703">Az.DataFactoryV2</span></span>
* <span data-ttu-id="30865-1704">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="30865-1704">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="30865-1705">Az.Network</span><span class="sxs-lookup"><span data-stu-id="30865-1705">Az.Network</span></span>
* <span data-ttu-id="30865-1706">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30865-1706">Added NetworkProfile functionality.</span></span> <span data-ttu-id="30865-1707">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="30865-1707">new cmdlets added</span></span>
    - <span data-ttu-id="30865-1708">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30865-1708">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="30865-1709">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30865-1709">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="30865-1710">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30865-1710">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="30865-1711">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="30865-1711">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="30865-1712">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1712">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="30865-1713">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1713">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="30865-1714">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="30865-1714">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="30865-1715">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="30865-1715">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="30865-1716">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="30865-1716">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="30865-1717">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="30865-1717">Az.RedisCache</span></span>
* <span data-ttu-id="30865-1718">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="30865-1718">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="30865-1719">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="30865-1719">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="30865-1720">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="30865-1720">Az.Resources</span></span>
* <span data-ttu-id="30865-1721">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="30865-1721">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="30865-1722">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="30865-1722">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="30865-1723">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="30865-1723">Az.Sql</span></span>
* <span data-ttu-id="30865-1724">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="30865-1724">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="30865-1725">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="30865-1725">Az.Websites</span></span>
* <span data-ttu-id="30865-1726">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="30865-1726">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="30865-1727">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="30865-1727">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="30865-1728">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="30865-1728">0.2.0 - September 2018</span></span>
 <span data-ttu-id="30865-1729">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="30865-1729">Initial Release</span></span>
