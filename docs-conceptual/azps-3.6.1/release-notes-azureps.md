---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: f24e5ef66f9c49976c550c9847903bd0608c5123
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/11/2020
ms.locfileid: "79111037"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="2c7c7-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c7c7-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="2c7c7-104">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="2c7c7-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-105">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-106">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="2c7c7-107">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="2c7c7-108">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-109">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-110">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="2c7c7-111">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="2c7c7-112">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="2c7c7-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="2c7c7-113">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-115">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-116">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-117">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2c7c7-118">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="2c7c7-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="2c7c7-123">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="2c7c7-124">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="2c7c7-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="2c7c7-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="2c7c7-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="2c7c7-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="2c7c7-129">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2c7c7-130">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="2c7c7-131">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="2c7c7-132">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="2c7c7-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="2c7c7-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="2c7c7-135">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-136">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-137">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-138">Az.Network</span></span>
* <span data-ttu-id="2c7c7-139">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="2c7c7-140">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="2c7c7-141">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="2c7c7-142">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-143">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-144">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="2c7c7-145">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="2c7c7-146">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="2c7c7-147">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="2c7c7-148">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="2c7c7-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="2c7c7-149">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="2c7c7-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="2c7c7-150">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="2c7c7-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="2c7c7-151">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="2c7c7-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2c7c7-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="2c7c7-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="2c7c7-155">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="2c7c7-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="2c7c7-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="2c7c7-157">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-157">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-158">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-159">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="2c7c7-160">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="2c7c7-161">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="2c7c7-161">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="2c7c7-162">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="2c7c7-163">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-163">Remove an LTR backup</span></span>
    - <span data-ttu-id="2c7c7-164">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="2c7c7-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="2c7c7-165">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="2c7c7-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="2c7c7-166">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="2c7c7-167">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-168">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-169">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="2c7c7-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="2c7c7-171">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="2c7c7-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="2c7c7-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="2c7c7-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-174">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-175">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="2c7c7-176">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="2c7c7-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="2c7c7-177">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="2c7c7-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="2c7c7-178">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="2c7c7-179">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2c7c7-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="2c7c7-180">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="2c7c7-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-181">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-181">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-182">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="2c7c7-183">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="2c7c7-184">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-185">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-186">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="2c7c7-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-187">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-188">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-190">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="2c7c7-191">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-192">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-193">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2c7c7-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-194">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-195">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="2c7c7-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-196">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-197">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="2c7c7-198">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="2c7c7-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="2c7c7-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-203">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-204">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="2c7c7-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-205">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-206">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="2c7c7-207">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="2c7c7-208">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-209">Az.Network</span></span>
* <span data-ttu-id="2c7c7-210">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="2c7c7-211">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2c7c7-212">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="2c7c7-213">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="2c7c7-214">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-214">No new cmdlets are added.</span></span> <span data-ttu-id="2c7c7-215">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-217">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-218">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-219">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="2c7c7-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="2c7c7-220">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="2c7c7-221">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="2c7c7-222">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="2c7c7-223">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="2c7c7-224">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="2c7c7-225">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="2c7c7-226">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-227">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-228">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="2c7c7-229">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="2c7c7-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="2c7c7-230">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2c7c7-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2c7c7-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2c7c7-232">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="2c7c7-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2c7c7-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2c7c7-233">Az.StorageSync</span></span>
* <span data-ttu-id="2c7c7-234">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="2c7c7-235">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="2c7c7-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-236">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-236">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-237">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="2c7c7-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="2c7c7-238">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-239">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-240">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="2c7c7-241">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="2c7c7-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-242">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-243">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="2c7c7-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="2c7c7-244">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="2c7c7-245">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="2c7c7-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="2c7c7-246">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-247">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-248">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="2c7c7-249">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="2c7c7-250">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="2c7c7-252">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-253">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-254">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2c7c7-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2c7c7-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="2c7c7-256">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="2c7c7-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="2c7c7-257">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="2c7c7-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-258">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-259">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-260">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-261">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-262">Az.Network</span></span>
* <span data-ttu-id="2c7c7-263">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="2c7c7-264">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="2c7c7-265">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-266">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="2c7c7-267">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="2c7c7-268">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="2c7c7-269">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="2c7c7-270">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="2c7c7-271">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-271">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="2c7c7-273">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="2c7c7-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="2c7c7-275">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2c7c7-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="2c7c7-277">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="2c7c7-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="2c7c7-278">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="2c7c7-279">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="2c7c7-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="2c7c7-280">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="2c7c7-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-282">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="2c7c7-283">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-284">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-285">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="2c7c7-286">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="2c7c7-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-287">Az.Sql</span></span>
<span data-ttu-id="2c7c7-288">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-289">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-290">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="2c7c7-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="2c7c7-292">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="2c7c7-293">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-294">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-295">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="2c7c7-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="2c7c7-296">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="2c7c7-297">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="2c7c7-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-298">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-299">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="2c7c7-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-300">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-301">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-302">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-303">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2c7c7-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="2c7c7-305">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2c7c7-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2c7c7-307">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2c7c7-308">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="2c7c7-309">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2c7c7-310">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="2c7c7-311">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2c7c7-312">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="2c7c7-313">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="2c7c7-314">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="2c7c7-315">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2c7c7-316">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="2c7c7-317">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2c7c7-318">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="2c7c7-319">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="2c7c7-320">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="2c7c7-321">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="2c7c7-322">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="2c7c7-323">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="2c7c7-324">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-325">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-326">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="2c7c7-327">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="2c7c7-328">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="2c7c7-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="2c7c7-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="2c7c7-330">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="2c7c7-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-331">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-332">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="2c7c7-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-333">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-334">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2c7c7-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2c7c7-335">Az.MachineLearning</span></span>
* <span data-ttu-id="2c7c7-336">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="2c7c7-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2c7c7-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="2c7c7-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="2c7c7-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2c7c7-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="2c7c7-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2c7c7-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="2c7c7-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="2c7c7-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="2c7c7-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="2c7c7-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="2c7c7-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-344">Az.Network</span></span>
* <span data-ttu-id="2c7c7-345">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="2c7c7-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-347">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="2c7c7-348">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2c7c7-349">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="2c7c7-350">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-351">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-352">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-353">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-354">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="2c7c7-355">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="2c7c7-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="2c7c7-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="2c7c7-357">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="2c7c7-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-358">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-359">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="2c7c7-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="2c7c7-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="2c7c7-361">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="2c7c7-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="2c7c7-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="2c7c7-363">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="2c7c7-364">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-364">General</span></span>
* <span data-ttu-id="2c7c7-365">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="2c7c7-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-366">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-367">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="2c7c7-368">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2c7c7-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-369">Az.Batch</span></span>
* <span data-ttu-id="2c7c7-370">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-371">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-372">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-373">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-374">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="2c7c7-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="2c7c7-375">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2c7c7-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2c7c7-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="2c7c7-377">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="2c7c7-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-378">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-379">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="2c7c7-380">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="2c7c7-381">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-382">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-383">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="2c7c7-384">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="2c7c7-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="2c7c7-385">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-386">Az.Network</span></span>
* <span data-ttu-id="2c7c7-387">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-388">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-389">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="2c7c7-390">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-391">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-392">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="2c7c7-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-393">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-394">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="2c7c7-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="2c7c7-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="2c7c7-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="2c7c7-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2c7c7-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="2c7c7-397">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="2c7c7-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="2c7c7-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="2c7c7-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="2c7c7-399">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="2c7c7-400">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="2c7c7-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="2c7c7-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="2c7c7-403">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="2c7c7-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="2c7c7-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="2c7c7-405">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="2c7c7-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="2c7c7-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="2c7c7-407">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-408">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-408">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-409">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="2c7c7-410">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-411">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-412">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-412">VM Reapply feature</span></span>
    - <span data-ttu-id="2c7c7-413">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="2c7c7-414">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="2c7c7-415">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="2c7c7-416">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="2c7c7-417">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2c7c7-418">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="2c7c7-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="2c7c7-419">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="2c7c7-420">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="2c7c7-421">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="2c7c7-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="2c7c7-422">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="2c7c7-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="2c7c7-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="2c7c7-424">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2c7c7-425">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-425">Get the Order</span></span>
* <span data-ttu-id="2c7c7-426">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2c7c7-427">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-427">Create new Order</span></span>
* <span data-ttu-id="2c7c7-428">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="2c7c7-429">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="2c7c7-429">Remove the Order</span></span>
* <span data-ttu-id="2c7c7-430">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="2c7c7-431">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-431">Now creates Local Share</span></span>
* <span data-ttu-id="2c7c7-432">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="2c7c7-433">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="2c7c7-434">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="2c7c7-435">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="2c7c7-436">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2c7c7-437">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="2c7c7-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="2c7c7-438">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2c7c7-439">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="2c7c7-439">Create new Triggers</span></span>
* <span data-ttu-id="2c7c7-440">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="2c7c7-441">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="2c7c7-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-442">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-443">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="2c7c7-444">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-446">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="2c7c7-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-447">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-448">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="2c7c7-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-449">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-450">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="2c7c7-451">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="2c7c7-452">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="2c7c7-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-454">Az.Network</span></span>
* <span data-ttu-id="2c7c7-455">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="2c7c7-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="2c7c7-456">Az.PrivateDns</span></span>
* <span data-ttu-id="2c7c7-457">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-459">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="2c7c7-460">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="2c7c7-461">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2c7c7-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-462">Az.RedisCache</span></span>
* <span data-ttu-id="2c7c7-463">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="2c7c7-464">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="2c7c7-465">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-466">Az.Resources</span></span>
- <span data-ttu-id="2c7c7-467">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="2c7c7-468">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="2c7c7-469">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="2c7c7-470">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="2c7c7-471">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-472">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-473">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="2c7c7-474">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="2c7c7-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="2c7c7-475">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="2c7c7-476">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-476">General</span></span>
* <span data-ttu-id="2c7c7-477">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-478">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-479">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2c7c7-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-480">Az.Advisor</span></span>
* <span data-ttu-id="2c7c7-481">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2c7c7-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-482">Az.Batch</span></span>
* <span data-ttu-id="2c7c7-483">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="2c7c7-484">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="2c7c7-485">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="2c7c7-486">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="2c7c7-487">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="2c7c7-488">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="2c7c7-489">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="2c7c7-490">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="2c7c7-491">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="2c7c7-492">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2c7c7-493">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="2c7c7-494">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="2c7c7-495">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="2c7c7-496">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="2c7c7-497">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="2c7c7-498">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="2c7c7-499">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="2c7c7-500">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="2c7c7-501">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="2c7c7-502">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="2c7c7-503">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2c7c7-504">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="2c7c7-505">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="2c7c7-506">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="2c7c7-507">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="2c7c7-508">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="2c7c7-509">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="2c7c7-510">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="2c7c7-511">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="2c7c7-512">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="2c7c7-513">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="2c7c7-514">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="2c7c7-515">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="2c7c7-516">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="2c7c7-517">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="2c7c7-518">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-519">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-520">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="2c7c7-521">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-522">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-523">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="2c7c7-524">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="2c7c7-525">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2c7c7-525">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="2c7c7-526">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-526">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2c7c7-527">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-527">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="2c7c7-528">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="2c7c7-528">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="2c7c7-529">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-529">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="2c7c7-530">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-530">Breaking changes</span></span>
    - <span data-ttu-id="2c7c7-531">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="2c7c7-531">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="2c7c7-532">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-532">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-533">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-533">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-534">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-534">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-535">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-535">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-536">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-536">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="2c7c7-537">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-537">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="2c7c7-538">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="2c7c7-538">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="2c7c7-539">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="2c7c7-539">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="2c7c7-540">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="2c7c7-540">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="2c7c7-541">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="2c7c7-541">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-542">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-542">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-543">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="2c7c7-543">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-544">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-544">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-545">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-545">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="2c7c7-546">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-546">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="2c7c7-547">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-547">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="2c7c7-548">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-548">Removed five cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-549">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2c7c7-549">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2c7c7-550">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2c7c7-550">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2c7c7-551">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="2c7c7-551">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="2c7c7-552">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c7c7-552">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="2c7c7-553">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c7c7-553">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="2c7c7-554">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-554">Added three cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-555">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2c7c7-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-556">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="2c7c7-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-557">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="2c7c7-558">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-558">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="2c7c7-559">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-559">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="2c7c7-560">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-560">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="2c7c7-561">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-561">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="2c7c7-562">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-562">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="2c7c7-563">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-563">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="2c7c7-564">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-564">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="2c7c7-565">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-565">Added some scenario test cases.</span></span>
* <span data-ttu-id="2c7c7-566">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-566">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-567">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-567">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-568">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-568">Breaking changes:</span></span>
    - <span data-ttu-id="2c7c7-569">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-569">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2c7c7-570">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-570">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2c7c7-571">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-571">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2c7c7-572">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-572">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2c7c7-573">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-573">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="2c7c7-574">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="2c7c7-575">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-575">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="2c7c7-576">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-576">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="2c7c7-577">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-577">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2c7c7-578">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-578">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="2c7c7-579">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-579">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="2c7c7-580">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-580">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-581">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-581">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-582">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-582">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-583">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-583">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="2c7c7-584">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-584">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="2c7c7-585">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-585">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-586">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-586">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-587">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-587">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-588">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-588">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-589">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-589">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-590">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="2c7c7-590">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-591">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-591">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-592">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-592">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-593">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-593">Az.Network</span></span>
* <span data-ttu-id="2c7c7-594">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-594">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="2c7c7-595">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-595">Updated cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-596">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-596">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-597">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-597">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-598">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-598">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-599">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-599">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-600">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-600">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2c7c7-601">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-601">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="2c7c7-602">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-602">New cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-603">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-603">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="2c7c7-604">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-604">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="2c7c7-605">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-605">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="2c7c7-606">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-606">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="2c7c7-607">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-607">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="2c7c7-608">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-608">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="2c7c7-609">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-609">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="2c7c7-610">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-610">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="2c7c7-611">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-611">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-612">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-612">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="2c7c7-613">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-613">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2c7c7-614">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-614">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2c7c7-615">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-615">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="2c7c7-616">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-616">Set-AzVirtualHub</span></span>
* <span data-ttu-id="2c7c7-617">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="2c7c7-617">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="2c7c7-618">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-618">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2c7c7-619">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="2c7c7-619">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2c7c7-620">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="2c7c7-620">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="2c7c7-621">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-621">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="2c7c7-622">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-622">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="2c7c7-623">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-623">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="2c7c7-624">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-624">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-625">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-625">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="2c7c7-626">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-626">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2c7c7-627">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-627">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2c7c7-628">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-628">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2c7c7-629">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-629">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2c7c7-630">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-630">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="2c7c7-631">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-631">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="2c7c7-632">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="2c7c7-632">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="2c7c7-633">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-633">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-634">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="2c7c7-634">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="2c7c7-635">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-635">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="2c7c7-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="2c7c7-636">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="2c7c7-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="2c7c7-637">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="2c7c7-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-638">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="2c7c7-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-639">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="2c7c7-640">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-640">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2c7c7-641">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-641">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="2c7c7-642">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-642">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="2c7c7-643">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="2c7c7-643">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="2c7c7-644">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-644">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="2c7c7-645">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-645">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="2c7c7-646">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-646">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="2c7c7-647">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-647">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="2c7c7-648">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="2c7c7-648">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="2c7c7-649">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-649">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="2c7c7-650">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-650">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="2c7c7-651">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-651">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-652">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-652">New-AzIpGroup</span></span>
        - <span data-ttu-id="2c7c7-653">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-653">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="2c7c7-654">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-654">Get-AzIpGroup</span></span>
        - <span data-ttu-id="2c7c7-655">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-655">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-656">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-656">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-657">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-657">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-658">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-658">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-659">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-659">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="2c7c7-660">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-660">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="2c7c7-661">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-661">Removed deprecated aliases:</span></span>
* <span data-ttu-id="2c7c7-662">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-662">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="2c7c7-663">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-663">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="2c7c7-664">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-664">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2c7c7-665">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-665">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="2c7c7-666">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-666">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="2c7c7-667">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-667">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-668">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-668">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-669">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-669">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="2c7c7-670">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-670">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2c7c7-671">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-671">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2c7c7-672">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="2c7c7-672">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="2c7c7-673">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2c7c7-673">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="2c7c7-674">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2c7c7-674">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="2c7c7-675">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-675">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="2c7c7-676">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-676">General</span></span>
* <span data-ttu-id="2c7c7-677">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-677">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-678">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-678">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-679">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-679">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-680">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-680">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-681">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-681">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="2c7c7-682">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="2c7c7-682">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-683">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-683">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-684">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-684">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2c7c7-685">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-685">Az.Batch</span></span>
* <span data-ttu-id="2c7c7-686">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-686">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-687">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-687">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-688">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-688">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="2c7c7-689">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-689">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="2c7c7-690">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-690">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="2c7c7-691">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-691">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-692">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-692">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-693">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-693">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="2c7c7-694">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-694">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="2c7c7-695">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-695">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-696">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-696">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-697">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="2c7c7-697">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="2c7c7-698">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="2c7c7-698">Az.HealthcareApis</span></span>
* <span data-ttu-id="2c7c7-699">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-699">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="2c7c7-700">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-700">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="2c7c7-701">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="2c7c7-701">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="2c7c7-702">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-702">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-703">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-703">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-704">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="2c7c7-704">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="2c7c7-705">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-705">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-706">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-706">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-707">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="2c7c7-707">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="2c7c7-708">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-708">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="2c7c7-709">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="2c7c7-709">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="2c7c7-710">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-710">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-711">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-711">Az.Network</span></span>
* <span data-ttu-id="2c7c7-712">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-712">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="2c7c7-713">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-713">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="2c7c7-714">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-714">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-715">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-715">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="2c7c7-716">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-716">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2c7c7-717">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="2c7c7-717">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="2c7c7-718">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-718">Updated cmdlets:</span></span>
        - <span data-ttu-id="2c7c7-719">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-719">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2c7c7-720">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-720">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2c7c7-721">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-721">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2c7c7-722">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="2c7c7-722">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="2c7c7-723">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="2c7c7-723">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="2c7c7-724">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-724">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="2c7c7-725">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-725">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2c7c7-726">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-726">Az.RedisCache</span></span>
* <span data-ttu-id="2c7c7-727">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="2c7c7-727">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-728">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-728">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-729">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-729">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-730">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-730">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-731">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-731">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="2c7c7-732">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2c7c7-732">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2c7c7-733">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="2c7c7-733">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="2c7c7-734">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="2c7c7-734">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="2c7c7-735">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-735">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2c7c7-736">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2c7c7-736">Az.StorageSync</span></span>
* <span data-ttu-id="2c7c7-737">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-737">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-738">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-738">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-739">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="2c7c7-739">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="2c7c7-740">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-740">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-741">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-741">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-742">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-742">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="2c7c7-743">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-743">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="2c7c7-744">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-744">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-745">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-745">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-746">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-746">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="2c7c7-747">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="2c7c7-747">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="2c7c7-748">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-748">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-749">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-749">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-750">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-750">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="2c7c7-751">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-751">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2c7c7-752">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-752">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="2c7c7-753">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-753">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="2c7c7-754">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-754">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="2c7c7-755">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-755">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="2c7c7-756">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-756">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="2c7c7-757">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-757">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="2c7c7-758">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-758">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-759">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-759">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-760">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-760">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="2c7c7-761">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="2c7c7-761">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-762">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-762">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-763">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-763">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-764">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-764">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-765">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-765">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="2c7c7-766">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-766">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="2c7c7-767">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-767">New cmdlets are:</span></span>
    - <span data-ttu-id="2c7c7-768">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-768">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2c7c7-769">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-769">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2c7c7-770">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-770">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="2c7c7-771">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-771">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-772">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-772">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-773">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-773">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="2c7c7-774">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-774">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="2c7c7-775">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-775">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="2c7c7-776">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-776">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="2c7c7-777">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-777">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="2c7c7-778">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-778">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="2c7c7-779">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-779">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="2c7c7-780">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-780">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="2c7c7-781">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-781">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2c7c7-782">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-782">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="2c7c7-783">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-783">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="2c7c7-784">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-784">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="2c7c7-785">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-785">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="2c7c7-786">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="2c7c7-786">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="2c7c7-787">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="2c7c7-787">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="2c7c7-788">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-788">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="2c7c7-789">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-789">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="2c7c7-790">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-790">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="2c7c7-791">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-791">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="2c7c7-792">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-792">Overall improved help files</span></span>
* <span data-ttu-id="2c7c7-793">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-793">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-794">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-794">Az.Network</span></span>
* <span data-ttu-id="2c7c7-795">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-795">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="2c7c7-796">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-796">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="2c7c7-797">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="2c7c7-797">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="2c7c7-798">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-798">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="2c7c7-799">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="2c7c7-799">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="2c7c7-800">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="2c7c7-800">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="2c7c7-801">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-801">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="2c7c7-802">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="2c7c7-802">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="2c7c7-803">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-803">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="2c7c7-804">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-804">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="2c7c7-805">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-805">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="2c7c7-806">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-806">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="2c7c7-807">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-807">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-808">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="2c7c7-808">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="2c7c7-809">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-809">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="2c7c7-810">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-810">Updated cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-811">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-811">New-VpnSite</span></span>
        - <span data-ttu-id="2c7c7-812">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-812">Update-VpnSite</span></span>
        - <span data-ttu-id="2c7c7-813">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-813">New-VpnConnection</span></span>
        - <span data-ttu-id="2c7c7-814">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-814">Update-VpnConnection</span></span>
* <span data-ttu-id="2c7c7-815">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-815">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-817">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-817">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="2c7c7-818">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-818">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-819">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-819">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-820">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-820">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-821">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-821">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-822">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-822">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="2c7c7-823">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-823">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="2c7c7-824">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2c7c7-824">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2c7c7-825">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-825">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2c7c7-826">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-826">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2c7c7-827">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-827">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="2c7c7-828">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2c7c7-828">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2c7c7-829">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2c7c7-829">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2c7c7-830">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-830">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2c7c7-831">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-831">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2c7c7-832">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-832">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="2c7c7-833">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="2c7c7-833">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="2c7c7-834">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-834">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="2c7c7-835">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="2c7c7-835">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="2c7c7-836">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="2c7c7-836">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="2c7c7-837">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-837">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2c7c7-838">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-838">Az.SignalR</span></span>
* <span data-ttu-id="2c7c7-839">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-839">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-840">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-840">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-841">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-841">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="2c7c7-842">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-842">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="2c7c7-843">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-843">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="2c7c7-844">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-844">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="2c7c7-845">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-845">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-846">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-846">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-847">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-847">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="2c7c7-848">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-848">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="2c7c7-849">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-849">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="2c7c7-850">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-850">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="2c7c7-851">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-851">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="2c7c7-852">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-852">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="2c7c7-853">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-853">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="2c7c7-854">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-854">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2c7c7-855">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-855">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2c7c7-856">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-856">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="2c7c7-857">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-857">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-858">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-858">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-859">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="2c7c7-859">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="2c7c7-860">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="2c7c7-860">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="2c7c7-861">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-861">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="2c7c7-862">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-862">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="2c7c7-863">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-863">General</span></span>
* <span data-ttu-id="2c7c7-864">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="2c7c7-864">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-865">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-865">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-866">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-866">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="2c7c7-867">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2c7c7-867">Az.Aks</span></span>
* <span data-ttu-id="2c7c7-868">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-868">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="2c7c7-869">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="2c7c7-869">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-870">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-870">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-871">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="2c7c7-871">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="2c7c7-872">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-872">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="2c7c7-873">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-873">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="2c7c7-874">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="2c7c7-874">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="2c7c7-875">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-875">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2c7c7-876">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-876">Az.Batch</span></span>
* <span data-ttu-id="2c7c7-877">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="2c7c7-877">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-878">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-878">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-879">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="2c7c7-879">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-880">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-880">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-881">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-881">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="2c7c7-882">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-882">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="2c7c7-883">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-883">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="2c7c7-884">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-884">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="2c7c7-885">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="2c7c7-885">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="2c7c7-886">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-886">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="2c7c7-887">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-887">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="2c7c7-888">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-888">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-889">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-889">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-890">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="2c7c7-890">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="2c7c7-891">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-891">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="2c7c7-892">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-892">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="2c7c7-893">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="2c7c7-893">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-894">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-894">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-895">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-895">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-896">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-896">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-897">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-897">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="2c7c7-898">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2c7c7-898">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="2c7c7-899">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2c7c7-899">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="2c7c7-900">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-900">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="2c7c7-901">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2c7c7-901">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2c7c7-902">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-902">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-903">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-903">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-904">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-904">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-905">Az.Network</span></span>
* <span data-ttu-id="2c7c7-906">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-906">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="2c7c7-907">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-907">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="2c7c7-908">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-908">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="2c7c7-909">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-909">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="2c7c7-910">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-910">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="2c7c7-911">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-911">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="2c7c7-912">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2c7c7-912">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-913">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-913">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-914">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-914">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="2c7c7-915">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="2c7c7-915">Added example</span></span>
    - <span data-ttu-id="2c7c7-916">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-916">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="2c7c7-917">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-917">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="2c7c7-918">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-918">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-919">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-919">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-920">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-920">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-921">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-921">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-922">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-922">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="2c7c7-923">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="2c7c7-923">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="2c7c7-924">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="2c7c7-924">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="2c7c7-925">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-925">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-926">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-926">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-927">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-927">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="2c7c7-928">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-928">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="2c7c7-929">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="2c7c7-929">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-930">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-930">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-931">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-931">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="2c7c7-932">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-932">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="2c7c7-933">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="2c7c7-933">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="2c7c7-934">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-934">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="2c7c7-935">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="2c7c7-935">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="2c7c7-936">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-936">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-937">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-937">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-938">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-938">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-939">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-939">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-940">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="2c7c7-940">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="2c7c7-941">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="2c7c7-941">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="2c7c7-942">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-942">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="2c7c7-943">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-943">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="2c7c7-944">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="2c7c7-944">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="2c7c7-945">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-945">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-946">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-946">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-947">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c7c7-947">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="2c7c7-948">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-948">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-949">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-949">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-950">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-950">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="2c7c7-951">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-951">Az.ApplicationInsights</span></span>
* <span data-ttu-id="2c7c7-952">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-952">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-953">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-953">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-954">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="2c7c7-954">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-955">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-955">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-956">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-956">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-957">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-957">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-958">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-958">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2c7c7-959">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2c7c7-959">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2c7c7-960">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="2c7c7-960">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="2c7c7-961">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="2c7c7-961">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-962">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-962">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-963">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-963">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="2c7c7-964">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-964">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-965">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-965">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-966">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2c7c7-966">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2c7c7-967">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-967">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-968">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-968">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-969">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-969">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2c7c7-970">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-970">Az.LogicApp</span></span>
* <span data-ttu-id="2c7c7-971">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="2c7c7-971">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="2c7c7-972">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="2c7c7-972">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="2c7c7-973">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-973">Az.ManagedServices</span></span>
* <span data-ttu-id="2c7c7-974">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-974">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-975">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-975">Az.Network</span></span>
* <span data-ttu-id="2c7c7-976">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-976">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="2c7c7-977">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-977">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-978">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-978">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2c7c7-979">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-979">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2c7c7-980">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-980">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-981">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-981">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-982">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-982">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-983">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-983">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="2c7c7-984">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="2c7c7-984">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="2c7c7-985">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-985">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="2c7c7-986">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="2c7c7-986">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="2c7c7-987">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-987">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="2c7c7-988">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-988">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="2c7c7-989">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-989">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="2c7c7-990">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-990">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="2c7c7-991">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="2c7c7-991">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="2c7c7-992">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-992">Updated cmdlets</span></span>
        - <span data-ttu-id="2c7c7-993">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-993">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2c7c7-994">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-994">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="2c7c7-995">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-995">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="2c7c7-996">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-996">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="2c7c7-997">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-997">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="2c7c7-998">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-998">Updated cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-999">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-999">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2c7c7-1000">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1000">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="2c7c7-1001">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1001">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="2c7c7-1002">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1002">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="2c7c7-1003">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1003">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="2c7c7-1004">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1004">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1005">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1005">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-1006">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1006">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="2c7c7-1007">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1007">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1008">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1008">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1009">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1009">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2c7c7-1010">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1010">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="2c7c7-1011">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1011">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="2c7c7-1012">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1012">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="2c7c7-1013">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1013">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="2c7c7-1014">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1014">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2c7c7-1015">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1015">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="2c7c7-1016">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1016">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="2c7c7-1017">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1017">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="2c7c7-1018">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1018">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1019">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1019">Az.Resources</span></span>
- <span data-ttu-id="2c7c7-1020">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1020">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="2c7c7-1021">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1021">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-1022">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1022">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-1023">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1023">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="2c7c7-1024">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1024">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1025">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1025">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1026">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1026">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="2c7c7-1027">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1027">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="2c7c7-1028">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1028">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1029">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1029">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1030">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1030">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2c7c7-1031">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1031">Az.StorageSync</span></span>
* <span data-ttu-id="2c7c7-1032">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1032">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="2c7c7-1033">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1033">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1034">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1034">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1035">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1035">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="2c7c7-1036">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1036">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="2c7c7-1037">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1037">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="2c7c7-1038">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1038">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1039">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1039">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1040">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1040">Add support for profile cmdlets</span></span>
* <span data-ttu-id="2c7c7-1041">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1041">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="2c7c7-1042">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1042">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="2c7c7-1043">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1043">Az.Advisor</span></span>
* <span data-ttu-id="2c7c7-1044">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1044">GA release of Az.Advisor</span></span>
* <span data-ttu-id="2c7c7-1045">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1045">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-1046">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1046">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-1047">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1047">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="2c7c7-1048">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1048">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="2c7c7-1049">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1049">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="2c7c7-1050">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1050">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="2c7c7-1051">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1051">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="2c7c7-1052">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1052">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="2c7c7-1053">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1053">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1054">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1054">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1055">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1055">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1056">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1056">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1057">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1057">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-1058">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1058">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-1059">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1059">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2c7c7-1060">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1060">Az.EventGrid</span></span>
* <span data-ttu-id="2c7c7-1061">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1061">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-1062">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1062">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-1063">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1063">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1064">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1064">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1065">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1065">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="2c7c7-1066">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1066">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2c7c7-1067">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1067">Az.PolicyInsights</span></span>
* <span data-ttu-id="2c7c7-1068">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1068">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="2c7c7-1069">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1069">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1070">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1070">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-1071">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1071">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1073">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1073">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1074">Az.Resources</span></span>
    - <span data-ttu-id="2c7c7-1075">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1075">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="2c7c7-1076">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1076">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="2c7c7-1077">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1077">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="2c7c7-1078">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1078">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-1080">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1080">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1081">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1082">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1082">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="2c7c7-1083">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1083">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="2c7c7-1084">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1084">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2c7c7-1085">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1085">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2c7c7-1086">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1086">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="2c7c7-1087">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1087">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2c7c7-1088">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1088">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="2c7c7-1089">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1089">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="2c7c7-1090">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1090">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1091">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1091">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1092">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1092">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="2c7c7-1093">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1093">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="2c7c7-1094">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1094">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="2c7c7-1095">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1095">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="2c7c7-1096">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1096">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="2c7c7-1097">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1097">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="2c7c7-1098">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1098">Set-AzStorageAccount</span></span>
* <span data-ttu-id="2c7c7-1099">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1099">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="2c7c7-1100">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1100">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="2c7c7-1101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1101">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="2c7c7-1102">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1102">Az.StorageSync</span></span>
* <span data-ttu-id="2c7c7-1103">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1103">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="2c7c7-1104">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1104">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1105">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1106">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1106">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="2c7c7-1107">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1107">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="2c7c7-1108">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1108">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="2c7c7-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1109">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="2c7c7-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1110">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1111">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1112">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1112">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="2c7c7-1113">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1113">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="2c7c7-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1114">Az.Dns</span></span>
* <span data-ttu-id="2c7c7-1115">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1115">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2c7c7-1116">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1116">Az.EventGrid</span></span>
* <span data-ttu-id="2c7c7-1117">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1117">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="2c7c7-1118">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1118">New cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-1119">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1119">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2c7c7-1120">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1120">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2c7c7-1121">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1121">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2c7c7-1122">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1122">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="2c7c7-1123">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1123">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="2c7c7-1124">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1124">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2c7c7-1125">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1125">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2c7c7-1126">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1126">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="2c7c7-1127">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1127">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="2c7c7-1128">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1128">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="2c7c7-1129">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1129">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2c7c7-1130">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1130">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="2c7c7-1131">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1131">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="2c7c7-1132">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1132">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="2c7c7-1133">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1133">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="2c7c7-1134">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1134">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="2c7c7-1135">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1135">Updated cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1136">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="2c7c7-1137">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1137">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2c7c7-1138">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1138">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="2c7c7-1139">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1139">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="2c7c7-1140">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1140">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="2c7c7-1141">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1141">Event subscription expiration date,</span></span>
            - <span data-ttu-id="2c7c7-1142">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1142">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="2c7c7-1143">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1143">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="2c7c7-1144">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1144">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="2c7c7-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1145">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="2c7c7-1146">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1146">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="2c7c7-1147">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1147">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="2c7c7-1148">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1148">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="2c7c7-1149">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1149">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-1150">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1150">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-1151">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1151">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="2c7c7-1152">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1152">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="2c7c7-1153">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1153">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="2c7c7-1154">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1154">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1155">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1155">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1156">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1156">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="2c7c7-1157">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1157">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1158">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="2c7c7-1159">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1159">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="2c7c7-1160">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1160">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1161">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1161">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="2c7c7-1162">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1162">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="2c7c7-1163">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1163">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1164">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1164">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2c7c7-1165">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1165">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2c7c7-1166">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1166">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="2c7c7-1167">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1167">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="2c7c7-1168">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1168">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="2c7c7-1169">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1169">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="2c7c7-1170">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1170">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1171">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1171">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2c7c7-1172">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1172">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2c7c7-1173">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1173">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="2c7c7-1174">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1174">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="2c7c7-1175">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1175">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="2c7c7-1176">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1176">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="2c7c7-1177">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1177">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="2c7c7-1178">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1178">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="2c7c7-1179">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1179">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="2c7c7-1180">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1180">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="2c7c7-1181">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1181">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="2c7c7-1182">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1182">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="2c7c7-1183">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1183">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="2c7c7-1184">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1184">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="2c7c7-1185">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1185">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="2c7c7-1186">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1186">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="2c7c7-1187">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1187">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="2c7c7-1188">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1188">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="2c7c7-1189">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1189">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-1190">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1190">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="2c7c7-1191">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1191">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="2c7c7-1192">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1192">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="2c7c7-1193">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1193">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="2c7c7-1194">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1194">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="2c7c7-1195">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1195">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2c7c7-1196">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1196">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="2c7c7-1197">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1197">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1198">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1198">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-1199">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1199">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1200">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1200">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1201">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1201">Support for additional Template Export options</span></span>
    - <span data-ttu-id="2c7c7-1202">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1202">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2c7c7-1203">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1203">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="2c7c7-1204">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1204">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-1205">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1205">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-1206">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1206">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1207">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1207">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1208">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1208">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="2c7c7-1209">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1209">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="2c7c7-1210">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1210">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="2c7c7-1211">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1211">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2c7c7-1212">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1212">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2c7c7-1213">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1213">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="2c7c7-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1214">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="2c7c7-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1215">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1216">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1216">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1217">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1217">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="2c7c7-1218">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1218">New-AzStorageAccount</span></span>
* <span data-ttu-id="2c7c7-1219">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1219">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="2c7c7-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1220">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1221">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1221">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1222">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1222">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="2c7c7-1223">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1223">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="2c7c7-1224">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1224">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="2c7c7-1225">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1225">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-1226">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1226">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1227">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1227">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1228">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1228">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="2c7c7-1229">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1229">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-1230">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1230">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-1231">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1231">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="2c7c7-1232">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1232">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1233">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1233">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1234">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1234">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="2c7c7-1235">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1235">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2c7c7-1236">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1236">Az.PolicyInsights</span></span>
* <span data-ttu-id="2c7c7-1237">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1237">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1238">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1238">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1239">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1239">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-1240">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1240">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-1241">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1241">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-1242">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1242">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-1243">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1243">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="2c7c7-1244">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1244">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1245">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1246">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1246">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="2c7c7-1247">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1247">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="2c7c7-1248">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1248">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="2c7c7-1249">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1249">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1250">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1250">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1251">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1251">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="2c7c7-1252">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1252">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-1253">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1253">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-1254">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1254">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="2c7c7-1255">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1255">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="2c7c7-1256">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1256">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="2c7c7-1257">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1257">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="2c7c7-1258">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1258">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="2c7c7-1259">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1259">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="2c7c7-1260">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1260">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="2c7c7-1261">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1261">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="2c7c7-1262">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1262">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="2c7c7-1263">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1263">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="2c7c7-1264">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1264">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="2c7c7-1265">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1265">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="2c7c7-1266">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1266">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="2c7c7-1267">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1267">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="2c7c7-1268">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1268">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="2c7c7-1269">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1269">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="2c7c7-1270">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1270">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="2c7c7-1271">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1271">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="2c7c7-1272">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1272">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="2c7c7-1273">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1273">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="2c7c7-1274">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1274">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="2c7c7-1275">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1275">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="2c7c7-1276">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1276">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="2c7c7-1277">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1277">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="2c7c7-1278">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1278">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="2c7c7-1279">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1279">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="2c7c7-1280">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1280">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="2c7c7-1281">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1281">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="2c7c7-1282">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1282">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="2c7c7-1283">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1283">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="2c7c7-1284">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1284">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="2c7c7-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1285">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="2c7c7-1286">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1286">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="2c7c7-1287">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1287">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2c7c7-1288">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1288">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="2c7c7-1289">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1289">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="2c7c7-1290">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1290">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="2c7c7-1291">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1291">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="2c7c7-1292">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1292">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="2c7c7-1293">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1293">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2c7c7-1294">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1294">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2c7c7-1295">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1295">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2c7c7-1296">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1296">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="2c7c7-1297">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1297">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2c7c7-1298">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1298">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="2c7c7-1299">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1299">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="2c7c7-1300">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1300">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="2c7c7-1301">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1301">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="2c7c7-1302">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1302">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="2c7c7-1303">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1303">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="2c7c7-1304">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1304">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="2c7c7-1305">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1305">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="2c7c7-1306">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1306">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="2c7c7-1307">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1307">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="2c7c7-1308">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1308">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="2c7c7-1309">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1309">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="2c7c7-1310">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1310">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2c7c7-1311">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1311">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2c7c7-1312">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1312">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2c7c7-1313">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1313">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2c7c7-1314">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1314">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="2c7c7-1315">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1315">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="2c7c7-1316">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1316">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="2c7c7-1317">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1317">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="2c7c7-1318">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1318">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="2c7c7-1319">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1319">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="2c7c7-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1320">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="2c7c7-1321">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1321">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="2c7c7-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1322">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="2c7c7-1323">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1323">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="2c7c7-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1324">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="2c7c7-1325">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1325">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="2c7c7-1326">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1326">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="2c7c7-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1327">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="2c7c7-1328">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1328">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="2c7c7-1329">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1329">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="2c7c7-1330">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1330">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1331">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1331">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1332">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1332">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="2c7c7-1333">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1333">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="2c7c7-1334">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="2c7c7-1335">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1335">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="2c7c7-1336">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1336">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="2c7c7-1337">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1337">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="2c7c7-1338">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1338">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1339">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1339">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1340">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1340">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="2c7c7-1341">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1341">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1342">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1342">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-1343">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1343">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-1344">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1344">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-1345">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1345">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1346">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1346">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1347">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1347">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="2c7c7-1348">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1348">Updated cmdlet:</span></span>
        - <span data-ttu-id="2c7c7-1349">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1349">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="2c7c7-1350">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1350">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1351">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1352">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1352">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1353">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1354">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1354">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="2c7c7-1355">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1355">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1356">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1356">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1357">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1357">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-1358">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1358">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-1359">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1359">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="2c7c7-1360">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1360">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1361">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1362">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1362">Proximity placement group feature.</span></span>
    - <span data-ttu-id="2c7c7-1363">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1363">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="2c7c7-1364">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1364">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="2c7c7-1365">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1365">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="2c7c7-1366">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1366">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="2c7c7-1367">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1367">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="2c7c7-1368">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1368">Breaking changes</span></span>
    - <span data-ttu-id="2c7c7-1369">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1369">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="2c7c7-1370">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1370">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="2c7c7-1371">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1371">Az.DeploymentManager</span></span>
* <span data-ttu-id="2c7c7-1372">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1372">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="2c7c7-1373">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1373">Az.Dns</span></span>
* <span data-ttu-id="2c7c7-1374">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1374">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="2c7c7-1375">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1375">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="2c7c7-1376">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1376">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-1377">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1377">Az.FrontDoor</span></span>
* <span data-ttu-id="2c7c7-1378">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1378">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="2c7c7-1379">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1379">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-1380">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1380">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-1381">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1381">Removed two cmdlets:</span></span>
    - <span data-ttu-id="2c7c7-1382">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1382">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="2c7c7-1383">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1383">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2c7c7-1384">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1384">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="2c7c7-1385">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1385">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="2c7c7-1386">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1386">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="2c7c7-1387">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1387">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-1388">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1388">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-1389">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1389">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="2c7c7-1390">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1390">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="2c7c7-1391">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1391">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="2c7c7-1392">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1392">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="2c7c7-1393">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1393">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="2c7c7-1394">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1394">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="2c7c7-1395">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1395">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="2c7c7-1396">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1396">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2c7c7-1397">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1397">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2c7c7-1398">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1398">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2c7c7-1399">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1399">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2c7c7-1400">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1400">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="2c7c7-1401">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1401">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="2c7c7-1402">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1402">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1403">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1403">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1404">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1404">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="2c7c7-1405">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1405">New cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1406">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1406">New-AzNatGateway</span></span>
        - <span data-ttu-id="2c7c7-1407">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1407">Get-AzNatGateway</span></span>
        - <span data-ttu-id="2c7c7-1408">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1408">Set-AzNatGateway</span></span>
        - <span data-ttu-id="2c7c7-1409">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1409">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="2c7c7-1410">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1410">Updated cmdlets</span></span>
        - <span data-ttu-id="2c7c7-1411">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1411">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="2c7c7-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1412">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="2c7c7-1413">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1413">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="2c7c7-1414">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1414">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="2c7c7-1415">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1415">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2c7c7-1416">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1416">Az.PolicyInsights</span></span>
* <span data-ttu-id="2c7c7-1417">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1417">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="2c7c7-1418">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1418">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="2c7c7-1419">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1419">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1420">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1420">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1421">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1421">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="2c7c7-1422">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1422">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="2c7c7-1423">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1423">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="2c7c7-1424">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1424">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="2c7c7-1425">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1425">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="2c7c7-1426">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1426">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="2c7c7-1427">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1427">Az.Relay</span></span>
* <span data-ttu-id="2c7c7-1428">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1428">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-1429">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1429">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-1430">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1430">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1431">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1431">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1432">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1432">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="2c7c7-1433">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1433">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="2c7c7-1434">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1434">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="2c7c7-1435">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1435">New-AzStorageAccount</span></span>
* <span data-ttu-id="2c7c7-1436">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1436">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="2c7c7-1437">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1437">New-AzStorageAccount</span></span>
    - <span data-ttu-id="2c7c7-1438">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1438">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="2c7c7-1439">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1439">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1440">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1440">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1441">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1441">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="2c7c7-1442">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1442">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="2c7c7-1443">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1443">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-1444">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1444">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-1445">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1445">General availability of `Az` module</span></span>
* <span data-ttu-id="2c7c7-1446">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1446">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2c7c7-1447">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1447">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2c7c7-1448">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1448">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2c7c7-1449">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1449">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2c7c7-1450">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1450">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1451">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1451">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1452">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1453">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1453">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="2c7c7-1454">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1454">Az.Batch</span></span>
* <span data-ttu-id="2c7c7-1455">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1455">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-1456">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1456">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-1457">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1457">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-1458">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1458">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-1459">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1459">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1460">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1460">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1461">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1461">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="2c7c7-1462">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1462">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1463">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1463">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-1464">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1464">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-1465">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1465">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1466">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1466">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-1467">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1467">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2c7c7-1468">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1468">Az.EventGrid</span></span>
* <span data-ttu-id="2c7c7-1469">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1469">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-1470">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1470">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-1471">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1471">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="2c7c7-1472">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1472">Az.HDInsight</span></span>
* <span data-ttu-id="2c7c7-1473">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-1474">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1474">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-1475">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-1476">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1476">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-1477">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1477">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1478">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1478">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="2c7c7-1479">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1479">Az.MachineLearning</span></span>
* <span data-ttu-id="2c7c7-1480">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="2c7c7-1481">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1481">Az.Media</span></span>
* <span data-ttu-id="2c7c7-1482">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1482">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-1483">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1483">Az.Monitor</span></span>
  * <span data-ttu-id="2c7c7-1484">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1484">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="2c7c7-1485">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1485">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="2c7c7-1486">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1486">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="2c7c7-1487">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1487">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2c7c7-1488">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1488">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="2c7c7-1489">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1489">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="2c7c7-1490">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1490">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1491">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1491">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1492">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1492">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1493">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1493">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="2c7c7-1494">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1494">Az.NotificationHubs</span></span>
* <span data-ttu-id="2c7c7-1495">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1495">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1496">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1496">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-1497">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1497">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="2c7c7-1498">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1498">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="2c7c7-1499">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1499">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1500">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1500">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1501">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1501">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1502">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1502">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="2c7c7-1503">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1503">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="2c7c7-1504">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1504">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2c7c7-1505">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1505">Az.RedisCache</span></span>
* <span data-ttu-id="2c7c7-1506">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1506">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1507">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1507">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1508">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1508">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1509">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1509">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1510">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1510">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="2c7c7-1511">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1511">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1512">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1512">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="2c7c7-1513">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1513">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="2c7c7-1514">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1514">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="2c7c7-1515">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1515">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="2c7c7-1516">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1516">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1517">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1517">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1518">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1518">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="2c7c7-1519">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1519">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="2c7c7-1520">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1520">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="2c7c7-1521">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1521">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="2c7c7-1522">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1522">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-1523">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1523">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-1524">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1524">General availability of `Az` module</span></span>
* <span data-ttu-id="2c7c7-1525">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1525">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2c7c7-1526">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1526">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2c7c7-1527">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1527">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2c7c7-1528">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1528">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2c7c7-1529">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1529">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1530">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1530">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1531">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1531">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1532">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1532">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2c7c7-1533">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1533">Az.AnalysisServices</span></span>
* <span data-ttu-id="2c7c7-1534">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1534">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="2c7c7-1535">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1535">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1536">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1536">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1537">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1537">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="2c7c7-1538">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1538">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="2c7c7-1539">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1539">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1540">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1540">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1541">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1541">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="2c7c7-1542">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1542">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="2c7c7-1543">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1543">Az.ContainerInstance</span></span>
* <span data-ttu-id="2c7c7-1544">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1544">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-1545">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1545">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-1546">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1546">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="2c7c7-1547">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1547">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1548">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1548">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1549">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1549">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="2c7c7-1550">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1550">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="2c7c7-1551">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1551">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="2c7c7-1552">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1552">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="2c7c7-1553">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1553">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="2c7c7-1554">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1554">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1555">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1555">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1556">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1556">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1557">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1557">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1558">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1558">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="2c7c7-1559">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1559">New-AzStorageContext</span></span>
* <span data-ttu-id="2c7c7-1560">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1560">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="2c7c7-1561">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1561">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2c7c7-1562">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1562">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="2c7c7-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1563">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="2c7c7-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1564">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="2c7c7-1565">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1565">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="2c7c7-1566">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1566">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2c7c7-1567">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1567">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="2c7c7-1568">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1568">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="2c7c7-1569">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1569">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="2c7c7-1570">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1570">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="2c7c7-1571">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1571">Highlights since the last major release</span></span>
* <span data-ttu-id="2c7c7-1572">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1572">General availability of `Az` module</span></span>
* <span data-ttu-id="2c7c7-1573">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1573">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="2c7c7-1574">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1574">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="2c7c7-1575">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1575">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="2c7c7-1576">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1576">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2c7c7-1577">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1577">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1578">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1578">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1579">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1579">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1580">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1580">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="2c7c7-1581">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1581">Dynamic grouping</span></span>
    * <span data-ttu-id="2c7c7-1582">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1582">Pre-Post script</span></span>
    * <span data-ttu-id="2c7c7-1583">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1583">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1584">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1584">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1585">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1585">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="2c7c7-1586">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1586">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-1587">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1587">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-1588">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1588">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1589">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1589">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1590">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1590">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="2c7c7-1591">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1591">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1592">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1592">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1593">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1593">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="2c7c7-1594">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1594">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1595">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1595">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1596">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1596">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="2c7c7-1597">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1597">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1598">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1598">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1599">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1599">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1600">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1600">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1601">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1601">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="2c7c7-1602">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1602">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2c7c7-1603">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1603">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2c7c7-1604">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1604">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="2c7c7-1605">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1605">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="2c7c7-1606">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1606">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="2c7c7-1607">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1607">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1608">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1608">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1609">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1609">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="2c7c7-1610">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1610">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1611">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1611">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1612">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1612">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="2c7c7-1613">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1613">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1614">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1614">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1615">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1615">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="2c7c7-1616">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1616">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="2c7c7-1617">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1617">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-1618">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1618">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-1619">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1619">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1620">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1620">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1621">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1621">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-1622">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1622">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-1623">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1623">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2c7c7-1624">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1624">Az.LogicApp</span></span>
* <span data-ttu-id="2c7c7-1625">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1625">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1626">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1626">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1627">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1627">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1628">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1628">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1629">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1629">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="2c7c7-1630">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1630">SDK Update</span></span>
* <span data-ttu-id="2c7c7-1631">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1631">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="2c7c7-1632">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1632">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1633">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1633">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1634">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1634">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="2c7c7-1635">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1635">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="2c7c7-1636">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1636">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="2c7c7-1637">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1637">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="2c7c7-1638">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1638">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="2c7c7-1639">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1639">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1640">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1640">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1641">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1641">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="2c7c7-1642">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1642">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1643">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1643">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1644">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1644">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="2c7c7-1645">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1645">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="2c7c7-1646">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1646">Az.AnalysisServices</span></span>
* <span data-ttu-id="2c7c7-1647">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1647">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1648">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1648">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1649">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1649">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="2c7c7-1650">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1650">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="2c7c7-1651">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1651">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-1652">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1652">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-1653">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1653">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1654">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1654">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1655">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1655">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="2c7c7-1656">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1656">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="2c7c7-1657">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1657">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="2c7c7-1658">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1658">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1659">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1659">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-1660">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1660">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="2c7c7-1661">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1661">Az.EventHub</span></span>
* <span data-ttu-id="2c7c7-1662">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1662">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-1663">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1663">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-1664">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1664">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2c7c7-1665">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1665">Az.LogicApp</span></span>
* <span data-ttu-id="2c7c7-1666">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1666">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="2c7c7-1667">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1667">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="2c7c7-1668">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1668">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="2c7c7-1669">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1669">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2c7c7-1670">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1670">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2c7c7-1671">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1671">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="2c7c7-1672">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1672">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="2c7c7-1673">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1673">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="2c7c7-1674">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1674">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2c7c7-1675">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1675">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2c7c7-1676">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1676">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="2c7c7-1677">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1677">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="2c7c7-1678">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1678">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="2c7c7-1679">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1679">Az.Monitor</span></span>
* <span data-ttu-id="2c7c7-1680">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1680">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1681">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1681">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1682">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1682">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1683">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1683">Az.OperationalInsights</span></span>
* <span data-ttu-id="2c7c7-1684">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1684">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="2c7c7-1685">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1685">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="2c7c7-1686">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1686">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1687">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1687">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1688">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1688">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2c7c7-1689">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="2c7c7-1690">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="2c7c7-1691">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1691">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1692">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1692">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1693">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1693">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="2c7c7-1694">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1694">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1695">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1695">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1696">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1696">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="2c7c7-1697">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1697">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1698">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1698">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1699">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1699">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2c7c7-1700">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1700">Az.AnalysisServices</span></span>
<span data-ttu-id="2c7c7-1701">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1701">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1702">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1702">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1703">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1703">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="2c7c7-1704">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1704">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="2c7c7-1705">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1705">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1706">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1706">Az.RecoveryServices</span></span>
<span data-ttu-id="2c7c7-1707">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1707">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1708">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1708">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1709">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1709">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="2c7c7-1710">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1710">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="2c7c7-1711">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1711">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="2c7c7-1712">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1712">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1713">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1713">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1714">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1714">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="2c7c7-1715">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1715">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="2c7c7-1716">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1716">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="2c7c7-1717">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1717">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1718">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1718">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1719">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1719">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="2c7c7-1720">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1720">Az.AnalysisServices</span></span>
* <span data-ttu-id="2c7c7-1721">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1721">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1722">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1722">Az.RecoveryServices</span></span>
* <span data-ttu-id="2c7c7-1723">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1723">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="2c7c7-1724">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1724">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1725">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1725">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1726">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1726">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="2c7c7-1727">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1727">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2c7c7-1728">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1728">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="2c7c7-1729">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1729">Az.Aks</span></span>
* <span data-ttu-id="2c7c7-1730">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1730">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="2c7c7-1731">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1731">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1732">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1732">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="2c7c7-1733">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1733">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="2c7c7-1734">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1734">Az.Cdn</span></span>
* <span data-ttu-id="2c7c7-1735">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1735">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1736">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1736">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1737">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1737">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="2c7c7-1738">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1738">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="2c7c7-1739">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1739">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="2c7c7-1740">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1740">Az.ContainerRegistry</span></span>
* <span data-ttu-id="2c7c7-1741">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1741">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="2c7c7-1742">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1742">Az.DataFactory</span></span>
* <span data-ttu-id="2c7c7-1743">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1743">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1744">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1744">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-1745">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1745">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="2c7c7-1746">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1746">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="2c7c7-1747">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1747">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-1748">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1748">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-1749">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1749">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-1750">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1750">Az.KeyVault</span></span>
* <span data-ttu-id="2c7c7-1751">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1751">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1752">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1752">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1753">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1753">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1754">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1754">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1755">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1755">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="2c7c7-1756">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1756">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="2c7c7-1757">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1757">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="2c7c7-1758">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1758">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="2c7c7-1759">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="2c7c7-1760">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1760">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="2c7c7-1761">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1761">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-1762">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1762">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-1763">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1763">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="2c7c7-1764">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1764">Fix some error messages.</span></span>
* <span data-ttu-id="2c7c7-1765">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1765">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="2c7c7-1766">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1766">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2c7c7-1767">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1767">Az.SignalR</span></span>
* <span data-ttu-id="2c7c7-1768">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1768">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1769">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1769">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1770">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1770">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2c7c7-1771">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1771">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="2c7c7-1772">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1772">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="2c7c7-1773">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1773">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1774">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1774">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1775">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1775">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2c7c7-1776">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1776">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="2c7c7-1777">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1777">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="2c7c7-1778">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1778">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="2c7c7-1779">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1779">Az.TrafficManager</span></span>
* <span data-ttu-id="2c7c7-1780">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1780">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1781">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1781">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1782">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1782">Update incorrect online help URLs</span></span>
* <span data-ttu-id="2c7c7-1783">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1783">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="2c7c7-1784">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1784">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="2c7c7-1785">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1785">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1786">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1786">Az.Accounts</span></span>
* <span data-ttu-id="2c7c7-1787">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1787">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-1788">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1788">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1789">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1789">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="2c7c7-1790">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1790">Updated the description of ID in help files</span></span>
* <span data-ttu-id="2c7c7-1791">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1791">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1792">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1792">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-1793">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1793">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="2c7c7-1794">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1794">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="2c7c7-1795">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1795">Az.EventGrid</span></span>
* <span data-ttu-id="2c7c7-1796">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1796">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="2c7c7-1797">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1797">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="2c7c7-1798">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1798">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2c7c7-1799">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1799">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2c7c7-1800">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1800">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2c7c7-1801">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1801">Dead letter endpoint.</span></span>
    - <span data-ttu-id="2c7c7-1802">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1802">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="2c7c7-1803">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1803">Event Time-To-Live,</span></span>
        - <span data-ttu-id="2c7c7-1804">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1804">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="2c7c7-1805">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1805">Dead letter endpoint.</span></span>
* <span data-ttu-id="2c7c7-1806">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1806">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="2c7c7-1807">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1807">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="2c7c7-1808">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1808">Az.IotHub</span></span>
* <span data-ttu-id="2c7c7-1809">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1809">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="2c7c7-1810">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1810">Az.LogicApp</span></span>
* <span data-ttu-id="2c7c7-1811">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1811">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-1812">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1812">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1813">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1813">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="2c7c7-1814">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1814">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="2c7c7-1815">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1815">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2c7c7-1816">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1816">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="2c7c7-1817">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1817">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="2c7c7-1818">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1818">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="2c7c7-1819">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1819">Az.SignalR</span></span>
* <span data-ttu-id="2c7c7-1820">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1820">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-1821">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1821">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1822">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1822">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="2c7c7-1823">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1823">Az.Storage</span></span>
* <span data-ttu-id="2c7c7-1824">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1824">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="2c7c7-1825">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1825">New-AzStorageContext</span></span>
* <span data-ttu-id="2c7c7-1826">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1826">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="2c7c7-1827">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1827">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1828">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1828">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-1829">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1829">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="2c7c7-1830">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1830">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="2c7c7-1831">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1831">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="2c7c7-1832">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1832">General</span></span>

- <span data-ttu-id="2c7c7-1833">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1833">General Availability of Az Module</span></span>
- <span data-ttu-id="2c7c7-1834">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1834">Online help for each module</span></span>
- <span data-ttu-id="2c7c7-1835">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1835">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="2c7c7-1836">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1836">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="2c7c7-1837">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1837">Az.Accounts</span></span>
- <span data-ttu-id="2c7c7-1838">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1838">Changed from Az.Profile</span></span>
- <span data-ttu-id="2c7c7-1839">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1839">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-1840">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1840">Az.ApiManagement</span></span>
- <span data-ttu-id="2c7c7-1841">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1841">Fixes for #7002</span></span>
- <span data-ttu-id="2c7c7-1842">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1842">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="2c7c7-1843">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1843">Az.Batch</span></span>
- <span data-ttu-id="2c7c7-1844">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1844">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="2c7c7-1845">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1845">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="2c7c7-1846">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1846">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="2c7c7-1847">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1847">Az.Billing</span></span>
- <span data-ttu-id="2c7c7-1848">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1848">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="2c7c7-1849">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1849">Az.CognitivServices</span></span>
- <span data-ttu-id="2c7c7-1850">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1850">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="2c7c7-1851">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1851">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2c7c7-1852">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1852">Az.ContainerInstance</span></span>
- <span data-ttu-id="2c7c7-1853">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1853">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="2c7c7-1854">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1854">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="2c7c7-1855">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1855">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1856">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1856">Az.DataLakeStore</span></span>
- <span data-ttu-id="2c7c7-1857">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1857">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="2c7c7-1858">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1858">Az.Monitor</span></span>
- <span data-ttu-id="2c7c7-1859">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1859">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="2c7c7-1860">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1860">Az.KeyVault</span></span>
- <span data-ttu-id="2c7c7-1861">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1861">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="2c7c7-1862">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1862">Az.MachineLearning</span></span>
- <span data-ttu-id="2c7c7-1863">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1863">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="2c7c7-1864">Az.Media</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1864">Az.Media</span></span>
- <span data-ttu-id="2c7c7-1865">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1865">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1866">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1866">Az.Network</span></span>
<span data-ttu-id="2c7c7-1867">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1867">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="2c7c7-1868">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1868">New cmdlets added:</span></span>
        - <span data-ttu-id="2c7c7-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1869">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1870">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1871">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1872">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1873">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1874">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1874">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="2c7c7-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1875">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="2c7c7-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1876">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="2c7c7-1877">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1877">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="2c7c7-1878">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1878">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="2c7c7-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1879">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2c7c7-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1880">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="2c7c7-1881">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1881">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="2c7c7-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1882">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="2c7c7-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1883">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="2c7c7-1884">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1884">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="2c7c7-1885">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1885">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2c7c7-1886">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1886">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="2c7c7-1887">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1887">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="2c7c7-1888">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1888">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="2c7c7-1889">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1889">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="2c7c7-1890">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1890">Az.OperationalInsights</span></span>
- <span data-ttu-id="2c7c7-1891">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1891">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="2c7c7-1892">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1892">Az.Profile</span></span>
- <span data-ttu-id="2c7c7-1893">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1893">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1894">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1894">Az.RecoveryServices</span></span>
- <span data-ttu-id="2c7c7-1895">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1895">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="2c7c7-1896">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1896">Az.Resources</span></span>
- <span data-ttu-id="2c7c7-1897">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1897">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-1898">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1898">Az.ServiceFabric</span></span>
- <span data-ttu-id="2c7c7-1899">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1899">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="2c7c7-1900">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1900">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="2c7c7-1901">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1901">Az.SIgnalR</span></span>
- <span data-ttu-id="2c7c7-1902">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1902">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="2c7c7-1903">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1903">Az.Sql</span></span>
- <span data-ttu-id="2c7c7-1904">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1904">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="2c7c7-1905">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1905">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="2c7c7-1906">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1906">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="2c7c7-1907">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1907">Az.Storage</span></span>
- <span data-ttu-id="2c7c7-1908">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1908">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1909">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1909">Az.Websites</span></span>
- <span data-ttu-id="2c7c7-1910">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1910">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="2c7c7-1911">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1911">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="2c7c7-1912">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1912">General</span></span>

* <span data-ttu-id="2c7c7-1913">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1913">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="2c7c7-1914">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1914">Az.Compute</span></span>

* <span data-ttu-id="2c7c7-1915">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1915">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-1916">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1916">Az.DataLakeStore</span></span>

* <span data-ttu-id="2c7c7-1917">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1917">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="2c7c7-1918">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1918">Az.FrontDoor</span></span>

* <span data-ttu-id="2c7c7-1919">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1919">Fixed some broken links</span></span>
    - <span data-ttu-id="2c7c7-1920">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1920">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="2c7c7-1921">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1921">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="2c7c7-1922">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1922">Az.RecoveryServices</span></span>

* <span data-ttu-id="2c7c7-1923">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1923">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="2c7c7-1924">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1924">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="2c7c7-1925">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1925">Az.Resources</span></span>

* <span data-ttu-id="2c7c7-1926">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1926">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="2c7c7-1927">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1927">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="2c7c7-1928">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1928">Az.Sql</span></span>

* <span data-ttu-id="2c7c7-1929">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1929">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="2c7c7-1930">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1930">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="2c7c7-1931">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1931">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="2c7c7-1932">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1932">Az.Storage</span></span>

* <span data-ttu-id="2c7c7-1933">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1933">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="2c7c7-1934">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1934">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="2c7c7-1935">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1935">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2c7c7-1936">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1936">Support Static Website configuration</span></span>
    - <span data-ttu-id="2c7c7-1937">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1937">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="2c7c7-1938">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1938">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="2c7c7-1939">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1939">Az.Websites</span></span>

* <span data-ttu-id="2c7c7-1940">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1940">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="2c7c7-1941">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1941">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="2c7c7-1942">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1942">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="2c7c7-1943">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1943">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="2c7c7-1944">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1944">Az.ApiManagement</span></span>
* <span data-ttu-id="2c7c7-1945">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1945">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="2c7c7-1946">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1946">Az.Automation</span></span>
* <span data-ttu-id="2c7c7-1947">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1947">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="2c7c7-1948">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1948">Added Update Management cmdlets</span></span>
* <span data-ttu-id="2c7c7-1949">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1949">Added Source Control cmdlets</span></span>
* <span data-ttu-id="2c7c7-1950">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1950">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="2c7c7-1951">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1951">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="2c7c7-1952">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1952">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-1953">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1953">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="2c7c7-1954">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1954">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="2c7c7-1955">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1955">Az.ContainerInstance</span></span>
* <span data-ttu-id="2c7c7-1956">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1956">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="2c7c7-1957">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1957">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="2c7c7-1958">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1958">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="2c7c7-1959">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1959">Az.Network</span></span>
* <span data-ttu-id="2c7c7-1960">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1960">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="2c7c7-1961">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1961">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="2c7c7-1962">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1962">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="2c7c7-1963">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1963">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="2c7c7-1964">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1964">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="2c7c7-1965">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1965">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="2c7c7-1966">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1966">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="2c7c7-1967">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1967">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="2c7c7-1968">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1968">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="2c7c7-1969">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1969">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="2c7c7-1970">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1970">Az.Relay</span></span>
* <span data-ttu-id="2c7c7-1971">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1971">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="2c7c7-1972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1972">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-1973">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1973">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="2c7c7-1974">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1974">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="2c7c7-1975">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1975">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-1976">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1976">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-1977">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1977">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="2c7c7-1978">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1978">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-1979">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1979">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="2c7c7-1980">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1980">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2c7c7-1981">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1981">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2c7c7-1982">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1982">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2c7c7-1983">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1983">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="2c7c7-1984">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1984">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2c7c7-1985">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1985">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2c7c7-1986">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1986">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="2c7c7-1987">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1987">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="2c7c7-1988">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1988">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="2c7c7-1989">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1989">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="2c7c7-1990">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1990">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="2c7c7-1991">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1991">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2c7c7-1992">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1992">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="2c7c7-1993">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1993">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="2c7c7-1994">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1994">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="2c7c7-1995">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1995">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="2c7c7-1996">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1996">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="2c7c7-1997">Generale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1997">General</span></span>
* <span data-ttu-id="2c7c7-1998">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1998">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="2c7c7-1999">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-1999">Az.Profile</span></span>
* <span data-ttu-id="2c7c7-2000">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2000">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="2c7c7-2001">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2001">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="2c7c7-2002">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2002">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="2c7c7-2003">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2003">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="2c7c7-2004">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2004">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="2c7c7-2005">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2005">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="2c7c7-2006">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2006">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-2007">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2007">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-2008">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2008">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-2009">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2009">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-2010">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2010">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="2c7c7-2011">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2011">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="2c7c7-2012">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2012">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-2013">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2013">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-2014">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2014">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="2c7c7-2015">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2015">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="2c7c7-2016">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2016">Az.Insights</span></span>
* <span data-ttu-id="2c7c7-2017">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2017">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="2c7c7-2018">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2018">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="2c7c7-2019">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2019">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="2c7c7-2020">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2020">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-2021">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2021">Az.Network</span></span>
* <span data-ttu-id="2c7c7-2022">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2022">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="2c7c7-2023">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2023">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="2c7c7-2024">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2024">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="2c7c7-2025">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2025">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="2c7c7-2026">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2026">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="2c7c7-2027">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2027">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="2c7c7-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2028">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="2c7c7-2029">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2029">Az.PolicyInsights</span></span>
* <span data-ttu-id="2c7c7-2030">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2030">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-2031">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2031">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-2032">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2032">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="2c7c7-2033">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2033">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="2c7c7-2034">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2034">Az.ServiceBus</span></span>
* <span data-ttu-id="2c7c7-2035">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2035">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="2c7c7-2036">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2036">Az.ServiceFabric</span></span>
* <span data-ttu-id="2c7c7-2037">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2037">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="2c7c7-2038">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2038">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="2c7c7-2039">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2039">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="2c7c7-2040">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2040">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="2c7c7-2041">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2041">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="2c7c7-2042">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2042">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="2c7c7-2043">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2043">Az.Profile</span></span>
* <span data-ttu-id="2c7c7-2044">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2044">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="2c7c7-2045">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2045">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-2046">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2046">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-2047">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2047">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="2c7c7-2048">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2048">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="2c7c7-2049">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2049">Az.DataLakeStore</span></span>
* <span data-ttu-id="2c7c7-2050">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2050">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="2c7c7-2051">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2051">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="2c7c7-2052">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2052">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2c7c7-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2053">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="2c7c7-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2054">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-2055">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2055">Az.Network</span></span>
* <span data-ttu-id="2c7c7-2056">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2056">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="2c7c7-2057">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2057">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-2058">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2058">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-2059">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2059">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="2c7c7-2060">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2060">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="2c7c7-2061">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2061">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="2c7c7-2062">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2062">Azure.Storage</span></span>
* <span data-ttu-id="2c7c7-2063">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2063">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="2c7c7-2064">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2064">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="2c7c7-2065">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2065">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="2c7c7-2066">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2066">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="2c7c7-2067">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2067">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="2c7c7-2068">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2068">Az.CognitiveServices</span></span>
* <span data-ttu-id="2c7c7-2069">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2069">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="2c7c7-2070">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2070">Az.Compute</span></span>
* <span data-ttu-id="2c7c7-2071">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2071">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="2c7c7-2072">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2072">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="2c7c7-2073">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2073">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="2c7c7-2074">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2074">Az.DataFactoryV2</span></span>
* <span data-ttu-id="2c7c7-2075">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2075">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="2c7c7-2076">Az.Network</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2076">Az.Network</span></span>
* <span data-ttu-id="2c7c7-2077">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2077">Added NetworkProfile functionality.</span></span> <span data-ttu-id="2c7c7-2078">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2078">new cmdlets added</span></span>
    - <span data-ttu-id="2c7c7-2079">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2079">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="2c7c7-2080">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2080">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="2c7c7-2081">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2081">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="2c7c7-2082">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2082">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="2c7c7-2083">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2083">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="2c7c7-2084">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2084">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="2c7c7-2085">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2085">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="2c7c7-2086">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2086">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="2c7c7-2087">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2087">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="2c7c7-2088">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2088">Az.RedisCache</span></span>
* <span data-ttu-id="2c7c7-2089">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2089">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="2c7c7-2090">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2090">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="2c7c7-2091">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2091">Az.Resources</span></span>
* <span data-ttu-id="2c7c7-2092">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2092">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="2c7c7-2093">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2093">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="2c7c7-2094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2094">Az.Sql</span></span>
* <span data-ttu-id="2c7c7-2095">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2095">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="2c7c7-2096">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2096">Az.Websites</span></span>
* <span data-ttu-id="2c7c7-2097">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2097">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="2c7c7-2098">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2098">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="2c7c7-2099">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2099">0.2.0 - September 2018</span></span>
 <span data-ttu-id="2c7c7-2100">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="2c7c7-2100">Initial Release</span></span>
