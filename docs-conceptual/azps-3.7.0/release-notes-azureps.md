---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: 9e60e76206127922902804112e0b3f837cf03d76
ms.sourcegitcommit: eeb720e053939a68873ae3973bc81d5826358c9f
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/31/2020
ms.locfileid: "80440504"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="53f32-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="53f32-103">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="53f32-104">3.7.0 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="53f32-104">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-105">Az.Accounts</span></span>
* <span data-ttu-id="53f32-106">Correzione dell'eccezione NullReferenceException generata da 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' in caso di mancato accesso [#10292]</span><span class="sxs-lookup"><span data-stu-id="53f32-106">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-107">Az.Compute</span></span>
* <span data-ttu-id="53f32-108">Aggiunta dei parametri seguenti al cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="53f32-108">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="53f32-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="53f32-109">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="53f32-110">Proprietà Encryption consentita per il parametro Target del cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="53f32-110">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="53f32-111">Correzione del problema tempDisk per i cmdlet 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="53f32-111">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="53f32-112">[#11354]</span><span class="sxs-lookup"><span data-stu-id="53f32-112">[#11354]</span></span>
* <span data-ttu-id="53f32-113">Aggiunta del supporto dei cmdlet seguenti per la nuova estensione SAP</span><span class="sxs-lookup"><span data-stu-id="53f32-113">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="53f32-114">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="53f32-114">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="53f32-115">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="53f32-115">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="53f32-116">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="53f32-116">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="53f32-117">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="53f32-117">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="53f32-118">Correzione di errori negli esempi del documento della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-118">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="53f32-119">Visualizzazione del valore stringa esatto per PowerState VM nel formato tabella.</span><span class="sxs-lookup"><span data-stu-id="53f32-119">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="53f32-120">'New-AzVmssConfig': correzione della serializzazione della proprietà AutomaticRepairs quando SinglePlacementGroup è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="53f32-120">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="53f32-121">[#11257]</span><span class="sxs-lookup"><span data-stu-id="53f32-121">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-122">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-122">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-123">Aggiornamento di ADF .NET SDK alla versione 4.8.0</span><span class="sxs-lookup"><span data-stu-id="53f32-123">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="53f32-124">Aggiunta di parametri facoltativi al comando 'Invoke-AzDataFactoryV2Pipeline' per supportare la riesecuzione</span><span class="sxs-lookup"><span data-stu-id="53f32-124">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-125">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-125">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-126">Aggiunta della descrizione della modifica di rilievo per 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="53f32-126">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="53f32-127">Aggiunta dell'opzione di codifica Byte per 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="53f32-127">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-128">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-128">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-129">Supporto della versione minima supportata di TLS durante la creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="53f32-129">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-130">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-130">Az.IotHub</span></span>
* <span data-ttu-id="53f32-131">Aggiunta del supporto per gestire le impostazioni distribuite per singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53f32-131">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="53f32-132">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="53f32-133">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="53f32-133">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="53f32-134">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="53f32-134">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-135">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-135">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-136">Aggiunta degli attributi della modifica di rilievo a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="53f32-136">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-137">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-137">Az.Monitor</span></span>
* <span data-ttu-id="53f32-138">Documentazione aggiornata per 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="53f32-138">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-139">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-139">Az.Network</span></span>
* <span data-ttu-id="53f32-140">Aggiornamento dei cmdlet per consentire VirtualHubVnetConnections tra tenant</span><span class="sxs-lookup"><span data-stu-id="53f32-140">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="53f32-141">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="53f32-141">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="53f32-142">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="53f32-142">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="53f32-143">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="53f32-143">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="53f32-144">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="53f32-144">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="53f32-145">Rimozione della dipendenza di SQL Management SDK</span><span class="sxs-lookup"><span data-stu-id="53f32-145">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-146">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-146">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-147">Miglioramento dei messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="53f32-147">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-148">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-148">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-149">Azure Site Recovery: aggiunto il supporto per la riprotezione e aggiornamento delle proprietà delle VM per le macchine virtuali con crittografia dischi di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-149">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="53f32-150">Azure Site Recovery: aggiunta del monitoraggio per il ripristino di emergenza nelle proprietà VmwareToAzure</span><span class="sxs-lookup"><span data-stu-id="53f32-150">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="53f32-151">Backup di Azure: aggiunta del supporto per la ripetizione dell'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="53f32-151">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="53f32-152">Backup di Azure: aggiunta del supporto per le impostazioni di esclusione disco durante il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="53f32-152">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="53f32-153">Backup di Azure: aggiunta del supporto per il ripristino di più file/cartelle in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="53f32-153">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="53f32-154">Backup di Azure: aggiunta del supporto per il gruppo di risorse specificato dall'utente durante l'aggiornamento dei criteri IaasVM</span><span class="sxs-lookup"><span data-stu-id="53f32-154">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-155">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-155">Az.Resources</span></span>
* <span data-ttu-id="53f32-156">Correzione di 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' per l'utilizzo del valore effettivo di apiVersion per le risorse invece di quello predefinito [#11267]</span><span class="sxs-lookup"><span data-stu-id="53f32-156">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="53f32-157">Aggiunta della registrazione di correlationId per gli scenari di errore</span><span class="sxs-lookup"><span data-stu-id="53f32-157">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="53f32-158">Modifica di lieve entità alla documentazione di 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="53f32-158">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="53f32-159">Aggiunta dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="53f32-159">Added example.</span></span>
* <span data-ttu-id="53f32-160">Aggiunta della virgoletta singola come carattere di escape nel valore di parametro 'Get-AzADUser' [#11317]</span><span class="sxs-lookup"><span data-stu-id="53f32-160">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="53f32-161">Aggiunta di nuovi cmdlet per gli script di distribuzione ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="53f32-161">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-162">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-162">Az.Sql</span></span>
* <span data-ttu-id="53f32-163">Aggiunta del parametro secondario leggibile a 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="53f32-163">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="53f32-164">Aggiunta del cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="53f32-164">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="53f32-165">Salvataggio della classificazione di riservatezza durante la classificazione delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="53f32-165">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="53f32-166">Az.Support</span><span class="sxs-lookup"><span data-stu-id="53f32-166">Az.Support</span></span>
* <span data-ttu-id="53f32-167">Disponibilità generale del modulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="53f32-167">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-168">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-168">Az.Websites</span></span>
* <span data-ttu-id="53f32-169">Aggiunta del supporto per l'uso delle regole di gestione del traffico delle app Web con i nuovi cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="53f32-169">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="53f32-170">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="53f32-170">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="53f32-171">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="53f32-171">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="53f32-172">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="53f32-172">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="53f32-173">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="53f32-173">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="53f32-174">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="53f32-174">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-175">Az.Accounts</span></span>
* <span data-ttu-id="53f32-176">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="53f32-176">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="53f32-177">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="53f32-177">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="53f32-178">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="53f32-178">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53f32-179">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-179">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-180">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="53f32-180">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="53f32-181">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="53f32-181">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="53f32-182">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="53f32-182">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="53f32-183">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="53f32-183">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-184">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-184">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-185">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="53f32-185">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-186">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-186">Az.IotHub</span></span>
* <span data-ttu-id="53f32-187">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-187">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="53f32-188">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-188">New Cmdlets are:</span></span>
    - <span data-ttu-id="53f32-189">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-189">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-190">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-190">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-191">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-191">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-192">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-192">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="53f32-193">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-193">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="53f32-194">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-194">New Cmdlets are:</span></span>
    - <span data-ttu-id="53f32-195">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="53f32-195">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="53f32-196">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="53f32-196">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="53f32-197">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="53f32-197">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="53f32-198">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="53f32-198">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="53f32-199">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-199">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="53f32-200">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-200">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="53f32-201">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-201">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="53f32-202">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-202">New Cmdlets are:</span></span>
    - <span data-ttu-id="53f32-203">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="53f32-203">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="53f32-204">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="53f32-204">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="53f32-205">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="53f32-205">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-206">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-206">Az.Monitor</span></span>
* <span data-ttu-id="53f32-207">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="53f32-207">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-208">Az.Network</span></span>
* <span data-ttu-id="53f32-209">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="53f32-209">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="53f32-210">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="53f32-210">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="53f32-211">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="53f32-211">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="53f32-212">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="53f32-212">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-213">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-213">Az.Resources</span></span>
* <span data-ttu-id="53f32-214">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="53f32-214">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="53f32-215">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="53f32-215">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="53f32-216">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="53f32-216">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="53f32-217">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="53f32-217">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="53f32-218">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="53f32-218">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="53f32-219">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="53f32-219">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="53f32-220">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="53f32-220">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="53f32-221">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-221">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="53f32-222">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-222">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="53f32-223">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-223">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="53f32-224">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-224">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="53f32-225">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="53f32-225">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="53f32-226">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-226">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="53f32-227">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="53f32-227">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-228">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-228">Az.Sql</span></span>
* <span data-ttu-id="53f32-229">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="53f32-229">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="53f32-230">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="53f32-230">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="53f32-231">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="53f32-231">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="53f32-232">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="53f32-232">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="53f32-233">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="53f32-233">Remove an LTR backup</span></span>
    - <span data-ttu-id="53f32-234">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="53f32-234">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="53f32-235">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="53f32-235">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="53f32-236">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-236">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="53f32-237">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-237">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-238">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-238">Az.Storage</span></span>
* <span data-ttu-id="53f32-239">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-239">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="53f32-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="53f32-240">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="53f32-241">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="53f32-241">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="53f32-242">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="53f32-242">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="53f32-243">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="53f32-243">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-244">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-244">Az.Websites</span></span>
* <span data-ttu-id="53f32-245">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="53f32-245">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="53f32-246">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="53f32-246">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="53f32-247">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="53f32-247">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="53f32-248">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="53f32-248">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="53f32-249">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="53f32-249">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="53f32-250">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="53f32-250">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-251">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-251">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-252">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="53f32-252">Updated client side telemetry.</span></span>
* <span data-ttu-id="53f32-253">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="53f32-253">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="53f32-254">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="53f32-254">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-255">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-255">Az.Accounts</span></span>
* <span data-ttu-id="53f32-256">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="53f32-256">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-257">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-257">Az.Automation</span></span>
* <span data-ttu-id="53f32-258">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="53f32-258">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-259">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-259">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-260">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="53f32-260">Updated SDK to 7.0</span></span>
* <span data-ttu-id="53f32-261">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="53f32-261">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-262">Az.Compute</span></span>
* <span data-ttu-id="53f32-263">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="53f32-263">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-264">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-264">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-265">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="53f32-265">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-266">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-266">Az.IotHub</span></span>
* <span data-ttu-id="53f32-267">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-267">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="53f32-268">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-268">New Cmdlets are:</span></span>
    - <span data-ttu-id="53f32-269">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-269">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-270">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-270">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-271">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-271">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="53f32-272">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="53f32-272">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-273">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-273">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-274">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="53f32-274">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-275">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-275">Az.Monitor</span></span>
* <span data-ttu-id="53f32-276">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="53f32-276">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="53f32-277">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="53f32-277">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="53f32-278">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="53f32-278">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-279">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-279">Az.Network</span></span>
* <span data-ttu-id="53f32-280">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="53f32-280">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="53f32-281">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="53f32-281">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="53f32-282">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="53f32-282">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="53f32-283">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-283">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="53f32-284">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="53f32-284">No new cmdlets are added.</span></span> <span data-ttu-id="53f32-285">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-285">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-286">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-286">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-287">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="53f32-287">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-288">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-288">Az.Resources</span></span>
* <span data-ttu-id="53f32-289">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="53f32-289">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="53f32-290">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53f32-290">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="53f32-291">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="53f32-291">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="53f32-292">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="53f32-292">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="53f32-293">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="53f32-293">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="53f32-294">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="53f32-294">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="53f32-295">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="53f32-295">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="53f32-296">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-296">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-297">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-297">Az.Sql</span></span>
* <span data-ttu-id="53f32-298">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="53f32-298">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="53f32-299">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="53f32-299">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="53f32-300">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="53f32-300">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="53f32-301">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="53f32-301">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="53f32-302">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="53f32-302">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53f32-303">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53f32-303">Az.StorageSync</span></span>
* <span data-ttu-id="53f32-304">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="53f32-304">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="53f32-305">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="53f32-305">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-306">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-306">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-307">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="53f32-307">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="53f32-308">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="53f32-308">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-309">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-309">Az.Accounts</span></span>
* <span data-ttu-id="53f32-310">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="53f32-310">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="53f32-311">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="53f32-311">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53f32-312">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-312">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-313">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="53f32-313">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="53f32-314">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="53f32-314">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="53f32-315">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="53f32-315">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="53f32-316">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-316">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-317">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-317">Az.Compute</span></span>
* <span data-ttu-id="53f32-318">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53f32-318">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="53f32-319">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="53f32-319">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="53f32-320">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f32-320">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="53f32-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-321">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="53f32-322">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="53f32-322">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-323">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-323">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-324">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="53f32-324">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="53f32-325">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="53f32-325">Az.DeploymentManager</span></span>
* <span data-ttu-id="53f32-326">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="53f32-326">Adds LIST operations for resources</span></span>
* <span data-ttu-id="53f32-327">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="53f32-327">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-328">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-328">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-329">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="53f32-329">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-330">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-330">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-331">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="53f32-331">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-332">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-332">Az.Network</span></span>
* <span data-ttu-id="53f32-333">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="53f32-333">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="53f32-334">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="53f32-334">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="53f32-335">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="53f32-335">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="53f32-336">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="53f32-336">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="53f32-337">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="53f32-337">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="53f32-338">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="53f32-338">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="53f32-339">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="53f32-339">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="53f32-340">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="53f32-340">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="53f32-341">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-341">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-342">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="53f32-343">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-343">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="53f32-344">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="53f32-344">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="53f32-345">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="53f32-345">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-346">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-346">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-347">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="53f32-347">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="53f32-348">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="53f32-348">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="53f32-349">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="53f32-349">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="53f32-350">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="53f32-350">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-351">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-351">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-352">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="53f32-352">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="53f32-353">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="53f32-353">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-354">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-354">Az.Resources</span></span>
* <span data-ttu-id="53f32-355">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="53f32-355">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="53f32-356">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="53f32-356">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-357">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-357">Az.Sql</span></span>
<span data-ttu-id="53f32-358">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="53f32-358">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-359">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-359">Az.Storage</span></span>
* <span data-ttu-id="53f32-360">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="53f32-360">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="53f32-361">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-361">New-AzStorageAccount</span></span>
* <span data-ttu-id="53f32-362">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="53f32-362">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="53f32-363">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-363">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-364">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-364">Az.Websites</span></span>
* <span data-ttu-id="53f32-365">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="53f32-365">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="53f32-366">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="53f32-366">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="53f32-367">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="53f32-367">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-368">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-368">Az.Accounts</span></span>
* <span data-ttu-id="53f32-369">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53f32-369">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-370">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-370">Az.Cdn</span></span>
* <span data-ttu-id="53f32-371">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-371">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-372">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-372">Az.Compute</span></span>
* <span data-ttu-id="53f32-373">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53f32-373">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="53f32-374">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-374">Az.ContainerInstance</span></span>
* <span data-ttu-id="53f32-375">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-375">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="53f32-376">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="53f32-376">Az.DataBoxEdge</span></span>
* <span data-ttu-id="53f32-377">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="53f32-377">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="53f32-378">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-378">Get the Edge Storage Container</span></span>
* <span data-ttu-id="53f32-379">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="53f32-379">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="53f32-380">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-380">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="53f32-381">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="53f32-381">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="53f32-382">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-382">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="53f32-383">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="53f32-383">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="53f32-384">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-384">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="53f32-385">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="53f32-385">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="53f32-386">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-386">Get the Edge Storage Account</span></span>
* <span data-ttu-id="53f32-387">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="53f32-387">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="53f32-388">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-388">Create new Edge Storage Account</span></span>
* <span data-ttu-id="53f32-389">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="53f32-389">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="53f32-390">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="53f32-390">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="53f32-391">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="53f32-391">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="53f32-392">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="53f32-392">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="53f32-393">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="53f32-393">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="53f32-394">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="53f32-394">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-395">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-395">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-396">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="53f32-396">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="53f32-397">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="53f32-397">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="53f32-398">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="53f32-398">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="53f32-399">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="53f32-399">Az.DevTestLabs</span></span>
* <span data-ttu-id="53f32-400">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="53f32-400">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-401">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-401">Az.EventHub</span></span>
* <span data-ttu-id="53f32-402">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="53f32-402">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-403">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-403">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-404">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="53f32-404">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="53f32-405">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="53f32-405">Az.MachineLearning</span></span>
* <span data-ttu-id="53f32-406">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="53f32-406">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="53f32-407">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="53f32-407">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="53f32-408">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="53f32-408">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="53f32-409">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="53f32-409">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="53f32-410">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="53f32-410">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="53f32-411">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="53f32-411">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="53f32-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="53f32-412">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="53f32-413">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="53f32-413">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-414">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-414">Az.Network</span></span>
* <span data-ttu-id="53f32-415">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="53f32-415">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-417">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-417">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="53f32-418">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-418">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="53f32-419">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-419">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="53f32-420">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-420">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-421">Az.Resources</span></span>
* <span data-ttu-id="53f32-422">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="53f32-422">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-423">Az.Sql</span></span>
* <span data-ttu-id="53f32-424">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="53f32-424">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="53f32-425">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="53f32-425">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="53f32-426">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="53f32-426">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="53f32-427">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="53f32-427">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-428">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-428">Az.Storage</span></span>
* <span data-ttu-id="53f32-429">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="53f32-429">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="53f32-430">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-430">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="53f32-431">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="53f32-431">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="53f32-432">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-432">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="53f32-433">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-433">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="53f32-434">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-434">General</span></span>
* <span data-ttu-id="53f32-435">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="53f32-435">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-436">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-436">Az.Accounts</span></span>
* <span data-ttu-id="53f32-437">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="53f32-437">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="53f32-438">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="53f32-438">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53f32-439">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-439">Az.Batch</span></span>
* <span data-ttu-id="53f32-440">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="53f32-440">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-441">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-441">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-442">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="53f32-442">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-443">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-443">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-444">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="53f32-444">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="53f32-445">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="53f32-445">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="53f32-446">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="53f32-446">Az.HealthcareApis</span></span>
* <span data-ttu-id="53f32-447">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="53f32-447">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-448">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-448">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-449">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="53f32-449">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="53f32-450">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="53f32-450">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="53f32-451">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="53f32-451">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-452">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-452">Az.Monitor</span></span>
* <span data-ttu-id="53f32-453">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="53f32-453">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="53f32-454">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="53f32-454">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="53f32-455">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="53f32-455">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-456">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-456">Az.Network</span></span>
* <span data-ttu-id="53f32-457">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="53f32-457">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-458">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-458">Az.Resources</span></span>
* <span data-ttu-id="53f32-459">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="53f32-459">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="53f32-460">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="53f32-460">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-461">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-461">Az.Sql</span></span>
* <span data-ttu-id="53f32-462">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="53f32-462">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-463">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-463">Az.Storage</span></span>
* <span data-ttu-id="53f32-464">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="53f32-464">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="53f32-465">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="53f32-465">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="53f32-466">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="53f32-466">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="53f32-467">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="53f32-467">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="53f32-468">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="53f32-468">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="53f32-469">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="53f32-469">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="53f32-470">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="53f32-470">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="53f32-471">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-471">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="53f32-472">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-472">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="53f32-473">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="53f32-473">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="53f32-474">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="53f32-474">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="53f32-475">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="53f32-475">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="53f32-476">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="53f32-476">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="53f32-477">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-477">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-478">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-478">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-479">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-479">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="53f32-480">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-480">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-481">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-481">Az.Compute</span></span>
* <span data-ttu-id="53f32-482">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-482">VM Reapply feature</span></span>
    - <span data-ttu-id="53f32-483">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="53f32-483">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="53f32-484">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="53f32-484">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="53f32-485">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-485">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="53f32-486">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="53f32-486">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="53f32-487">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-487">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="53f32-488">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="53f32-488">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="53f32-489">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="53f32-489">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="53f32-490">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="53f32-490">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="53f32-491">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="53f32-491">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="53f32-492">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-492">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="53f32-493">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="53f32-493">Az.DataBoxEdge</span></span>
* <span data-ttu-id="53f32-494">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="53f32-494">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="53f32-495">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="53f32-495">Get the Order</span></span>
* <span data-ttu-id="53f32-496">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="53f32-496">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="53f32-497">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="53f32-497">Create new Order</span></span>
* <span data-ttu-id="53f32-498">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="53f32-498">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="53f32-499">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="53f32-499">Remove the Order</span></span>
* <span data-ttu-id="53f32-500">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="53f32-500">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="53f32-501">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="53f32-501">Now creates Local Share</span></span>
* <span data-ttu-id="53f32-502">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="53f32-502">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="53f32-503">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="53f32-503">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="53f32-504">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="53f32-504">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="53f32-505">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="53f32-505">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="53f32-506">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="53f32-506">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="53f32-507">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="53f32-507">Gets the information about Triggers</span></span>
* <span data-ttu-id="53f32-508">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="53f32-508">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="53f32-509">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="53f32-509">Create new Triggers</span></span>
* <span data-ttu-id="53f32-510">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="53f32-510">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="53f32-511">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="53f32-511">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-512">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-512">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-513">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="53f32-513">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="53f32-514">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="53f32-514">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-515">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-515">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-516">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="53f32-516">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-517">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-517">Az.EventHub</span></span>
* <span data-ttu-id="53f32-518">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="53f32-518">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-519">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-519">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-520">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="53f32-520">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="53f32-521">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="53f32-521">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="53f32-522">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="53f32-522">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="53f32-523">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="53f32-523">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-524">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-524">Az.Network</span></span>
* <span data-ttu-id="53f32-525">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="53f32-525">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="53f32-526">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="53f32-526">Az.PrivateDns</span></span>
* <span data-ttu-id="53f32-527">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-527">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-528">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-528">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-529">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="53f32-529">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="53f32-530">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="53f32-530">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="53f32-531">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-531">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53f32-532">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53f32-532">Az.RedisCache</span></span>
* <span data-ttu-id="53f32-533">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="53f32-533">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="53f32-534">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="53f32-534">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="53f32-535">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="53f32-535">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-536">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-536">Az.Resources</span></span>
- <span data-ttu-id="53f32-537">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53f32-537">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="53f32-538">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="53f32-538">Updated create policy definition help example</span></span>
- <span data-ttu-id="53f32-539">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="53f32-539">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="53f32-540">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="53f32-540">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="53f32-541">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="53f32-541">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-542">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-542">Az.Sql</span></span>
* <span data-ttu-id="53f32-543">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="53f32-543">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="53f32-544">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="53f32-544">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="53f32-545">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-545">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="53f32-546">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-546">General</span></span>
* <span data-ttu-id="53f32-547">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-547">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-548">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-548">Az.Accounts</span></span>
* <span data-ttu-id="53f32-549">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="53f32-549">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="53f32-550">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="53f32-550">Az.Advisor</span></span>
* <span data-ttu-id="53f32-551">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="53f32-551">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53f32-552">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-552">Az.Batch</span></span>
* <span data-ttu-id="53f32-553">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="53f32-553">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="53f32-554">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="53f32-554">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="53f32-555">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="53f32-555">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="53f32-556">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="53f32-556">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="53f32-557">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53f32-557">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="53f32-558">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53f32-558">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="53f32-559">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="53f32-559">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="53f32-560">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="53f32-560">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="53f32-561">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="53f32-561">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="53f32-562">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="53f32-562">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="53f32-563">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="53f32-563">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="53f32-564">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="53f32-564">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="53f32-565">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="53f32-565">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="53f32-566">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="53f32-566">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="53f32-567">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="53f32-567">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="53f32-568">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="53f32-568">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="53f32-569">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="53f32-569">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="53f32-570">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53f32-570">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="53f32-571">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="53f32-571">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="53f32-572">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="53f32-572">This operation is no longer supported.</span></span>
* <span data-ttu-id="53f32-573">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53f32-573">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="53f32-574">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="53f32-574">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="53f32-575">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="53f32-575">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="53f32-576">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="53f32-576">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="53f32-577">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="53f32-577">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="53f32-578">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="53f32-578">New non-verified images are also now returned.</span></span> <span data-ttu-id="53f32-579">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="53f32-579">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="53f32-580">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="53f32-580">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="53f32-581">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="53f32-581">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="53f32-582">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="53f32-582">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="53f32-583">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="53f32-583">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="53f32-584">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="53f32-584">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="53f32-585">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="53f32-585">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="53f32-586">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="53f32-586">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="53f32-587">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="53f32-587">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="53f32-588">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="53f32-588">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-589">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-589">Az.Cdn</span></span>
* <span data-ttu-id="53f32-590">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="53f32-590">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="53f32-591">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="53f32-591">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-592">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-592">Az.Compute</span></span>
* <span data-ttu-id="53f32-593">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="53f32-593">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="53f32-594">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="53f32-594">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="53f32-595">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53f32-595">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="53f32-596">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-596">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53f32-597">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-597">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="53f32-598">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="53f32-598">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="53f32-599">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-599">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="53f32-600">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="53f32-600">Breaking changes</span></span>
    - <span data-ttu-id="53f32-601">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="53f32-601">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="53f32-602">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="53f32-602">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-603">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-603">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-604">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="53f32-604">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-605">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-605">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-606">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="53f32-606">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="53f32-607">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="53f32-607">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="53f32-608">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="53f32-608">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="53f32-609">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="53f32-609">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="53f32-610">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="53f32-610">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="53f32-611">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="53f32-611">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-612">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-612">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-613">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="53f32-613">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-614">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-614">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-615">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="53f32-615">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="53f32-616">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="53f32-616">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="53f32-617">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="53f32-617">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="53f32-618">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-618">Removed five cmdlets:</span></span>
    - <span data-ttu-id="53f32-619">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53f32-619">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53f32-620">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53f32-620">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53f32-621">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="53f32-621">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="53f32-622">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53f32-622">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="53f32-623">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53f32-623">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="53f32-624">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-624">Added three cmdlets:</span></span>
    - <span data-ttu-id="53f32-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53f32-625">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="53f32-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53f32-626">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="53f32-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="53f32-627">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="53f32-628">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="53f32-628">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="53f32-629">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="53f32-629">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="53f32-630">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="53f32-630">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="53f32-631">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f32-631">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="53f32-632">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="53f32-632">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="53f32-633">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="53f32-633">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="53f32-634">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="53f32-634">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="53f32-635">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="53f32-635">Added some scenario test cases.</span></span>
* <span data-ttu-id="53f32-636">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="53f32-636">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-637">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-637">Az.IotHub</span></span>
* <span data-ttu-id="53f32-638">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="53f32-638">Breaking changes:</span></span>
    - <span data-ttu-id="53f32-639">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="53f32-639">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53f32-640">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="53f32-640">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53f32-641">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="53f32-641">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53f32-642">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="53f32-642">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53f32-643">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="53f32-643">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="53f32-644">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="53f32-644">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="53f32-645">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="53f32-645">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="53f32-646">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="53f32-646">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="53f32-647">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="53f32-647">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53f32-648">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="53f32-648">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="53f32-649">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="53f32-649">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="53f32-650">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="53f32-650">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-651">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-651">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-652">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-652">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-653">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-653">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="53f32-654">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-654">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="53f32-655">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-655">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-656">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-656">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-657">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-657">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-658">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-658">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-659">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-659">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-660">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="53f32-660">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-661">Az.Resources</span></span>
* <span data-ttu-id="53f32-662">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="53f32-662">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-663">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-663">Az.Network</span></span>
* <span data-ttu-id="53f32-664">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="53f32-664">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="53f32-665">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="53f32-665">Updated cmdlet:</span></span>
        - <span data-ttu-id="53f32-666">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-666">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-667">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-667">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-668">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-668">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-669">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-669">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-670">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-670">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="53f32-671">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="53f32-671">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="53f32-672">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-672">New cmdlet:</span></span>
        - <span data-ttu-id="53f32-673">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="53f32-673">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="53f32-674">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="53f32-674">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="53f32-675">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-675">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="53f32-676">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-676">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="53f32-677">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="53f32-677">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="53f32-678">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="53f32-678">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="53f32-679">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-679">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="53f32-680">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="53f32-680">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="53f32-681">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-681">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-682">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="53f32-682">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="53f32-683">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-683">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53f32-684">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-684">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53f32-685">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-685">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="53f32-686">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="53f32-686">Set-AzVirtualHub</span></span>
* <span data-ttu-id="53f32-687">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="53f32-687">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="53f32-688">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="53f32-688">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53f32-689">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="53f32-689">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="53f32-690">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="53f32-690">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="53f32-691">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="53f32-691">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="53f32-692">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="53f32-692">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="53f32-693">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-693">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="53f32-694">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-694">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-695">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-695">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="53f32-696">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="53f32-696">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53f32-697">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53f32-697">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53f32-698">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53f32-698">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53f32-699">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53f32-699">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53f32-700">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53f32-700">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="53f32-701">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="53f32-701">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="53f32-702">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="53f32-702">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="53f32-703">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-703">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-704">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="53f32-704">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="53f32-705">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="53f32-705">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="53f32-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="53f32-706">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="53f32-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="53f32-707">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="53f32-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="53f32-708">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="53f32-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-709">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="53f32-710">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="53f32-710">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53f32-711">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="53f32-711">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="53f32-712">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="53f32-712">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="53f32-713">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="53f32-713">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="53f32-714">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="53f32-714">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="53f32-715">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="53f32-715">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="53f32-716">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53f32-716">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="53f32-717">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="53f32-717">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="53f32-718">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="53f32-718">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="53f32-719">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-719">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="53f32-720">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-720">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="53f32-721">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-721">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-722">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-722">New-AzIpGroup</span></span>
        - <span data-ttu-id="53f32-723">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-723">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="53f32-724">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-724">Get-AzIpGroup</span></span>
        - <span data-ttu-id="53f32-725">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-725">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-726">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-726">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-727">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="53f32-727">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-728">Az.Sql</span></span>
* <span data-ttu-id="53f32-729">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="53f32-729">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="53f32-730">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="53f32-730">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="53f32-731">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="53f32-731">Removed deprecated aliases:</span></span>
* <span data-ttu-id="53f32-732">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="53f32-732">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="53f32-733">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="53f32-733">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="53f32-734">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-734">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="53f32-735">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="53f32-735">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="53f32-736">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="53f32-736">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="53f32-737">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="53f32-737">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-738">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-738">Az.Storage</span></span>
* <span data-ttu-id="53f32-739">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="53f32-739">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="53f32-740">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-740">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="53f32-741">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-741">Set-AzStorageAccount</span></span>
* <span data-ttu-id="53f32-742">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="53f32-742">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="53f32-743">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53f32-743">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="53f32-744">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53f32-744">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="53f32-745">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-745">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="53f32-746">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-746">General</span></span>
* <span data-ttu-id="53f32-747">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-747">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-748">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-748">Az.Accounts</span></span>
* <span data-ttu-id="53f32-749">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="53f32-749">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53f32-750">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-750">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-751">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="53f32-751">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="53f32-752">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="53f32-752">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-753">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-753">Az.Automation</span></span>
* <span data-ttu-id="53f32-754">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="53f32-754">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53f32-755">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-755">Az.Batch</span></span>
* <span data-ttu-id="53f32-756">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="53f32-756">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-757">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-757">Az.Compute</span></span>
* <span data-ttu-id="53f32-758">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-758">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="53f32-759">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="53f32-759">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="53f32-760">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="53f32-760">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="53f32-761">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="53f32-761">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-762">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-762">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-763">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="53f32-763">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="53f32-764">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="53f32-764">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="53f32-765">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="53f32-765">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-766">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-767">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="53f32-767">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="53f32-768">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="53f32-768">Az.HealthcareApis</span></span>
* <span data-ttu-id="53f32-769">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-769">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="53f32-770">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="53f32-770">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="53f32-771">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="53f32-771">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="53f32-772">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="53f32-772">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-773">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-773">Az.IotHub</span></span>
* <span data-ttu-id="53f32-774">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="53f32-774">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="53f32-775">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="53f32-775">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-776">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-776">Az.Monitor</span></span>
* <span data-ttu-id="53f32-777">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="53f32-777">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="53f32-778">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="53f32-778">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="53f32-779">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="53f32-779">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="53f32-780">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="53f32-780">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-781">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-781">Az.Network</span></span>
* <span data-ttu-id="53f32-782">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="53f32-782">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="53f32-783">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-783">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="53f32-784">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-784">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-785">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-785">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="53f32-786">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-786">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="53f32-787">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="53f32-787">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="53f32-788">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-788">Updated cmdlets:</span></span>
        - <span data-ttu-id="53f32-789">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-789">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53f32-790">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-790">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53f32-791">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-791">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="53f32-792">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="53f32-792">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="53f32-793">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="53f32-793">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="53f32-794">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="53f32-794">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="53f32-795">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="53f32-795">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53f32-796">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53f32-796">Az.RedisCache</span></span>
* <span data-ttu-id="53f32-797">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="53f32-797">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-798">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-798">Az.Sql</span></span>
* <span data-ttu-id="53f32-799">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="53f32-799">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-800">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-800">Az.Storage</span></span>
* <span data-ttu-id="53f32-801">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="53f32-801">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="53f32-802">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="53f32-802">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="53f32-803">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="53f32-803">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="53f32-804">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="53f32-804">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="53f32-805">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-805">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53f32-806">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53f32-806">Az.StorageSync</span></span>
* <span data-ttu-id="53f32-807">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="53f32-807">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-808">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-808">Az.Websites</span></span>
* <span data-ttu-id="53f32-809">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="53f32-809">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="53f32-810">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-810">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="53f32-811">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-811">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-812">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="53f32-812">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="53f32-813">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="53f32-813">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="53f32-814">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="53f32-814">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-815">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-815">Az.Automation</span></span>
* <span data-ttu-id="53f32-816">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="53f32-816">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="53f32-817">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="53f32-817">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="53f32-818">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="53f32-818">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-819">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-819">Az.Compute</span></span>
* <span data-ttu-id="53f32-820">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-820">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="53f32-821">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-821">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53f32-822">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="53f32-822">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="53f32-823">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="53f32-823">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="53f32-824">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53f32-824">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="53f32-825">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53f32-825">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="53f32-826">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="53f32-826">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="53f32-827">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="53f32-827">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="53f32-828">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="53f32-828">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-829">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-829">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-830">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="53f32-830">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="53f32-831">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="53f32-831">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-832">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-832">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-833">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="53f32-833">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-834">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-834">Az.IotHub</span></span>
* <span data-ttu-id="53f32-835">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="53f32-835">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="53f32-836">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="53f32-836">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="53f32-837">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="53f32-837">New cmdlets are:</span></span>
    - <span data-ttu-id="53f32-838">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="53f32-838">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53f32-839">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="53f32-839">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53f32-840">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="53f32-840">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="53f32-841">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="53f32-841">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-842">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-842">Az.Monitor</span></span>
* <span data-ttu-id="53f32-843">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="53f32-843">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="53f32-844">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="53f32-844">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="53f32-845">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="53f32-845">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="53f32-846">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="53f32-846">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="53f32-847">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="53f32-847">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="53f32-848">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="53f32-848">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="53f32-849">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f32-849">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="53f32-850">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="53f32-850">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="53f32-851">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="53f32-851">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="53f32-852">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="53f32-852">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="53f32-853">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="53f32-853">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="53f32-854">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="53f32-854">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="53f32-855">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="53f32-855">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="53f32-856">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="53f32-856">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="53f32-857">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="53f32-857">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="53f32-858">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="53f32-858">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="53f32-859">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="53f32-859">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="53f32-860">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-860">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="53f32-861">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="53f32-861">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="53f32-862">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-862">Overall improved help files</span></span>
* <span data-ttu-id="53f32-863">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="53f32-863">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-864">Az.Network</span></span>
* <span data-ttu-id="53f32-865">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="53f32-865">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="53f32-866">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="53f32-866">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="53f32-867">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="53f32-867">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="53f32-868">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="53f32-868">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="53f32-869">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="53f32-869">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="53f32-870">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="53f32-870">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="53f32-871">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="53f32-871">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="53f32-872">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="53f32-872">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="53f32-873">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-873">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="53f32-874">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="53f32-874">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="53f32-875">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-875">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="53f32-876">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-876">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="53f32-877">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-877">New cmdlets</span></span>
        - <span data-ttu-id="53f32-878">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="53f32-878">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="53f32-879">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-879">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="53f32-880">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="53f32-880">Updated cmdlet:</span></span>
        - <span data-ttu-id="53f32-881">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="53f32-881">New-VpnSite</span></span>
        - <span data-ttu-id="53f32-882">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="53f32-882">Update-VpnSite</span></span>
        - <span data-ttu-id="53f32-883">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-883">New-VpnConnection</span></span>
        - <span data-ttu-id="53f32-884">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-884">Update-VpnConnection</span></span>
* <span data-ttu-id="53f32-885">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="53f32-885">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-886">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-886">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-887">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="53f32-887">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="53f32-888">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="53f32-888">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-889">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-889">Az.Resources</span></span>
* <span data-ttu-id="53f32-890">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="53f32-890">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-891">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-891">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-892">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="53f32-892">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="53f32-893">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="53f32-893">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="53f32-894">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="53f32-894">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53f32-895">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="53f32-895">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53f32-896">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="53f32-896">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53f32-897">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="53f32-897">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="53f32-898">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="53f32-898">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53f32-899">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="53f32-899">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53f32-900">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="53f32-900">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53f32-901">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="53f32-901">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53f32-902">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="53f32-902">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="53f32-903">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="53f32-903">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="53f32-904">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="53f32-904">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="53f32-905">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="53f32-905">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="53f32-906">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="53f32-906">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="53f32-907">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="53f32-907">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53f32-908">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53f32-908">Az.SignalR</span></span>
* <span data-ttu-id="53f32-909">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="53f32-909">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-910">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-910">Az.Sql</span></span>
* <span data-ttu-id="53f32-911">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="53f32-911">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="53f32-912">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="53f32-912">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="53f32-913">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-913">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="53f32-914">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="53f32-914">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="53f32-915">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="53f32-915">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-916">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-916">Az.Storage</span></span>
* <span data-ttu-id="53f32-917">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="53f32-917">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="53f32-918">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="53f32-918">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="53f32-919">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53f32-919">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="53f32-920">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53f32-920">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="53f32-921">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="53f32-921">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="53f32-922">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53f32-922">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="53f32-923">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="53f32-923">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="53f32-924">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-924">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53f32-925">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-925">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53f32-926">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-926">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="53f32-927">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="53f32-927">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-928">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-928">Az.Websites</span></span>
* <span data-ttu-id="53f32-929">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="53f32-929">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="53f32-930">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="53f32-930">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="53f32-931">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="53f32-931">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="53f32-932">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-932">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="53f32-933">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-933">General</span></span>
* <span data-ttu-id="53f32-934">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="53f32-934">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-935">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-935">Az.Accounts</span></span>
* <span data-ttu-id="53f32-936">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="53f32-936">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="53f32-937">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="53f32-937">Az.Aks</span></span>
* <span data-ttu-id="53f32-938">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="53f32-938">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="53f32-939">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="53f32-939">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53f32-940">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-940">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-941">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="53f32-941">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="53f32-942">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="53f32-942">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="53f32-943">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="53f32-943">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="53f32-944">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="53f32-944">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="53f32-945">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="53f32-945">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53f32-946">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-946">Az.Batch</span></span>
* <span data-ttu-id="53f32-947">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="53f32-947">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-948">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-948">Az.Cdn</span></span>
* <span data-ttu-id="53f32-949">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="53f32-949">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-950">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-950">Az.Compute</span></span>
* <span data-ttu-id="53f32-951">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-951">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="53f32-952">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-952">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="53f32-953">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-953">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="53f32-954">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-954">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="53f32-955">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="53f32-955">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="53f32-956">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="53f32-956">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="53f32-957">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="53f32-957">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="53f32-958">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="53f32-958">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-959">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-959">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-960">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="53f32-960">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="53f32-961">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="53f32-961">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="53f32-962">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="53f32-962">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="53f32-963">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="53f32-963">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-964">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-964">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-965">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="53f32-965">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-966">Az.EventHub</span></span>
* <span data-ttu-id="53f32-967">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-967">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="53f32-968">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="53f32-968">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="53f32-969">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="53f32-969">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="53f32-970">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="53f32-970">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="53f32-971">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="53f32-971">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="53f32-972">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="53f32-972">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-973">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-973">Az.Monitor</span></span>
* <span data-ttu-id="53f32-974">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-974">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-975">Az.Network</span></span>
* <span data-ttu-id="53f32-976">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-976">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="53f32-977">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="53f32-977">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="53f32-978">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="53f32-978">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="53f32-979">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="53f32-979">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="53f32-980">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="53f32-980">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="53f32-981">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="53f32-981">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="53f32-982">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="53f32-982">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-983">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-983">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-984">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="53f32-984">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="53f32-985">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="53f32-985">Added example</span></span>
    - <span data-ttu-id="53f32-986">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="53f32-986">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="53f32-987">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="53f32-987">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="53f32-988">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="53f32-988">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-989">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-989">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-990">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-990">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-991">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-991">Az.Resources</span></span>
* <span data-ttu-id="53f32-992">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="53f32-992">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="53f32-993">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="53f32-993">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="53f32-994">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="53f32-994">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="53f32-995">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-995">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-996">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-997">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-997">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="53f32-998">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="53f32-998">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="53f32-999">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="53f32-999">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-1000">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1000">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-1001">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="53f32-1001">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="53f32-1002">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="53f32-1002">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="53f32-1003">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="53f32-1003">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="53f32-1004">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="53f32-1004">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="53f32-1005">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="53f32-1005">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="53f32-1006">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="53f32-1006">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1007">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1007">Az.Sql</span></span>
* <span data-ttu-id="53f32-1008">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="53f32-1008">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1009">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1009">Az.Storage</span></span>
* <span data-ttu-id="53f32-1010">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="53f32-1010">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="53f32-1011">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="53f32-1011">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="53f32-1012">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53f32-1012">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="53f32-1013">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-1013">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="53f32-1014">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="53f32-1014">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="53f32-1015">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-1015">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1016">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1016">Az.Websites</span></span>
* <span data-ttu-id="53f32-1017">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53f32-1017">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="53f32-1018">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1018">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1019">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1019">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1020">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="53f32-1020">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="53f32-1021">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1021">Az.ApplicationInsights</span></span>
* <span data-ttu-id="53f32-1022">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="53f32-1022">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1023">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1023">Az.Automation</span></span>
* <span data-ttu-id="53f32-1024">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="53f32-1024">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-1025">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1025">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-1026">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="53f32-1026">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1027">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1027">Az.Compute</span></span>
* <span data-ttu-id="53f32-1028">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="53f32-1028">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="53f32-1029">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="53f32-1029">Az.ContainerRegistry</span></span>
* <span data-ttu-id="53f32-1030">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="53f32-1030">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="53f32-1031">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="53f32-1031">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1032">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1033">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="53f32-1033">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="53f32-1034">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="53f32-1034">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-1035">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1035">Az.EventHub</span></span>
* <span data-ttu-id="53f32-1036">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="53f32-1036">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="53f32-1037">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="53f32-1037">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-1038">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1038">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-1039">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="53f32-1039">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53f32-1040">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1040">Az.LogicApp</span></span>
* <span data-ttu-id="53f32-1041">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="53f32-1041">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="53f32-1042">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="53f32-1042">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="53f32-1043">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1043">Az.ManagedServices</span></span>
* <span data-ttu-id="53f32-1044">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="53f32-1044">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1045">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1045">Az.Network</span></span>
* <span data-ttu-id="53f32-1046">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="53f32-1046">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="53f32-1047">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1047">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1048">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-1048">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53f32-1049">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1049">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53f32-1050">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1050">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-1051">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1051">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-1052">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1052">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-1053">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1053">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="53f32-1054">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="53f32-1054">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="53f32-1055">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1055">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="53f32-1056">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="53f32-1056">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="53f32-1057">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1057">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="53f32-1058">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="53f32-1058">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="53f32-1059">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="53f32-1059">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="53f32-1060">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="53f32-1060">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="53f32-1061">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="53f32-1061">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="53f32-1062">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1062">Updated cmdlets</span></span>
        - <span data-ttu-id="53f32-1063">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1063">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53f32-1064">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1064">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="53f32-1065">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1065">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="53f32-1066">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1066">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="53f32-1067">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1067">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="53f32-1068">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="53f32-1068">Updated cmdlet:</span></span>
        - <span data-ttu-id="53f32-1069">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1069">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="53f32-1070">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1070">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="53f32-1071">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1071">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="53f32-1072">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="53f32-1072">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="53f32-1073">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="53f32-1073">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="53f32-1074">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="53f32-1074">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1075">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1075">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-1076">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="53f32-1076">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="53f32-1077">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="53f32-1077">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1078">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1078">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1079">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1079">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="53f32-1080">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1080">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="53f32-1081">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1081">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="53f32-1082">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1082">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="53f32-1083">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1083">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="53f32-1084">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1084">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="53f32-1085">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1085">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="53f32-1086">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1086">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="53f32-1087">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1087">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="53f32-1088">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="53f32-1088">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1089">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1089">Az.Resources</span></span>
- <span data-ttu-id="53f32-1090">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="53f32-1090">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="53f32-1091">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="53f32-1091">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-1092">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-1092">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-1093">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="53f32-1093">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="53f32-1094">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="53f32-1094">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1095">Az.Sql</span></span>
* <span data-ttu-id="53f32-1096">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="53f32-1096">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="53f32-1097">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="53f32-1097">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="53f32-1098">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="53f32-1098">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1099">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1099">Az.Storage</span></span>
* <span data-ttu-id="53f32-1100">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="53f32-1100">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53f32-1101">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53f32-1101">Az.StorageSync</span></span>
* <span data-ttu-id="53f32-1102">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="53f32-1102">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="53f32-1103">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="53f32-1103">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1104">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1104">Az.Websites</span></span>
* <span data-ttu-id="53f32-1105">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1105">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="53f32-1106">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1106">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="53f32-1107">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="53f32-1107">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="53f32-1108">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1108">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1109">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1109">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1110">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="53f32-1110">Add support for profile cmdlets</span></span>
* <span data-ttu-id="53f32-1111">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="53f32-1111">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="53f32-1112">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="53f32-1112">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="53f32-1113">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="53f32-1113">Az.Advisor</span></span>
* <span data-ttu-id="53f32-1114">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="53f32-1114">GA release of Az.Advisor</span></span>
* <span data-ttu-id="53f32-1115">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="53f32-1115">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="53f32-1116">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-1116">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-1117">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="53f32-1117">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="53f32-1118">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="53f32-1118">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="53f32-1119">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="53f32-1119">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="53f32-1120">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="53f32-1120">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="53f32-1121">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="53f32-1121">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="53f32-1122">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="53f32-1122">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="53f32-1123">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="53f32-1123">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1124">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1124">Az.Automation</span></span>
* <span data-ttu-id="53f32-1125">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="53f32-1125">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1126">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1126">Az.Compute</span></span>
* <span data-ttu-id="53f32-1127">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1127">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1128">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1128">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1129">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="53f32-1129">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53f32-1130">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53f32-1130">Az.EventGrid</span></span>
* <span data-ttu-id="53f32-1131">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="53f32-1131">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-1132">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1132">Az.IotHub</span></span>
* <span data-ttu-id="53f32-1133">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1133">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1134">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1134">Az.Network</span></span>
* <span data-ttu-id="53f32-1135">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="53f32-1135">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="53f32-1136">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="53f32-1136">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-1137">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1137">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-1138">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="53f32-1138">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="53f32-1139">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="53f32-1139">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1140">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1140">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-1141">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="53f32-1141">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1142">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1142">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1143">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="53f32-1143">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1144">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1144">Az.Resources</span></span>
    - <span data-ttu-id="53f32-1145">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="53f32-1145">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="53f32-1146">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="53f32-1146">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="53f32-1147">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="53f32-1147">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="53f32-1148">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="53f32-1148">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-1149">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-1149">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-1150">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="53f32-1150">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1151">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1151">Az.Sql</span></span>
* <span data-ttu-id="53f32-1152">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="53f32-1152">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="53f32-1153">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1153">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="53f32-1154">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1154">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53f32-1155">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1155">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53f32-1156">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1156">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="53f32-1157">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1157">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="53f32-1158">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1158">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="53f32-1159">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="53f32-1159">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="53f32-1160">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="53f32-1160">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1161">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1161">Az.Storage</span></span>
* <span data-ttu-id="53f32-1162">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1162">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="53f32-1163">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53f32-1163">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="53f32-1164">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="53f32-1164">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="53f32-1165">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="53f32-1165">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="53f32-1166">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1166">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="53f32-1167">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1167">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="53f32-1168">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1168">Set-AzStorageAccount</span></span>
* <span data-ttu-id="53f32-1169">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="53f32-1169">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="53f32-1170">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53f32-1170">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="53f32-1171">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="53f32-1171">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="53f32-1172">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="53f32-1172">Az.StorageSync</span></span>
* <span data-ttu-id="53f32-1173">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="53f32-1173">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="53f32-1174">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1174">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1175">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1175">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1176">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="53f32-1176">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="53f32-1177">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="53f32-1177">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="53f32-1178">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="53f32-1178">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="53f32-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="53f32-1179">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="53f32-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="53f32-1180">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1181">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1181">Az.Compute</span></span>
* <span data-ttu-id="53f32-1182">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1182">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="53f32-1183">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="53f32-1183">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="53f32-1184">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="53f32-1184">Az.Dns</span></span>
* <span data-ttu-id="53f32-1185">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1185">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53f32-1186">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53f32-1186">Az.EventGrid</span></span>
* <span data-ttu-id="53f32-1187">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="53f32-1187">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="53f32-1188">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1188">New cmdlets:</span></span>
    - <span data-ttu-id="53f32-1189">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53f32-1189">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53f32-1190">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1190">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53f32-1191">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53f32-1191">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53f32-1192">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1192">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="53f32-1193">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="53f32-1193">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="53f32-1194">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1194">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53f32-1195">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="53f32-1195">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="53f32-1196">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1196">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="53f32-1197">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="53f32-1197">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="53f32-1198">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="53f32-1198">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="53f32-1199">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="53f32-1199">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="53f32-1200">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1200">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="53f32-1201">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="53f32-1201">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="53f32-1202">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1202">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="53f32-1203">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="53f32-1203">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="53f32-1204">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="53f32-1204">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="53f32-1205">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1205">Updated cmdlets:</span></span>
    - <span data-ttu-id="53f32-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53f32-1206">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="53f32-1207">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="53f32-1207">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="53f32-1208">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="53f32-1208">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="53f32-1209">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="53f32-1209">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="53f32-1210">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="53f32-1210">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="53f32-1211">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="53f32-1211">Event subscription expiration date,</span></span>
            - <span data-ttu-id="53f32-1212">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1212">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="53f32-1213">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1213">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="53f32-1214">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1214">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="53f32-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53f32-1215">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="53f32-1216">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1216">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="53f32-1217">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="53f32-1217">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="53f32-1218">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="53f32-1218">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="53f32-1219">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="53f32-1219">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-1220">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-1220">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-1221">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="53f32-1221">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="53f32-1222">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="53f32-1222">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="53f32-1223">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="53f32-1223">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="53f32-1224">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="53f32-1224">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1225">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1225">Az.Network</span></span>
* <span data-ttu-id="53f32-1226">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-1226">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="53f32-1227">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1227">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="53f32-1228">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="53f32-1229">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="53f32-1229">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="53f32-1230">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1230">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1231">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="53f32-1231">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="53f32-1232">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1232">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="53f32-1233">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1233">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1234">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1234">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53f32-1235">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1235">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53f32-1236">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="53f32-1236">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="53f32-1237">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1237">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="53f32-1238">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1238">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="53f32-1239">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-1239">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="53f32-1240">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1240">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1241">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-1241">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53f32-1242">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-1242">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53f32-1243">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="53f32-1243">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="53f32-1244">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1244">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="53f32-1245">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="53f32-1245">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="53f32-1246">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="53f32-1246">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="53f32-1247">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="53f32-1247">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="53f32-1248">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="53f32-1248">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="53f32-1249">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="53f32-1249">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="53f32-1250">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="53f32-1250">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="53f32-1251">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1251">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="53f32-1252">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="53f32-1252">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="53f32-1253">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1253">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="53f32-1254">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="53f32-1254">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="53f32-1255">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1255">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="53f32-1256">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1256">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="53f32-1257">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="53f32-1257">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="53f32-1258">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1258">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="53f32-1259">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="53f32-1259">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="53f32-1260">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="53f32-1260">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="53f32-1261">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-1261">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="53f32-1262">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="53f32-1262">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="53f32-1263">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="53f32-1263">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="53f32-1264">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="53f32-1264">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="53f32-1265">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1265">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="53f32-1266">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1266">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="53f32-1267">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1267">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1268">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1268">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-1269">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="53f32-1269">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1270">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1270">Az.Resources</span></span>
* <span data-ttu-id="53f32-1271">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="53f32-1271">Support for additional Template Export options</span></span>
    - <span data-ttu-id="53f32-1272">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-1272">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="53f32-1273">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-1273">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="53f32-1274">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="53f32-1274">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-1275">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1275">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-1276">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="53f32-1276">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1277">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1277">Az.Sql</span></span>
* <span data-ttu-id="53f32-1278">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="53f32-1278">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="53f32-1279">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="53f32-1279">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="53f32-1280">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="53f32-1280">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="53f32-1281">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53f32-1281">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53f32-1282">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53f32-1282">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53f32-1283">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="53f32-1283">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="53f32-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="53f32-1284">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="53f32-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="53f32-1285">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1286">Az.Storage</span></span>
* <span data-ttu-id="53f32-1287">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1287">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="53f32-1288">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1288">New-AzStorageAccount</span></span>
* <span data-ttu-id="53f32-1289">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="53f32-1289">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="53f32-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1290">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1291">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1291">Az.Websites</span></span>
* <span data-ttu-id="53f32-1292">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="53f32-1292">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="53f32-1293">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="53f32-1293">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="53f32-1294">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1294">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="53f32-1295">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-1295">Az.Cdn</span></span>
* <span data-ttu-id="53f32-1296">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="53f32-1296">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1297">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1297">Az.Compute</span></span>
* <span data-ttu-id="53f32-1298">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1298">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="53f32-1299">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="53f32-1299">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-1300">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1300">Az.EventHub</span></span>
* <span data-ttu-id="53f32-1301">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="53f32-1301">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="53f32-1302">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f32-1302">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1303">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1303">Az.Network</span></span>
* <span data-ttu-id="53f32-1304">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="53f32-1304">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="53f32-1305">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="53f32-1305">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-1306">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1306">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-1307">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="53f32-1307">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1309">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="53f32-1309">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-1310">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-1310">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-1311">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f32-1311">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-1312">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1312">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-1313">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="53f32-1313">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="53f32-1314">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1314">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1315">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1315">Az.Sql</span></span>
* <span data-ttu-id="53f32-1316">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="53f32-1316">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="53f32-1317">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1317">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="53f32-1318">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="53f32-1318">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="53f32-1319">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="53f32-1319">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1320">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1320">Az.Websites</span></span>
* <span data-ttu-id="53f32-1321">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="53f32-1321">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="53f32-1322">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1322">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="53f32-1323">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-1323">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-1324">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="53f32-1324">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="53f32-1325">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1325">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="53f32-1326">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1326">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="53f32-1327">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="53f32-1327">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="53f32-1328">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1328">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="53f32-1329">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="53f32-1329">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="53f32-1330">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1330">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="53f32-1331">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1331">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="53f32-1332">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-1332">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="53f32-1333">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="53f32-1333">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="53f32-1334">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1334">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="53f32-1335">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="53f32-1335">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="53f32-1336">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="53f32-1336">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="53f32-1337">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1337">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="53f32-1338">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1338">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="53f32-1339">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1339">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="53f32-1340">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1340">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="53f32-1341">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="53f32-1341">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="53f32-1342">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="53f32-1342">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="53f32-1343">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1343">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="53f32-1344">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="53f32-1344">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="53f32-1345">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53f32-1345">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="53f32-1346">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="53f32-1346">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="53f32-1347">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-1347">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="53f32-1348">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="53f32-1348">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="53f32-1349">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="53f32-1349">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="53f32-1350">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1350">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="53f32-1351">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53f32-1351">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="53f32-1352">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="53f32-1352">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="53f32-1353">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="53f32-1353">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="53f32-1354">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="53f32-1354">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="53f32-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="53f32-1355">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="53f32-1356">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="53f32-1356">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="53f32-1357">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="53f32-1357">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="53f32-1358">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="53f32-1358">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="53f32-1359">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="53f32-1359">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="53f32-1360">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="53f32-1360">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="53f32-1361">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="53f32-1361">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="53f32-1362">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="53f32-1362">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="53f32-1363">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="53f32-1363">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="53f32-1364">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1364">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="53f32-1365">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="53f32-1365">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="53f32-1366">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1366">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="53f32-1367">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="53f32-1367">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="53f32-1368">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="53f32-1368">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="53f32-1369">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1369">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="53f32-1370">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="53f32-1370">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="53f32-1371">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="53f32-1371">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="53f32-1372">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="53f32-1372">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="53f32-1373">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1373">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="53f32-1374">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="53f32-1374">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="53f32-1375">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="53f32-1375">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="53f32-1376">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="53f32-1376">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="53f32-1377">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="53f32-1377">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="53f32-1378">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="53f32-1378">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="53f32-1379">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="53f32-1379">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="53f32-1380">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="53f32-1380">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="53f32-1381">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="53f32-1381">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="53f32-1382">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="53f32-1382">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="53f32-1383">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1383">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="53f32-1384">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="53f32-1384">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="53f32-1385">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="53f32-1385">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="53f32-1386">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="53f32-1386">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="53f32-1387">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1387">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="53f32-1388">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="53f32-1388">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="53f32-1389">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="53f32-1389">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="53f32-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="53f32-1390">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="53f32-1391">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="53f32-1391">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="53f32-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="53f32-1392">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="53f32-1393">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="53f32-1393">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="53f32-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="53f32-1394">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="53f32-1395">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="53f32-1395">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="53f32-1396">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="53f32-1396">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="53f32-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1397">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="53f32-1398">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="53f32-1398">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="53f32-1399">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="53f32-1399">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="53f32-1400">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="53f32-1400">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1401">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1401">Az.Automation</span></span>
* <span data-ttu-id="53f32-1402">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="53f32-1402">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="53f32-1403">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="53f32-1403">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="53f32-1404">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="53f32-1404">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="53f32-1405">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="53f32-1405">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="53f32-1406">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="53f32-1406">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="53f32-1407">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="53f32-1407">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="53f32-1408">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="53f32-1408">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1409">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1409">Az.Compute</span></span>
* <span data-ttu-id="53f32-1410">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="53f32-1410">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="53f32-1411">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="53f32-1411">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1412">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1412">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-1413">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1413">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-1414">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-1414">Az.Monitor</span></span>
* <span data-ttu-id="53f32-1415">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-1415">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1416">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1416">Az.Network</span></span>
* <span data-ttu-id="53f32-1417">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="53f32-1417">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="53f32-1418">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="53f32-1418">Updated cmdlet:</span></span>
        - <span data-ttu-id="53f32-1419">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-1419">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="53f32-1420">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="53f32-1420">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1421">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1421">Az.Resources</span></span>
* <span data-ttu-id="53f32-1422">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="53f32-1422">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1423">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1423">Az.Sql</span></span>
* <span data-ttu-id="53f32-1424">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="53f32-1424">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="53f32-1425">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1425">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1426">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1427">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="53f32-1427">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-1428">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1428">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-1429">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="53f32-1429">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="53f32-1430">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="53f32-1430">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1431">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1431">Az.Compute</span></span>
* <span data-ttu-id="53f32-1432">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="53f32-1432">Proximity placement group feature.</span></span>
    - <span data-ttu-id="53f32-1433">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-1433">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="53f32-1434">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1434">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="53f32-1435">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="53f32-1435">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="53f32-1436">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="53f32-1436">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="53f32-1437">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-1437">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="53f32-1438">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="53f32-1438">Breaking changes</span></span>
    - <span data-ttu-id="53f32-1439">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="53f32-1439">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="53f32-1440">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="53f32-1440">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="53f32-1441">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="53f32-1441">Az.DeploymentManager</span></span>
* <span data-ttu-id="53f32-1442">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="53f32-1442">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="53f32-1443">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="53f32-1443">Az.Dns</span></span>
* <span data-ttu-id="53f32-1444">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="53f32-1444">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="53f32-1445">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="53f32-1445">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="53f32-1446">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="53f32-1446">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="53f32-1447">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-1447">Az.FrontDoor</span></span>
* <span data-ttu-id="53f32-1448">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1448">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="53f32-1449">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="53f32-1449">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="53f32-1450">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-1450">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-1451">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1451">Removed two cmdlets:</span></span>
    - <span data-ttu-id="53f32-1452">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53f32-1452">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="53f32-1453">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53f32-1453">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="53f32-1454">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="53f32-1454">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="53f32-1455">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="53f32-1455">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="53f32-1456">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="53f32-1456">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="53f32-1457">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1457">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-1458">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-1458">Az.Monitor</span></span>
* <span data-ttu-id="53f32-1459">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="53f32-1459">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="53f32-1460">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="53f32-1460">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="53f32-1461">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-1461">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="53f32-1462">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="53f32-1462">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="53f32-1463">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="53f32-1463">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="53f32-1464">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="53f32-1464">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="53f32-1465">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="53f32-1465">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="53f32-1466">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1466">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53f32-1467">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1467">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53f32-1468">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1468">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53f32-1469">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1469">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53f32-1470">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1470">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="53f32-1471">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="53f32-1471">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="53f32-1472">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="53f32-1472">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1473">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1473">Az.Network</span></span>
* <span data-ttu-id="53f32-1474">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="53f32-1474">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="53f32-1475">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-1475">New cmdlets</span></span>
        - <span data-ttu-id="53f32-1476">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1476">New-AzNatGateway</span></span>
        - <span data-ttu-id="53f32-1477">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1477">Get-AzNatGateway</span></span>
        - <span data-ttu-id="53f32-1478">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1478">Set-AzNatGateway</span></span>
        - <span data-ttu-id="53f32-1479">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1479">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="53f32-1480">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="53f32-1480">Updated cmdlets</span></span>
        - <span data-ttu-id="53f32-1481">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="53f32-1481">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="53f32-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="53f32-1482">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="53f32-1483">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1483">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="53f32-1484">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1484">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="53f32-1485">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="53f32-1485">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-1486">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1486">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-1487">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="53f32-1487">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="53f32-1488">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="53f32-1488">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="53f32-1489">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="53f32-1489">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1490">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1490">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1491">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="53f32-1491">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="53f32-1492">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53f32-1492">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="53f32-1493">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="53f32-1493">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="53f32-1494">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1494">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="53f32-1495">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="53f32-1495">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="53f32-1496">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="53f32-1496">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="53f32-1497">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="53f32-1497">Az.Relay</span></span>
* <span data-ttu-id="53f32-1498">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="53f32-1498">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-1499">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-1499">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-1500">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53f32-1500">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1501">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1501">Az.Storage</span></span>
* <span data-ttu-id="53f32-1502">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="53f32-1502">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="53f32-1503">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="53f32-1503">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="53f32-1504">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="53f32-1504">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="53f32-1505">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1505">New-AzStorageAccount</span></span>
* <span data-ttu-id="53f32-1506">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="53f32-1506">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="53f32-1507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1507">New-AzStorageAccount</span></span>
    - <span data-ttu-id="53f32-1508">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1508">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="53f32-1509">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1509">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1510">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1510">Az.Websites</span></span>
* <span data-ttu-id="53f32-1511">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1511">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="53f32-1512">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="53f32-1512">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="53f32-1513">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1513">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-1514">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-1514">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-1515">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="53f32-1515">General availability of `Az` module</span></span>
* <span data-ttu-id="53f32-1516">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53f32-1516">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53f32-1517">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53f32-1517">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53f32-1518">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1518">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53f32-1519">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="53f32-1519">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53f32-1520">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1520">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53f32-1521">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="53f32-1521">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-1522">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1522">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1523">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="53f32-1523">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="53f32-1524">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-1524">Az.Batch</span></span>
* <span data-ttu-id="53f32-1525">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1525">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-1526">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-1526">Az.Cdn</span></span>
* <span data-ttu-id="53f32-1527">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1527">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-1528">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1528">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-1529">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1529">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1530">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1530">Az.Compute</span></span>
* <span data-ttu-id="53f32-1531">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="53f32-1531">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="53f32-1532">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1532">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1533">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="53f32-1533">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1534">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1535">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="53f32-1535">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1536">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-1537">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1537">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53f32-1538">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53f32-1538">Az.EventGrid</span></span>
* <span data-ttu-id="53f32-1539">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="53f32-1539">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-1540">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1540">Az.EventHub</span></span>
* <span data-ttu-id="53f32-1541">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="53f32-1541">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="53f32-1542">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="53f32-1542">Az.HDInsight</span></span>
* <span data-ttu-id="53f32-1543">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1543">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-1544">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1544">Az.IotHub</span></span>
* <span data-ttu-id="53f32-1545">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1545">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-1546">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1546">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-1547">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1547">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1548">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="53f32-1548">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="53f32-1549">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="53f32-1549">Az.MachineLearning</span></span>
* <span data-ttu-id="53f32-1550">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1550">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="53f32-1551">Az.Media</span><span class="sxs-lookup"><span data-stu-id="53f32-1551">Az.Media</span></span>
* <span data-ttu-id="53f32-1552">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1552">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-1553">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-1553">Az.Monitor</span></span>
  * <span data-ttu-id="53f32-1554">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="53f32-1554">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="53f32-1555">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="53f32-1555">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="53f32-1556">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="53f32-1556">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="53f32-1557">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53f32-1557">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="53f32-1558">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53f32-1558">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="53f32-1559">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="53f32-1559">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="53f32-1560">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="53f32-1560">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1561">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1561">Az.Network</span></span>
* <span data-ttu-id="53f32-1562">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1562">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1563">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="53f32-1563">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="53f32-1564">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="53f32-1564">Az.NotificationHubs</span></span>
* <span data-ttu-id="53f32-1565">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1565">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1566">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1566">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-1567">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1567">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="53f32-1568">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="53f32-1568">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="53f32-1569">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1569">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1570">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1570">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1571">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1571">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1572">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1572">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="53f32-1573">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="53f32-1573">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="53f32-1574">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="53f32-1574">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53f32-1575">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53f32-1575">Az.RedisCache</span></span>
* <span data-ttu-id="53f32-1576">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1576">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1577">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1577">Az.Resources</span></span>
* <span data-ttu-id="53f32-1578">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="53f32-1578">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1579">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1579">Az.Sql</span></span>
* <span data-ttu-id="53f32-1580">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="53f32-1580">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="53f32-1581">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1581">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1582">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="53f32-1582">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="53f32-1583">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="53f32-1583">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="53f32-1584">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="53f32-1584">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="53f32-1585">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="53f32-1585">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="53f32-1586">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="53f32-1586">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1587">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1587">Az.Websites</span></span>
* <span data-ttu-id="53f32-1588">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="53f32-1588">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="53f32-1589">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="53f32-1589">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="53f32-1590">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="53f32-1590">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="53f32-1591">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="53f32-1591">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="53f32-1592">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1592">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-1593">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-1593">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-1594">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="53f32-1594">General availability of `Az` module</span></span>
* <span data-ttu-id="53f32-1595">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53f32-1595">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53f32-1596">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53f32-1596">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53f32-1597">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1597">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53f32-1598">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="53f32-1598">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53f32-1599">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1599">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53f32-1600">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="53f32-1600">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="53f32-1601">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1601">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1602">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53f32-1602">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53f32-1603">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1603">Az.AnalysisServices</span></span>
* <span data-ttu-id="53f32-1604">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="53f32-1604">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="53f32-1605">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="53f32-1605">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1606">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1606">Az.Automation</span></span>
* <span data-ttu-id="53f32-1607">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="53f32-1607">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="53f32-1608">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="53f32-1608">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="53f32-1609">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1609">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1610">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1610">Az.Compute</span></span>
* <span data-ttu-id="53f32-1611">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1611">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="53f32-1612">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="53f32-1612">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="53f32-1613">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-1613">Az.ContainerInstance</span></span>
* <span data-ttu-id="53f32-1614">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="53f32-1614">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1615">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1615">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1616">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="53f32-1616">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="53f32-1617">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="53f32-1617">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1618">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1618">Az.Resources</span></span>
* <span data-ttu-id="53f32-1619">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="53f32-1619">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="53f32-1620">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="53f32-1620">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="53f32-1621">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="53f32-1621">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="53f32-1622">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="53f32-1622">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="53f32-1623">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="53f32-1623">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="53f32-1624">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="53f32-1624">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1625">Az.Sql</span></span>
* <span data-ttu-id="53f32-1626">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="53f32-1626">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1627">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1627">Az.Storage</span></span>
* <span data-ttu-id="53f32-1628">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="53f32-1628">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="53f32-1629">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="53f32-1629">New-AzStorageContext</span></span>
* <span data-ttu-id="53f32-1630">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="53f32-1630">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="53f32-1631">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="53f32-1631">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="53f32-1632">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="53f32-1632">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="53f32-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1633">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="53f32-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1634">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="53f32-1635">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="53f32-1635">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="53f32-1636">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53f32-1636">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="53f32-1637">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="53f32-1637">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="53f32-1638">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53f32-1638">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="53f32-1639">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="53f32-1639">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="53f32-1640">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1640">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="53f32-1641">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="53f32-1641">Highlights since the last major release</span></span>
* <span data-ttu-id="53f32-1642">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="53f32-1642">General availability of `Az` module</span></span>
* <span data-ttu-id="53f32-1643">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="53f32-1643">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="53f32-1644">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="53f32-1644">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="53f32-1645">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1645">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="53f32-1646">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="53f32-1646">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53f32-1647">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1647">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="53f32-1648">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="53f32-1648">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1649">Az.Automation</span></span>
* <span data-ttu-id="53f32-1650">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f32-1650">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="53f32-1651">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="53f32-1651">Dynamic grouping</span></span>
    * <span data-ttu-id="53f32-1652">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="53f32-1652">Pre-Post script</span></span>
    * <span data-ttu-id="53f32-1653">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="53f32-1653">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1654">Az.Compute</span></span>
* <span data-ttu-id="53f32-1655">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="53f32-1655">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="53f32-1656">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="53f32-1656">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-1657">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1657">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-1658">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1658">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1659">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1659">Az.Network</span></span>
* <span data-ttu-id="53f32-1660">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1660">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="53f32-1661">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="53f32-1661">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1662">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1662">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1663">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="53f32-1663">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="53f32-1664">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="53f32-1664">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1665">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1665">Az.Resources</span></span>
* <span data-ttu-id="53f32-1666">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-1666">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="53f32-1667">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="53f32-1667">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1668">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1668">Az.Sql</span></span>
* <span data-ttu-id="53f32-1669">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="53f32-1669">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1670">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1670">Az.Storage</span></span>
* <span data-ttu-id="53f32-1671">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1671">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="53f32-1672">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1672">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53f32-1673">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1673">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53f32-1674">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1674">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="53f32-1675">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="53f32-1675">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="53f32-1676">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="53f32-1676">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="53f32-1677">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1677">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1678">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1678">Az.Websites</span></span>
* <span data-ttu-id="53f32-1679">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="53f32-1679">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="53f32-1680">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1680">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1681">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1681">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1682">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="53f32-1682">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="53f32-1683">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1683">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1684">Az.Automation</span></span>
* <span data-ttu-id="53f32-1685">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1685">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="53f32-1686">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="53f32-1686">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="53f32-1687">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="53f32-1687">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-1688">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-1688">Az.Cdn</span></span>
* <span data-ttu-id="53f32-1689">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="53f32-1689">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1690">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1690">Az.Compute</span></span>
* <span data-ttu-id="53f32-1691">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="53f32-1691">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1692">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1693">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="53f32-1693">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53f32-1694">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1694">Az.LogicApp</span></span>
* <span data-ttu-id="53f32-1695">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="53f32-1695">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1696">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1696">Az.Network</span></span>
* <span data-ttu-id="53f32-1697">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1697">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1698">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1698">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1699">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-1699">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="53f32-1700">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="53f32-1700">SDK Update</span></span>
* <span data-ttu-id="53f32-1701">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="53f32-1701">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="53f32-1702">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="53f32-1702">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1703">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1703">Az.Resources</span></span>
* <span data-ttu-id="53f32-1704">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="53f32-1704">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="53f32-1705">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="53f32-1705">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="53f32-1706">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="53f32-1706">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="53f32-1707">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="53f32-1707">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="53f32-1708">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="53f32-1708">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="53f32-1709">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="53f32-1709">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1710">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1710">Az.Sql</span></span>
* <span data-ttu-id="53f32-1711">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="53f32-1711">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="53f32-1712">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="53f32-1712">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1713">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1713">Az.Storage</span></span>
* <span data-ttu-id="53f32-1714">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1714">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="53f32-1715">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1715">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="53f32-1716">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1716">Az.AnalysisServices</span></span>
* <span data-ttu-id="53f32-1717">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="53f32-1717">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1718">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1718">Az.Automation</span></span>
* <span data-ttu-id="53f32-1719">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1719">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="53f32-1720">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1720">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="53f32-1721">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1721">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-1722">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1722">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-1723">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="53f32-1723">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1724">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1724">Az.Compute</span></span>
* <span data-ttu-id="53f32-1725">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="53f32-1725">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="53f32-1726">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="53f32-1726">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="53f32-1727">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="53f32-1727">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="53f32-1728">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="53f32-1728">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1729">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1729">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-1730">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="53f32-1730">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="53f32-1731">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1731">Az.EventHub</span></span>
* <span data-ttu-id="53f32-1732">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="53f32-1732">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-1733">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1733">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-1734">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="53f32-1734">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53f32-1735">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1735">Az.LogicApp</span></span>
* <span data-ttu-id="53f32-1736">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1736">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="53f32-1737">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="53f32-1737">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="53f32-1738">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1738">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="53f32-1739">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="53f32-1739">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53f32-1740">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="53f32-1740">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53f32-1741">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="53f32-1741">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="53f32-1742">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="53f32-1742">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="53f32-1743">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1743">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="53f32-1744">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1744">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53f32-1745">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1745">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53f32-1746">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1746">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="53f32-1747">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1747">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="53f32-1748">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="53f32-1748">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="53f32-1749">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-1749">Az.Monitor</span></span>
* <span data-ttu-id="53f32-1750">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="53f32-1750">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1751">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1751">Az.Network</span></span>
* <span data-ttu-id="53f32-1752">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="53f32-1752">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1753">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1753">Az.OperationalInsights</span></span>
* <span data-ttu-id="53f32-1754">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="53f32-1754">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="53f32-1755">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="53f32-1755">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="53f32-1756">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="53f32-1756">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1757">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1757">Az.Resources</span></span>
* <span data-ttu-id="53f32-1758">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="53f32-1758">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="53f32-1759">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="53f32-1759">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="53f32-1760">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="53f32-1760">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="53f32-1761">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="53f32-1761">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1762">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1762">Az.Sql</span></span>
* <span data-ttu-id="53f32-1763">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="53f32-1763">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="53f32-1764">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="53f32-1764">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1765">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1765">Az.Websites</span></span>
* <span data-ttu-id="53f32-1766">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="53f32-1766">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="53f32-1767">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1767">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1768">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1768">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1769">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="53f32-1769">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53f32-1770">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1770">Az.AnalysisServices</span></span>
<span data-ttu-id="53f32-1771">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="53f32-1771">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1772">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1772">Az.Compute</span></span>
* <span data-ttu-id="53f32-1773">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="53f32-1773">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="53f32-1774">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="53f32-1774">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="53f32-1775">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="53f32-1775">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1776">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1776">Az.RecoveryServices</span></span>
<span data-ttu-id="53f32-1777">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="53f32-1777">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1778">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1778">Az.Resources</span></span>
* <span data-ttu-id="53f32-1779">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="53f32-1779">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="53f32-1780">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="53f32-1780">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="53f32-1781">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="53f32-1781">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="53f32-1782">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="53f32-1782">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1783">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1783">Az.Sql</span></span>
* <span data-ttu-id="53f32-1784">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="53f32-1784">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="53f32-1785">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="53f32-1785">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="53f32-1786">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="53f32-1786">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="53f32-1787">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1787">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1788">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1788">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1789">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1789">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="53f32-1790">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1790">Az.AnalysisServices</span></span>
* <span data-ttu-id="53f32-1791">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1791">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1792">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1792">Az.RecoveryServices</span></span>
* <span data-ttu-id="53f32-1793">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1793">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="53f32-1794">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1794">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1795">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1795">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1796">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="53f32-1796">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="53f32-1797">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1797">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53f32-1798">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="53f32-1798">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="53f32-1799">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="53f32-1799">Az.Aks</span></span>
* <span data-ttu-id="53f32-1800">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1800">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="53f32-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-1801">Az.Automation</span></span>
* <span data-ttu-id="53f32-1802">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="53f32-1802">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="53f32-1803">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1803">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="53f32-1804">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="53f32-1804">Az.Cdn</span></span>
* <span data-ttu-id="53f32-1805">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1805">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1806">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1806">Az.Compute</span></span>
* <span data-ttu-id="53f32-1807">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="53f32-1807">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="53f32-1808">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="53f32-1808">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="53f32-1809">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="53f32-1809">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="53f32-1810">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="53f32-1810">Az.ContainerRegistry</span></span>
* <span data-ttu-id="53f32-1811">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1811">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="53f32-1812">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="53f32-1812">Az.DataFactory</span></span>
* <span data-ttu-id="53f32-1813">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="53f32-1813">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1814">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1814">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-1815">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="53f32-1815">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="53f32-1816">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="53f32-1816">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="53f32-1817">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1817">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-1818">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1818">Az.IotHub</span></span>
* <span data-ttu-id="53f32-1819">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="53f32-1819">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="53f32-1820">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1820">Az.KeyVault</span></span>
* <span data-ttu-id="53f32-1821">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1821">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-1822">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1822">Az.Network</span></span>
* <span data-ttu-id="53f32-1823">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1823">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1824">Az.Resources</span></span>
* <span data-ttu-id="53f32-1825">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="53f32-1825">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="53f32-1826">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="53f32-1826">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="53f32-1827">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="53f32-1827">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="53f32-1828">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="53f32-1828">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="53f32-1829">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="53f32-1829">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="53f32-1830">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="53f32-1830">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="53f32-1831">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="53f32-1831">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-1832">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1832">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-1833">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="53f32-1833">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="53f32-1834">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="53f32-1834">Fix some error messages.</span></span>
* <span data-ttu-id="53f32-1835">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="53f32-1835">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="53f32-1836">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="53f32-1836">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53f32-1837">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53f32-1837">Az.SignalR</span></span>
* <span data-ttu-id="53f32-1838">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1838">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1839">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1839">Az.Sql</span></span>
* <span data-ttu-id="53f32-1840">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1840">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53f32-1841">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="53f32-1841">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="53f32-1842">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="53f32-1842">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="53f32-1843">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="53f32-1843">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1844">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1844">Az.Storage</span></span>
* <span data-ttu-id="53f32-1845">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1845">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53f32-1846">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="53f32-1846">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="53f32-1847">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="53f32-1847">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="53f32-1848">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="53f32-1848">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="53f32-1849">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="53f32-1849">Az.TrafficManager</span></span>
* <span data-ttu-id="53f32-1850">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1850">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1851">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1851">Az.Websites</span></span>
* <span data-ttu-id="53f32-1852">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="53f32-1852">Update incorrect online help URLs</span></span>
* <span data-ttu-id="53f32-1853">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1853">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="53f32-1854">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="53f32-1854">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="53f32-1855">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="53f32-1855">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="53f32-1856">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1856">Az.Accounts</span></span>
* <span data-ttu-id="53f32-1857">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="53f32-1857">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-1858">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1858">Az.Compute</span></span>
* <span data-ttu-id="53f32-1859">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="53f32-1859">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="53f32-1860">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="53f32-1860">Updated the description of ID in help files</span></span>
* <span data-ttu-id="53f32-1861">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1861">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1862">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1862">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-1863">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="53f32-1863">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="53f32-1864">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="53f32-1864">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="53f32-1865">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="53f32-1865">Az.EventGrid</span></span>
* <span data-ttu-id="53f32-1866">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="53f32-1866">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="53f32-1867">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="53f32-1867">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="53f32-1868">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="53f32-1868">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="53f32-1869">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="53f32-1869">Event Time-To-Live,</span></span>
        - <span data-ttu-id="53f32-1870">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="53f32-1870">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="53f32-1871">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="53f32-1871">Dead letter endpoint.</span></span>
    - <span data-ttu-id="53f32-1872">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="53f32-1872">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="53f32-1873">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="53f32-1873">Event Time-To-Live,</span></span>
        - <span data-ttu-id="53f32-1874">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="53f32-1874">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="53f32-1875">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="53f32-1875">Dead letter endpoint.</span></span>
* <span data-ttu-id="53f32-1876">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="53f32-1876">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="53f32-1877">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="53f32-1877">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="53f32-1878">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1878">Az.IotHub</span></span>
* <span data-ttu-id="53f32-1879">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="53f32-1879">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="53f32-1880">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="53f32-1880">Az.LogicApp</span></span>
* <span data-ttu-id="53f32-1881">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="53f32-1881">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-1882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1882">Az.Resources</span></span>
* <span data-ttu-id="53f32-1883">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="53f32-1883">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="53f32-1884">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="53f32-1884">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="53f32-1885">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53f32-1885">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="53f32-1886">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="53f32-1886">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="53f32-1887">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="53f32-1887">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="53f32-1888">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="53f32-1888">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="53f32-1889">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="53f32-1889">Az.SignalR</span></span>
* <span data-ttu-id="53f32-1890">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1890">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-1891">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1891">Az.Sql</span></span>
* <span data-ttu-id="53f32-1892">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="53f32-1892">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="53f32-1893">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1893">Az.Storage</span></span>
* <span data-ttu-id="53f32-1894">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="53f32-1894">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="53f32-1895">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="53f32-1895">New-AzStorageContext</span></span>
* <span data-ttu-id="53f32-1896">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="53f32-1896">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="53f32-1897">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="53f32-1897">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-1898">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1898">Az.Websites</span></span>
* <span data-ttu-id="53f32-1899">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="53f32-1899">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="53f32-1900">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1900">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="53f32-1901">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-1901">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="53f32-1902">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-1902">General</span></span>

- <span data-ttu-id="53f32-1903">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="53f32-1903">General Availability of Az Module</span></span>
- <span data-ttu-id="53f32-1904">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="53f32-1904">Online help for each module</span></span>
- <span data-ttu-id="53f32-1905">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="53f32-1905">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="53f32-1906">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="53f32-1906">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="53f32-1907">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1907">Az.Accounts</span></span>
- <span data-ttu-id="53f32-1908">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53f32-1908">Changed from Az.Profile</span></span>
- <span data-ttu-id="53f32-1909">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="53f32-1909">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="53f32-1910">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-1910">Az.ApiManagement</span></span>
- <span data-ttu-id="53f32-1911">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="53f32-1911">Fixes for #7002</span></span>
- <span data-ttu-id="53f32-1912">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1912">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="53f32-1913">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="53f32-1913">Az.Batch</span></span>
- <span data-ttu-id="53f32-1914">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="53f32-1914">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="53f32-1915">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="53f32-1915">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="53f32-1916">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1916">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="53f32-1917">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="53f32-1917">Az.Billing</span></span>
- <span data-ttu-id="53f32-1918">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1918">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="53f32-1919">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1919">Az.CognitivServices</span></span>
- <span data-ttu-id="53f32-1920">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-1920">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="53f32-1921">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="53f32-1921">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="53f32-1922">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-1922">Az.ContainerInstance</span></span>
- <span data-ttu-id="53f32-1923">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="53f32-1923">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="53f32-1924">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="53f32-1924">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="53f32-1925">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1925">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1926">Az.DataLakeStore</span></span>
- <span data-ttu-id="53f32-1927">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1927">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="53f32-1928">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="53f32-1928">Az.Monitor</span></span>
- <span data-ttu-id="53f32-1929">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1929">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="53f32-1930">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="53f32-1930">Az.KeyVault</span></span>
- <span data-ttu-id="53f32-1931">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="53f32-1931">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="53f32-1932">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="53f32-1932">Az.MachineLearning</span></span>
- <span data-ttu-id="53f32-1933">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="53f32-1933">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="53f32-1934">Az.Media</span><span class="sxs-lookup"><span data-stu-id="53f32-1934">Az.Media</span></span>
- <span data-ttu-id="53f32-1935">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="53f32-1935">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="53f32-1936">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-1936">Az.Network</span></span>
<span data-ttu-id="53f32-1937">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="53f32-1937">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="53f32-1938">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="53f32-1938">New cmdlets added:</span></span>
        - <span data-ttu-id="53f32-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1939">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1940">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1941">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1942">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1943">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1944">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1944">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="53f32-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1945">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="53f32-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="53f32-1946">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="53f32-1947">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="53f32-1947">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="53f32-1948">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="53f32-1948">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="53f32-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1949">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="53f32-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="53f32-1950">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="53f32-1951">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1951">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="53f32-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-1952">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="53f32-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="53f32-1953">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="53f32-1954">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="53f32-1954">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="53f32-1955">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f32-1955">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="53f32-1956">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f32-1956">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="53f32-1957">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="53f32-1957">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="53f32-1958">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="53f32-1958">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="53f32-1959">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1959">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="53f32-1960">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-1960">Az.OperationalInsights</span></span>
- <span data-ttu-id="53f32-1961">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1961">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="53f32-1962">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53f32-1962">Az.Profile</span></span>
- <span data-ttu-id="53f32-1963">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="53f32-1963">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1964">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1964">Az.RecoveryServices</span></span>
- <span data-ttu-id="53f32-1965">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1965">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="53f32-1966">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1966">Az.Resources</span></span>
- <span data-ttu-id="53f32-1967">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1967">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="53f32-1968">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-1968">Az.ServiceFabric</span></span>
- <span data-ttu-id="53f32-1969">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="53f32-1969">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="53f32-1970">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1970">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="53f32-1971">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="53f32-1971">Az.SIgnalR</span></span>
- <span data-ttu-id="53f32-1972">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="53f32-1972">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="53f32-1973">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1973">Az.Sql</span></span>
- <span data-ttu-id="53f32-1974">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="53f32-1974">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="53f32-1975">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1975">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="53f32-1976">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1976">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="53f32-1977">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-1977">Az.Storage</span></span>
- <span data-ttu-id="53f32-1978">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1978">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="53f32-1979">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-1979">Az.Websites</span></span>
- <span data-ttu-id="53f32-1980">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="53f32-1980">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="53f32-1981">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-1981">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="53f32-1982">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-1982">General</span></span>

* <span data-ttu-id="53f32-1983">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="53f32-1983">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="53f32-1984">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-1984">Az.Compute</span></span>

* <span data-ttu-id="53f32-1985">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="53f32-1985">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="53f32-1986">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-1986">Az.DataLakeStore</span></span>

* <span data-ttu-id="53f32-1987">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="53f32-1987">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="53f32-1988">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="53f32-1988">Az.FrontDoor</span></span>

* <span data-ttu-id="53f32-1989">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="53f32-1989">Fixed some broken links</span></span>
    - <span data-ttu-id="53f32-1990">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="53f32-1990">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="53f32-1991">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="53f32-1991">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="53f32-1992">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="53f32-1992">Az.RecoveryServices</span></span>

* <span data-ttu-id="53f32-1993">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-1993">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="53f32-1994">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="53f32-1994">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="53f32-1995">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-1995">Az.Resources</span></span>

* <span data-ttu-id="53f32-1996">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="53f32-1996">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="53f32-1997">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="53f32-1997">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="53f32-1998">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-1998">Az.Sql</span></span>

* <span data-ttu-id="53f32-1999">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="53f32-1999">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="53f32-2000">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="53f32-2000">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="53f32-2001">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="53f32-2001">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="53f32-2002">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-2002">Az.Storage</span></span>

* <span data-ttu-id="53f32-2003">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-2003">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="53f32-2004">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="53f32-2004">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="53f32-2005">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-2005">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="53f32-2006">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="53f32-2006">Support Static Website configuration</span></span>
    - <span data-ttu-id="53f32-2007">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53f32-2007">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="53f32-2008">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="53f32-2008">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="53f32-2009">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-2009">Az.Websites</span></span>

* <span data-ttu-id="53f32-2010">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="53f32-2010">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="53f32-2011">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="53f32-2011">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="53f32-2012">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="53f32-2012">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="53f32-2013">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-2013">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="53f32-2014">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="53f32-2014">Az.ApiManagement</span></span>
* <span data-ttu-id="53f32-2015">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="53f32-2015">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="53f32-2016">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="53f32-2016">Az.Automation</span></span>
* <span data-ttu-id="53f32-2017">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="53f32-2017">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="53f32-2018">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="53f32-2018">Added Update Management cmdlets</span></span>
* <span data-ttu-id="53f32-2019">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="53f32-2019">Added Source Control cmdlets</span></span>
* <span data-ttu-id="53f32-2020">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="53f32-2020">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="53f32-2021">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="53f32-2021">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="53f32-2022">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-2022">Az.Compute</span></span>
* <span data-ttu-id="53f32-2023">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="53f32-2023">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="53f32-2024">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="53f32-2024">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="53f32-2025">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-2025">Az.ContainerInstance</span></span>
* <span data-ttu-id="53f32-2026">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="53f32-2026">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="53f32-2027">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="53f32-2027">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="53f32-2028">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="53f32-2028">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="53f32-2029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-2029">Az.Network</span></span>
* <span data-ttu-id="53f32-2030">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="53f32-2030">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="53f32-2031">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="53f32-2031">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="53f32-2032">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="53f32-2032">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="53f32-2033">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="53f32-2033">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="53f32-2034">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="53f32-2034">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="53f32-2035">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="53f32-2035">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="53f32-2036">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="53f32-2036">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="53f32-2037">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="53f32-2037">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="53f32-2038">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="53f32-2038">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="53f32-2039">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="53f32-2039">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="53f32-2040">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="53f32-2040">Az.Relay</span></span>
* <span data-ttu-id="53f32-2041">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="53f32-2041">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="53f32-2042">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-2042">Az.Resources</span></span>
* <span data-ttu-id="53f32-2043">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="53f32-2043">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="53f32-2044">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="53f32-2044">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="53f32-2045">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="53f32-2045">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="53f32-2046">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-2046">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-2047">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="53f32-2047">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="53f32-2048">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-2048">Az.Sql</span></span>
* <span data-ttu-id="53f32-2049">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="53f32-2049">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="53f32-2050">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-2050">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53f32-2051">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-2051">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53f32-2052">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-2052">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53f32-2053">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="53f32-2053">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="53f32-2054">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="53f32-2054">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53f32-2055">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="53f32-2055">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53f32-2056">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="53f32-2056">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="53f32-2057">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="53f32-2057">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="53f32-2058">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="53f32-2058">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="53f32-2059">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="53f32-2059">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="53f32-2060">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="53f32-2060">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="53f32-2061">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="53f32-2061">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="53f32-2062">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="53f32-2062">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="53f32-2063">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="53f32-2063">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="53f32-2064">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="53f32-2064">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="53f32-2065">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="53f32-2065">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="53f32-2066">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-2066">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="53f32-2067">Generale</span><span class="sxs-lookup"><span data-stu-id="53f32-2067">General</span></span>
* <span data-ttu-id="53f32-2068">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="53f32-2068">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="53f32-2069">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53f32-2069">Az.Profile</span></span>
* <span data-ttu-id="53f32-2070">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="53f32-2070">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="53f32-2071">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="53f32-2071">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="53f32-2072">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="53f32-2072">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="53f32-2073">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="53f32-2073">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="53f32-2074">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="53f32-2074">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="53f32-2075">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="53f32-2075">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="53f32-2076">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="53f32-2076">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-2077">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-2077">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-2078">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="53f32-2078">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-2079">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-2079">Az.Compute</span></span>
* <span data-ttu-id="53f32-2080">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="53f32-2080">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="53f32-2081">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="53f32-2081">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="53f32-2082">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="53f32-2082">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-2083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-2083">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-2084">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="53f32-2084">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="53f32-2085">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="53f32-2085">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="53f32-2086">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="53f32-2086">Az.Insights</span></span>
* <span data-ttu-id="53f32-2087">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="53f32-2087">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="53f32-2088">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="53f32-2088">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="53f32-2089">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="53f32-2089">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="53f32-2090">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="53f32-2090">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-2091">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-2091">Az.Network</span></span>
* <span data-ttu-id="53f32-2092">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="53f32-2092">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="53f32-2093">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-2093">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="53f32-2094">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="53f32-2094">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="53f32-2095">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="53f32-2095">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="53f32-2096">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="53f32-2096">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="53f32-2097">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="53f32-2097">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="53f32-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="53f32-2098">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="53f32-2099">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="53f32-2099">Az.PolicyInsights</span></span>
* <span data-ttu-id="53f32-2100">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="53f32-2100">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-2101">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-2101">Az.Resources</span></span>
* <span data-ttu-id="53f32-2102">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="53f32-2102">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="53f32-2103">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="53f32-2103">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="53f32-2104">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="53f32-2104">Az.ServiceBus</span></span>
* <span data-ttu-id="53f32-2105">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="53f32-2105">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="53f32-2106">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="53f32-2106">Az.ServiceFabric</span></span>
* <span data-ttu-id="53f32-2107">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="53f32-2107">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="53f32-2108">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="53f32-2108">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="53f32-2109">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="53f32-2109">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="53f32-2110">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="53f32-2110">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="53f32-2111">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="53f32-2111">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="53f32-2112">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-2112">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="53f32-2113">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="53f32-2113">Az.Profile</span></span>
* <span data-ttu-id="53f32-2114">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="53f32-2114">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="53f32-2115">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="53f32-2115">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-2116">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-2116">Az.Compute</span></span>
* <span data-ttu-id="53f32-2117">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="53f32-2117">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="53f32-2118">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f32-2118">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="53f32-2119">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="53f32-2119">Az.DataLakeStore</span></span>
* <span data-ttu-id="53f32-2120">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="53f32-2120">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="53f32-2121">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53f32-2121">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="53f32-2122">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="53f32-2122">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="53f32-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="53f32-2123">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="53f32-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="53f32-2124">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-2125">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-2125">Az.Network</span></span>
* <span data-ttu-id="53f32-2126">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="53f32-2126">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="53f32-2127">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f32-2127">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-2128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-2128">Az.Resources</span></span>
* <span data-ttu-id="53f32-2129">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="53f32-2129">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="53f32-2130">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="53f32-2130">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="53f32-2131">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-2131">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="53f32-2132">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="53f32-2132">Azure.Storage</span></span>
* <span data-ttu-id="53f32-2133">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="53f32-2133">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="53f32-2134">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-2134">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="53f32-2135">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="53f32-2135">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="53f32-2136">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="53f32-2136">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="53f32-2137">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="53f32-2137">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="53f32-2138">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="53f32-2138">Az.CognitiveServices</span></span>
* <span data-ttu-id="53f32-2139">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="53f32-2139">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="53f32-2140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="53f32-2140">Az.Compute</span></span>
* <span data-ttu-id="53f32-2141">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="53f32-2141">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="53f32-2142">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="53f32-2142">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="53f32-2143">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="53f32-2143">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="53f32-2144">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="53f32-2144">Az.DataFactoryV2</span></span>
* <span data-ttu-id="53f32-2145">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="53f32-2145">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="53f32-2146">Az.Network</span><span class="sxs-lookup"><span data-stu-id="53f32-2146">Az.Network</span></span>
* <span data-ttu-id="53f32-2147">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53f32-2147">Added NetworkProfile functionality.</span></span> <span data-ttu-id="53f32-2148">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="53f32-2148">new cmdlets added</span></span>
    - <span data-ttu-id="53f32-2149">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53f32-2149">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="53f32-2150">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53f32-2150">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="53f32-2151">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53f32-2151">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="53f32-2152">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="53f32-2152">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="53f32-2153">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-2153">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="53f32-2154">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-2154">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="53f32-2155">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="53f32-2155">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="53f32-2156">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="53f32-2156">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="53f32-2157">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="53f32-2157">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="53f32-2158">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="53f32-2158">Az.RedisCache</span></span>
* <span data-ttu-id="53f32-2159">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="53f32-2159">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="53f32-2160">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="53f32-2160">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="53f32-2161">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="53f32-2161">Az.Resources</span></span>
* <span data-ttu-id="53f32-2162">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="53f32-2162">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="53f32-2163">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="53f32-2163">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="53f32-2164">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="53f32-2164">Az.Sql</span></span>
* <span data-ttu-id="53f32-2165">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="53f32-2165">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="53f32-2166">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="53f32-2166">Az.Websites</span></span>
* <span data-ttu-id="53f32-2167">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="53f32-2167">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="53f32-2168">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="53f32-2168">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="53f32-2169">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="53f32-2169">0.2.0 - September 2018</span></span>
 <span data-ttu-id="53f32-2170">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="53f32-2170">Initial Release</span></span>
