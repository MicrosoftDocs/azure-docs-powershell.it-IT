---
ms.openlocfilehash: 911e1f7ff56feab2735f397a0128aab4aa7757c7
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498676"
---
## <a name="220---june-2019"></a><span data-ttu-id="a90d0-101">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-101">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="a90d0-102">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a90d0-102">Az.Cdn</span></span>
* <span data-ttu-id="a90d0-103">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="a90d0-103">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-104">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-104">Az.Compute</span></span>
* <span data-ttu-id="a90d0-105">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-105">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="a90d0-106">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="a90d0-106">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a90d0-107">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-107">Az.EventHub</span></span>
* <span data-ttu-id="a90d0-108">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="a90d0-108">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="a90d0-109">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90d0-109">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-110">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-110">Az.Network</span></span>
* <span data-ttu-id="a90d0-111">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="a90d0-111">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="a90d0-112">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="a90d0-112">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a90d0-113">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-113">Az.PolicyInsights</span></span>
* <span data-ttu-id="a90d0-114">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="a90d0-114">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-115">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-115">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-116">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="a90d0-116">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a90d0-117">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90d0-117">Az.ServiceBus</span></span>
* <span data-ttu-id="a90d0-118">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a90d0-118">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a90d0-119">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-119">Az.ServiceFabric</span></span>
* <span data-ttu-id="a90d0-120">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="a90d0-120">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="a90d0-121">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-121">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-122">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-122">Az.Sql</span></span>
* <span data-ttu-id="a90d0-123">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="a90d0-123">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="a90d0-124">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-124">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="a90d0-125">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a90d0-125">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="a90d0-126">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="a90d0-126">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-127">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-127">Az.Websites</span></span>
* <span data-ttu-id="a90d0-128">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="a90d0-128">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="a90d0-129">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-129">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="a90d0-130">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90d0-130">Az.ApiManagement</span></span>
* <span data-ttu-id="a90d0-131">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="a90d0-131">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="a90d0-132">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-132">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="a90d0-133">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-133">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="a90d0-134">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="a90d0-134">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="a90d0-135">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="a90d0-135">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="a90d0-136">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="a90d0-136">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="a90d0-137">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-137">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="a90d0-138">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-138">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="a90d0-139">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90d0-139">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="a90d0-140">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="a90d0-140">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="a90d0-141">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-141">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="a90d0-142">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="a90d0-142">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="a90d0-143">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="a90d0-143">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="a90d0-144">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-144">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="a90d0-145">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-145">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="a90d0-146">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-146">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="a90d0-147">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-147">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="a90d0-148">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="a90d0-148">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="a90d0-149">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="a90d0-149">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="a90d0-150">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-150">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="a90d0-151">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="a90d0-151">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="a90d0-152">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a90d0-152">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="a90d0-153">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="a90d0-153">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="a90d0-154">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90d0-154">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="a90d0-155">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="a90d0-155">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="a90d0-156">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="a90d0-156">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="a90d0-157">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-157">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="a90d0-158">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a90d0-158">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="a90d0-159">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a90d0-159">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="a90d0-160">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="a90d0-160">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="a90d0-161">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="a90d0-161">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="a90d0-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="a90d0-162">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="a90d0-163">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a90d0-163">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="a90d0-164">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a90d0-164">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a90d0-165">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="a90d0-165">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="a90d0-166">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="a90d0-166">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="a90d0-167">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="a90d0-167">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="a90d0-168">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="a90d0-168">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="a90d0-169">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="a90d0-169">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="a90d0-170">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a90d0-170">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="a90d0-171">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-171">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a90d0-172">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a90d0-172">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="a90d0-173">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-173">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="a90d0-174">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="a90d0-174">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a90d0-175">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="a90d0-175">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="a90d0-176">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-176">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="a90d0-177">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a90d0-177">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="a90d0-178">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="a90d0-178">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="a90d0-179">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="a90d0-179">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="a90d0-180">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-180">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="a90d0-181">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="a90d0-181">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="a90d0-182">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="a90d0-182">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="a90d0-183">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="a90d0-183">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="a90d0-184">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="a90d0-184">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="a90d0-185">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="a90d0-185">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="a90d0-186">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="a90d0-186">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="a90d0-187">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a90d0-187">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a90d0-188">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a90d0-188">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a90d0-189">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a90d0-189">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a90d0-190">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-190">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a90d0-191">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="a90d0-191">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="a90d0-192">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a90d0-192">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="a90d0-193">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="a90d0-193">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="a90d0-194">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-194">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="a90d0-195">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="a90d0-195">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="a90d0-196">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="a90d0-196">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="a90d0-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="a90d0-197">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="a90d0-198">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="a90d0-198">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="a90d0-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="a90d0-199">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="a90d0-200">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a90d0-200">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="a90d0-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="a90d0-201">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="a90d0-202">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="a90d0-202">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="a90d0-203">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="a90d0-203">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="a90d0-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-204">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="a90d0-205">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="a90d0-205">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="a90d0-206">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="a90d0-206">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="a90d0-207">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="a90d0-207">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-208">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-208">Az.Automation</span></span>
* <span data-ttu-id="a90d0-209">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="a90d0-209">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="a90d0-210">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="a90d0-210">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="a90d0-211">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="a90d0-211">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="a90d0-212">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="a90d0-212">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="a90d0-213">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="a90d0-213">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="a90d0-214">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="a90d0-214">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="a90d0-215">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a90d0-215">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-216">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-216">Az.Compute</span></span>
* <span data-ttu-id="a90d0-217">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="a90d0-217">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="a90d0-218">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="a90d0-218">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-219">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-219">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-220">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-220">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a90d0-221">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a90d0-221">Az.Monitor</span></span>
* <span data-ttu-id="a90d0-222">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="a90d0-222">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-223">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-223">Az.Network</span></span>
* <span data-ttu-id="a90d0-224">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="a90d0-224">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="a90d0-225">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="a90d0-225">Updated cmdlet:</span></span>
        - <span data-ttu-id="a90d0-226">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="a90d0-226">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="a90d0-227">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a90d0-227">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-228">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-228">Az.Resources</span></span>
* <span data-ttu-id="a90d0-229">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="a90d0-229">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-230">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-230">Az.Sql</span></span>
* <span data-ttu-id="a90d0-231">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="a90d0-231">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="a90d0-232">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-232">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-233">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-233">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-234">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="a90d0-234">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a90d0-235">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-235">Az.CognitiveServices</span></span>
* <span data-ttu-id="a90d0-236">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="a90d0-236">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="a90d0-237">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="a90d0-237">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-238">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-238">Az.Compute</span></span>
* <span data-ttu-id="a90d0-239">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="a90d0-239">Proximity placement group feature.</span></span>
    - <span data-ttu-id="a90d0-240">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="a90d0-240">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="a90d0-241">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-241">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="a90d0-242">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="a90d0-242">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="a90d0-243">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="a90d0-243">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="a90d0-244">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a90d0-244">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="a90d0-245">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="a90d0-245">Breaking changes</span></span>
    - <span data-ttu-id="a90d0-246">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="a90d0-246">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="a90d0-247">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="a90d0-247">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="a90d0-248">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="a90d0-248">Az.DeploymentManager</span></span>
* <span data-ttu-id="a90d0-249">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="a90d0-249">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="a90d0-250">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="a90d0-250">Az.Dns</span></span>
* <span data-ttu-id="a90d0-251">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="a90d0-251">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="a90d0-252">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="a90d0-252">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="a90d0-253">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="a90d0-253">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="a90d0-254">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a90d0-254">Az.FrontDoor</span></span>
* <span data-ttu-id="a90d0-255">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-255">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="a90d0-256">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="a90d0-256">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="a90d0-257">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a90d0-257">Az.HDInsight</span></span>
* <span data-ttu-id="a90d0-258">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a90d0-258">Removed two cmdlets:</span></span>
    - <span data-ttu-id="a90d0-259">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a90d0-259">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="a90d0-260">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a90d0-260">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a90d0-261">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a90d0-261">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="a90d0-262">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="a90d0-262">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="a90d0-263">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="a90d0-263">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="a90d0-264">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-264">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a90d0-265">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a90d0-265">Az.Monitor</span></span>
* <span data-ttu-id="a90d0-266">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="a90d0-266">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="a90d0-267">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="a90d0-267">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="a90d0-268">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a90d0-268">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="a90d0-269">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="a90d0-269">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="a90d0-270">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="a90d0-270">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="a90d0-271">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="a90d0-271">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="a90d0-272">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="a90d0-272">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="a90d0-273">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-273">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a90d0-274">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-274">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a90d0-275">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-275">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a90d0-276">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-276">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a90d0-277">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-277">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="a90d0-278">[Altre](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="a90d0-278">[More](https://docs.microsoft.com/en-us/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="a90d0-279">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="a90d0-279">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-280">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-280">Az.Network</span></span>
* <span data-ttu-id="a90d0-281">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="a90d0-281">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="a90d0-282">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a90d0-282">New cmdlets</span></span>
        - <span data-ttu-id="a90d0-283">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a90d0-283">New-AzNatGateway</span></span>
        - <span data-ttu-id="a90d0-284">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a90d0-284">Get-AzNatGateway</span></span>
        - <span data-ttu-id="a90d0-285">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a90d0-285">Set-AzNatGateway</span></span>
        - <span data-ttu-id="a90d0-286">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="a90d0-286">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="a90d0-287">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="a90d0-287">Updated cmdlets</span></span>
        - <span data-ttu-id="a90d0-288">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a90d0-288">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="a90d0-289">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="a90d0-289">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="a90d0-290">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="a90d0-290">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="a90d0-291">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a90d0-291">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="a90d0-292">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="a90d0-292">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a90d0-293">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-293">Az.PolicyInsights</span></span>
* <span data-ttu-id="a90d0-294">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="a90d0-294">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="a90d0-295">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="a90d0-295">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="a90d0-296">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-296">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-297">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-297">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-298">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="a90d0-298">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="a90d0-299">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a90d0-299">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="a90d0-300">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a90d0-300">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="a90d0-301">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="a90d0-301">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="a90d0-302">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="a90d0-302">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="a90d0-303">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="a90d0-303">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="a90d0-304">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a90d0-304">Az.Relay</span></span>
* <span data-ttu-id="a90d0-305">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="a90d0-305">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a90d0-306">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90d0-306">Az.ServiceBus</span></span>
* <span data-ttu-id="a90d0-307">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a90d0-307">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-308">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-308">Az.Storage</span></span>
* <span data-ttu-id="a90d0-309">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="a90d0-309">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="a90d0-310">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="a90d0-310">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="a90d0-311">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="a90d0-311">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="a90d0-312">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-312">New-AzStorageAccount</span></span>
* <span data-ttu-id="a90d0-313">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="a90d0-313">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="a90d0-314">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-314">New-AzStorageAccount</span></span>
    - <span data-ttu-id="a90d0-315">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-315">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="a90d0-316">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-316">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-317">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-317">Az.Websites</span></span>
* <span data-ttu-id="a90d0-318">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a90d0-318">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="a90d0-319">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="a90d0-319">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="a90d0-320">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-320">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a90d0-321">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a90d0-321">Highlights since the last major release</span></span>
* <span data-ttu-id="a90d0-322">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a90d0-322">General availability of `Az` module</span></span>
* <span data-ttu-id="a90d0-323">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a90d0-323">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a90d0-324">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a90d0-324">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a90d0-325">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-325">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a90d0-326">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a90d0-326">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a90d0-327">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-327">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a90d0-328">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a90d0-328">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a90d0-329">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-329">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-330">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="a90d0-330">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="a90d0-331">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a90d0-331">Az.Batch</span></span>
* <span data-ttu-id="a90d0-332">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-332">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a90d0-333">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a90d0-333">Az.Cdn</span></span>
* <span data-ttu-id="a90d0-334">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-334">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a90d0-335">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-335">Az.CognitiveServices</span></span>
* <span data-ttu-id="a90d0-336">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-336">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-337">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-337">Az.Compute</span></span>
* <span data-ttu-id="a90d0-338">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="a90d0-338">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="a90d0-339">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-339">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-340">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a90d0-340">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a90d0-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a90d0-341">Az.DataFactory</span></span>
* <span data-ttu-id="a90d0-342">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="a90d0-342">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-344">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-344">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a90d0-345">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a90d0-345">Az.EventGrid</span></span>
* <span data-ttu-id="a90d0-346">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="a90d0-346">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a90d0-347">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-347">Az.EventHub</span></span>
* <span data-ttu-id="a90d0-348">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a90d0-348">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="a90d0-349">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="a90d0-349">Az.HDInsight</span></span>
* <span data-ttu-id="a90d0-350">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-350">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a90d0-351">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-351">Az.IotHub</span></span>
* <span data-ttu-id="a90d0-352">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-352">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a90d0-353">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-353">Az.KeyVault</span></span>
* <span data-ttu-id="a90d0-354">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-354">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-355">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a90d0-355">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="a90d0-356">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a90d0-356">Az.MachineLearning</span></span>
* <span data-ttu-id="a90d0-357">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-357">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="a90d0-358">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a90d0-358">Az.Media</span></span>
* <span data-ttu-id="a90d0-359">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-359">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a90d0-360">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a90d0-360">Az.Monitor</span></span>
  * <span data-ttu-id="a90d0-361">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="a90d0-361">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="a90d0-362">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="a90d0-362">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="a90d0-363">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="a90d0-363">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="a90d0-364">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a90d0-364">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a90d0-365">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a90d0-365">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="a90d0-366">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="a90d0-366">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="a90d0-367">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="a90d0-367">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-368">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-368">Az.Network</span></span>
* <span data-ttu-id="a90d0-369">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-369">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-370">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a90d0-370">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="a90d0-371">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="a90d0-371">Az.NotificationHubs</span></span>
* <span data-ttu-id="a90d0-372">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-372">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a90d0-373">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-373">Az.OperationalInsights</span></span>
* <span data-ttu-id="a90d0-374">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-374">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="a90d0-375">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="a90d0-375">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="a90d0-376">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-376">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-377">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-377">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-378">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-378">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-379">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-379">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="a90d0-380">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="a90d0-380">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="a90d0-381">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="a90d0-381">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a90d0-382">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a90d0-382">Az.RedisCache</span></span>
* <span data-ttu-id="a90d0-383">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-383">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-384">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-384">Az.Resources</span></span>
* <span data-ttu-id="a90d0-385">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a90d0-385">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-386">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-386">Az.Sql</span></span>
* <span data-ttu-id="a90d0-387">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="a90d0-387">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="a90d0-388">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-388">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-389">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="a90d0-389">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="a90d0-390">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a90d0-390">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="a90d0-391">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="a90d0-391">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="a90d0-392">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="a90d0-392">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="a90d0-393">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="a90d0-393">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-394">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-394">Az.Websites</span></span>
* <span data-ttu-id="a90d0-395">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="a90d0-395">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="a90d0-396">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="a90d0-396">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="a90d0-397">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="a90d0-397">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="a90d0-398">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="a90d0-398">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="a90d0-399">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-399">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a90d0-400">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a90d0-400">Highlights since the last major release</span></span>
* <span data-ttu-id="a90d0-401">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a90d0-401">General availability of `Az` module</span></span>
* <span data-ttu-id="a90d0-402">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a90d0-402">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a90d0-403">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a90d0-403">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a90d0-404">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-404">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a90d0-405">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a90d0-405">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a90d0-406">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-406">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a90d0-407">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a90d0-407">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="a90d0-408">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-408">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-409">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a90d0-409">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a90d0-410">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-410">Az.AnalysisServices</span></span>
* <span data-ttu-id="a90d0-411">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="a90d0-411">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="a90d0-412">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="a90d0-412">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-413">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-413">Az.Automation</span></span>
* <span data-ttu-id="a90d0-414">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="a90d0-414">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="a90d0-415">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="a90d0-415">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="a90d0-416">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-416">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-417">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-417">Az.Compute</span></span>
* <span data-ttu-id="a90d0-418">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-418">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="a90d0-419">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="a90d0-419">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="a90d0-420">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-420">Az.ContainerInstance</span></span>
* <span data-ttu-id="a90d0-421">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="a90d0-421">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a90d0-422">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a90d0-422">Az.DataFactory</span></span>
* <span data-ttu-id="a90d0-423">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="a90d0-423">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="a90d0-424">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a90d0-424">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-425">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-425">Az.Resources</span></span>
* <span data-ttu-id="a90d0-426">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="a90d0-426">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="a90d0-427">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="a90d0-427">Improve error handling for for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="a90d0-428">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="a90d0-428">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="a90d0-429">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a90d0-429">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="a90d0-430">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="a90d0-430">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="a90d0-431">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="a90d0-431">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-432">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-432">Az.Sql</span></span>
* <span data-ttu-id="a90d0-433">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="a90d0-433">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-434">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-434">Az.Storage</span></span>
* <span data-ttu-id="a90d0-435">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="a90d0-435">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="a90d0-436">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a90d0-436">New-AzStorageContext</span></span>
* <span data-ttu-id="a90d0-437">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="a90d0-437">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="a90d0-438">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a90d0-438">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a90d0-439">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a90d0-439">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="a90d0-440">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-440">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="a90d0-441">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-441">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="a90d0-442">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="a90d0-442">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="a90d0-443">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a90d0-443">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a90d0-444">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a90d0-444">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="a90d0-445">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a90d0-445">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="a90d0-446">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="a90d0-446">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="a90d0-447">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-447">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="a90d0-448">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="a90d0-448">Highlights since the last major release</span></span>
* <span data-ttu-id="a90d0-449">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="a90d0-449">General availability of `Az` module</span></span>
* <span data-ttu-id="a90d0-450">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="a90d0-450">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="a90d0-451">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="a90d0-451">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/en-us/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="a90d0-452">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-452">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="a90d0-453">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a90d0-453">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a90d0-454">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-454">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="a90d0-455">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="a90d0-455">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-456">Az.Automation</span></span>
* <span data-ttu-id="a90d0-457">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="a90d0-457">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="a90d0-458">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="a90d0-458">Dynamic grouping</span></span>
    * <span data-ttu-id="a90d0-459">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="a90d0-459">Pre-Post script</span></span>
    * <span data-ttu-id="a90d0-460">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="a90d0-460">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-461">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-461">Az.Compute</span></span>
* <span data-ttu-id="a90d0-462">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="a90d0-462">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="a90d0-463">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="a90d0-463">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a90d0-464">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-464">Az.KeyVault</span></span>
* <span data-ttu-id="a90d0-465">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-465">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-466">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-466">Az.Network</span></span>
* <span data-ttu-id="a90d0-467">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-467">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="a90d0-468">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="a90d0-468">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-469">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-469">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-470">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="a90d0-470">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="a90d0-471">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="a90d0-471">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-472">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-472">Az.Resources</span></span>
* <span data-ttu-id="a90d0-473">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a90d0-473">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="a90d0-474">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="a90d0-474">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-475">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-475">Az.Sql</span></span>
* <span data-ttu-id="a90d0-476">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="a90d0-476">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-477">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-477">Az.Storage</span></span>
* <span data-ttu-id="a90d0-478">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-478">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="a90d0-479">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-479">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a90d0-480">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-480">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a90d0-481">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-481">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="a90d0-482">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="a90d0-482">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="a90d0-483">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="a90d0-483">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="a90d0-484">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-484">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-485">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-485">Az.Websites</span></span>
* <span data-ttu-id="a90d0-486">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="a90d0-486">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="a90d0-487">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-487">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-488">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-488">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-489">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="a90d0-489">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="a90d0-490">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-490">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-491">Az.Automation</span></span>
* <span data-ttu-id="a90d0-492">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-492">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="a90d0-493">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="a90d0-493">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="a90d0-494">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="a90d0-494">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a90d0-495">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a90d0-495">Az.Cdn</span></span>
* <span data-ttu-id="a90d0-496">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="a90d0-496">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-497">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-497">Az.Compute</span></span>
* <span data-ttu-id="a90d0-498">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="a90d0-498">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a90d0-499">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a90d0-499">Az.DataFactory</span></span>
* <span data-ttu-id="a90d0-500">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="a90d0-500">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a90d0-501">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a90d0-501">Az.LogicApp</span></span>
* <span data-ttu-id="a90d0-502">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="a90d0-502">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-503">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-503">Az.Network</span></span>
* <span data-ttu-id="a90d0-504">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-504">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-505">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-505">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-506">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-506">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="a90d0-507">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="a90d0-507">SDK Update</span></span>
* <span data-ttu-id="a90d0-508">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a90d0-508">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="a90d0-509">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a90d0-509">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-510">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-510">Az.Resources</span></span>
* <span data-ttu-id="a90d0-511">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="a90d0-511">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="a90d0-512">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="a90d0-512">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="a90d0-513">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a90d0-513">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="a90d0-514">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="a90d0-514">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="a90d0-515">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="a90d0-515">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="a90d0-516">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="a90d0-516">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-517">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-517">Az.Sql</span></span>
* <span data-ttu-id="a90d0-518">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="a90d0-518">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="a90d0-519">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="a90d0-519">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-520">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-520">Az.Storage</span></span>
* <span data-ttu-id="a90d0-521">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-521">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="a90d0-522">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-522">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="a90d0-523">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-523">Az.AnalysisServices</span></span>
* <span data-ttu-id="a90d0-524">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="a90d0-524">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-525">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-525">Az.Automation</span></span>
* <span data-ttu-id="a90d0-526">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-526">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="a90d0-527">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-527">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="a90d0-528">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-528">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="a90d0-529">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-529">Az.CognitiveServices</span></span>
* <span data-ttu-id="a90d0-530">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a90d0-530">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-531">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-531">Az.Compute</span></span>
* <span data-ttu-id="a90d0-532">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="a90d0-532">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="a90d0-533">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="a90d0-533">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="a90d0-534">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a90d0-534">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="a90d0-535">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a90d0-535">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-536">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-536">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-537">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="a90d0-537">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="a90d0-538">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-538">Az.EventHub</span></span>
* <span data-ttu-id="a90d0-539">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="a90d0-539">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="a90d0-540">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-540">Az.KeyVault</span></span>
* <span data-ttu-id="a90d0-541">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a90d0-541">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a90d0-542">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a90d0-542">Az.LogicApp</span></span>
* <span data-ttu-id="a90d0-543">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-543">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="a90d0-544">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="a90d0-544">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="a90d0-545">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-545">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="a90d0-546">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a90d0-546">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a90d0-547">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a90d0-547">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a90d0-548">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a90d0-548">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="a90d0-549">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a90d0-549">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="a90d0-550">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-550">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="a90d0-551">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-551">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a90d0-552">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-552">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a90d0-553">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-553">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="a90d0-554">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-554">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="a90d0-555">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="a90d0-555">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="a90d0-556">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a90d0-556">Az.Monitor</span></span>
* <span data-ttu-id="a90d0-557">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="a90d0-557">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-558">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-558">Az.Network</span></span>
* <span data-ttu-id="a90d0-559">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="a90d0-559">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="a90d0-560">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-560">Az.OperationalInsights</span></span>
* <span data-ttu-id="a90d0-561">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a90d0-561">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="a90d0-562">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="a90d0-562">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="a90d0-563">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="a90d0-563">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="a90d0-564">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-564">Az.Resources</span></span>
* <span data-ttu-id="a90d0-565">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a90d0-565">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a90d0-566">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a90d0-566">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="a90d0-567">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="a90d0-567">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="a90d0-568">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="a90d0-568">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-569">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-569">Az.Sql</span></span>
* <span data-ttu-id="a90d0-570">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="a90d0-570">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="a90d0-571">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="a90d0-571">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-572">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-572">Az.Websites</span></span>
* <span data-ttu-id="a90d0-573">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="a90d0-573">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="a90d0-574">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-574">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-575">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-575">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-576">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a90d0-576">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a90d0-577">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-577">Az.AnalysisServices</span></span>
<span data-ttu-id="a90d0-578">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="a90d0-578">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-579">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-579">Az.Compute</span></span>
* <span data-ttu-id="a90d0-580">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="a90d0-580">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="a90d0-581">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="a90d0-581">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="a90d0-582">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="a90d0-582">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-583">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-583">Az.RecoveryServices</span></span>
<span data-ttu-id="a90d0-584">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="a90d0-584">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-585">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-585">Az.Resources</span></span>
* <span data-ttu-id="a90d0-586">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="a90d0-586">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="a90d0-587">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="a90d0-587">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="a90d0-588">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="a90d0-588">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="a90d0-589">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="a90d0-589">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-590">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-590">Az.Sql</span></span>
* <span data-ttu-id="a90d0-591">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a90d0-591">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="a90d0-592">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="a90d0-592">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="a90d0-593">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="a90d0-593">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="a90d0-594">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-594">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-595">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-595">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-596">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-596">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="a90d0-597">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-597">Az.AnalysisServices</span></span>
* <span data-ttu-id="a90d0-598">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-598">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-599">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-599">Az.RecoveryServices</span></span>
* <span data-ttu-id="a90d0-600">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-600">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="a90d0-601">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-601">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-602">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-602">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-603">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="a90d0-603">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="a90d0-604">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-604">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a90d0-605">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="a90d0-605">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="a90d0-606">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="a90d0-606">Az.Aks</span></span>
* <span data-ttu-id="a90d0-607">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-607">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="a90d0-608">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-608">Az.Automation</span></span>
* <span data-ttu-id="a90d0-609">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="a90d0-609">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="a90d0-610">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-610">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="a90d0-611">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="a90d0-611">Az.Cdn</span></span>
* <span data-ttu-id="a90d0-612">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-612">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-613">Az.Compute</span></span>
* <span data-ttu-id="a90d0-614">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="a90d0-614">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="a90d0-615">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="a90d0-615">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="a90d0-616">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="a90d0-616">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="a90d0-617">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="a90d0-617">Az.ContainerRegistry</span></span>
* <span data-ttu-id="a90d0-618">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-618">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="a90d0-619">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="a90d0-619">Az.DataFactory</span></span>
* <span data-ttu-id="a90d0-620">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="a90d0-620">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-621">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-621">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-622">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="a90d0-622">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="a90d0-623">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="a90d0-623">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="a90d0-624">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-624">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a90d0-625">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-625">Az.IotHub</span></span>
* <span data-ttu-id="a90d0-626">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a90d0-626">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="a90d0-627">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-627">Az.KeyVault</span></span>
* <span data-ttu-id="a90d0-628">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-628">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-629">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-629">Az.Network</span></span>
* <span data-ttu-id="a90d0-630">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-630">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-631">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-631">Az.Resources</span></span>
* <span data-ttu-id="a90d0-632">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="a90d0-632">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="a90d0-633">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a90d0-633">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="a90d0-634">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="a90d0-634">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="a90d0-635">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="a90d0-635">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="a90d0-636">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="a90d0-636">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="a90d0-637">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="a90d0-637">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="a90d0-638">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="a90d0-638">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a90d0-639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-639">Az.ServiceFabric</span></span>
* <span data-ttu-id="a90d0-640">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="a90d0-640">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="a90d0-641">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="a90d0-641">Fix some error messages.</span></span>
* <span data-ttu-id="a90d0-642">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="a90d0-642">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="a90d0-643">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-643">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a90d0-644">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a90d0-644">Az.SignalR</span></span>
* <span data-ttu-id="a90d0-645">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-645">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-646">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-646">Az.Sql</span></span>
* <span data-ttu-id="a90d0-647">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-647">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a90d0-648">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="a90d0-648">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="a90d0-649">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="a90d0-649">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="a90d0-650">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="a90d0-650">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-651">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-651">Az.Storage</span></span>
* <span data-ttu-id="a90d0-652">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-652">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a90d0-653">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="a90d0-653">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="a90d0-654">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="a90d0-654">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="a90d0-655">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="a90d0-655">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="a90d0-656">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a90d0-656">Az.TrafficManager</span></span>
* <span data-ttu-id="a90d0-657">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-657">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-658">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-658">Az.Websites</span></span>
* <span data-ttu-id="a90d0-659">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="a90d0-659">Update incorrect online help URLs</span></span>
* <span data-ttu-id="a90d0-660">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="a90d0-660">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="a90d0-661">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="a90d0-661">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="a90d0-662">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="a90d0-662">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="a90d0-663">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-663">Az.Accounts</span></span>
* <span data-ttu-id="a90d0-664">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="a90d0-664">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-665">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-665">Az.Compute</span></span>
* <span data-ttu-id="a90d0-666">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="a90d0-666">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="a90d0-667">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="a90d0-667">Updated the description of ID in help files</span></span>
* <span data-ttu-id="a90d0-668">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-668">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-669">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-669">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-670">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="a90d0-670">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="a90d0-671">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="a90d0-671">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="a90d0-672">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="a90d0-672">Az.EventGrid</span></span>
* <span data-ttu-id="a90d0-673">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="a90d0-673">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="a90d0-674">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="a90d0-674">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="a90d0-675">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="a90d0-675">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a90d0-676">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="a90d0-676">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a90d0-677">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="a90d0-677">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a90d0-678">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="a90d0-678">Dead letter endpoint.</span></span>
    - <span data-ttu-id="a90d0-679">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="a90d0-679">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="a90d0-680">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="a90d0-680">Event Time-To-Live,</span></span>
        - <span data-ttu-id="a90d0-681">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="a90d0-681">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="a90d0-682">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="a90d0-682">Dead letter endpoint.</span></span>
* <span data-ttu-id="a90d0-683">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="a90d0-683">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="a90d0-684">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a90d0-684">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="a90d0-685">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-685">Az.IotHub</span></span>
* <span data-ttu-id="a90d0-686">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="a90d0-686">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="a90d0-687">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="a90d0-687">Az.LogicApp</span></span>
* <span data-ttu-id="a90d0-688">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="a90d0-688">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-689">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-689">Az.Resources</span></span>
* <span data-ttu-id="a90d0-690">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="a90d0-690">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="a90d0-691">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="a90d0-691">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="a90d0-692">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a90d0-692">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a90d0-693">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a90d0-693">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="a90d0-694">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="a90d0-694">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="a90d0-695">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="a90d0-695">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="a90d0-696">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="a90d0-696">Az.SignalR</span></span>
* <span data-ttu-id="a90d0-697">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-697">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-698">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-698">Az.Sql</span></span>
* <span data-ttu-id="a90d0-699">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="a90d0-699">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="a90d0-700">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-700">Az.Storage</span></span>
* <span data-ttu-id="a90d0-701">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="a90d0-701">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="a90d0-702">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a90d0-702">New-AzStorageContext</span></span>
* <span data-ttu-id="a90d0-703">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="a90d0-703">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="a90d0-704">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="a90d0-704">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-705">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-705">Az.Websites</span></span>
* <span data-ttu-id="a90d0-706">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="a90d0-706">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="a90d0-707">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-707">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="a90d0-708">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-708">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="a90d0-709">Generale</span><span class="sxs-lookup"><span data-stu-id="a90d0-709">General</span></span>

- <span data-ttu-id="a90d0-710">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="a90d0-710">General Availability of Az Module</span></span>
- <span data-ttu-id="a90d0-711">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="a90d0-711">Online help for each module</span></span>
- <span data-ttu-id="a90d0-712">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="a90d0-712">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="a90d0-713">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="a90d0-713">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="a90d0-714">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-714">Az.Accounts</span></span>
- <span data-ttu-id="a90d0-715">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a90d0-715">Changed from Az.Profile</span></span>
- <span data-ttu-id="a90d0-716">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="a90d0-716">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a90d0-717">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90d0-717">Az.ApiManagement</span></span>
- <span data-ttu-id="a90d0-718">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="a90d0-718">Fixes for #7002</span></span>
- <span data-ttu-id="a90d0-719">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-719">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="a90d0-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="a90d0-720">Az.Batch</span></span>
- <span data-ttu-id="a90d0-721">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="a90d0-721">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="a90d0-722">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="a90d0-722">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="a90d0-723">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-723">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="a90d0-724">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="a90d0-724">Az.Billing</span></span>
- <span data-ttu-id="a90d0-725">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-725">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="a90d0-726">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-726">Az.CognitivServices</span></span>
- <span data-ttu-id="a90d0-727">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-727">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="a90d0-728">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="a90d0-728">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a90d0-729">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-729">Az.ContainerInstance</span></span>
- <span data-ttu-id="a90d0-730">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="a90d0-730">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="a90d0-731">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="a90d0-731">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="a90d0-732">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-732">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-733">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-733">Az.DataLakeStore</span></span>
- <span data-ttu-id="a90d0-734">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-734">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="a90d0-735">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="a90d0-735">Az.Monitor</span></span>
- <span data-ttu-id="a90d0-736">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-736">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="a90d0-737">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="a90d0-737">Az.KeyVault</span></span>
- <span data-ttu-id="a90d0-738">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="a90d0-738">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="a90d0-739">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="a90d0-739">Az.MachineLearning</span></span>
- <span data-ttu-id="a90d0-740">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="a90d0-740">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="a90d0-741">Az.Media</span><span class="sxs-lookup"><span data-stu-id="a90d0-741">Az.Media</span></span>
- <span data-ttu-id="a90d0-742">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="a90d0-742">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a90d0-743">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-743">Az.Network</span></span>
<span data-ttu-id="a90d0-744">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-744">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="a90d0-745">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="a90d0-745">New cmdlets added:</span></span>
        - <span data-ttu-id="a90d0-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-746">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-747">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-748">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-748">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-749">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-750">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-751">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-751">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="a90d0-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-752">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="a90d0-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="a90d0-753">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="a90d0-754">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="a90d0-754">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="a90d0-755">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a90d0-755">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="a90d0-756">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-756">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a90d0-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="a90d0-757">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="a90d0-758">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-758">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="a90d0-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-759">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="a90d0-760">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="a90d0-760">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="a90d0-761">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="a90d0-761">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="a90d0-762">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a90d0-762">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a90d0-763">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a90d0-763">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="a90d0-764">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a90d0-764">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="a90d0-765">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a90d0-765">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="a90d0-766">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-766">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="a90d0-767">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-767">Az.OperationalInsights</span></span>
- <span data-ttu-id="a90d0-768">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-768">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="a90d0-769">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a90d0-769">Az.Profile</span></span>
- <span data-ttu-id="a90d0-770">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="a90d0-770">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-771">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-771">Az.RecoveryServices</span></span>
- <span data-ttu-id="a90d0-772">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-772">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="a90d0-773">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-773">Az.Resources</span></span>
- <span data-ttu-id="a90d0-774">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-774">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a90d0-775">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-775">Az.ServiceFabric</span></span>
- <span data-ttu-id="a90d0-776">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="a90d0-776">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="a90d0-777">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-777">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="a90d0-778">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a90d0-778">Az.SIgnalR</span></span>
- <span data-ttu-id="a90d0-779">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="a90d0-779">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="a90d0-780">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-780">Az.Sql</span></span>
- <span data-ttu-id="a90d0-781">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="a90d0-781">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="a90d0-782">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-782">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="a90d0-783">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-783">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="a90d0-784">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-784">Az.Storage</span></span>
- <span data-ttu-id="a90d0-785">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-785">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a90d0-786">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-786">Az.Websites</span></span>
- <span data-ttu-id="a90d0-787">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="a90d0-787">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="a90d0-788">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-788">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="a90d0-789">Generale</span><span class="sxs-lookup"><span data-stu-id="a90d0-789">General</span></span>

* <span data-ttu-id="a90d0-790">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="a90d0-790">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="a90d0-791">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-791">Az.Compute</span></span>

* <span data-ttu-id="a90d0-792">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="a90d0-792">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-793">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-793">Az.DataLakeStore</span></span>

* <span data-ttu-id="a90d0-794">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="a90d0-794">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="a90d0-795">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="a90d0-795">Az.FrontDoor</span></span>

* <span data-ttu-id="a90d0-796">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="a90d0-796">Fixed some broken links</span></span>
    - <span data-ttu-id="a90d0-797">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="a90d0-797">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="a90d0-798">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="a90d0-798">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="a90d0-799">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-799">Az.RecoveryServices</span></span>

* <span data-ttu-id="a90d0-800">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="a90d0-800">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="a90d0-801">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="a90d0-801">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="a90d0-802">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-802">Az.Resources</span></span>

* <span data-ttu-id="a90d0-803">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="a90d0-803">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="a90d0-804">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="a90d0-804">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="a90d0-805">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-805">Az.Sql</span></span>

* <span data-ttu-id="a90d0-806">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="a90d0-806">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="a90d0-807">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="a90d0-807">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="a90d0-808">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="a90d0-808">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="a90d0-809">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-809">Az.Storage</span></span>

* <span data-ttu-id="a90d0-810">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-810">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="a90d0-811">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="a90d0-811">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="a90d0-812">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a90d0-812">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a90d0-813">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="a90d0-813">Support Static Website configuration</span></span>
    - <span data-ttu-id="a90d0-814">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a90d0-814">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="a90d0-815">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="a90d0-815">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="a90d0-816">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-816">Az.Websites</span></span>

* <span data-ttu-id="a90d0-817">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a90d0-817">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="a90d0-818">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="a90d0-818">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="a90d0-819">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a90d0-819">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="a90d0-820">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-820">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="a90d0-821">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a90d0-821">Az.ApiManagement</span></span>
* <span data-ttu-id="a90d0-822">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a90d0-822">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="a90d0-823">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="a90d0-823">Az.Automation</span></span>
* <span data-ttu-id="a90d0-824">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="a90d0-824">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="a90d0-825">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="a90d0-825">Added Update Management cmdlets</span></span>
* <span data-ttu-id="a90d0-826">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="a90d0-826">Added Source Control cmdlets</span></span>
* <span data-ttu-id="a90d0-827">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="a90d0-827">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="a90d0-828">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="a90d0-828">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="a90d0-829">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-829">Az.Compute</span></span>
* <span data-ttu-id="a90d0-830">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="a90d0-830">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="a90d0-831">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a90d0-831">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="a90d0-832">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-832">Az.ContainerInstance</span></span>
* <span data-ttu-id="a90d0-833">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a90d0-833">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="a90d0-834">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="a90d0-834">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="a90d0-835">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="a90d0-835">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="a90d0-836">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-836">Az.Network</span></span>
* <span data-ttu-id="a90d0-837">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="a90d0-837">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="a90d0-838">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="a90d0-838">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="a90d0-839">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-839">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="a90d0-840">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a90d0-840">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="a90d0-841">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="a90d0-841">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="a90d0-842">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="a90d0-842">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="a90d0-843">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="a90d0-843">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="a90d0-844">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="a90d0-844">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="a90d0-845">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a90d0-845">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="a90d0-846">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="a90d0-846">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="a90d0-847">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="a90d0-847">Az.Relay</span></span>
* <span data-ttu-id="a90d0-848">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="a90d0-848">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="a90d0-849">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-849">Az.Resources</span></span>
* <span data-ttu-id="a90d0-850">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="a90d0-850">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="a90d0-851">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="a90d0-851">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="a90d0-852">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="a90d0-852">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="a90d0-853">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-853">Az.ServiceFabric</span></span>
* <span data-ttu-id="a90d0-854">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="a90d0-854">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="a90d0-855">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-855">Az.Sql</span></span>
* <span data-ttu-id="a90d0-856">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="a90d0-856">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="a90d0-857">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-857">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a90d0-858">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-858">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a90d0-859">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-859">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a90d0-860">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="a90d0-860">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="a90d0-861">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a90d0-861">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a90d0-862">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a90d0-862">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a90d0-863">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a90d0-863">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="a90d0-864">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="a90d0-864">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="a90d0-865">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="a90d0-865">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="a90d0-866">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="a90d0-866">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="a90d0-867">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="a90d0-867">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="a90d0-868">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a90d0-868">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a90d0-869">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="a90d0-869">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="a90d0-870">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a90d0-870">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="a90d0-871">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="a90d0-871">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="a90d0-872">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-872">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="a90d0-873">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-873">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="a90d0-874">Generale</span><span class="sxs-lookup"><span data-stu-id="a90d0-874">General</span></span>
* <span data-ttu-id="a90d0-875">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="a90d0-875">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="a90d0-876">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a90d0-876">Az.Profile</span></span>
* <span data-ttu-id="a90d0-877">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a90d0-877">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="a90d0-878">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="a90d0-878">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="a90d0-879">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="a90d0-879">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="a90d0-880">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="a90d0-880">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="a90d0-881">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="a90d0-881">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="a90d0-882">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="a90d0-882">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="a90d0-883">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="a90d0-883">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="a90d0-884">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-884">Az.CognitiveServices</span></span>
* <span data-ttu-id="a90d0-885">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="a90d0-885">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-886">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-886">Az.Compute</span></span>
* <span data-ttu-id="a90d0-887">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="a90d0-887">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="a90d0-888">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="a90d0-888">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="a90d0-889">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="a90d0-889">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-890">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-891">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="a90d0-891">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="a90d0-892">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="a90d0-892">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="a90d0-893">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="a90d0-893">Az.Insights</span></span>
* <span data-ttu-id="a90d0-894">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="a90d0-894">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="a90d0-895">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="a90d0-895">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="a90d0-896">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-896">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="a90d0-897">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="a90d0-897">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-898">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-898">Az.Network</span></span>
* <span data-ttu-id="a90d0-899">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="a90d0-899">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="a90d0-900">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="a90d0-900">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="a90d0-901">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="a90d0-901">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="a90d0-902">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a90d0-902">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="a90d0-903">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="a90d0-903">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="a90d0-904">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="a90d0-904">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="a90d0-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="a90d0-905">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="a90d0-906">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="a90d0-906">Az.PolicyInsights</span></span>
* <span data-ttu-id="a90d0-907">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="a90d0-907">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-908">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-908">Az.Resources</span></span>
* <span data-ttu-id="a90d0-909">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="a90d0-909">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="a90d0-910">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="a90d0-910">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="a90d0-911">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a90d0-911">Az.ServiceBus</span></span>
* <span data-ttu-id="a90d0-912">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="a90d0-912">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="a90d0-913">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="a90d0-913">Az.ServiceFabric</span></span>
* <span data-ttu-id="a90d0-914">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="a90d0-914">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="a90d0-915">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="a90d0-915">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="a90d0-916">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="a90d0-916">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="a90d0-917">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="a90d0-917">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="a90d0-918">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="a90d0-918">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="a90d0-919">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-919">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="a90d0-920">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="a90d0-920">Az.Profile</span></span>
* <span data-ttu-id="a90d0-921">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="a90d0-921">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="a90d0-922">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="a90d0-922">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-923">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-923">Az.Compute</span></span>
* <span data-ttu-id="a90d0-924">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="a90d0-924">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="a90d0-925">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a90d0-925">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="a90d0-926">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a90d0-926">Az.DataLakeStore</span></span>
* <span data-ttu-id="a90d0-927">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="a90d0-927">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="a90d0-928">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a90d0-928">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="a90d0-929">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a90d0-929">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a90d0-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="a90d0-930">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="a90d0-931">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a90d0-931">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-932">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-932">Az.Network</span></span>
* <span data-ttu-id="a90d0-933">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="a90d0-933">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="a90d0-934">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a90d0-934">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-935">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-935">Az.Resources</span></span>
* <span data-ttu-id="a90d0-936">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="a90d0-936">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="a90d0-937">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="a90d0-937">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="a90d0-938">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-938">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="a90d0-939">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="a90d0-939">Azure.Storage</span></span>
* <span data-ttu-id="a90d0-940">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="a90d0-940">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="a90d0-941">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="a90d0-941">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="a90d0-942">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="a90d0-942">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="a90d0-943">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="a90d0-943">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="a90d0-944">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="a90d0-944">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="a90d0-945">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="a90d0-945">Az.CognitiveServices</span></span>
* <span data-ttu-id="a90d0-946">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="a90d0-946">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="a90d0-947">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="a90d0-947">Az.Compute</span></span>
* <span data-ttu-id="a90d0-948">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="a90d0-948">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="a90d0-949">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="a90d0-949">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="a90d0-950">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="a90d0-950">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="a90d0-951">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a90d0-951">Az.DataFactoryV2</span></span>
* <span data-ttu-id="a90d0-952">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="a90d0-952">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="a90d0-953">Az.Network</span><span class="sxs-lookup"><span data-stu-id="a90d0-953">Az.Network</span></span>
* <span data-ttu-id="a90d0-954">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a90d0-954">Added NetworkProfile functionality.</span></span> <span data-ttu-id="a90d0-955">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="a90d0-955">new cmdlets added</span></span>
    - <span data-ttu-id="a90d0-956">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a90d0-956">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="a90d0-957">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a90d0-957">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="a90d0-958">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a90d0-958">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="a90d0-959">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="a90d0-959">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="a90d0-960">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-960">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="a90d0-961">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-961">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="a90d0-962">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="a90d0-962">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="a90d0-963">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="a90d0-963">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="a90d0-964">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="a90d0-964">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="a90d0-965">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="a90d0-965">Az.RedisCache</span></span>
* <span data-ttu-id="a90d0-966">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="a90d0-966">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="a90d0-967">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="a90d0-967">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="a90d0-968">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="a90d0-968">Az.Resources</span></span>
* <span data-ttu-id="a90d0-969">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a90d0-969">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="a90d0-970">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="a90d0-970">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="a90d0-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="a90d0-971">Az.Sql</span></span>
* <span data-ttu-id="a90d0-972">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="a90d0-972">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="a90d0-973">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="a90d0-973">Az.Websites</span></span>
* <span data-ttu-id="a90d0-974">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="a90d0-974">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="a90d0-975">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="a90d0-975">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="a90d0-976">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="a90d0-976">0.2.0 - September 2018</span></span>
 <span data-ttu-id="a90d0-977">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="a90d0-977">Initial Release</span></span>