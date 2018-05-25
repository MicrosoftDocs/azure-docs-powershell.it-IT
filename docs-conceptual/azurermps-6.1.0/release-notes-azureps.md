---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 5/1/2018
ms.openlocfilehash: 0b7902155c47f2e6355e9147c203867288caab81
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a><span data-ttu-id="0a02e-103">Note sulla versione</span><span class="sxs-lookup"><span data-stu-id="0a02e-103">Release notes</span></span>

<span data-ttu-id="0a02e-104">Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.</span><span class="sxs-lookup"><span data-stu-id="0a02e-104">This is a list of changes made to Azure PowerShell in this release.</span></span>

---
## <a name="610---may-2018"></a><span data-ttu-id="0a02e-105">6.1.0 - Maggio 2018</span><span class="sxs-lookup"><span data-stu-id="0a02e-105">6.1.0 - May 2018</span></span>
#### <a name="azurermprofile"></a><span data-ttu-id="0a02e-106">AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="0a02e-106">AzureRM.Profile</span></span>
* <span data-ttu-id="0a02e-107">Risoluzione del problema relativo all'esecuzione di 'Clear-AzureRmContext' che mantiene un contesto vuoto con il nome del contesto predefinito precedente, impedendo all'utente di creare un nuovo contesto con il nome precedente</span><span class="sxs-lookup"><span data-stu-id="0a02e-107">Fix issue where running 'Clear-AzureRmContext' would keep an empty context with the name of the previous default context, which prevented the user from creating a new context with the old name</span></span>

#### <a name="azurermanalysisservices"></a><span data-ttu-id="0a02e-108">AzureRM.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a02e-108">AzureRM.AnalysisServices</span></span>
* <span data-ttu-id="0a02e-109">Abilitazione delle operazioni di associazione/disassociazione del gateway in Analysis Services.</span><span class="sxs-lookup"><span data-stu-id="0a02e-109">Enable Gateway assocaite/disassociate operations on AS.</span></span>

#### <a name="azurermapimanagement"></a><span data-ttu-id="0a02e-110">AzureRM.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a02e-110">AzureRM.ApiManagement</span></span>
* <span data-ttu-id="0a02e-111">Aggiunta di supporto per ApiVersions, ApiReleases e ApiRevisions</span><span class="sxs-lookup"><span data-stu-id="0a02e-111">Added support for ApiVersions, ApiReleases and ApiRevisions</span></span>
* <span data-ttu-id="0a02e-112">Aggiunta di supporto per il back-end di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0a02e-112">Added suppport for ServiceFabric Backend</span></span>
* <span data-ttu-id="0a02e-113">Aggiunta di supporto per il logger di Application Insights</span><span class="sxs-lookup"><span data-stu-id="0a02e-113">Added support for Application Insights Logger</span></span>
* <span data-ttu-id="0a02e-114">Aggiunta di supporto per il riconoscimento dello SKU 'Basic' come SKU valido del servizio Gestione API</span><span class="sxs-lookup"><span data-stu-id="0a02e-114">Added support for recognizing 'Basic' sku as a valid sku of Api Management service</span></span>
* <span data-ttu-id="0a02e-115">Aggiunta di supporto per l'installazione di certificati rilasciati da un'autorità di certificazione privata come radice o CA</span><span class="sxs-lookup"><span data-stu-id="0a02e-115">Added support for installing Certificates issued by private CA as Root or CA</span></span>
* <span data-ttu-id="0a02e-116">Aggiunta di supporto per l'accettazione di certificati SSL personalizzati tramite KeyVault e più nomi host proxy</span><span class="sxs-lookup"><span data-stu-id="0a02e-116">Added support for accepting Custom SSL certificates via KeyVault and Multiple proxy hostnames</span></span>
* <span data-ttu-id="0a02e-117">Aggiunta di supporto per identità di MSI</span><span class="sxs-lookup"><span data-stu-id="0a02e-117">Added support for MSI identity</span></span>
* <span data-ttu-id="0a02e-118">Aggiunta di supporto per l'accettazione di criteri tramite URL. NOTA: i cmdlet seguenti verranno deprecati nelle versioni future</span><span class="sxs-lookup"><span data-stu-id="0a02e-118">Added support for accepting Policies via Url NOTE: The following cmdlets will be deprecated in future release</span></span>
   - <span data-ttu-id="0a02e-119">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="0a02e-119">Import-AzureRmApiManagementHostnameCertificate</span></span>
   - <span data-ttu-id="0a02e-120">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a02e-120">New-AzureRmApiManagementHostnameConfiguration</span></span>
   - <span data-ttu-id="0a02e-121">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="0a02e-121">Set-AzureRmApiManagementHostnames</span></span>
   - <span data-ttu-id="0a02e-122">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0a02e-122">Update-AzureRmApiManagementDeployment</span></span>

#### <a name="azurermbatch"></a><span data-ttu-id="0a02e-123">AzureRM.Batch</span><span class="sxs-lookup"><span data-stu-id="0a02e-123">AzureRM.Batch</span></span>
* <span data-ttu-id="0a02e-124">Rilascio del nuovo cmdlet Get-AzureBatchPoolNodeCounts</span><span class="sxs-lookup"><span data-stu-id="0a02e-124">Release new cmdlet Get-AzureBatchPoolNodeCounts</span></span>
* <span data-ttu-id="0a02e-125">Rilascio del nuovo cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span><span class="sxs-lookup"><span data-stu-id="0a02e-125">Release new cmdlet Start-AzureBatchComputeNodeServiceLogUpload</span></span>

#### <a name="azurermconsumption"></a><span data-ttu-id="0a02e-126">AzureRM.Consumption</span><span class="sxs-lookup"><span data-stu-id="0a02e-126">AzureRM.Consumption</span></span>
* <span data-ttu-id="0a02e-127">Aggiunta di nuovi parametri Expand, ResourceGroup, InstanceName, InstanceId, Tags e Top nel cmdlet Get-AzureRmConsumptionUsageDetail</span><span class="sxs-lookup"><span data-stu-id="0a02e-127">Add new parameters Expand, ResourceGroup, InstanceName, InstanceId, Tags, and Top on Cmdlet Get-AzureRmConsumptionUsageDetail</span></span>

#### <a name="azurermdatalakestore"></a><span data-ttu-id="0a02e-128">AzureRM.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a02e-128">AzureRM.DataLakeStore</span></span>
* <span data-ttu-id="0a02e-129">Correzione dell'esempio per Export-AzureRmDataLakeStoreChildItemProperties</span><span class="sxs-lookup"><span data-stu-id="0a02e-129">Fix example for Export-AzureRmDataLakeStoreChildItemProperties</span></span>
* <span data-ttu-id="0a02e-130">Correzione dell'eccezione del parametro Null in caso di ricorsione in Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a02e-130">Fix null parameter exception for Recurse case in Set-AzureRmDataLakeStoreItemAclEntry</span></span> 
* <span data-ttu-id="0a02e-131">Correzione dei file della Guida per Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0a02e-131">Fix the help files for Set-AzureRmDataLakeStoreItemAclEntry, Set-AzureRmDataLakeStoreItemAcl, Remove-AzureRmDataLakeStoreItemAclEntry</span></span> 

#### <a name="azurermnetwork"></a><span data-ttu-id="0a02e-132">AzureRM.Network</span><span class="sxs-lookup"><span data-stu-id="0a02e-132">AzureRM.Network</span></span>
* <span data-ttu-id="0a02e-133">Incremento della versione di Network SDK da 18.0.0-preview a 19.0.0-preview</span><span class="sxs-lookup"><span data-stu-id="0a02e-133">Bump up Network SDK version from 18.0.0-preview to 19.0.0-preview</span></span>
* <span data-ttu-id="0a02e-134">Aggiunta di un cmdlet per la creazione della configurazione del protocollo</span><span class="sxs-lookup"><span data-stu-id="0a02e-134">Added cmdlet to create protocol configuration</span></span>
    - <span data-ttu-id="0a02e-135">New-AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a02e-135">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>
* <span data-ttu-id="0a02e-136">Aggiunta di un cmdlet per aggiungere una nuova connessione a circuito a un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="0a02e-136">Added cmdlet to add a new circuit connection to an existing express route circuit.</span></span>
    - <span data-ttu-id="0a02e-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a02e-137">Add-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0a02e-138">Aggiunta di un cmdlet per la rimozione di una connessione a circuito da un circuito di ExpressRoute esistente.</span><span class="sxs-lookup"><span data-stu-id="0a02e-138">Added cmdlet to remove a circuit connection from an existing express route circuit.</span></span>
    - <span data-ttu-id="0a02e-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a02e-139">Remove-AzureRmExpressRouteCircuitConnectionConfig</span></span>
* <span data-ttu-id="0a02e-140">Aggiunta di un cmdlet per il recupero di una connessione a circuito</span><span class="sxs-lookup"><span data-stu-id="0a02e-140">Added cmdlet to retrieve a circuit connection</span></span>
    - <span data-ttu-id="0a02e-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span><span class="sxs-lookup"><span data-stu-id="0a02e-141">Get-AzureRmExpressRouteCircuitConnectionConfig</span></span>

#### <a name="azurermservicefabric"></a><span data-ttu-id="0a02e-142">AzureRM.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a02e-142">AzureRM.ServiceFabric</span></span>
* <span data-ttu-id="0a02e-143">Correzione dell'utilizzo dell'autenticazione del server con certificati generati (problema #5998)</span><span class="sxs-lookup"><span data-stu-id="0a02e-143">Fixed server authentication usage with generated certificates (Issue #5998)</span></span>

#### <a name="azurermsql"></a><span data-ttu-id="0a02e-144">AzureRM.Sql</span><span class="sxs-lookup"><span data-stu-id="0a02e-144">AzureRM.Sql</span></span>
* <span data-ttu-id="0a02e-145">Aggiornamento dei cmdlet di controllo per consentire la rimozione di AuditActions o AuditActionGroups</span><span class="sxs-lookup"><span data-stu-id="0a02e-145">Updated Auditing cmdlets to allow removing AuditActions or AuditActionGroups</span></span>
* <span data-ttu-id="0a02e-146">Correzione del problema relativo a Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy durante l'impostazione di un nuovo criterio di conservazione flessibile che provocava l'errore del comando con un messaggio analogo al seguente: 'La configurazione dei criteri di conservazione a lungo termine con l'insieme di credenziali del servizio di ripristino di Azure e i criteri non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="0a02e-146">Fixed issue with Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy when setting a new flexible retention policy where the command would fail with 'Configure long term retention policy with azure recovery service vault and policy is no longer supported.</span></span> <span data-ttu-id="0a02e-147">Inviare la richiesta con i nuovi criteri di conservazione flessibili'.</span><span class="sxs-lookup"><span data-stu-id="0a02e-147">Please submit request with the new flexible retention policy'.</span></span>
* <span data-ttu-id="0a02e-148">Aggiornamento di tutti i cmdlet correlati a database SQL di Azure/creazione di pool elastici/aggiornamento in modo che venga usata la nuova API del database che supporta la proprietà SKU per il ridimensionamento e le proprietà correlate ai livelli.</span><span class="sxs-lookup"><span data-stu-id="0a02e-148">Update all Azure Sql Database/ElasticPool Creation/Update related cmdlets to use the new Database API, which support Sku property for scale and tier-related properties.</span></span>
* <span data-ttu-id="0a02e-149">I cmdlet aggiornati includono:</span><span class="sxs-lookup"><span data-stu-id="0a02e-149">The updated cmdlets including:</span></span> 
    - <span data-ttu-id="0a02e-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a02e-150">New-AzureRmSqlDatabase; Set-AzureRmSqlDatabase</span></span>
    - <span data-ttu-id="0a02e-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0a02e-151">New-AzureRmSqlElasticPool; Set-AzureRmSqlElasticPool</span></span>
    - <span data-ttu-id="0a02e-152">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="0a02e-152">New-AzureRmSqlDatabaseCopy</span></span>
    - <span data-ttu-id="0a02e-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0a02e-153">New-AzureRmSqlDatabaseSecondary</span></span>
    - <span data-ttu-id="0a02e-154">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0a02e-154">Restore-AzureRmSqlDatabase</span></span>

#### <a name="azurermtrafficmanager"></a><span data-ttu-id="0a02e-155">AzureRM.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a02e-155">AzureRM.TrafficManager</span></span>
* <span data-ttu-id="0a02e-156">Aggiornamento dei parametri per 'Get-AzureRmTrafficManagerProfile' in modo che il parametro -ResourceGroupName sia necessario quando si usa il parametro -Name.</span><span class="sxs-lookup"><span data-stu-id="0a02e-156">Update the parameters for 'Get-AzureRmTrafficManagerProfile' so that -ResourceGroupName parameter is required when using -Name parameter.</span></span>