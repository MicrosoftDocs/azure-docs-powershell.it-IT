---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/09/2020
ms.openlocfilehash: 4c7ea19a225d63307ecf4a6fe5ebfa14ccd78d7e
ms.sourcegitcommit: f6fa6543be1e0f6330b1598f01528b2928cc426c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2020
ms.locfileid: "79036162"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0e611-103">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e611-103">Azure PowerShell release notes</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="0e611-104">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="0e611-104">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-105">Az.Accounts</span></span>
* <span data-ttu-id="0e611-106">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="0e611-106">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="0e611-107">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="0e611-107">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="0e611-108">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="0e611-108">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0e611-109">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-109">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-110">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="0e611-110">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="0e611-111">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="0e611-111">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="0e611-112">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="0e611-112">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="0e611-113">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="0e611-113">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-114">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-114">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-115">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="0e611-115">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-116">Az.IotHub</span></span>
* <span data-ttu-id="0e611-117">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-117">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0e611-118">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0e611-118">New Cmdlets are:</span></span>
    - <span data-ttu-id="0e611-119">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-119">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-120">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-120">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-121">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-121">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-122">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-122">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="0e611-123">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-123">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="0e611-124">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0e611-124">New Cmdlets are:</span></span>
    - <span data-ttu-id="0e611-125">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0e611-125">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="0e611-126">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0e611-126">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="0e611-127">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0e611-127">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="0e611-128">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0e611-128">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="0e611-129">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-129">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0e611-130">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-130">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0e611-131">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-131">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="0e611-132">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0e611-132">New Cmdlets are:</span></span>
    - <span data-ttu-id="0e611-133">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0e611-133">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="0e611-134">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0e611-134">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="0e611-135">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0e611-135">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-136">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-136">Az.Monitor</span></span>
* <span data-ttu-id="0e611-137">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="0e611-137">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-138">Az.Network</span></span>
* <span data-ttu-id="0e611-139">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="0e611-139">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="0e611-140">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="0e611-140">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="0e611-141">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="0e611-141">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="0e611-142">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="0e611-142">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-143">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-143">Az.Resources</span></span>
* <span data-ttu-id="0e611-144">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="0e611-144">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="0e611-145">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="0e611-145">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="0e611-146">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="0e611-146">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="0e611-147">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="0e611-147">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="0e611-148">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="0e611-148">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="0e611-149">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="0e611-149">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="0e611-150">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="0e611-150">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="0e611-151">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-151">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="0e611-152">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-152">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0e611-153">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-153">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0e611-154">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-154">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="0e611-155">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="0e611-155">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="0e611-156">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-156">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="0e611-157">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="0e611-157">Brought ScopedDeployment from SDK 3.3.0</span></span> 

#### <a name="azsql"></a><span data-ttu-id="0e611-158">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-158">Az.Sql</span></span>
* <span data-ttu-id="0e611-159">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="0e611-159">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="0e611-160">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="0e611-160">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="0e611-161">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="0e611-161">Get/Set LTR policy on a managed database</span></span> 
    - <span data-ttu-id="0e611-162">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="0e611-162">Get LTR backup(s) by managed database, managed instance, or by location</span></span> 
    - <span data-ttu-id="0e611-163">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="0e611-163">Remove an LTR backup</span></span> 
    - <span data-ttu-id="0e611-164">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="0e611-164">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="0e611-165">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0e611-165">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="0e611-166">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-166">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="0e611-167">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-167">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-168">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-168">Az.Storage</span></span>
* <span data-ttu-id="0e611-169">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-169">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="0e611-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="0e611-170">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="0e611-171">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0e611-171">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="0e611-172">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0e611-172">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="0e611-173">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0e611-173">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-174">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-174">Az.Websites</span></span>
* <span data-ttu-id="0e611-175">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="0e611-175">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="0e611-176">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="0e611-176">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="0e611-177">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="0e611-177">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="0e611-178">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="0e611-178">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="0e611-179">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0e611-179">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0e611-180">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="0e611-180">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-181">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-181">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-182">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="0e611-182">Updated client side telemetry.</span></span>
* <span data-ttu-id="0e611-183">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0e611-183">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0e611-184">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0e611-184">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-185">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-185">Az.Accounts</span></span>
* <span data-ttu-id="0e611-186">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="0e611-186">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-187">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-187">Az.Automation</span></span>
* <span data-ttu-id="0e611-188">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0e611-188">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-189">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-189">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-190">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="0e611-190">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0e611-191">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="0e611-191">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-192">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-192">Az.Compute</span></span>
* <span data-ttu-id="0e611-193">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0e611-193">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-194">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-194">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-195">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="0e611-195">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-196">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-196">Az.IotHub</span></span>
* <span data-ttu-id="0e611-197">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-197">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0e611-198">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0e611-198">New Cmdlets are:</span></span>
    - <span data-ttu-id="0e611-199">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-199">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-200">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-200">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-201">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-201">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0e611-202">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0e611-202">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-203">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-204">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="0e611-204">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-205">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-205">Az.Monitor</span></span>
* <span data-ttu-id="0e611-206">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="0e611-206">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0e611-207">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="0e611-207">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0e611-208">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="0e611-208">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-209">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-209">Az.Network</span></span>
* <span data-ttu-id="0e611-210">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="0e611-210">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0e611-211">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0e611-211">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0e611-212">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0e611-212">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0e611-213">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-213">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0e611-214">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="0e611-214">No new cmdlets are added.</span></span> <span data-ttu-id="0e611-215">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-215">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-216">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-216">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-217">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="0e611-217">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-218">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-218">Az.Resources</span></span>
* <span data-ttu-id="0e611-219">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="0e611-219">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0e611-220">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0e611-220">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0e611-221">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0e611-221">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0e611-222">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0e611-222">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0e611-223">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0e611-223">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0e611-224">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="0e611-224">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0e611-225">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="0e611-225">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0e611-226">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-226">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-227">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-227">Az.Sql</span></span>
* <span data-ttu-id="0e611-228">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0e611-228">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0e611-229">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="0e611-229">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0e611-230">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0e611-230">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0e611-231">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e611-231">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0e611-232">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="0e611-232">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0e611-233">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0e611-233">Az.StorageSync</span></span>
* <span data-ttu-id="0e611-234">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="0e611-234">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0e611-235">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="0e611-235">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-236">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-236">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-237">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0e611-237">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0e611-238">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="0e611-238">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-239">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-239">Az.Accounts</span></span>
* <span data-ttu-id="0e611-240">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="0e611-240">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0e611-241">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="0e611-241">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0e611-242">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-242">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-243">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0e611-243">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0e611-244">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0e611-244">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0e611-245">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="0e611-245">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0e611-246">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-246">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-247">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-247">Az.Compute</span></span>
* <span data-ttu-id="0e611-248">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e611-248">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0e611-249">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0e611-249">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0e611-250">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e611-250">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0e611-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-251">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0e611-252">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="0e611-252">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-253">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-253">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-254">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="0e611-254">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0e611-255">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0e611-255">Az.DeploymentManager</span></span>
* <span data-ttu-id="0e611-256">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="0e611-256">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0e611-257">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="0e611-257">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0e611-258">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-258">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-259">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="0e611-259">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-260">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-260">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-261">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0e611-261">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-262">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-262">Az.Network</span></span>
* <span data-ttu-id="0e611-263">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="0e611-263">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0e611-264">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="0e611-264">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0e611-265">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0e611-265">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0e611-266">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0e611-266">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0e611-267">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="0e611-267">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0e611-268">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="0e611-268">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0e611-269">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="0e611-269">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0e611-270">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0e611-270">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0e611-271">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-271">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-272">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0e611-273">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-273">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0e611-274">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0e611-274">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0e611-275">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="0e611-275">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e611-276">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-276">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e611-277">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="0e611-277">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0e611-278">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0e611-278">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0e611-279">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="0e611-279">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0e611-280">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="0e611-280">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-281">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-281">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-282">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="0e611-282">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0e611-283">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0e611-283">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-284">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-284">Az.Resources</span></span>
* <span data-ttu-id="0e611-285">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="0e611-285">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0e611-286">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="0e611-286">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-287">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-287">Az.Sql</span></span>
<span data-ttu-id="0e611-288">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0e611-288">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-289">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-289">Az.Storage</span></span>
* <span data-ttu-id="0e611-290">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e611-290">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0e611-291">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-291">New-AzStorageAccount</span></span>
* <span data-ttu-id="0e611-292">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="0e611-292">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0e611-293">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-293">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-294">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-294">Az.Websites</span></span>
* <span data-ttu-id="0e611-295">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="0e611-295">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0e611-296">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0e611-296">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0e611-297">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="0e611-297">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-298">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-298">Az.Accounts</span></span>
* <span data-ttu-id="0e611-299">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0e611-299">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-300">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-300">Az.Cdn</span></span>
* <span data-ttu-id="0e611-301">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-301">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-302">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-302">Az.Compute</span></span>
* <span data-ttu-id="0e611-303">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0e611-303">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0e611-304">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-304">Az.ContainerInstance</span></span>
* <span data-ttu-id="0e611-305">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-305">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0e611-306">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0e611-306">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0e611-307">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0e611-307">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0e611-308">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-308">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0e611-309">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0e611-309">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0e611-310">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-310">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0e611-311">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0e611-311">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0e611-312">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-312">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0e611-313">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0e611-313">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0e611-314">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-314">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0e611-315">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0e611-315">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0e611-316">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-316">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0e611-317">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0e611-317">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0e611-318">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-318">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0e611-319">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0e611-319">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0e611-320">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0e611-320">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0e611-321">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="0e611-321">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0e611-322">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="0e611-322">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0e611-323">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="0e611-323">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0e611-324">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="0e611-324">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-325">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-325">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-326">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0e611-326">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0e611-327">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="0e611-327">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0e611-328">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="0e611-328">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0e611-329">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0e611-329">Az.DevTestLabs</span></span>
* <span data-ttu-id="0e611-330">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="0e611-330">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-331">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-331">Az.EventHub</span></span>
* <span data-ttu-id="0e611-332">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="0e611-332">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0e611-333">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-333">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-334">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="0e611-334">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0e611-335">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0e611-335">Az.MachineLearning</span></span>
* <span data-ttu-id="0e611-336">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="0e611-336">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0e611-337">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0e611-337">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0e611-338">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0e611-338">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0e611-339">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0e611-339">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0e611-340">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0e611-340">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0e611-341">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0e611-341">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0e611-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0e611-342">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0e611-343">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0e611-343">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-344">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-344">Az.Network</span></span>
* <span data-ttu-id="0e611-345">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="0e611-345">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-346">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-346">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-347">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-347">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0e611-348">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-348">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0e611-349">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-349">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0e611-350">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-350">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-351">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-351">Az.Resources</span></span>
* <span data-ttu-id="0e611-352">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="0e611-352">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-353">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-353">Az.Sql</span></span>
* <span data-ttu-id="0e611-354">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="0e611-354">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0e611-355">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="0e611-355">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0e611-356">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0e611-356">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0e611-357">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="0e611-357">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-358">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-358">Az.Storage</span></span>
* <span data-ttu-id="0e611-359">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0e611-359">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0e611-360">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-360">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0e611-361">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="0e611-361">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="0e611-362">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-362">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0e611-363">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-363">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0e611-364">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-364">General</span></span>
* <span data-ttu-id="0e611-365">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="0e611-365">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-366">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-366">Az.Accounts</span></span>
* <span data-ttu-id="0e611-367">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="0e611-367">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0e611-368">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="0e611-368">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0e611-369">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-369">Az.Batch</span></span>
* <span data-ttu-id="0e611-370">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="0e611-370">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-371">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-371">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-372">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="0e611-372">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-373">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-373">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-374">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="0e611-374">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0e611-375">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="0e611-375">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0e611-376">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0e611-376">Az.HealthcareApis</span></span>
* <span data-ttu-id="0e611-377">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="0e611-377">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-378">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-378">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-379">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="0e611-379">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0e611-380">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="0e611-380">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0e611-381">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="0e611-381">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-382">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-382">Az.Monitor</span></span>
* <span data-ttu-id="0e611-383">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0e611-383">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0e611-384">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="0e611-384">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0e611-385">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="0e611-385">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-386">Az.Network</span></span>
* <span data-ttu-id="0e611-387">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="0e611-387">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-388">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-388">Az.Resources</span></span>
* <span data-ttu-id="0e611-389">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="0e611-389">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0e611-390">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="0e611-390">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-391">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-391">Az.Sql</span></span>
* <span data-ttu-id="0e611-392">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="0e611-392">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-393">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-393">Az.Storage</span></span>
* <span data-ttu-id="0e611-394">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="0e611-394">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0e611-395">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0e611-395">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0e611-396">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0e611-396">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0e611-397">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="0e611-397">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0e611-398">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0e611-398">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0e611-399">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="0e611-399">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0e611-400">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="0e611-400">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="0e611-401">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-401">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0e611-402">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-402">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0e611-403">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="0e611-403">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0e611-404">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0e611-404">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0e611-405">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="0e611-405">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0e611-406">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0e611-406">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0e611-407">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-407">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-408">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-408">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-409">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-409">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0e611-410">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-410">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-411">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-411">Az.Compute</span></span>
* <span data-ttu-id="0e611-412">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-412">VM Reapply feature</span></span>
    - <span data-ttu-id="0e611-413">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e611-413">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0e611-414">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="0e611-414">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0e611-415">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-415">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0e611-416">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e611-416">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0e611-417">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-417">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0e611-418">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e611-418">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0e611-419">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="0e611-419">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0e611-420">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0e611-420">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0e611-421">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="0e611-421">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0e611-422">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-422">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0e611-423">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0e611-423">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0e611-424">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0e611-424">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0e611-425">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="0e611-425">Get the Order</span></span>
* <span data-ttu-id="0e611-426">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0e611-426">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0e611-427">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="0e611-427">Create new Order</span></span>
* <span data-ttu-id="0e611-428">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0e611-428">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0e611-429">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="0e611-429">Remove the Order</span></span>
* <span data-ttu-id="0e611-430">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="0e611-430">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0e611-431">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="0e611-431">Now creates Local Share</span></span>
* <span data-ttu-id="0e611-432">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="0e611-432">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0e611-433">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="0e611-433">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0e611-434">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="0e611-434">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0e611-435">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="0e611-435">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0e611-436">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0e611-436">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0e611-437">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="0e611-437">Gets the information about Triggers</span></span>
* <span data-ttu-id="0e611-438">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0e611-438">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0e611-439">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="0e611-439">Create new Triggers</span></span>
* <span data-ttu-id="0e611-440">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0e611-440">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0e611-441">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="0e611-441">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-442">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-442">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-443">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="0e611-443">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0e611-444">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0e611-444">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-445">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-445">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-446">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0e611-446">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-447">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-447">Az.EventHub</span></span>
* <span data-ttu-id="0e611-448">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="0e611-448">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-449">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-449">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-450">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0e611-450">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0e611-451">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0e611-451">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0e611-452">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="0e611-452">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0e611-453">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0e611-453">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-454">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-454">Az.Network</span></span>
* <span data-ttu-id="0e611-455">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="0e611-455">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0e611-456">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0e611-456">Az.PrivateDns</span></span>
* <span data-ttu-id="0e611-457">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-457">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-458">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-458">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-459">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="0e611-459">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0e611-460">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0e611-460">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0e611-461">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-461">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e611-462">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e611-462">Az.RedisCache</span></span>
* <span data-ttu-id="0e611-463">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0e611-463">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0e611-464">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0e611-464">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0e611-465">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="0e611-465">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-466">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-466">Az.Resources</span></span>
- <span data-ttu-id="0e611-467">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0e611-467">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0e611-468">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="0e611-468">Updated create policy definition help example</span></span>
- <span data-ttu-id="0e611-469">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0e611-469">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0e611-470">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0e611-470">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0e611-471">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="0e611-471">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-472">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-472">Az.Sql</span></span>
* <span data-ttu-id="0e611-473">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="0e611-473">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0e611-474">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="0e611-474">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0e611-475">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-475">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0e611-476">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-476">General</span></span>
* <span data-ttu-id="0e611-477">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-477">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-478">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-478">Az.Accounts</span></span>
* <span data-ttu-id="0e611-479">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="0e611-479">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0e611-480">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0e611-480">Az.Advisor</span></span>
* <span data-ttu-id="0e611-481">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="0e611-481">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0e611-482">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-482">Az.Batch</span></span>
* <span data-ttu-id="0e611-483">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="0e611-483">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0e611-484">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0e611-484">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0e611-485">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="0e611-485">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0e611-486">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="0e611-486">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0e611-487">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0e611-487">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0e611-488">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0e611-488">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0e611-489">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="0e611-489">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0e611-490">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="0e611-490">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0e611-491">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="0e611-491">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0e611-492">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0e611-492">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0e611-493">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="0e611-493">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0e611-494">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0e611-494">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0e611-495">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0e611-495">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0e611-496">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="0e611-496">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0e611-497">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="0e611-497">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0e611-498">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="0e611-498">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0e611-499">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0e611-499">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0e611-500">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0e611-500">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0e611-501">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="0e611-501">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0e611-502">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="0e611-502">This operation is no longer supported.</span></span>
* <span data-ttu-id="0e611-503">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0e611-503">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0e611-504">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0e611-504">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0e611-505">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="0e611-505">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0e611-506">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="0e611-506">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="0e611-507">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="0e611-507">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0e611-508">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="0e611-508">New non-verified images are also now returned.</span></span> <span data-ttu-id="0e611-509">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="0e611-509">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0e611-510">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="0e611-510">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0e611-511">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="0e611-511">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0e611-512">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="0e611-512">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0e611-513">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="0e611-513">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0e611-514">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="0e611-514">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0e611-515">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="0e611-515">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0e611-516">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0e611-516">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0e611-517">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="0e611-517">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0e611-518">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="0e611-518">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-519">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-519">Az.Cdn</span></span>
* <span data-ttu-id="0e611-520">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="0e611-520">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0e611-521">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="0e611-521">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-522">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-522">Az.Compute</span></span>
* <span data-ttu-id="0e611-523">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="0e611-523">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0e611-524">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0e611-524">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0e611-525">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-525">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="0e611-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e611-526">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0e611-527">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-527">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0e611-528">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-528">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0e611-529">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="0e611-529">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0e611-530">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-530">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0e611-531">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0e611-531">Breaking changes</span></span>
    - <span data-ttu-id="0e611-532">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0e611-532">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0e611-533">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0e611-533">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-534">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-534">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-535">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="0e611-535">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-537">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="0e611-537">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0e611-538">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="0e611-538">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0e611-539">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="0e611-539">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0e611-540">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="0e611-540">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0e611-541">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="0e611-541">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0e611-542">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="0e611-542">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-543">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-543">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-544">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="0e611-544">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0e611-545">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-545">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-546">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="0e611-546">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0e611-547">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0e611-547">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0e611-548">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="0e611-548">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0e611-549">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-549">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0e611-550">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0e611-550">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0e611-551">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0e611-551">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0e611-552">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0e611-552">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0e611-553">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e611-553">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0e611-554">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e611-554">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0e611-555">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-555">Added three cmdlets:</span></span>
    - <span data-ttu-id="0e611-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0e611-556">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0e611-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0e611-557">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0e611-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0e611-558">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0e611-559">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="0e611-559">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0e611-560">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="0e611-560">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0e611-561">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="0e611-561">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0e611-562">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e611-562">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0e611-563">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="0e611-563">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0e611-564">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="0e611-564">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0e611-565">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="0e611-565">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0e611-566">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="0e611-566">Added some scenario test cases.</span></span>
* <span data-ttu-id="0e611-567">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="0e611-567">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-568">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-568">Az.IotHub</span></span>
* <span data-ttu-id="0e611-569">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="0e611-569">Breaking changes:</span></span>
    - <span data-ttu-id="0e611-570">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0e611-570">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0e611-571">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0e611-571">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0e611-572">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0e611-572">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0e611-573">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0e611-573">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0e611-574">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0e611-574">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0e611-575">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0e611-575">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0e611-576">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0e611-576">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0e611-577">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0e611-577">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0e611-578">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0e611-578">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0e611-579">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0e611-579">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0e611-580">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0e611-580">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0e611-581">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0e611-581">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-582">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-582">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-583">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-583">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-584">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-584">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0e611-585">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-585">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0e611-586">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-586">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-587">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-587">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-588">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-588">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-589">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-589">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-590">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-590">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-591">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="0e611-591">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-592">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-592">Az.Resources</span></span>
* <span data-ttu-id="0e611-593">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="0e611-593">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-594">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-594">Az.Network</span></span>
* <span data-ttu-id="0e611-595">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="0e611-595">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0e611-596">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0e611-596">Updated cmdlet:</span></span>
        - <span data-ttu-id="0e611-597">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-597">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-598">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-598">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-599">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-599">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-600">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-600">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-601">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-601">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0e611-602">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="0e611-602">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0e611-603">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-603">New cmdlet:</span></span>
        - <span data-ttu-id="0e611-604">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0e611-604">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0e611-605">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="0e611-605">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0e611-606">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-606">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0e611-607">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-607">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0e611-608">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="0e611-608">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0e611-609">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="0e611-609">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0e611-610">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-610">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0e611-611">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="0e611-611">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0e611-612">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-612">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-613">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0e611-613">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0e611-614">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-614">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0e611-615">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-615">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0e611-616">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-616">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0e611-617">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0e611-617">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0e611-618">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0e611-618">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0e611-619">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0e611-619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0e611-620">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="0e611-620">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0e611-621">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="0e611-621">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0e611-622">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0e611-622">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0e611-623">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0e611-623">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0e611-624">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-624">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0e611-625">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-625">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-626">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-626">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0e611-627">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0e611-627">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0e611-628">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0e611-628">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0e611-629">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0e611-629">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0e611-630">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0e611-630">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0e611-631">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0e611-631">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0e611-632">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0e611-632">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0e611-633">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="0e611-633">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0e611-634">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-634">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-635">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0e611-635">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0e611-636">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0e611-636">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0e611-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0e611-637">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0e611-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0e611-638">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0e611-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0e611-639">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0e611-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-640">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0e611-641">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0e611-641">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0e611-642">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0e611-642">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0e611-643">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="0e611-643">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0e611-644">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0e611-644">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0e611-645">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="0e611-645">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0e611-646">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0e611-646">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0e611-647">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0e611-647">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0e611-648">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0e611-648">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0e611-649">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="0e611-649">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0e611-650">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-650">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0e611-651">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-651">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0e611-652">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-652">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-653">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-653">New-AzIpGroup</span></span>
        - <span data-ttu-id="0e611-654">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-654">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0e611-655">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-655">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0e611-656">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-656">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-657">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-657">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-658">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="0e611-658">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-659">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-659">Az.Sql</span></span>
* <span data-ttu-id="0e611-660">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0e611-660">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0e611-661">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="0e611-661">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0e611-662">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="0e611-662">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0e611-663">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="0e611-663">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0e611-664">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="0e611-664">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0e611-665">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-665">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0e611-666">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="0e611-666">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0e611-667">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="0e611-667">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="0e611-668">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="0e611-668">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-669">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-669">Az.Storage</span></span>
* <span data-ttu-id="0e611-670">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e611-670">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0e611-671">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-671">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0e611-672">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-672">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0e611-673">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="0e611-673">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0e611-674">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0e611-674">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0e611-675">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0e611-675">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="0e611-676">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-676">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0e611-677">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-677">General</span></span>
* <span data-ttu-id="0e611-678">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-678">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-679">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-679">Az.Accounts</span></span>
* <span data-ttu-id="0e611-680">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="0e611-680">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0e611-681">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-681">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-682">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0e611-682">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0e611-683">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="0e611-683">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-684">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-684">Az.Automation</span></span>
* <span data-ttu-id="0e611-685">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="0e611-685">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="0e611-686">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-686">Az.Batch</span></span>
* <span data-ttu-id="0e611-687">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="0e611-687">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-688">Az.Compute</span></span>
* <span data-ttu-id="0e611-689">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-689">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0e611-690">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0e611-690">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0e611-691">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="0e611-691">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="0e611-692">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0e611-692">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-693">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-693">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-694">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0e611-694">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0e611-695">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0e611-695">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0e611-696">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="0e611-696">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-697">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-697">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-698">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="0e611-698">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0e611-699">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0e611-699">Az.HealthcareApis</span></span>
* <span data-ttu-id="0e611-700">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-700">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0e611-701">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="0e611-701">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0e611-702">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="0e611-702">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0e611-703">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="0e611-703">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-704">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-704">Az.IotHub</span></span>
* <span data-ttu-id="0e611-705">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0e611-705">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0e611-706">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e611-706">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="0e611-707">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-707">Az.Monitor</span></span>
* <span data-ttu-id="0e611-708">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0e611-708">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0e611-709">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="0e611-709">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0e611-710">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="0e611-710">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0e611-711">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0e611-711">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-712">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-712">Az.Network</span></span>
* <span data-ttu-id="0e611-713">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="0e611-713">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0e611-714">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-714">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0e611-715">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-715">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-716">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-716">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0e611-717">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-717">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0e611-718">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="0e611-718">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0e611-719">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-719">Updated cmdlets:</span></span>
        - <span data-ttu-id="0e611-720">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-720">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0e611-721">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-721">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0e611-722">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-722">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0e611-723">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="0e611-723">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0e611-724">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0e611-724">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0e611-725">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0e611-725">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0e611-726">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0e611-726">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e611-727">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e611-727">Az.RedisCache</span></span>
* <span data-ttu-id="0e611-728">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="0e611-728">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-729">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-729">Az.Sql</span></span>
* <span data-ttu-id="0e611-730">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="0e611-730">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-731">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-731">Az.Storage</span></span>
* <span data-ttu-id="0e611-732">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="0e611-732">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0e611-733">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0e611-733">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0e611-734">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0e611-734">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0e611-735">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0e611-735">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0e611-736">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-736">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0e611-737">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0e611-737">Az.StorageSync</span></span>
* <span data-ttu-id="0e611-738">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="0e611-738">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-739">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-739">Az.Websites</span></span>
* <span data-ttu-id="0e611-740">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="0e611-740">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0e611-741">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-741">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0e611-742">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-742">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-743">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="0e611-743">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0e611-744">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0e611-744">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0e611-745">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="0e611-745">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-746">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-746">Az.Automation</span></span>
* <span data-ttu-id="0e611-747">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="0e611-747">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0e611-748">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="0e611-748">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0e611-749">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="0e611-749">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-750">Az.Compute</span></span>
* <span data-ttu-id="0e611-751">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-751">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0e611-752">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-752">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0e611-753">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="0e611-753">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0e611-754">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="0e611-754">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0e611-755">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0e611-755">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0e611-756">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0e611-756">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0e611-757">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="0e611-757">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0e611-758">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="0e611-758">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0e611-759">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0e611-759">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-760">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-760">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-761">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0e611-761">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0e611-762">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="0e611-762">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0e611-763">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-763">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-764">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0e611-764">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-765">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-765">Az.IotHub</span></span>
* <span data-ttu-id="0e611-766">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="0e611-766">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0e611-767">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0e611-767">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0e611-768">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0e611-768">New cmdlets are:</span></span>
    - <span data-ttu-id="0e611-769">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0e611-769">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0e611-770">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0e611-770">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0e611-771">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0e611-771">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0e611-772">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0e611-772">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-773">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-773">Az.Monitor</span></span>
* <span data-ttu-id="0e611-774">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="0e611-774">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0e611-775">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="0e611-775">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0e611-776">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="0e611-776">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0e611-777">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="0e611-777">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0e611-778">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="0e611-778">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0e611-779">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="0e611-779">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0e611-780">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e611-780">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0e611-781">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="0e611-781">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0e611-782">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="0e611-782">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0e611-783">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="0e611-783">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0e611-784">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="0e611-784">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0e611-785">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="0e611-785">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0e611-786">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="0e611-786">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0e611-787">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="0e611-787">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0e611-788">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="0e611-788">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0e611-789">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="0e611-789">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0e611-790">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="0e611-790">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0e611-791">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-791">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0e611-792">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="0e611-792">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0e611-793">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-793">Overall improved help files</span></span>
* <span data-ttu-id="0e611-794">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="0e611-794">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-795">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-795">Az.Network</span></span>
* <span data-ttu-id="0e611-796">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="0e611-796">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="0e611-797">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="0e611-797">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0e611-798">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="0e611-798">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0e611-799">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="0e611-799">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0e611-800">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="0e611-800">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0e611-801">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="0e611-801">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0e611-802">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="0e611-802">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0e611-803">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0e611-803">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0e611-804">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-804">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0e611-805">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="0e611-805">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0e611-806">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-806">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0e611-807">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-807">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0e611-808">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-808">New cmdlets</span></span>
        - <span data-ttu-id="0e611-809">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0e611-809">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0e611-810">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-810">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0e611-811">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0e611-811">Updated cmdlet:</span></span>
        - <span data-ttu-id="0e611-812">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0e611-812">New-VpnSite</span></span>
        - <span data-ttu-id="0e611-813">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0e611-813">Update-VpnSite</span></span>
        - <span data-ttu-id="0e611-814">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-814">New-VpnConnection</span></span>
        - <span data-ttu-id="0e611-815">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-815">Update-VpnConnection</span></span>
* <span data-ttu-id="0e611-816">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="0e611-816">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-817">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-817">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-818">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="0e611-818">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0e611-819">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="0e611-819">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-820">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-820">Az.Resources</span></span>
* <span data-ttu-id="0e611-821">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="0e611-821">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-822">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-822">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-823">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0e611-823">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0e611-824">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="0e611-824">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0e611-825">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0e611-825">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0e611-826">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0e611-826">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0e611-827">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0e611-827">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0e611-828">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0e611-828">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0e611-829">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0e611-829">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0e611-830">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0e611-830">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0e611-831">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0e611-831">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0e611-832">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0e611-832">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0e611-833">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0e611-833">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0e611-834">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0e611-834">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0e611-835">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0e611-835">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0e611-836">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0e611-836">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0e611-837">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0e611-837">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0e611-838">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0e611-838">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0e611-839">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0e611-839">Az.SignalR</span></span>
* <span data-ttu-id="0e611-840">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="0e611-840">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-841">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-841">Az.Sql</span></span>
* <span data-ttu-id="0e611-842">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="0e611-842">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0e611-843">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="0e611-843">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0e611-844">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-844">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0e611-845">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="0e611-845">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0e611-846">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="0e611-846">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-847">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-847">Az.Storage</span></span>
* <span data-ttu-id="0e611-848">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="0e611-848">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0e611-849">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="0e611-849">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0e611-850">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e611-850">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0e611-851">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e611-851">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0e611-852">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="0e611-852">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0e611-853">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e611-853">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0e611-854">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="0e611-854">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0e611-855">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-855">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0e611-856">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-856">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0e611-857">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-857">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0e611-858">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0e611-858">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-859">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-859">Az.Websites</span></span>
* <span data-ttu-id="0e611-860">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="0e611-860">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0e611-861">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="0e611-861">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0e611-862">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="0e611-862">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0e611-863">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-863">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0e611-864">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-864">General</span></span>
* <span data-ttu-id="0e611-865">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="0e611-865">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-866">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-866">Az.Accounts</span></span>
* <span data-ttu-id="0e611-867">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="0e611-867">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0e611-868">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0e611-868">Az.Aks</span></span>
* <span data-ttu-id="0e611-869">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="0e611-869">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0e611-870">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0e611-870">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0e611-871">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-871">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-872">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="0e611-872">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0e611-873">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="0e611-873">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0e611-874">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="0e611-874">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0e611-875">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0e611-875">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0e611-876">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0e611-876">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0e611-877">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-877">Az.Batch</span></span>
* <span data-ttu-id="0e611-878">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="0e611-878">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-879">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-879">Az.Cdn</span></span>
* <span data-ttu-id="0e611-880">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="0e611-880">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-881">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-881">Az.Compute</span></span>
* <span data-ttu-id="0e611-882">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-882">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0e611-883">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-883">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0e611-884">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-884">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0e611-885">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-885">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0e611-886">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0e611-886">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0e611-887">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e611-887">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0e611-888">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="0e611-888">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0e611-889">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="0e611-889">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-890">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-890">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-891">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="0e611-891">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0e611-892">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="0e611-892">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0e611-893">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="0e611-893">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0e611-894">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="0e611-894">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-895">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-895">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-896">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="0e611-896">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-897">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-897">Az.EventHub</span></span>
* <span data-ttu-id="0e611-898">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-898">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0e611-899">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0e611-899">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0e611-900">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0e611-900">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0e611-901">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="0e611-901">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0e611-902">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0e611-902">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0e611-903">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="0e611-903">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-904">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-904">Az.Monitor</span></span>
* <span data-ttu-id="0e611-905">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-905">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-906">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-906">Az.Network</span></span>
* <span data-ttu-id="0e611-907">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-907">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0e611-908">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="0e611-908">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0e611-909">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="0e611-909">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0e611-910">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="0e611-910">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0e611-911">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="0e611-911">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="0e611-912">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="0e611-912">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0e611-913">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0e611-913">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-914">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-914">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-915">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="0e611-915">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0e611-916">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0e611-916">Added example</span></span>
    - <span data-ttu-id="0e611-917">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="0e611-917">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0e611-918">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0e611-918">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0e611-919">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0e611-919">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-920">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-920">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-921">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-921">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-922">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-922">Az.Resources</span></span>
* <span data-ttu-id="0e611-923">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="0e611-923">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0e611-924">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="0e611-924">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0e611-925">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="0e611-925">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0e611-926">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-926">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-927">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-927">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-928">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-928">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0e611-929">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="0e611-929">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0e611-930">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="0e611-930">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-931">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-931">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-932">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="0e611-932">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0e611-933">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0e611-933">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0e611-934">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0e611-934">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0e611-935">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="0e611-935">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0e611-936">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0e611-936">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0e611-937">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0e611-937">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-938">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-938">Az.Sql</span></span>
* <span data-ttu-id="0e611-939">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="0e611-939">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-940">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-940">Az.Storage</span></span>
* <span data-ttu-id="0e611-941">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0e611-941">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0e611-942">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="0e611-942">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0e611-943">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e611-943">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0e611-944">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-944">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0e611-945">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="0e611-945">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0e611-946">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-946">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-947">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-947">Az.Websites</span></span>
* <span data-ttu-id="0e611-948">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e611-948">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0e611-949">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-949">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-950">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-950">Az.Accounts</span></span>
* <span data-ttu-id="0e611-951">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0e611-951">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0e611-952">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-952">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0e611-953">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="0e611-953">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="0e611-954">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-954">Az.Automation</span></span>
* <span data-ttu-id="0e611-955">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="0e611-955">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-956">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-956">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-957">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0e611-957">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-958">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-958">Az.Compute</span></span>
* <span data-ttu-id="0e611-959">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e611-959">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0e611-960">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e611-960">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0e611-961">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="0e611-961">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0e611-962">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0e611-962">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-963">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-963">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-964">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0e611-964">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0e611-965">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="0e611-965">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-966">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-966">Az.EventHub</span></span>
* <span data-ttu-id="0e611-967">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0e611-967">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0e611-968">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="0e611-968">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-969">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-969">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-970">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="0e611-970">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e611-971">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e611-971">Az.LogicApp</span></span>
* <span data-ttu-id="0e611-972">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="0e611-972">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0e611-973">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="0e611-973">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0e611-974">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0e611-974">Az.ManagedServices</span></span>
* <span data-ttu-id="0e611-975">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="0e611-975">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-976">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-976">Az.Network</span></span>
* <span data-ttu-id="0e611-977">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0e611-977">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0e611-978">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-978">New cmdlets</span></span>
        - <span data-ttu-id="0e611-979">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-979">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e611-980">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-980">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0e611-981">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-981">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-982">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-982">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-983">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-983">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-984">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-984">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0e611-985">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0e611-985">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0e611-986">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-986">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0e611-987">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="0e611-987">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0e611-988">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-988">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0e611-989">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="0e611-989">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0e611-990">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="0e611-990">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0e611-991">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="0e611-991">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0e611-992">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="0e611-992">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0e611-993">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-993">Updated cmdlets</span></span>
        - <span data-ttu-id="0e611-994">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-994">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0e611-995">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-995">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0e611-996">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-996">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0e611-997">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-997">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0e611-998">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-998">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0e611-999">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0e611-999">Updated cmdlet:</span></span>
        - <span data-ttu-id="0e611-1000">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1000">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0e611-1001">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1001">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0e611-1002">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1002">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0e611-1003">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="0e611-1003">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0e611-1004">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="0e611-1004">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0e611-1005">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="0e611-1005">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-1007">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="0e611-1007">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="0e611-1008">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="0e611-1008">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1009">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1009">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1010">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1010">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0e611-1011">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1011">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0e611-1012">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1012">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0e611-1013">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1013">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0e611-1014">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1014">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0e611-1015">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1015">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0e611-1016">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1016">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0e611-1017">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1017">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0e611-1018">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1018">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0e611-1019">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="0e611-1019">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1020">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1020">Az.Resources</span></span>
- <span data-ttu-id="0e611-1021">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0e611-1021">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0e611-1022">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0e611-1022">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-1023">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-1023">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-1024">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0e611-1024">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0e611-1025">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="0e611-1025">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1026">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1026">Az.Sql</span></span>
* <span data-ttu-id="0e611-1027">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0e611-1027">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0e611-1028">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="0e611-1028">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0e611-1029">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="0e611-1029">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1030">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1030">Az.Storage</span></span>
* <span data-ttu-id="0e611-1031">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="0e611-1031">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0e611-1032">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0e611-1032">Az.StorageSync</span></span>
* <span data-ttu-id="0e611-1033">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="0e611-1033">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0e611-1034">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="0e611-1034">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1035">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1035">Az.Websites</span></span>
* <span data-ttu-id="0e611-1036">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1036">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0e611-1037">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1037">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0e611-1038">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0e611-1038">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0e611-1039">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1039">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1040">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1040">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1041">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="0e611-1041">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0e611-1042">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="0e611-1042">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0e611-1043">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0e611-1043">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0e611-1044">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0e611-1044">Az.Advisor</span></span>
* <span data-ttu-id="0e611-1045">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0e611-1045">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0e611-1046">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="0e611-1046">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0e611-1047">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1047">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-1048">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="0e611-1048">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0e611-1049">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0e611-1049">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0e611-1050">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="0e611-1050">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0e611-1051">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="0e611-1051">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0e611-1052">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="0e611-1052">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0e611-1053">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e611-1053">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0e611-1054">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="0e611-1054">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1055">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1055">Az.Automation</span></span>
* <span data-ttu-id="0e611-1056">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="0e611-1056">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1057">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1057">Az.Compute</span></span>
* <span data-ttu-id="0e611-1058">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1058">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-1059">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-1059">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-1060">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="0e611-1060">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e611-1061">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e611-1061">Az.EventGrid</span></span>
* <span data-ttu-id="0e611-1062">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="0e611-1062">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-1063">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1063">Az.IotHub</span></span>
* <span data-ttu-id="0e611-1064">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1064">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1065">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1065">Az.Network</span></span>
* <span data-ttu-id="0e611-1066">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="0e611-1066">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0e611-1067">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="0e611-1067">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e611-1068">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1068">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e611-1069">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="0e611-1069">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0e611-1070">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0e611-1070">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1071">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1071">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-1072">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0e611-1072">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1073">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1073">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1074">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="0e611-1074">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1075">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1075">Az.Resources</span></span>
    - <span data-ttu-id="0e611-1076">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="0e611-1076">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0e611-1077">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="0e611-1077">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0e611-1078">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="0e611-1078">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0e611-1079">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="0e611-1079">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-1080">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-1080">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-1081">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="0e611-1081">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1082">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1082">Az.Sql</span></span>
* <span data-ttu-id="0e611-1083">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="0e611-1083">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0e611-1084">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1084">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0e611-1085">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1085">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0e611-1086">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1086">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0e611-1087">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1087">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0e611-1088">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1088">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0e611-1089">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1089">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0e611-1090">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0e611-1090">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0e611-1091">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="0e611-1091">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1092">Az.Storage</span></span>
* <span data-ttu-id="0e611-1093">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-1093">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0e611-1094">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0e611-1094">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0e611-1095">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="0e611-1095">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0e611-1096">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="0e611-1096">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0e611-1097">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1097">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0e611-1098">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1098">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0e611-1099">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1099">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0e611-1100">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="0e611-1100">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0e611-1101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0e611-1101">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0e611-1102">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0e611-1102">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0e611-1103">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0e611-1103">Az.StorageSync</span></span>
* <span data-ttu-id="0e611-1104">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="0e611-1104">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0e611-1105">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1105">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1106">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1107">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="0e611-1107">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0e611-1108">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0e611-1108">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0e611-1109">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="0e611-1109">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0e611-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0e611-1110">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0e611-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0e611-1111">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1112">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1112">Az.Compute</span></span>
* <span data-ttu-id="0e611-1113">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1113">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0e611-1114">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="0e611-1114">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0e611-1115">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0e611-1115">Az.Dns</span></span>
* <span data-ttu-id="0e611-1116">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1116">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e611-1117">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e611-1117">Az.EventGrid</span></span>
* <span data-ttu-id="0e611-1118">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0e611-1118">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0e611-1119">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-1119">New cmdlets:</span></span>
    - <span data-ttu-id="0e611-1120">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e611-1120">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e611-1121">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1121">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e611-1122">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e611-1122">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e611-1123">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1123">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0e611-1124">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0e611-1124">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0e611-1125">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1125">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e611-1126">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0e611-1126">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0e611-1127">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1127">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0e611-1128">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0e611-1128">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0e611-1129">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="0e611-1129">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0e611-1130">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0e611-1130">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0e611-1131">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1131">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0e611-1132">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0e611-1132">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0e611-1133">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1133">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="0e611-1134">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0e611-1134">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0e611-1135">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="0e611-1135">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0e611-1136">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-1136">Updated cmdlets:</span></span>
    - <span data-ttu-id="0e611-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e611-1137">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0e611-1138">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0e611-1138">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0e611-1139">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0e611-1139">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0e611-1140">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="0e611-1140">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0e611-1141">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0e611-1141">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0e611-1142">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="0e611-1142">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0e611-1143">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1143">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0e611-1144">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1144">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0e611-1145">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1145">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="0e611-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e611-1146">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0e611-1147">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1147">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0e611-1148">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0e611-1148">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0e611-1149">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0e611-1149">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0e611-1150">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0e611-1150">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-1151">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-1151">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-1152">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0e611-1152">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0e611-1153">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="0e611-1153">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0e611-1154">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0e611-1154">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0e611-1155">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="0e611-1155">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1156">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1156">Az.Network</span></span>
* <span data-ttu-id="0e611-1157">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-1157">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0e611-1158">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-1158">New cmdlets</span></span>
        - <span data-ttu-id="0e611-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0e611-1159">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0e611-1160">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0e611-1160">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0e611-1161">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-1161">New cmdlets</span></span> 
        - <span data-ttu-id="0e611-1162">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0e611-1162">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0e611-1163">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-1163">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0e611-1164">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-1164">New cmdlets</span></span> 
        - <span data-ttu-id="0e611-1165">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-1165">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="0e611-1166">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-1166">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0e611-1167">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0e611-1167">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0e611-1168">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1168">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0e611-1169">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-1169">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0e611-1170">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-1170">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0e611-1171">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-1171">New cmdlets</span></span>
        - <span data-ttu-id="0e611-1172">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-1172">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e611-1173">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-1173">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e611-1174">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0e611-1174">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0e611-1175">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-1175">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0e611-1176">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0e611-1176">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0e611-1177">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="0e611-1177">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0e611-1178">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="0e611-1178">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0e611-1179">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0e611-1179">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0e611-1180">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0e611-1180">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0e611-1181">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0e611-1181">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0e611-1182">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1182">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0e611-1183">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="0e611-1183">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0e611-1184">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1184">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0e611-1185">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="0e611-1185">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0e611-1186">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1186">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0e611-1187">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1187">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0e611-1188">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0e611-1188">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0e611-1189">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1189">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0e611-1190">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0e611-1190">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0e611-1191">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0e611-1191">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0e611-1192">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-1192">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0e611-1193">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0e611-1193">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0e611-1194">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0e611-1194">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="0e611-1195">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e611-1195">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="0e611-1196">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1196">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0e611-1197">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1197">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0e611-1198">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1198">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1199">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1199">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-1200">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="0e611-1200">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1201">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1201">Az.Resources</span></span>
* <span data-ttu-id="0e611-1202">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="0e611-1202">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0e611-1203">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1203">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0e611-1204">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1204">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0e611-1205">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="0e611-1205">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-1206">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1206">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-1207">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="0e611-1207">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1208">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1208">Az.Sql</span></span>
* <span data-ttu-id="0e611-1209">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e611-1209">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0e611-1210">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e611-1210">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0e611-1211">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="0e611-1211">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0e611-1212">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e611-1212">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e611-1213">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e611-1213">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e611-1214">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0e611-1214">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0e611-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0e611-1215">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0e611-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0e611-1216">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1217">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1217">Az.Storage</span></span>
* <span data-ttu-id="0e611-1218">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1218">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0e611-1219">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1219">New-AzStorageAccount</span></span>
* <span data-ttu-id="0e611-1220">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="0e611-1220">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0e611-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1221">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1222">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1222">Az.Websites</span></span>
* <span data-ttu-id="0e611-1223">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="0e611-1223">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0e611-1224">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0e611-1224">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0e611-1225">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1225">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0e611-1226">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-1226">Az.Cdn</span></span>
* <span data-ttu-id="0e611-1227">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="0e611-1227">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1228">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1228">Az.Compute</span></span>
* <span data-ttu-id="0e611-1229">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1229">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0e611-1230">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e611-1230">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-1231">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1231">Az.EventHub</span></span>
* <span data-ttu-id="0e611-1232">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="0e611-1232">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0e611-1233">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e611-1233">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1234">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1234">Az.Network</span></span>
* <span data-ttu-id="0e611-1235">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="0e611-1235">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0e611-1236">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="0e611-1236">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e611-1237">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1237">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e611-1238">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0e611-1238">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1239">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1239">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1240">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="0e611-1240">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-1241">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-1241">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-1242">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e611-1242">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-1243">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1243">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-1244">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0e611-1244">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0e611-1245">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1245">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1246">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1246">Az.Sql</span></span>
* <span data-ttu-id="0e611-1247">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="0e611-1247">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0e611-1248">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1248">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0e611-1249">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0e611-1249">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0e611-1250">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="0e611-1250">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1251">Az.Websites</span></span>
* <span data-ttu-id="0e611-1252">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="0e611-1252">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0e611-1253">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1253">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0e611-1254">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1254">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-1255">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="0e611-1255">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0e611-1256">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1256">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0e611-1257">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1257">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0e611-1258">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="0e611-1258">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0e611-1259">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1259">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0e611-1260">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="0e611-1260">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0e611-1261">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1261">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0e611-1262">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1262">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0e611-1263">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1263">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0e611-1264">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="0e611-1264">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0e611-1265">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1265">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0e611-1266">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="0e611-1266">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0e611-1267">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="0e611-1267">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0e611-1268">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1268">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0e611-1269">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1269">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0e611-1270">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1270">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0e611-1271">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1271">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0e611-1272">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="0e611-1272">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0e611-1273">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="0e611-1273">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="0e611-1274">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1274">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0e611-1275">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="0e611-1275">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0e611-1276">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e611-1276">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0e611-1277">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="0e611-1277">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0e611-1278">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1278">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="0e611-1279">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="0e611-1279">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0e611-1280">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="0e611-1280">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0e611-1281">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1281">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0e611-1282">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e611-1282">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0e611-1283">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0e611-1283">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0e611-1284">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="0e611-1284">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0e611-1285">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="0e611-1285">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="0e611-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0e611-1286">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0e611-1287">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0e611-1287">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0e611-1288">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e611-1288">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0e611-1289">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0e611-1289">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0e611-1290">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="0e611-1290">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0e611-1291">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="0e611-1291">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0e611-1292">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="0e611-1292">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0e611-1293">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="0e611-1293">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0e611-1294">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e611-1294">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="0e611-1295">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1295">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0e611-1296">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0e611-1296">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0e611-1297">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1297">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0e611-1298">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="0e611-1298">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0e611-1299">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0e611-1299">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0e611-1300">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1300">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0e611-1301">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0e611-1301">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="0e611-1302">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="0e611-1302">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="0e611-1303">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="0e611-1303">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0e611-1304">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1304">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0e611-1305">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="0e611-1305">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0e611-1306">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="0e611-1306">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0e611-1307">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="0e611-1307">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0e611-1308">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="0e611-1308">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0e611-1309">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="0e611-1309">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0e611-1310">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="0e611-1310">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0e611-1311">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0e611-1311">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0e611-1312">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0e611-1312">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0e611-1313">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0e611-1313">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0e611-1314">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1314">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0e611-1315">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0e611-1315">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0e611-1316">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0e611-1316">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0e611-1317">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0e611-1317">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0e611-1318">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1318">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0e611-1319">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="0e611-1319">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0e611-1320">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0e611-1320">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0e611-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0e611-1321">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0e611-1322">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0e611-1322">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0e611-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0e611-1323">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0e611-1324">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0e611-1324">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0e611-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0e611-1325">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0e611-1326">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0e611-1326">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0e611-1327">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0e611-1327">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0e611-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1328">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0e611-1329">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0e611-1329">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="0e611-1330">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0e611-1330">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0e611-1331">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0e611-1331">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1332">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1332">Az.Automation</span></span>
* <span data-ttu-id="0e611-1333">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="0e611-1333">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0e611-1334">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0e611-1334">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0e611-1335">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0e611-1335">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0e611-1336">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="0e611-1336">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0e611-1337">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0e611-1337">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0e611-1338">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="0e611-1338">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0e611-1339">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0e611-1339">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1340">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1340">Az.Compute</span></span>
* <span data-ttu-id="0e611-1341">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="0e611-1341">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0e611-1342">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="0e611-1342">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1343">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-1344">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1344">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-1345">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-1345">Az.Monitor</span></span>
* <span data-ttu-id="0e611-1346">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-1346">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1347">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1347">Az.Network</span></span>
* <span data-ttu-id="0e611-1348">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="0e611-1348">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0e611-1349">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0e611-1349">Updated cmdlet:</span></span>
        - <span data-ttu-id="0e611-1350">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-1350">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0e611-1351">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0e611-1351">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1352">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1352">Az.Resources</span></span>
* <span data-ttu-id="0e611-1353">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="0e611-1353">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1354">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1354">Az.Sql</span></span>
* <span data-ttu-id="0e611-1355">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="0e611-1355">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0e611-1356">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1356">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1357">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1357">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1358">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="0e611-1358">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-1359">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1359">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-1360">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="0e611-1360">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0e611-1361">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="0e611-1361">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1362">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1362">Az.Compute</span></span>
* <span data-ttu-id="0e611-1363">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="0e611-1363">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0e611-1364">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1364">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0e611-1365">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1365">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0e611-1366">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="0e611-1366">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0e611-1367">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0e611-1367">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0e611-1368">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-1368">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="0e611-1369">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0e611-1369">Breaking changes</span></span>
    - <span data-ttu-id="0e611-1370">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0e611-1370">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0e611-1371">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0e611-1371">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0e611-1372">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0e611-1372">Az.DeploymentManager</span></span>
* <span data-ttu-id="0e611-1373">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="0e611-1373">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0e611-1374">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0e611-1374">Az.Dns</span></span>
* <span data-ttu-id="0e611-1375">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="0e611-1375">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0e611-1376">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="0e611-1376">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0e611-1377">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="0e611-1377">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0e611-1378">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-1378">Az.FrontDoor</span></span>
* <span data-ttu-id="0e611-1379">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1379">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0e611-1380">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="0e611-1380">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0e611-1381">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-1381">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-1382">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-1382">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0e611-1383">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e611-1383">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0e611-1384">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e611-1384">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0e611-1385">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0e611-1385">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0e611-1386">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="0e611-1386">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0e611-1387">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="0e611-1387">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0e611-1388">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1388">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-1389">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-1389">Az.Monitor</span></span>
* <span data-ttu-id="0e611-1390">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="0e611-1390">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="0e611-1391">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0e611-1391">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0e611-1392">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1392">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0e611-1393">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0e611-1393">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0e611-1394">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0e611-1394">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0e611-1395">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0e611-1395">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0e611-1396">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0e611-1396">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0e611-1397">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1397">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e611-1398">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1398">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e611-1399">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1399">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e611-1400">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1400">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e611-1401">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1401">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0e611-1402">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="0e611-1402">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0e611-1403">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="0e611-1403">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1404">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1404">Az.Network</span></span>
* <span data-ttu-id="0e611-1405">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="0e611-1405">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0e611-1406">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-1406">New cmdlets</span></span>
        - <span data-ttu-id="0e611-1407">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1407">New-AzNatGateway</span></span>
        - <span data-ttu-id="0e611-1408">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1408">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0e611-1409">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1409">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0e611-1410">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1410">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0e611-1411">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0e611-1411">Updated cmdlets</span></span>
        - <span data-ttu-id="0e611-1412">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0e611-1412">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0e611-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0e611-1413">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0e611-1414">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1414">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0e611-1415">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1415">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0e611-1416">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0e611-1416">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e611-1417">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1417">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e611-1418">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0e611-1418">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0e611-1419">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0e611-1419">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0e611-1420">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="0e611-1420">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1421">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1421">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1422">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0e611-1422">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0e611-1423">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0e611-1423">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0e611-1424">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0e611-1424">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0e611-1425">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1425">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0e611-1426">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="0e611-1426">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0e611-1427">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="0e611-1427">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0e611-1428">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0e611-1428">Az.Relay</span></span>
* <span data-ttu-id="0e611-1429">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="0e611-1429">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-1430">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-1430">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-1431">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e611-1431">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1432">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1432">Az.Storage</span></span>
* <span data-ttu-id="0e611-1433">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="0e611-1433">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0e611-1434">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="0e611-1434">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0e611-1435">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="0e611-1435">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0e611-1436">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1436">New-AzStorageAccount</span></span>
* <span data-ttu-id="0e611-1437">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="0e611-1437">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0e611-1438">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1438">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0e611-1439">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1439">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0e611-1440">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1440">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1441">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1441">Az.Websites</span></span>
* <span data-ttu-id="0e611-1442">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1442">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0e611-1443">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="0e611-1443">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0e611-1444">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1444">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-1445">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-1445">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-1446">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0e611-1446">General availability of `Az` module</span></span>
* <span data-ttu-id="0e611-1447">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e611-1447">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e611-1448">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e611-1448">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e611-1449">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1449">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e611-1450">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e611-1450">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e611-1451">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1451">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e611-1452">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0e611-1452">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-1453">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1453">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1454">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="0e611-1454">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0e611-1455">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-1455">Az.Batch</span></span>
* <span data-ttu-id="0e611-1456">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-1457">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-1457">Az.Cdn</span></span>
* <span data-ttu-id="0e611-1458">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1458">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-1459">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1459">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-1460">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1460">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1461">Az.Compute</span></span>
* <span data-ttu-id="0e611-1462">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="0e611-1462">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0e611-1463">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1463">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1464">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0e611-1464">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-1465">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-1465">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-1466">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="0e611-1466">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-1468">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1468">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e611-1469">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e611-1469">Az.EventGrid</span></span>
* <span data-ttu-id="0e611-1470">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0e611-1470">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-1471">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1471">Az.EventHub</span></span>
* <span data-ttu-id="0e611-1472">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0e611-1472">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="0e611-1473">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0e611-1473">Az.HDInsight</span></span>
* <span data-ttu-id="0e611-1474">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1474">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-1475">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1475">Az.IotHub</span></span>
* <span data-ttu-id="0e611-1476">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1476">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-1477">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1477">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-1478">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1478">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1479">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0e611-1479">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0e611-1480">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0e611-1480">Az.MachineLearning</span></span>
* <span data-ttu-id="0e611-1481">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1481">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0e611-1482">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0e611-1482">Az.Media</span></span>
* <span data-ttu-id="0e611-1483">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1483">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-1484">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-1484">Az.Monitor</span></span>
  * <span data-ttu-id="0e611-1485">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="0e611-1485">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0e611-1486">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0e611-1486">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0e611-1487">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0e611-1487">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0e611-1488">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e611-1488">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0e611-1489">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e611-1489">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0e611-1490">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0e611-1490">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0e611-1491">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="0e611-1491">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1492">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1492">Az.Network</span></span>
* <span data-ttu-id="0e611-1493">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1494">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0e611-1494">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0e611-1495">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0e611-1495">Az.NotificationHubs</span></span>
* <span data-ttu-id="0e611-1496">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1496">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1497">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1497">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-1498">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1498">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0e611-1499">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0e611-1499">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0e611-1500">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1500">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1501">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1501">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1502">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1502">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1503">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1503">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0e611-1504">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0e611-1504">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0e611-1505">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="0e611-1505">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e611-1506">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e611-1506">Az.RedisCache</span></span>
* <span data-ttu-id="0e611-1507">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1507">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1508">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1508">Az.Resources</span></span>
* <span data-ttu-id="0e611-1509">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0e611-1509">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1510">Az.Sql</span></span>
* <span data-ttu-id="0e611-1511">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="0e611-1511">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0e611-1512">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1512">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1513">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="0e611-1513">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0e611-1514">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0e611-1514">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0e611-1515">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="0e611-1515">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0e611-1516">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0e611-1516">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0e611-1517">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0e611-1517">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1518">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1518">Az.Websites</span></span>
* <span data-ttu-id="0e611-1519">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="0e611-1519">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0e611-1520">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0e611-1520">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0e611-1521">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="0e611-1521">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0e611-1522">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0e611-1522">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0e611-1523">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1523">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-1524">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-1524">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-1525">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0e611-1525">General availability of `Az` module</span></span>
* <span data-ttu-id="0e611-1526">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e611-1526">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e611-1527">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e611-1527">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e611-1528">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1528">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e611-1529">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e611-1529">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e611-1530">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1530">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e611-1531">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0e611-1531">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0e611-1532">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1532">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1533">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0e611-1533">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e611-1534">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1534">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e611-1535">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="0e611-1535">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0e611-1536">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0e611-1536">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1537">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1537">Az.Automation</span></span>
* <span data-ttu-id="0e611-1538">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="0e611-1538">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0e611-1539">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="0e611-1539">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0e611-1540">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1540">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1541">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1541">Az.Compute</span></span>
* <span data-ttu-id="0e611-1542">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1542">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0e611-1543">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="0e611-1543">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="0e611-1544">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1544">Az.ContainerInstance</span></span>
* <span data-ttu-id="0e611-1545">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="0e611-1545">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-1546">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-1546">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-1547">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="0e611-1547">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0e611-1548">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0e611-1548">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1549">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1549">Az.Resources</span></span>
* <span data-ttu-id="0e611-1550">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="0e611-1550">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0e611-1551">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0e611-1551">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0e611-1552">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="0e611-1552">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0e611-1553">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0e611-1553">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0e611-1554">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="0e611-1554">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0e611-1555">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0e611-1555">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1556">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1556">Az.Sql</span></span>
* <span data-ttu-id="0e611-1557">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="0e611-1557">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1558">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1558">Az.Storage</span></span>
* <span data-ttu-id="0e611-1559">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="0e611-1559">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0e611-1560">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e611-1560">New-AzStorageContext</span></span>
* <span data-ttu-id="0e611-1561">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="0e611-1561">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0e611-1562">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0e611-1562">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0e611-1563">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0e611-1563">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0e611-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1564">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0e611-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1565">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0e611-1566">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="0e611-1566">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0e611-1567">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e611-1567">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0e611-1568">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0e611-1568">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0e611-1569">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e611-1569">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0e611-1570">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0e611-1570">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0e611-1571">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1571">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0e611-1572">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0e611-1572">Highlights since the last major release</span></span>
* <span data-ttu-id="0e611-1573">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0e611-1573">General availability of `Az` module</span></span>
* <span data-ttu-id="0e611-1574">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0e611-1574">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0e611-1575">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0e611-1575">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0e611-1576">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1576">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0e611-1577">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e611-1577">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e611-1578">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1578">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0e611-1579">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0e611-1579">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1580">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1580">Az.Automation</span></span>
* <span data-ttu-id="0e611-1581">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e611-1581">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0e611-1582">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="0e611-1582">Dynamic grouping</span></span>
    * <span data-ttu-id="0e611-1583">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="0e611-1583">Pre-Post script</span></span>
    * <span data-ttu-id="0e611-1584">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="0e611-1584">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1585">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1585">Az.Compute</span></span>
* <span data-ttu-id="0e611-1586">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0e611-1586">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0e611-1587">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0e611-1587">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-1588">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1588">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-1589">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1589">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1590">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1590">Az.Network</span></span>
* <span data-ttu-id="0e611-1591">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1591">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0e611-1592">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="0e611-1592">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1593">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1593">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1594">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="0e611-1594">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0e611-1595">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="0e611-1595">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1596">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1596">Az.Resources</span></span>
* <span data-ttu-id="0e611-1597">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1597">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0e611-1598">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="0e611-1598">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1599">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1599">Az.Sql</span></span>
* <span data-ttu-id="0e611-1600">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="0e611-1600">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1601">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1601">Az.Storage</span></span>
* <span data-ttu-id="0e611-1602">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1602">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0e611-1603">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1603">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e611-1604">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1604">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e611-1605">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1605">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0e611-1606">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0e611-1606">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0e611-1607">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0e611-1607">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0e611-1608">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1608">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1609">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1609">Az.Websites</span></span>
* <span data-ttu-id="0e611-1610">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="0e611-1610">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="0e611-1611">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1611">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1612">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1612">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1613">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="0e611-1613">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0e611-1614">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1614">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1615">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1615">Az.Automation</span></span>
* <span data-ttu-id="0e611-1616">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1616">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0e611-1617">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="0e611-1617">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0e611-1618">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="0e611-1618">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-1619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-1619">Az.Cdn</span></span>
* <span data-ttu-id="0e611-1620">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="0e611-1620">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1621">Az.Compute</span></span>
* <span data-ttu-id="0e611-1622">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="0e611-1622">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-1623">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-1623">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-1624">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="0e611-1624">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e611-1625">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1625">Az.LogicApp</span></span>
* <span data-ttu-id="0e611-1626">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="0e611-1626">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1627">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1627">Az.Network</span></span>
* <span data-ttu-id="0e611-1628">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1628">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1629">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1629">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1630">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-1630">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0e611-1631">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="0e611-1631">SDK Update</span></span>
* <span data-ttu-id="0e611-1632">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e611-1632">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0e611-1633">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e611-1633">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1634">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1634">Az.Resources</span></span>
* <span data-ttu-id="0e611-1635">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="0e611-1635">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0e611-1636">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0e611-1636">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0e611-1637">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0e611-1637">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0e611-1638">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0e611-1638">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0e611-1639">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0e611-1639">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0e611-1640">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0e611-1640">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1641">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1641">Az.Sql</span></span>
* <span data-ttu-id="0e611-1642">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0e611-1642">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0e611-1643">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0e611-1643">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1644">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1644">Az.Storage</span></span>
* <span data-ttu-id="0e611-1645">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1645">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0e611-1646">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1646">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0e611-1647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1647">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e611-1648">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="0e611-1648">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1649">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1649">Az.Automation</span></span>
* <span data-ttu-id="0e611-1650">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1650">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0e611-1651">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1651">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0e611-1652">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1652">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-1653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1653">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-1654">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0e611-1654">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1655">Az.Compute</span></span>
* <span data-ttu-id="0e611-1656">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="0e611-1656">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0e611-1657">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="0e611-1657">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0e611-1658">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0e611-1658">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0e611-1659">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0e611-1659">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1660">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1660">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-1661">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="0e611-1661">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0e611-1662">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1662">Az.EventHub</span></span>
* <span data-ttu-id="0e611-1663">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="0e611-1663">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-1664">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1664">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-1665">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e611-1665">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e611-1666">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1666">Az.LogicApp</span></span>
* <span data-ttu-id="0e611-1667">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1667">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0e611-1668">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="0e611-1668">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0e611-1669">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1669">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0e611-1670">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e611-1670">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e611-1671">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e611-1671">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e611-1672">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e611-1672">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0e611-1673">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0e611-1673">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0e611-1674">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1674">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0e611-1675">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1675">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e611-1676">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1676">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e611-1677">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1677">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0e611-1678">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1678">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0e611-1679">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0e611-1679">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0e611-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-1680">Az.Monitor</span></span>
* <span data-ttu-id="0e611-1681">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0e611-1681">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1682">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1682">Az.Network</span></span>
* <span data-ttu-id="0e611-1683">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0e611-1683">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1684">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1684">Az.OperationalInsights</span></span>
* <span data-ttu-id="0e611-1685">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="0e611-1685">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0e611-1686">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0e611-1686">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="0e611-1687">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="0e611-1687">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="0e611-1688">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1688">Az.Resources</span></span>
* <span data-ttu-id="0e611-1689">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0e611-1689">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0e611-1690">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0e611-1690">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0e611-1691">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0e611-1691">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0e611-1692">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0e611-1692">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1693">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1693">Az.Sql</span></span>
* <span data-ttu-id="0e611-1694">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="0e611-1694">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0e611-1695">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="0e611-1695">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1696">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1696">Az.Websites</span></span>
* <span data-ttu-id="0e611-1697">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0e611-1697">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0e611-1698">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1698">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1699">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1700">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0e611-1700">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e611-1701">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1701">Az.AnalysisServices</span></span>
<span data-ttu-id="0e611-1702">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0e611-1702">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1703">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1703">Az.Compute</span></span>
* <span data-ttu-id="0e611-1704">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="0e611-1704">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0e611-1705">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0e611-1705">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0e611-1706">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0e611-1706">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1707">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1707">Az.RecoveryServices</span></span>
<span data-ttu-id="0e611-1708">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0e611-1708">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1709">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1709">Az.Resources</span></span>
* <span data-ttu-id="0e611-1710">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="0e611-1710">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="0e611-1711">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0e611-1711">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0e611-1712">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="0e611-1712">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="0e611-1713">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0e611-1713">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1714">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1714">Az.Sql</span></span>
* <span data-ttu-id="0e611-1715">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0e611-1715">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0e611-1716">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="0e611-1716">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0e611-1717">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="0e611-1717">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0e611-1718">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1718">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1719">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1719">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1720">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1720">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0e611-1721">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1721">Az.AnalysisServices</span></span>
* <span data-ttu-id="0e611-1722">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1722">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1723">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1723">Az.RecoveryServices</span></span>
* <span data-ttu-id="0e611-1724">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1724">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0e611-1725">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1725">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1726">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1726">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1727">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0e611-1727">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0e611-1728">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1728">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e611-1729">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0e611-1729">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0e611-1730">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0e611-1730">Az.Aks</span></span>
* <span data-ttu-id="0e611-1731">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1731">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0e611-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1732">Az.Automation</span></span>
* <span data-ttu-id="0e611-1733">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="0e611-1733">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0e611-1734">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1734">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0e611-1735">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0e611-1735">Az.Cdn</span></span>
* <span data-ttu-id="0e611-1736">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1736">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1737">Az.Compute</span></span>
* <span data-ttu-id="0e611-1738">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0e611-1738">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0e611-1739">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0e611-1739">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0e611-1740">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0e611-1740">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0e611-1741">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0e611-1741">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0e611-1742">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1742">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0e611-1743">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e611-1743">Az.DataFactory</span></span>
* <span data-ttu-id="0e611-1744">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="0e611-1744">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1745">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1745">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-1746">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0e611-1746">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0e611-1747">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0e611-1747">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0e611-1748">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1748">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-1749">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1749">Az.IotHub</span></span>
* <span data-ttu-id="0e611-1750">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0e611-1750">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0e611-1751">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1751">Az.KeyVault</span></span>
* <span data-ttu-id="0e611-1752">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1752">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-1753">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1753">Az.Network</span></span>
* <span data-ttu-id="0e611-1754">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1754">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1755">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1755">Az.Resources</span></span>
* <span data-ttu-id="0e611-1756">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="0e611-1756">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0e611-1757">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0e611-1757">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0e611-1758">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="0e611-1758">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0e611-1759">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0e611-1759">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0e611-1760">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0e611-1760">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0e611-1761">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="0e611-1761">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0e611-1762">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0e611-1762">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-1763">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1763">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-1764">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0e611-1764">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0e611-1765">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="0e611-1765">Fix some error messages.</span></span>
* <span data-ttu-id="0e611-1766">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="0e611-1766">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0e611-1767">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1767">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0e611-1768">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0e611-1768">Az.SignalR</span></span>
* <span data-ttu-id="0e611-1769">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1769">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1770">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1770">Az.Sql</span></span>
* <span data-ttu-id="0e611-1771">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1771">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e611-1772">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="0e611-1772">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0e611-1773">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="0e611-1773">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0e611-1774">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="0e611-1774">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1775">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1775">Az.Storage</span></span>
* <span data-ttu-id="0e611-1776">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1776">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e611-1777">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="0e611-1777">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0e611-1778">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0e611-1778">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0e611-1779">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0e611-1779">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0e611-1780">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0e611-1780">Az.TrafficManager</span></span>
* <span data-ttu-id="0e611-1781">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1781">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1782">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1782">Az.Websites</span></span>
* <span data-ttu-id="0e611-1783">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0e611-1783">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0e611-1784">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1784">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0e611-1785">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="0e611-1785">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0e611-1786">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0e611-1786">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0e611-1787">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1787">Az.Accounts</span></span>
* <span data-ttu-id="0e611-1788">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0e611-1788">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-1789">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1789">Az.Compute</span></span>
* <span data-ttu-id="0e611-1790">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0e611-1790">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0e611-1791">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0e611-1791">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0e611-1792">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1792">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1793">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-1794">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="0e611-1794">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0e611-1795">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="0e611-1795">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0e611-1796">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0e611-1796">Az.EventGrid</span></span>
* <span data-ttu-id="0e611-1797">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0e611-1797">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0e611-1798">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0e611-1798">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0e611-1799">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0e611-1799">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0e611-1800">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0e611-1800">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0e611-1801">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0e611-1801">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0e611-1802">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0e611-1802">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0e611-1803">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0e611-1803">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0e611-1804">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0e611-1804">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0e611-1805">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0e611-1805">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0e611-1806">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0e611-1806">Dead letter endpoint.</span></span>
* <span data-ttu-id="0e611-1807">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0e611-1807">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0e611-1808">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0e611-1808">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0e611-1809">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1809">Az.IotHub</span></span>
* <span data-ttu-id="0e611-1810">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="0e611-1810">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0e611-1811">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0e611-1811">Az.LogicApp</span></span>
* <span data-ttu-id="0e611-1812">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="0e611-1812">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-1813">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1813">Az.Resources</span></span>
* <span data-ttu-id="0e611-1814">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0e611-1814">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0e611-1815">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0e611-1815">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0e611-1816">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0e611-1816">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0e611-1817">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0e611-1817">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0e611-1818">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="0e611-1818">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0e611-1819">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0e611-1819">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0e611-1820">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0e611-1820">Az.SignalR</span></span>
* <span data-ttu-id="0e611-1821">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1821">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-1822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1822">Az.Sql</span></span>
* <span data-ttu-id="0e611-1823">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="0e611-1823">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0e611-1824">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1824">Az.Storage</span></span>
* <span data-ttu-id="0e611-1825">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="0e611-1825">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0e611-1826">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0e611-1826">New-AzStorageContext</span></span>
* <span data-ttu-id="0e611-1827">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="0e611-1827">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0e611-1828">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0e611-1828">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-1829">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1829">Az.Websites</span></span>
* <span data-ttu-id="0e611-1830">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="0e611-1830">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0e611-1831">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1831">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0e611-1832">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-1832">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0e611-1833">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-1833">General</span></span>

- <span data-ttu-id="0e611-1834">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="0e611-1834">General Availability of Az Module</span></span>
- <span data-ttu-id="0e611-1835">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="0e611-1835">Online help for each module</span></span>
- <span data-ttu-id="0e611-1836">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0e611-1836">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0e611-1837">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="0e611-1837">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0e611-1838">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1838">Az.Accounts</span></span>
- <span data-ttu-id="0e611-1839">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e611-1839">Changed from Az.Profile</span></span>
- <span data-ttu-id="0e611-1840">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="0e611-1840">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0e611-1841">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1841">Az.ApiManagement</span></span>
- <span data-ttu-id="0e611-1842">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="0e611-1842">Fixes for #7002</span></span>
- <span data-ttu-id="0e611-1843">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1843">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0e611-1844">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0e611-1844">Az.Batch</span></span>
- <span data-ttu-id="0e611-1845">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0e611-1845">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0e611-1846">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="0e611-1846">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0e611-1847">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1847">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0e611-1848">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0e611-1848">Az.Billing</span></span>
- <span data-ttu-id="0e611-1849">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1849">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0e611-1850">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1850">Az.CognitivServices</span></span>
- <span data-ttu-id="0e611-1851">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1851">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0e611-1852">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="0e611-1852">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0e611-1853">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1853">Az.ContainerInstance</span></span>
- <span data-ttu-id="0e611-1854">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0e611-1854">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0e611-1855">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0e611-1855">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0e611-1856">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1856">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1857">Az.DataLakeStore</span></span>
- <span data-ttu-id="0e611-1858">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1858">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0e611-1859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0e611-1859">Az.Monitor</span></span>
- <span data-ttu-id="0e611-1860">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1860">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0e611-1861">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0e611-1861">Az.KeyVault</span></span>
- <span data-ttu-id="0e611-1862">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="0e611-1862">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0e611-1863">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0e611-1863">Az.MachineLearning</span></span>
- <span data-ttu-id="0e611-1864">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0e611-1864">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0e611-1865">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0e611-1865">Az.Media</span></span>
- <span data-ttu-id="0e611-1866">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0e611-1866">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0e611-1867">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1867">Az.Network</span></span>
<span data-ttu-id="0e611-1868">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1868">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0e611-1869">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0e611-1869">New cmdlets added:</span></span>
        - <span data-ttu-id="0e611-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1870">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1871">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1872">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1873">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1874">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1875">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1875">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0e611-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1876">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0e611-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e611-1877">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0e611-1878">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e611-1878">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0e611-1879">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e611-1879">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0e611-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1880">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0e611-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0e611-1881">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0e611-1882">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1882">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0e611-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-1883">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0e611-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="0e611-1884">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0e611-1885">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0e611-1885">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0e611-1886">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e611-1886">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0e611-1887">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e611-1887">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0e611-1888">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0e611-1888">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0e611-1889">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0e611-1889">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0e611-1890">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1890">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0e611-1891">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-1891">Az.OperationalInsights</span></span>
- <span data-ttu-id="0e611-1892">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1892">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0e611-1893">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e611-1893">Az.Profile</span></span>
- <span data-ttu-id="0e611-1894">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0e611-1894">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1895">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1895">Az.RecoveryServices</span></span>
- <span data-ttu-id="0e611-1896">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1896">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0e611-1897">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1897">Az.Resources</span></span>
- <span data-ttu-id="0e611-1898">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1898">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0e611-1899">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1899">Az.ServiceFabric</span></span>
- <span data-ttu-id="0e611-1900">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="0e611-1900">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0e611-1901">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1901">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0e611-1902">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0e611-1902">Az.SIgnalR</span></span>
- <span data-ttu-id="0e611-1903">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0e611-1903">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0e611-1904">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1904">Az.Sql</span></span>
- <span data-ttu-id="0e611-1905">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="0e611-1905">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0e611-1906">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1906">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0e611-1907">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1907">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0e611-1908">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1908">Az.Storage</span></span>
- <span data-ttu-id="0e611-1909">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1909">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0e611-1910">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1910">Az.Websites</span></span>
- <span data-ttu-id="0e611-1911">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0e611-1911">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0e611-1912">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-1912">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0e611-1913">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-1913">General</span></span>

* <span data-ttu-id="0e611-1914">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0e611-1914">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0e611-1915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1915">Az.Compute</span></span>

* <span data-ttu-id="0e611-1916">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0e611-1916">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0e611-1917">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-1917">Az.DataLakeStore</span></span>

* <span data-ttu-id="0e611-1918">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="0e611-1918">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0e611-1919">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0e611-1919">Az.FrontDoor</span></span>

* <span data-ttu-id="0e611-1920">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="0e611-1920">Fixed some broken links</span></span>
    - <span data-ttu-id="0e611-1921">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0e611-1921">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0e611-1922">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0e611-1922">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0e611-1923">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0e611-1923">Az.RecoveryServices</span></span>

* <span data-ttu-id="0e611-1924">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1924">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0e611-1925">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="0e611-1925">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0e611-1926">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1926">Az.Resources</span></span>

* <span data-ttu-id="0e611-1927">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0e611-1927">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0e611-1928">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="0e611-1928">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0e611-1929">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1929">Az.Sql</span></span>

* <span data-ttu-id="0e611-1930">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0e611-1930">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0e611-1931">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="0e611-1931">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0e611-1932">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="0e611-1932">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0e611-1933">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-1933">Az.Storage</span></span>

* <span data-ttu-id="0e611-1934">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-1934">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0e611-1935">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="0e611-1935">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0e611-1936">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-1936">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0e611-1937">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="0e611-1937">Support Static Website configuration</span></span>
    - <span data-ttu-id="0e611-1938">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0e611-1938">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0e611-1939">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0e611-1939">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0e611-1940">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-1940">Az.Websites</span></span>

* <span data-ttu-id="0e611-1941">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0e611-1941">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="0e611-1942">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0e611-1942">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0e611-1943">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e611-1943">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0e611-1944">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-1944">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0e611-1945">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0e611-1945">Az.ApiManagement</span></span>
* <span data-ttu-id="0e611-1946">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e611-1946">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0e611-1947">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0e611-1947">Az.Automation</span></span>
* <span data-ttu-id="0e611-1948">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="0e611-1948">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0e611-1949">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="0e611-1949">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0e611-1950">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="0e611-1950">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0e611-1951">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="0e611-1951">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0e611-1952">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="0e611-1952">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0e611-1953">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-1953">Az.Compute</span></span>
* <span data-ttu-id="0e611-1954">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0e611-1954">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0e611-1955">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e611-1955">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0e611-1956">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1956">Az.ContainerInstance</span></span>
* <span data-ttu-id="0e611-1957">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e611-1957">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0e611-1958">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0e611-1958">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0e611-1959">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="0e611-1959">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0e611-1960">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-1960">Az.Network</span></span>
* <span data-ttu-id="0e611-1961">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0e611-1961">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0e611-1962">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="0e611-1962">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0e611-1963">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0e611-1963">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="0e611-1964">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0e611-1964">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0e611-1965">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0e611-1965">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0e611-1966">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="0e611-1966">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0e611-1967">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="0e611-1967">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0e611-1968">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0e611-1968">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0e611-1969">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0e611-1969">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0e611-1970">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0e611-1970">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0e611-1971">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0e611-1971">Az.Relay</span></span>
* <span data-ttu-id="0e611-1972">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0e611-1972">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0e611-1973">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-1973">Az.Resources</span></span>
* <span data-ttu-id="0e611-1974">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="0e611-1974">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0e611-1975">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="0e611-1975">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0e611-1976">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0e611-1976">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0e611-1977">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-1977">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-1978">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0e611-1978">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0e611-1979">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-1979">Az.Sql</span></span>
* <span data-ttu-id="0e611-1980">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="0e611-1980">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0e611-1981">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1981">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e611-1982">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1982">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e611-1983">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1983">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e611-1984">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0e611-1984">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0e611-1985">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e611-1985">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e611-1986">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e611-1986">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e611-1987">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e611-1987">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0e611-1988">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0e611-1988">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0e611-1989">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="0e611-1989">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0e611-1990">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="0e611-1990">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0e611-1991">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="0e611-1991">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0e611-1992">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e611-1992">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0e611-1993">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e611-1993">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0e611-1994">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e611-1994">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0e611-1995">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0e611-1995">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0e611-1996">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e611-1996">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0e611-1997">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-1997">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0e611-1998">Generale</span><span class="sxs-lookup"><span data-stu-id="0e611-1998">General</span></span>
* <span data-ttu-id="0e611-1999">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="0e611-1999">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0e611-2000">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e611-2000">Az.Profile</span></span>
* <span data-ttu-id="0e611-2001">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0e611-2001">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0e611-2002">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="0e611-2002">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0e611-2003">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0e611-2003">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0e611-2004">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="0e611-2004">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0e611-2005">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="0e611-2005">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0e611-2006">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0e611-2006">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0e611-2007">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="0e611-2007">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-2008">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-2008">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-2009">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0e611-2009">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-2010">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-2010">Az.Compute</span></span>
* <span data-ttu-id="0e611-2011">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0e611-2011">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0e611-2012">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0e611-2012">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0e611-2013">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="0e611-2013">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-2014">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-2014">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-2015">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0e611-2015">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0e611-2016">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="0e611-2016">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0e611-2017">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0e611-2017">Az.Insights</span></span>
* <span data-ttu-id="0e611-2018">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="0e611-2018">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0e611-2019">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="0e611-2019">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0e611-2020">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="0e611-2020">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0e611-2021">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="0e611-2021">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-2022">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-2022">Az.Network</span></span>
* <span data-ttu-id="0e611-2023">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0e611-2023">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0e611-2024">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-2024">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0e611-2025">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0e611-2025">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0e611-2026">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0e611-2026">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0e611-2027">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0e611-2027">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0e611-2028">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0e611-2028">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0e611-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0e611-2029">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0e611-2030">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0e611-2030">Az.PolicyInsights</span></span>
* <span data-ttu-id="0e611-2031">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="0e611-2031">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-2032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-2032">Az.Resources</span></span>
* <span data-ttu-id="0e611-2033">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0e611-2033">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0e611-2034">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0e611-2034">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0e611-2035">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0e611-2035">Az.ServiceBus</span></span>
* <span data-ttu-id="0e611-2036">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="0e611-2036">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0e611-2037">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0e611-2037">Az.ServiceFabric</span></span>
* <span data-ttu-id="0e611-2038">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="0e611-2038">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0e611-2039">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="0e611-2039">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0e611-2040">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0e611-2040">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0e611-2041">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0e611-2041">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0e611-2042">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0e611-2042">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0e611-2043">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-2043">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0e611-2044">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0e611-2044">Az.Profile</span></span>
* <span data-ttu-id="0e611-2045">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="0e611-2045">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0e611-2046">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0e611-2046">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-2047">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-2047">Az.Compute</span></span>
* <span data-ttu-id="0e611-2048">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="0e611-2048">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0e611-2049">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e611-2049">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0e611-2050">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0e611-2050">Az.DataLakeStore</span></span>
* <span data-ttu-id="0e611-2051">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0e611-2051">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0e611-2052">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e611-2052">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0e611-2053">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0e611-2053">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0e611-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0e611-2054">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0e611-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0e611-2055">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-2056">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-2056">Az.Network</span></span>
* <span data-ttu-id="0e611-2057">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="0e611-2057">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0e611-2058">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e611-2058">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-2059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-2059">Az.Resources</span></span>
* <span data-ttu-id="0e611-2060">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="0e611-2060">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0e611-2061">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="0e611-2061">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0e611-2062">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-2062">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0e611-2063">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0e611-2063">Azure.Storage</span></span>
* <span data-ttu-id="0e611-2064">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="0e611-2064">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0e611-2065">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-2065">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0e611-2066">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0e611-2066">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0e611-2067">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="0e611-2067">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0e611-2068">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0e611-2068">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="0e611-2069">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0e611-2069">Az.CognitiveServices</span></span>
* <span data-ttu-id="0e611-2070">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="0e611-2070">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0e611-2071">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0e611-2071">Az.Compute</span></span>
* <span data-ttu-id="0e611-2072">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="0e611-2072">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0e611-2073">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0e611-2073">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0e611-2074">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="0e611-2074">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0e611-2075">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0e611-2075">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0e611-2076">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="0e611-2076">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0e611-2077">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0e611-2077">Az.Network</span></span>
* <span data-ttu-id="0e611-2078">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-2078">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0e611-2079">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e611-2079">new cmdlets added</span></span>
    - <span data-ttu-id="0e611-2080">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-2080">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e611-2081">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-2081">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e611-2082">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-2082">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e611-2083">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0e611-2083">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0e611-2084">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-2084">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0e611-2085">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-2085">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0e611-2086">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="0e611-2086">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0e611-2087">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0e611-2087">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0e611-2088">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0e611-2088">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0e611-2089">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0e611-2089">Az.RedisCache</span></span>
* <span data-ttu-id="0e611-2090">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="0e611-2090">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0e611-2091">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="0e611-2091">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0e611-2092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0e611-2092">Az.Resources</span></span>
* <span data-ttu-id="0e611-2093">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0e611-2093">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0e611-2094">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="0e611-2094">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0e611-2095">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0e611-2095">Az.Sql</span></span>
* <span data-ttu-id="0e611-2096">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="0e611-2096">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0e611-2097">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0e611-2097">Az.Websites</span></span>
* <span data-ttu-id="0e611-2098">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="0e611-2098">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0e611-2099">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="0e611-2099">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0e611-2100">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="0e611-2100">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0e611-2101">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="0e611-2101">Initial Release</span></span>
