---
title: Note sulla versione di Azure PowerShell
description: Informazioni su tutti gli aggiornamenti più recenti per i moduli di Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.openlocfilehash: bee24af99da4b36e89cff9852c77214e2e09a542
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "81740542"
---
## <a name="380---april-2020"></a><span data-ttu-id="0a960-103">3.8.0 - Aprile 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-103">3.8.0 - April 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-104">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-104">Az.Accounts</span></span>
* <span data-ttu-id="0a960-105">Aggiornamento dell'URL del sondaggio di Azure PowerShell in 'Resolve-AzError' [#11507]</span><span class="sxs-lookup"><span data-stu-id="0a960-105">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-106">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-107">Aggiunta di un avviso di modifica di rilievo per la modifica dell'output dei cmdlet di File di Azure in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0a960-107">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="0a960-108">Aggiornamento della documentazione di 'Set-AzApiManagementGroup' per specificare il parametro GroupId</span><span class="sxs-lookup"><span data-stu-id="0a960-108">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-109">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-109">Az.Cdn</span></span>
* <span data-ttu-id="0a960-110">Correzione della visualizzazione dello SKU con prezzi relativi a ChinaCDN</span><span class="sxs-lookup"><span data-stu-id="0a960-110">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-111">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-111">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-112">Supporto di Identity, Encryption, UserOwnedStorage</span><span class="sxs-lookup"><span data-stu-id="0a960-112">Supported Identity, Encryption, UserOwnedStorage</span></span> 

#### <a name="azcompute"></a><span data-ttu-id="0a960-113">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-113">Az.Compute</span></span>
* <span data-ttu-id="0a960-114">Aggiunta del cmdlet 'Set-AzVmssOrchestrationServiceState'.</span><span class="sxs-lookup"><span data-stu-id="0a960-114">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="0a960-115">'Get-AzVmss' con -InstanceView visualizza gli stati OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="0a960-115">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-116">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-116">Az.IotHub</span></span>
* <span data-ttu-id="0a960-117">Gestione della configurazione dei dispositivi gemelli IoT. I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-117">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="0a960-118">'Get-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="0a960-118">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="0a960-119">'Update-AzIotHubDeviceTwin'</span><span class="sxs-lookup"><span data-stu-id="0a960-119">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="0a960-120">Aggiunta del cmdlet per richiamare il metodo diretto in un dispositivo di un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-120">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="0a960-121">Gestione della configurazione dei dispositivi gemelli del modulo per i dispositivi. I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-121">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="0a960-122">'Get-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="0a960-122">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="0a960-123">'Update-AzIotHubModuleTwin'</span><span class="sxs-lookup"><span data-stu-id="0a960-123">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="0a960-124">Gestione della configurazione della gestione automatica dei dispositivi IoT su larga scala.</span><span class="sxs-lookup"><span data-stu-id="0a960-124">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="0a960-125">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-125">New cmdlets are:</span></span>
    - <span data-ttu-id="0a960-126">'Add-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0a960-126">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0a960-127">'Get-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0a960-127">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0a960-128">'Remove-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0a960-128">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="0a960-129">'Set-AzIotHubConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0a960-129">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="0a960-130">Aggiunta del cmdlet per richiamare un metodo del modulo Edge in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-130">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-131">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-131">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-132">Aggiunta di un nuovo cmdlet 'Update-AzKeyVault' che può abilitare l'eliminazione temporanea e la protezione da eliminazione in un insieme di credenziali</span><span class="sxs-lookup"><span data-stu-id="0a960-132">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="0a960-133">Aggiunta del supporto a Microsoft.PowerShell.SecretManagement [#11178]</span><span class="sxs-lookup"><span data-stu-id="0a960-133">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="0a960-134">Correzione dell'errore negli esempi di 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span><span class="sxs-lookup"><span data-stu-id="0a960-134">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="0a960-135">Aggiunta del supporto per l'endpoint privato</span><span class="sxs-lookup"><span data-stu-id="0a960-135">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="0a960-136">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="0a960-136">Az.Maintenance</span></span>
* <span data-ttu-id="0a960-137">Pubblicazione della versione finale dei cmdlet di manutenzione per la disponibilità generale</span><span class="sxs-lookup"><span data-stu-id="0a960-137">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-138">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-138">Az.Monitor</span></span>
* <span data-ttu-id="0a960-139">Aggiunta di cmdlet per l'ambito di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0a960-139">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="0a960-140">'Get-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0a960-140">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0a960-141">'Remove-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0a960-141">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0a960-142">'New-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0a960-142">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0a960-143">'Update-AzInsightsPrivateLinkScope'</span><span class="sxs-lookup"><span data-stu-id="0a960-143">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="0a960-144">'Get-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0a960-144">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="0a960-145">'New-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0a960-145">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="0a960-146">'Remove-AzInsightsPrivateLinkScopedResource'</span><span class="sxs-lookup"><span data-stu-id="0a960-146">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-147">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-147">Az.Network</span></span>
* <span data-ttu-id="0a960-148">Aggiornamento dei cmdlet per abilitare la connessione su IP privato per il gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-148">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="0a960-149">'New-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0a960-149">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="0a960-150">'Set-AzVirtualNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0a960-150">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="0a960-151">'New-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="0a960-151">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="0a960-152">'Set-AzVirtualNetworkGatewayConnection'</span><span class="sxs-lookup"><span data-stu-id="0a960-152">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="0a960-153">Aggiornamento dei cmdlet per abilitare LocalNetworkGateways e VpnSites basati su FQDN</span><span class="sxs-lookup"><span data-stu-id="0a960-153">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="0a960-154">'New-AzLocalNetworkGateway'</span><span class="sxs-lookup"><span data-stu-id="0a960-154">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="0a960-155">'New-AzVpnSiteLink'</span><span class="sxs-lookup"><span data-stu-id="0a960-155">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="0a960-156">Aggiunta del supporto per la famiglia di indirizzi IPv6 in ExpressRouteCircuitConnectionConfig (Copertura globale)</span><span class="sxs-lookup"><span data-stu-id="0a960-156">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="0a960-157">Aggiunta di 'Set-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="0a960-157">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="0a960-158">Consente di impostare tutte le proprietà esistenti, tra cui IPv6CircuitConnectionProperties</span><span class="sxs-lookup"><span data-stu-id="0a960-158">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="0a960-159">Aggiornamento di 'Add-AzExpressRouteCircuitConnectionConfig'</span><span class="sxs-lookup"><span data-stu-id="0a960-159">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="0a960-160">Aggiunta di un altro parametro facoltativo AddressPrefixType per specificare la famiglia di indirizzi del prefisso di indirizzi</span><span class="sxs-lookup"><span data-stu-id="0a960-160">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="0a960-161">Aggiornamento dei cmdlet per consentire l'impostazione del timeout DPD nelle connessioni del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-161">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="0a960-162">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-162">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="0a960-163">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-163">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-164">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-164">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-165">Aggiunta del cmdlet 'Start-AzPolicyComplianceScan' per attivare le analisi di conformità ai criteri</span><span class="sxs-lookup"><span data-stu-id="0a960-165">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="0a960-166">Aggiunta di definizione dei criteri, definizione di set e versioni di assegnazione all'output di 'Get-AzPolicyState'</span><span class="sxs-lookup"><span data-stu-id="0a960-166">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-167">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-167">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-168">Miglioramento della formattazione del codice e dell'usabilità degli esempi di 'New-AzServiceFabricCluster'</span><span class="sxs-lookup"><span data-stu-id="0a960-168">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-169">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-169">Az.Sql</span></span>
* <span data-ttu-id="0a960-170">Aggiunta dei cmdlet 'Get-AzSqlInstanceOperation' e 'Stop-AzSqlInstanceOperation'</span><span class="sxs-lookup"><span data-stu-id="0a960-170">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="0a960-171">Supporto del controllo di un account di archiviazione nella rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-171">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-172">Az.Storage</span></span>
* <span data-ttu-id="0a960-173">Aggiunta di un avviso di modifica di rilievo per la modifica dell'output dei cmdlet di File di Azure in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0a960-173">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="0a960-174">Supporto dei nuovi elementi SkuName StandardGZRS, StandardRAGZRS per la creazione e l'aggiornamento di account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-174">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="0a960-175">'New-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0a960-175">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="0a960-176">'Set-AzStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0a960-176">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="0a960-177">Supporto di DataLake Gen2</span><span class="sxs-lookup"><span data-stu-id="0a960-177">Supported DataLake Gen2</span></span> 
    - <span data-ttu-id="0a960-178">'New-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0a960-178">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0a960-179">'Get-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0a960-179">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0a960-180">'Get-AzDataLakeGen2ChildItem'</span><span class="sxs-lookup"><span data-stu-id="0a960-180">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="0a960-181">'Move-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0a960-181">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0a960-182">'Set-AzDataLakeGen2ItemAclObject'</span><span class="sxs-lookup"><span data-stu-id="0a960-182">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="0a960-183">'Update-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0a960-183">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="0a960-184">'Get-AzDataLakeGen2ItemContent'</span><span class="sxs-lookup"><span data-stu-id="0a960-184">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="0a960-185">'Remove-AzDataLakeGen2Item'</span><span class="sxs-lookup"><span data-stu-id="0a960-185">'Remove-AzDataLakeGen2Item'</span></span>

# <a name="azure-powershell-release-notes"></a><span data-ttu-id="0a960-186">Note sulla versione di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a960-186">Azure PowerShell release notes</span></span>
## <a name="370---march-2020"></a><span data-ttu-id="0a960-187">3.7.0 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-187">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-188">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-188">Az.Accounts</span></span>
* <span data-ttu-id="0a960-189">Correzione dell'eccezione NullReferenceException generata da 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' in caso di mancato accesso [#10292]</span><span class="sxs-lookup"><span data-stu-id="0a960-189">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-190">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-190">Az.Compute</span></span>
* <span data-ttu-id="0a960-191">Aggiunta dei parametri seguenti al cmdlet 'New-AzDiskConfig':</span><span class="sxs-lookup"><span data-stu-id="0a960-191">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span> 
    - <span data-ttu-id="0a960-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="0a960-192">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="0a960-193">Proprietà Encryption consentita per il parametro Target del cmdlet 'New-AzGalleryImageVersion'.</span><span class="sxs-lookup"><span data-stu-id="0a960-193">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="0a960-194">Correzione del problema tempDisk per i cmdlet 'Set-AzVmss' -Reimage e 'Invoke-AzVMReimage'.</span><span class="sxs-lookup"><span data-stu-id="0a960-194">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="0a960-195">[#11354]</span><span class="sxs-lookup"><span data-stu-id="0a960-195">[#11354]</span></span>
* <span data-ttu-id="0a960-196">Aggiunta del supporto dei cmdlet seguenti per la nuova estensione SAP</span><span class="sxs-lookup"><span data-stu-id="0a960-196">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="0a960-197">'Set-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="0a960-197">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a960-198">'Get-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="0a960-198">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a960-199">'Remove-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="0a960-199">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="0a960-200">'Update-AzVMAEMExtension'</span><span class="sxs-lookup"><span data-stu-id="0a960-200">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="0a960-201">Correzione di errori negli esempi del documento della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-201">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="0a960-202">Visualizzazione del valore stringa esatto per PowerState VM nel formato tabella.</span><span class="sxs-lookup"><span data-stu-id="0a960-202">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="0a960-203">'New-AzVmssConfig': correzione della serializzazione della proprietà AutomaticRepairs quando SinglePlacementGroup è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0a960-203">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="0a960-204">[#11257]</span><span class="sxs-lookup"><span data-stu-id="0a960-204">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-205">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-206">Aggiornamento di ADF .NET SDK alla versione 4.8.0</span><span class="sxs-lookup"><span data-stu-id="0a960-206">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="0a960-207">Aggiunta di parametri facoltativi al comando 'Invoke-AzDataFactoryV2Pipeline' per supportare la riesecuzione</span><span class="sxs-lookup"><span data-stu-id="0a960-207">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-208">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-208">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-209">Aggiunta della descrizione della modifica di rilievo per 'Export-AzDataLakeStoreItem' e 'Import-AzDataLakeStoreItem'</span><span class="sxs-lookup"><span data-stu-id="0a960-209">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="0a960-210">Aggiunta dell'opzione di codifica Byte per 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent' e 'Get-AzDAtaLakeStoreItemContent'</span><span class="sxs-lookup"><span data-stu-id="0a960-210">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-211">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-211">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-212">Supporto della versione minima supportata di TLS durante la creazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a960-212">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-213">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-213">Az.IotHub</span></span>
* <span data-ttu-id="0a960-214">Aggiunta del supporto per gestire le impostazioni distribuite per singolo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a960-214">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="0a960-215">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-215">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a960-216">'Get-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="0a960-216">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="0a960-217">'Set-AzIotHubDistributedTracing'</span><span class="sxs-lookup"><span data-stu-id="0a960-217">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-218">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-218">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-219">Aggiunta degli attributi della modifica di rilievo a 'New-AzKeyVault'</span><span class="sxs-lookup"><span data-stu-id="0a960-219">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-220">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-220">Az.Monitor</span></span>
* <span data-ttu-id="0a960-221">Documentazione aggiornata per 'New-AzScheduledQueryRuleLogMetricTrigger'</span><span class="sxs-lookup"><span data-stu-id="0a960-221">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-222">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-222">Az.Network</span></span>
* <span data-ttu-id="0a960-223">Aggiornamento dei cmdlet per consentire VirtualHubVnetConnections tra tenant</span><span class="sxs-lookup"><span data-stu-id="0a960-223">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="0a960-224">'New-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="0a960-224">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0a960-225">'Update-AzVirtualHubVnetConnection'</span><span class="sxs-lookup"><span data-stu-id="0a960-225">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="0a960-226">'New-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="0a960-226">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="0a960-227">'Update-AzVirtualHub'</span><span class="sxs-lookup"><span data-stu-id="0a960-227">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="0a960-228">Rimozione della dipendenza di SQL Management SDK</span><span class="sxs-lookup"><span data-stu-id="0a960-228">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-229">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-229">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-230">Miglioramento dei messaggi di errore</span><span class="sxs-lookup"><span data-stu-id="0a960-230">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-231">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-231">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-232">Azure Site Recovery: aggiunto il supporto per la riprotezione e aggiornamento delle proprietà delle VM per le macchine virtuali con crittografia dischi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-232">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="0a960-233">Azure Site Recovery: aggiunta del monitoraggio per il ripristino di emergenza nelle proprietà VmwareToAzure</span><span class="sxs-lookup"><span data-stu-id="0a960-233">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="0a960-234">Backup di Azure: aggiunta del supporto per la ripetizione dell'aggiornamento dei criteri per gli elementi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="0a960-234">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="0a960-235">Backup di Azure: aggiunta del supporto per le impostazioni di esclusione disco durante il backup e il ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a960-235">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="0a960-236">Backup di Azure: aggiunta del supporto per il ripristino di più file/cartelle in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0a960-236">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="0a960-237">Backup di Azure: aggiunta del supporto per il gruppo di risorse specificato dall'utente durante l'aggiornamento dei criteri IaasVM</span><span class="sxs-lookup"><span data-stu-id="0a960-237">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-238">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-238">Az.Resources</span></span>
* <span data-ttu-id="0a960-239">Correzione di 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' per l'utilizzo del valore effettivo di apiVersion per le risorse invece di quello predefinito [#11267]</span><span class="sxs-lookup"><span data-stu-id="0a960-239">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="0a960-240">Aggiunta della registrazione di correlationId per gli scenari di errore</span><span class="sxs-lookup"><span data-stu-id="0a960-240">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="0a960-241">Modifica di lieve entità alla documentazione di 'Get-AzResourceLock'.</span><span class="sxs-lookup"><span data-stu-id="0a960-241">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="0a960-242">Aggiunta dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="0a960-242">Added example.</span></span>
* <span data-ttu-id="0a960-243">Aggiunta della virgoletta singola come carattere di escape nel valore di parametro 'Get-AzADUser' [#11317]</span><span class="sxs-lookup"><span data-stu-id="0a960-243">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="0a960-244">Aggiunta di nuovi cmdlet per gli script di distribuzione ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span><span class="sxs-lookup"><span data-stu-id="0a960-244">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-245">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-245">Az.Sql</span></span>
* <span data-ttu-id="0a960-246">Aggiunta del parametro secondario leggibile a 'Invoke-AzSqlDatabaseFailover'</span><span class="sxs-lookup"><span data-stu-id="0a960-246">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="0a960-247">Aggiunta del cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span><span class="sxs-lookup"><span data-stu-id="0a960-247">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="0a960-248">Salvataggio della classificazione di riservatezza durante la classificazione delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="0a960-248">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="0a960-249">Az.Support</span><span class="sxs-lookup"><span data-stu-id="0a960-249">Az.Support</span></span>
* <span data-ttu-id="0a960-250">Disponibilità generale del modulo 'Az.Support'</span><span class="sxs-lookup"><span data-stu-id="0a960-250">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-251">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-251">Az.Websites</span></span>
* <span data-ttu-id="0a960-252">Aggiunta del supporto per l'uso delle regole di gestione del traffico delle app Web con i nuovi cmdlet seguenti</span><span class="sxs-lookup"><span data-stu-id="0a960-252">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="0a960-253">'Get-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="0a960-253">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a960-254">'Update-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="0a960-254">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a960-255">'Add-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="0a960-255">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="0a960-256">'Remove-AzWebAppTrafficRouting'</span><span class="sxs-lookup"><span data-stu-id="0a960-256">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="0a960-257">3.6.1 - Marzo 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-257">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-258">Az.Accounts</span></span>
* <span data-ttu-id="0a960-259">Apertura della pagina del sondaggio di Azure PowerShell in 'Send-Feedback' [#11020]</span><span class="sxs-lookup"><span data-stu-id="0a960-259">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="0a960-260">Visualizzazione dell'URL del sondaggio di Azure PowerShell in 'Resolve-Error' [#11021]</span><span class="sxs-lookup"><span data-stu-id="0a960-260">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="0a960-261">Aggiunta la versione Az in UserAgent</span><span class="sxs-lookup"><span data-stu-id="0a960-261">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-262">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-262">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-263">Aggiunta del supporto per il recupero e la configurazione di un dominio personalizzato nell'endpoint DeveloperPortal [#11007]</span><span class="sxs-lookup"><span data-stu-id="0a960-263">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="0a960-264">'Export-AzApiManagementApi': aggiunta del supporto per il download della definizione API in formato JSON [#9987]</span><span class="sxs-lookup"><span data-stu-id="0a960-264">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="0a960-265">'Import-AzApiManagementApi': aggiunta del supporto per l'importazione della definizione OpenApi 3.0 dal documento JSON</span><span class="sxs-lookup"><span data-stu-id="0a960-265">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="0a960-266">'New-AzApiManagementIdentityProvider' e 'Set-AzApiManagementIdentityProvider': aggiunta del supporto per la configurazione del 'tenant di accesso' per il provider AAD B2C [#9784]</span><span class="sxs-lookup"><span data-stu-id="0a960-266">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-267">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-267">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-268">Aggiunta del riferimento a System.Buffers in modo esplicito in csproj e psd1.</span><span class="sxs-lookup"><span data-stu-id="0a960-268">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-269">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-269">Az.IotHub</span></span>
* <span data-ttu-id="0a960-270">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-270">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0a960-271">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-271">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a960-272">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-272">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-273">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-273">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-274">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-274">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-275">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-275">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="0a960-276">Aggiunta del supporto per la gestione dei moduli in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-276">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="0a960-277">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-277">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a960-278">'Add-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0a960-278">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a960-279">'Get-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0a960-279">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a960-280">'Remove-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0a960-280">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="0a960-281">'Set-AzIotHubModule'</span><span class="sxs-lookup"><span data-stu-id="0a960-281">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="0a960-282">Aggiunta del cmdlet per ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-282">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0a960-283">Aggiunta del cmdlet per ottenere la stringa di connessione di un modulo in un dispositivo IoT di destinazione in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-283">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="0a960-284">Aggiunta del supporto per ottenere/impostare il dispositivo padre di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-284">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="0a960-285">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-285">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a960-286">'Get-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0a960-286">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="0a960-287">'Set-AzIotHubDeviceParent'</span><span class="sxs-lookup"><span data-stu-id="0a960-287">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="0a960-288">Aggiunta del supporto per gestire la relazione padre-figlio del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a960-288">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-289">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-289">Az.Monitor</span></span>
* <span data-ttu-id="0a960-290">Correzione del valore di output per 'Get-AzMetricDefinition' [#9714]</span><span class="sxs-lookup"><span data-stu-id="0a960-290">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-291">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-291">Az.Network</span></span>
* <span data-ttu-id="0a960-292">Aggiornamento di SQL Management SDK.</span><span class="sxs-lookup"><span data-stu-id="0a960-292">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="0a960-293">Correzione di un problema di differenza di denominazione nella classe PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="0a960-293">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="0a960-294">Mapping del campo ActionsRequired a ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="0a960-294">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="0a960-295">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="0a960-295">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-296">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-296">Az.Resources</span></span>
* <span data-ttu-id="0a960-297">Correzione per il bug di riferimento Null in 'Get-AzRoleAssignment'</span><span class="sxs-lookup"><span data-stu-id="0a960-297">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="0a960-298">Contrassegno delle opzioni '-Force' e '-PassThru' come facoltative in 'Remove-AzADGroup' [#10849]</span><span class="sxs-lookup"><span data-stu-id="0a960-298">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="0a960-299">Correzione del problema relativo alla mancata restituzione di 'MailNickname' in 'Remove-AzADGroup' [#11167]</span><span class="sxs-lookup"><span data-stu-id="0a960-299">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="0a960-300">Correzione del problema relativo al mancato funzionamento dell'operazione pipe 'Remove-AzADGroup' [#11171]</span><span class="sxs-lookup"><span data-stu-id="0a960-300">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="0a960-301">Correzione di un bug di riferimento Null in GetAzureRoleAssignmentCommand</span><span class="sxs-lookup"><span data-stu-id="0a960-301">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="0a960-302">Aggiunta degli attributi di modifica che causa un'interruzione per le modifiche imminenti ai cmdlet dei criteri</span><span class="sxs-lookup"><span data-stu-id="0a960-302">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="0a960-303">Aggiornamento di 'Get-AzResourceGroup' per l'esecuzione del filtro dei tag del gruppo di risorse sul lato server</span><span class="sxs-lookup"><span data-stu-id="0a960-303">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="0a960-304">Estensione dei cmdlet Tag per l'accettazione di -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-304">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="0a960-305">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-305">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0a960-306">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-306">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="0a960-307">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-307">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="0a960-308">Aggiunta di nuovi cmdlet Tag</span><span class="sxs-lookup"><span data-stu-id="0a960-308">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="0a960-309">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-309">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="0a960-310">Inclusione di ScopedDeployment da SDK 3.3.0</span><span class="sxs-lookup"><span data-stu-id="0a960-310">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-311">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-311">Az.Sql</span></span>
* <span data-ttu-id="0a960-312">Aggiunta di PublicNetworkAccess a 'New-AzSqlServer' e 'Set-AzSqlServer'</span><span class="sxs-lookup"><span data-stu-id="0a960-312">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="0a960-313">Aggiunta del supporto per la configurazione del backup con conservazione a lungo termine per i database gestiti</span><span class="sxs-lookup"><span data-stu-id="0a960-313">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="0a960-314">Recupero e impostazione dei criteri di conservazione a lungo termine su un database gestito</span><span class="sxs-lookup"><span data-stu-id="0a960-314">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="0a960-315">Recupero dei backup con conservazione a lungo termine per database gestito, istanza gestita o per posizione</span><span class="sxs-lookup"><span data-stu-id="0a960-315">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="0a960-316">Rimozione di un backup con conservazione a lungo termine</span><span class="sxs-lookup"><span data-stu-id="0a960-316">Remove an LTR backup</span></span>
    - <span data-ttu-id="0a960-317">Ripristino di un backup con conservazione a lungo termine per creare un nuovo database gestito</span><span class="sxs-lookup"><span data-stu-id="0a960-317">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="0a960-318">Aggiunta di MinimalTlsVersion a New-AzSqlServer e Set-AzSqlServer</span><span class="sxs-lookup"><span data-stu-id="0a960-318">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="0a960-319">Aggiunta di MinimalTlsVersion a New-AzSqlInstance e Set-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-319">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="0a960-320">Bump della versione di SQL SDK per Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-320">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-321">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-321">Az.Storage</span></span>
* <span data-ttu-id="0a960-322">Supporto di AllowProtectedAppendWrite in ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-322">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="0a960-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span><span class="sxs-lookup"><span data-stu-id="0a960-323">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="0a960-324">Aggiunta del messaggio di avviso per modifiche che causano un'interruzione relative alla modifica del tipo di AzureStorageTable in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0a960-324">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="0a960-325">'New-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0a960-325">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="0a960-326">'Get-AzStorageTable'</span><span class="sxs-lookup"><span data-stu-id="0a960-326">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-327">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-327">Az.Websites</span></span>
* <span data-ttu-id="0a960-328">Aggiunta del parametro Tag per 'New-AzAppServicePlan' e 'Set-AzAppServicePlan'</span><span class="sxs-lookup"><span data-stu-id="0a960-328">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="0a960-329">Arresto dell'esecuzione del cmdlet se viene generata un'eccezione durante l'aggiunta di un dominio personalizzato a un sito Web</span><span class="sxs-lookup"><span data-stu-id="0a960-329">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="0a960-330">Aggiunta del supporto per l'esecuzione di operazioni per i servizi app che non risiedono nello stesso gruppo di risorse del piano di servizio app</span><span class="sxs-lookup"><span data-stu-id="0a960-330">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="0a960-331">Applicazione della restrizione di accesso per app Web/funzioni in gruppi di risorse diversi</span><span class="sxs-lookup"><span data-stu-id="0a960-331">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="0a960-332">Correzione del problema per l'impostazione di nomi host personalizzati per WebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0a960-332">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="0a960-333">3.5.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-333">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-334">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-334">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-335">Aggiornamento dei dati di telemetria lato client.</span><span class="sxs-lookup"><span data-stu-id="0a960-335">Updated client side telemetry.</span></span>
* <span data-ttu-id="0a960-336">Aggiunta di cmdlet Az.IotHub per supportare la gestione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0a960-336">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="0a960-337">Aggiunta di cmdlet Az.SqlVirtualMachine per il listener del gruppo di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="0a960-337">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-338">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-338">Az.Accounts</span></span>
* <span data-ttu-id="0a960-339">Aggiunta di SubscriptionId, TenantId e tempo di esecuzione nei dati di telemetria lato client</span><span class="sxs-lookup"><span data-stu-id="0a960-339">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-340">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-340">Az.Automation</span></span>
* <span data-ttu-id="0a960-341">Correzione dell'errore di ortografia nell'esempio 1 della documentazione di riferimento per 'New-AzAutomationSoftwareUpdateConfiguration'</span><span class="sxs-lookup"><span data-stu-id="0a960-341">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-342">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-342">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-343">Aggiornamento dell'SDK alla versione 7.0</span><span class="sxs-lookup"><span data-stu-id="0a960-343">Updated SDK to 7.0</span></span>
* <span data-ttu-id="0a960-344">Miglioramento del messaggio di errore visualizzato quando il corpo delle risposte del server è vuoto</span><span class="sxs-lookup"><span data-stu-id="0a960-344">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-345">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-345">Az.Compute</span></span>
* <span data-ttu-id="0a960-346">Valore vuoto consentito per ProximityPlacementGroupId durante l'aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0a960-346">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-347">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-348">Aggiunta di un cmdlet per ottenere definizioni di regole gestite che è possibile usare in WAF</span><span class="sxs-lookup"><span data-stu-id="0a960-348">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-349">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-349">Az.IotHub</span></span>
* <span data-ttu-id="0a960-350">Aggiunta del supporto per la gestione dei dispositivi in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-350">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="0a960-351">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-351">New Cmdlets are:</span></span>
    - <span data-ttu-id="0a960-352">'Add-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-352">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-353">'Get-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-353">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-354">'Remove-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-354">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="0a960-355">'Set-AzIotHubDevice'</span><span class="sxs-lookup"><span data-stu-id="0a960-355">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-356">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-356">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-357">Correzione del testo duplicato per Add-AzKeyVaultKey.md</span><span class="sxs-lookup"><span data-stu-id="0a960-357">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-358">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-358">Az.Monitor</span></span>
* <span data-ttu-id="0a960-359">Correzione della descrizione del cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="0a960-359">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="0a960-360">Aggiunta di un nuovo parametro denominato ActionGroupId al comando 'New-AzMetricAlertRuleV2'.</span><span class="sxs-lookup"><span data-stu-id="0a960-360">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="0a960-361">L'utente può specificare ActionGroupId(string) o ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="0a960-361">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-362">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-362">Az.Network</span></span>
* <span data-ttu-id="0a960-363">Aggiunta di un'altra nota per il parametro '-EnableProxyProtocol' per il cmdlet 'New-AzPrivateLinkService'.</span><span class="sxs-lookup"><span data-stu-id="0a960-363">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="0a960-364">Correzione dell'esempio FilterData in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0a960-364">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a960-365">Aggiunta dell'esempio di acquisizione di tutti i pacchetti interni ed esterni in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md e Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="0a960-365">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="0a960-366">Supporto di criteri firewall di Azure nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-366">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="0a960-367">Nessun nuovo cmdlet aggiunto.</span><span class="sxs-lookup"><span data-stu-id="0a960-367">No new cmdlets are added.</span></span> <span data-ttu-id="0a960-368">Riduzione della restrizione per i criteri firewall nei firewall di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-368">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-369">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-370">Aggiunta del supporto del ripristino come file per database SQL.</span><span class="sxs-lookup"><span data-stu-id="0a960-370">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-371">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-371">Az.Resources</span></span>
* <span data-ttu-id="0a960-372">Refactoring dei cmdlet per la distribuzione di modelli</span><span class="sxs-lookup"><span data-stu-id="0a960-372">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="0a960-373">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nel gruppo di gestione: \*-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="0a960-373">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="0a960-374">Aggiunta di nuovi cmdlet per la gestione delle distribuzioni nell'ambito del tenant: \*-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="0a960-374">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="0a960-375">Refactoring dei cmdlet \*-AzDeployment per l'uso specifico nell'ambito della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="0a960-375">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="0a960-376">Creazione degli alias \*-AzSubscriptionDeployment per i cmdlet \*-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a960-376">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="0a960-377">Correzione di 'Update-AzADApplication' quando il parametro 'AvailableToOtherTenants' non è impostato</span><span class="sxs-lookup"><span data-stu-id="0a960-377">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="0a960-378">Rimozione di ApplicationObjectWithoutCredentialParameterSet per evitare AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="0a960-378">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="0a960-379">Rigenerazione dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-379">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-380">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-380">Az.Sql</span></span>
* <span data-ttu-id="0a960-381">Aggiunta del supporto per il ripristino temporizzato tra sottoscrizioni nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0a960-381">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="0a960-382">Aggiunta del supporto per la modifica della generazione dell'hardware per l'istanza gestita SQL esistente</span><span class="sxs-lookup"><span data-stu-id="0a960-382">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="0a960-383">Correzione degli esempi della Guida di 'Update-AzSqlServerVulnerabilityAssessmentSetting' help: output di parametri/proprietà - EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0a960-383">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a960-384">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a960-384">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a960-385">Aggiunta di cmdlet per il listener del gruppo di disponibilità</span><span class="sxs-lookup"><span data-stu-id="0a960-385">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a960-386">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a960-386">Az.StorageSync</span></span>
* <span data-ttu-id="0a960-387">Aggiornamento dei set di caratteri supportati in 'Invoke-AzStorageSyncCompatibilityCheck'.</span><span class="sxs-lookup"><span data-stu-id="0a960-387">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="0a960-388">3.4.0 - Febbraio 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-388">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-389">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-389">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-390">Rilascio della versione iniziale 0.1.0 di Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0a960-390">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="0a960-391">Aggiunta del supporto di Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="0a960-391">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-392">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-392">Az.Accounts</span></span>
* <span data-ttu-id="0a960-393">Disabilitazione del salvataggio automatico del contesto quando AzureRmContext.json non è disponibile</span><span class="sxs-lookup"><span data-stu-id="0a960-393">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="0a960-394">Aggiornamento del riferimento ad Azure PowerShell Common a 1.3.5-preview</span><span class="sxs-lookup"><span data-stu-id="0a960-394">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-395">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-395">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-396">**Get-AzApiManagementApiSchema** Risoluzione del problema nell'ottenere uno schema Open-API associato a un'API   https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="0a960-396">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="0a960-397">**New-AzApiManagementProduct**\* e **Set-AzApiManagementProduct**</span><span class="sxs-lookup"><span data-stu-id="0a960-397">**New-AzApiManagementProduct**\* and **Set-AzApiManagementProduct**</span></span>
  - <span data-ttu-id="0a960-398">Correzione della documentazione per https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="0a960-398">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="0a960-399">**Set-AzApiManagementApi** Aggiunto esempio per illustrare come aggiornare ServiceUrl usando il cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-399">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-400">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-400">Az.Compute</span></span>
* <span data-ttu-id="0a960-401">Limite del numero dello stato della macchina virtuale a 100 per evitare la limitazione quando viene eseguito Get-AzVM -Status senza il nome della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-401">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="0a960-402">Aggiunta del cmdlet Update-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0a960-402">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="0a960-403">Aggiunta dei parametri EncryptionType e DiskEncryptionSetId ai cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a960-403">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="0a960-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-404">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="0a960-405">Aggiunta del parametro ColocationStatus al cmdlet Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="0a960-405">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-406">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-406">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-407">Aggiornamento di ADF .NET SDK alla versione 4.7.0</span><span class="sxs-lookup"><span data-stu-id="0a960-407">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a960-408">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a960-408">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a960-409">Aggiunta di operazioni LIST per le risorse</span><span class="sxs-lookup"><span data-stu-id="0a960-409">Adds LIST operations for resources</span></span>
* <span data-ttu-id="0a960-410">Aggiunta della funzionalità per l'esecuzione di operazioni nei passaggi di controllo integrità</span><span class="sxs-lookup"><span data-stu-id="0a960-410">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-411">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-411">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-412">Correzione dell'errore di documentazione di New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="0a960-412">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-413">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-413">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-414">Aggiunta dell'alias Name all'attributo VaultName per rendere Remove-AzureKeyVault coerente con New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0a960-414">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-415">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-415">Az.Network</span></span>
* <span data-ttu-id="0a960-416">Aggiunto nuovo esempio a Set-AzNetworkWatcherConfigFlowLog.md per illustrare lo scenario di disabilitazione di Analisi del traffico.</span><span class="sxs-lookup"><span data-stu-id="0a960-416">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="0a960-417">Aggiunta del supporto per l'assegnazione della configurazione IP di gestione al Firewall di Azure: una subnet dedicata e un indirizzo IP pubblico che il firewall userà per il traffico di gestione</span><span class="sxs-lookup"><span data-stu-id="0a960-417">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="0a960-418">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0a960-418">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a960-419">Aggiunta del parametro -ManagementPublicIpAddress (non obbligatorio) che accetta un oggetto Indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0a960-419">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="0a960-420">Aggiunta del metodo SetManagementIpConfiguration nell'oggetto firewall. Richiede una subnet e un indirizzo IP pubblico come input. Il nome della subnet deve essere 'AzureFirewallManagementSubnet'</span><span class="sxs-lookup"><span data-stu-id="0a960-420">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="0a960-421">Correzione degli esempi di Get-AzNetworkSecurityGroup per mostrare esempi di gruppi di sicurezza di rete anziché di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="0a960-421">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="0a960-422">Correzione di un errore di digitazione nel comando New-AzVpnSite che impediva allo strumento di completamento dell'ID risorsa di completare un parametro.</span><span class="sxs-lookup"><span data-stu-id="0a960-422">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="0a960-423">Aggiunta del supporto per la configurazione dell'URL nel set di azioni delle regole di riscrittura nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0a960-423">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="0a960-424">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-424">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-425">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="0a960-426">Cmdlet aggiornati con il parametro facoltativo -UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-426">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="0a960-427">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a960-427">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="0a960-428">Aggiunta del supporto per le risorse di NetworkWatcher ConnectionMonitor versione 2</span><span class="sxs-lookup"><span data-stu-id="0a960-428">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-429">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-429">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-430">Supporto della valutazione della conformità prima di determinare la risorsa da correggere</span><span class="sxs-lookup"><span data-stu-id="0a960-430">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="0a960-431">Aggiunta del parametro '-ResourceDiscoverMode' a Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="0a960-431">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="0a960-432">Aggiunta del cmdlet Get-AzPolicyMetadata per ottenere le risorse metadati dei criteri</span><span class="sxs-lookup"><span data-stu-id="0a960-432">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="0a960-433">Aggiornamento di Get-AzPolicyState e Get-AzPolicyStateSummary per l'API versione 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="0a960-433">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-434">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-434">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-435">Supporto di Azure Site Recovery per la rimozione di un disco replicato.</span><span class="sxs-lookup"><span data-stu-id="0a960-435">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="0a960-436">Aggiunto il supporto di Backup di Azure per aggiungere tag durante la creazione di un insieme di credenziali di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a960-436">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-437">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-437">Az.Resources</span></span>
* <span data-ttu-id="0a960-438">-Scope diventato facoltativo nei cmdlet \*-AzPolicyAssignment con sottoscrizione del contesto predefinita</span><span class="sxs-lookup"><span data-stu-id="0a960-438">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="0a960-439">Aggiunta di esempi di creazione di ADServicePrincipal con password e credenziale della chiave</span><span class="sxs-lookup"><span data-stu-id="0a960-439">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-440">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-440">Az.Sql</span></span>
<span data-ttu-id="0a960-441">Correzione del cmdlet New-AzSqlDatabaseSecondary per verificare l'esistenza di PartnerDatabaseName anziché l'esistenza di DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0a960-441">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-442">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-442">Az.Storage</span></span>
* <span data-ttu-id="0a960-443">Supporto dell'impostazione del tipo di chiave di crittografia di tabelle/code nella creazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-443">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="0a960-444">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-444">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a960-445">Visualizzazione di RequestId quando StorageException non ha ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="0a960-445">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="0a960-446">Correzione dell'esempio 6 del cmdlet Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-446">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-447">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-447">Az.Websites</span></span>
* <span data-ttu-id="0a960-448">Supporto delle proprietà AlwaysOn, MinTls e FtpsState in Set-AzWebapp e Set-AzWebappSlot</span><span class="sxs-lookup"><span data-stu-id="0a960-448">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="0a960-449">Correzione di un problema per cui l'esecuzione contemporanea delle operazioni di impostazione di HttpsOnly e modifica di AppservicePlan con il singolo comando Set-AzWebApp comportava la reimpostazione del valore predefinito di HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="0a960-449">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="0a960-450">3.3.0 - Gennaio 2020</span><span class="sxs-lookup"><span data-stu-id="0a960-450">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-451">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-451">Az.Accounts</span></span>
* <span data-ttu-id="0a960-452">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare i parametri AzureAttestationServiceEndpointResourceId e AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="0a960-452">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-453">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-453">Az.Cdn</span></span>
* <span data-ttu-id="0a960-454">Visualizzazione dei dettagli della risposta di errore nel cmdlet New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-454">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-455">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-455">Az.Compute</span></span>
* <span data-ttu-id="0a960-456">Correzione del cmdlet Set-AzVMCustomScriptExtension per una macchina virtuale con disco gestito del sistema operativo senza profilo del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0a960-456">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a960-457">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-457">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a960-458">Correzione dei nomi di parametri usati dall'esempio di New-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-458">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a960-459">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a960-459">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a960-460">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0a960-460">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a960-461">Ottiene il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-461">Get the Edge Storage Container</span></span>
* <span data-ttu-id="0a960-462">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0a960-462">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a960-463">Crea un nuovo contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-463">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="0a960-464">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0a960-464">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a960-465">Rimuove il contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-465">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="0a960-466">Aggiunta del cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span><span class="sxs-lookup"><span data-stu-id="0a960-466">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="0a960-467">Richiama l'azione per aggiornare i dati nel contenitore di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-467">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="0a960-468">Aggiunta del cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0a960-468">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a960-469">Ottiene l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-469">Get the Edge Storage Account</span></span>
* <span data-ttu-id="0a960-470">Aggiunta del cmdlet 'New-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0a960-470">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a960-471">Crea un nuovo account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-471">Create new Edge Storage Account</span></span>
* <span data-ttu-id="0a960-472">Aggiunta del cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span><span class="sxs-lookup"><span data-stu-id="0a960-472">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="0a960-473">Rimuove l'account di archiviazione Edge</span><span class="sxs-lookup"><span data-stu-id="0a960-473">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="0a960-474">Richiama il cmdlet 'Invoke-AzDataBoxEdgeShare'</span><span class="sxs-lookup"><span data-stu-id="0a960-474">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="0a960-475">Richiama l'azione per aggiornare i dati nella condivisione</span><span class="sxs-lookup"><span data-stu-id="0a960-475">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="0a960-476">Aggiunta del cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span><span class="sxs-lookup"><span data-stu-id="0a960-476">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="0a960-477">Imposta le credenziali dell'account di archiviazione az databoxedge</span><span class="sxs-lookup"><span data-stu-id="0a960-477">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-478">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-478">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-479">Aggiunta delle proprietà AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId e VersionStatus per il cmdlet Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="0a960-479">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="0a960-480">Aggiornamento di ADF .NET SDK alla versione 4.6.0</span><span class="sxs-lookup"><span data-stu-id="0a960-480">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="0a960-481">Aggiunta del parametro 'PublicIPs' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare la creazione di Azure-SSIS IR con indirizzi IP pubblici statici.</span><span class="sxs-lookup"><span data-stu-id="0a960-481">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="0a960-482">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="0a960-482">Az.DevTestLabs</span></span>
* <span data-ttu-id="0a960-483">Rimozione del collegamento interrotto in Get-AzDtlAllowedVMSizesPolicy.md</span><span class="sxs-lookup"><span data-stu-id="0a960-483">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-484">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-484">Az.EventHub</span></span>
* <span data-ttu-id="0a960-485">Correzione del problema 10634: correzione del riferimento a un oggetto Null per la rimozione di eventhubnamespace</span><span class="sxs-lookup"><span data-stu-id="0a960-485">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-486">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-486">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-487">Correzione dell'errore Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="0a960-487">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a960-488">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a960-488">Az.MachineLearning</span></span>
* <span data-ttu-id="0a960-489">Rimozione dei cmdlet seguenti perché MachineLearningCompute non è più disponibile</span><span class="sxs-lookup"><span data-stu-id="0a960-489">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="0a960-490">Get-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a960-490">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a960-491">Get-AzMlOpClusterKey</span><span class="sxs-lookup"><span data-stu-id="0a960-491">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="0a960-492">New-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a960-492">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a960-493">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a960-493">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a960-494">Set-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="0a960-494">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="0a960-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span><span class="sxs-lookup"><span data-stu-id="0a960-495">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="0a960-496">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="0a960-496">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-497">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-497">Az.Network</span></span>
* <span data-ttu-id="0a960-498">Aggiornamento della dipendenza di Microsoft.Azure.Management.Sql da 1.36-preview a 1.37-preview</span><span class="sxs-lookup"><span data-stu-id="0a960-498">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-499">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-499">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-500">Modifica del supporto di Azure Site Recovery per le VM con dischi gestiti crittografati quando inattivi con le chiavi gestite dal cliente per il provider da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-500">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="0a960-501">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-501">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a960-502">Supporto di Azure Site Recovery per l'immissione dell'ID set di crittografia dischi come input facoltativo a livello di disco per abilitare la protezione per Vmware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-502">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="0a960-503">Supporto di Azure Site Recovery per l'aggiornamento di un elemento protetto da replica con la mappa del set di crittografia dischi per HyperV in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-503">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-504">Az.Resources</span></span>
* <span data-ttu-id="0a960-505">Correzione di un errore nel documento della Guida di 'Remove-AzTag'.</span><span class="sxs-lookup"><span data-stu-id="0a960-505">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-506">Az.Sql</span></span>
* <span data-ttu-id="0a960-507">Correzione della funzionalità dei cmdlet per la baseline del set di valutazioni per l'uso nel database master per il database di Azure e limitazione ai database di sistema con istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="0a960-507">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="0a960-508">Correzione di un errore durante la creazione del gruppo di failover dell'istanza di SQL</span><span class="sxs-lookup"><span data-stu-id="0a960-508">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="0a960-509">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="0a960-509">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="0a960-510">Aggiunta del ripristino di emergenza come nuovo tipo di licenza valido</span><span class="sxs-lookup"><span data-stu-id="0a960-510">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-511">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-511">Az.Storage</span></span>
* <span data-ttu-id="0a960-512">Aggiunta del messaggio di avviso per modifiche di rilievo relative al valore di DefaultAction in una versione futura</span><span class="sxs-lookup"><span data-stu-id="0a960-512">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="0a960-513">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-513">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="0a960-514">Supporto per ottenere l'ora dell'ultima sincronizzazione dell'account di archiviazione eseguendo get-AzureRMStorageAccount con il parametro -IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="0a960-514">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="0a960-515">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-515">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="0a960-516">3.2.0 - Dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-516">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="0a960-517">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-517">General</span></span>
* <span data-ttu-id="0a960-518">Aggiornamento dei riferimenti nel file con estensione psd1 per l'uso del percorso relativo per tutti i moduli</span><span class="sxs-lookup"><span data-stu-id="0a960-518">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-519">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-519">Az.Accounts</span></span>
* <span data-ttu-id="0a960-520">Impostazione del parametro UserAgent corretto per la telemetria lato client per l'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="0a960-520">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="0a960-521">Visualizzazione di un messaggio di errore descritto quando il contesto è Null nell'anteprima di Az 4.0</span><span class="sxs-lookup"><span data-stu-id="0a960-521">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a960-522">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-522">Az.Batch</span></span>
* <span data-ttu-id="0a960-523">Correzione del problema [#10602](https://github.com/Azure/azure-powershell/issues/10602), per cui **New-AzBatchPool** non invia correttamente 'VirtualMachineConfiguration.ContainerConfiguration' o 'VirtualMachineConfiguration.DataDisks' al server.</span><span class="sxs-lookup"><span data-stu-id="0a960-523">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-524">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-524">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-525">Aggiornamento di ADF .NET SDK alla versione 4.5.0</span><span class="sxs-lookup"><span data-stu-id="0a960-525">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-526">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-526">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-527">Aggiunta del supporto per l'esclusione di regole gestite di Web Application Firewall</span><span class="sxs-lookup"><span data-stu-id="0a960-527">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="0a960-528">Aggiunta di SocketAddr al completamento automatico</span><span class="sxs-lookup"><span data-stu-id="0a960-528">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a960-529">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a960-529">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a960-530">Gestione delle eccezioni</span><span class="sxs-lookup"><span data-stu-id="0a960-530">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-531">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-531">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-532">Correzione dell'errore relativo all'accesso di un valore potenzialmente non impostato</span><span class="sxs-lookup"><span data-stu-id="0a960-532">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="0a960-533">Gestione del certificato di crittografia a curva ellittica (ECC)</span><span class="sxs-lookup"><span data-stu-id="0a960-533">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="0a960-534">Aggiunta del supporto per la specifica della curva per i criteri del certificato</span><span class="sxs-lookup"><span data-stu-id="0a960-534">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-535">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-535">Az.Monitor</span></span>
* <span data-ttu-id="0a960-536">Aggiunta dell'argomento facoltativo al comando Aggiungi impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0a960-536">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="0a960-537">Un argomento switch che, se presente, indica che l'esportazione a Log Analytics deve essere uno schema fisso (ossia</span><span class="sxs-lookup"><span data-stu-id="0a960-537">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="0a960-538">un tipo di dati dedicato)</span><span class="sxs-lookup"><span data-stu-id="0a960-538">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-539">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-539">Az.Network</span></span>
* <span data-ttu-id="0a960-540">Supporto per IpGroups nelle regole dell'applicazione Firewall di Azure, NAT e rete.</span><span class="sxs-lookup"><span data-stu-id="0a960-540">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-541">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-541">Az.Resources</span></span>
* <span data-ttu-id="0a960-542">Correzione di un problema per cui durante la distribuzione di modelli non è possibile leggere un relativo parametro se il nome è in conflitto con il nome di un parametro predefinito.</span><span class="sxs-lookup"><span data-stu-id="0a960-542">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="0a960-543">Aggiornamento dei cmdlet dei criteri per l'uso della nuova versione 2019-09-01 dell'API che introduce il supporto del raggruppamento all'interno delle definizioni dei set di criteri.</span><span class="sxs-lookup"><span data-stu-id="0a960-543">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-544">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-544">Az.Sql</span></span>
* <span data-ttu-id="0a960-545">Aggiornamento a StorageV2 della creazione di spazio di archiviazione nell'abilitazione automatica di Valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="0a960-545">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-546">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-546">Az.Storage</span></span>
* <span data-ttu-id="0a960-547">Supporto della generazione di token di firma di accesso condiviso basati su identità di BLOB/contenitori con il contesto di archiviazione basato su autenticazione Oauth</span><span class="sxs-lookup"><span data-stu-id="0a960-547">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="0a960-548">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="0a960-548">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="0a960-549">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a960-549">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="0a960-550">Supporto del comando Revoca chiavi di delega utente dell'account di archiviazione, per cui vengono revocati tutti i token di firma di accesso condiviso basati su identità</span><span class="sxs-lookup"><span data-stu-id="0a960-550">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="0a960-551">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="0a960-551">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="0a960-552">Aggiornamento a Microsoft.Azure.Management.Storage 14.2.0 per supportare la nuova versione 2019-06-01 dell'API.</span><span class="sxs-lookup"><span data-stu-id="0a960-552">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="0a960-553">Supporto di QuotaGiB (quota di condivisione in Gibibyte) per valori maggiori di 5120 nel piano di gestione dei cmdlet di condivisione file e aggiunta dell'alias del parametro 'Quota' al parametro 'QuotaGiB'.</span><span class="sxs-lookup"><span data-stu-id="0a960-553">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="0a960-554">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-554">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="0a960-555">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-555">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="0a960-556">Aggiunta dell'alias 'QuotaGiB' al parametro 'Quota'</span><span class="sxs-lookup"><span data-stu-id="0a960-556">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="0a960-557">Set-AzStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="0a960-557">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="0a960-558">Correzione del problema per cui Set-AzStorageContainerAcl può pulire i criteri di accesso archiviati</span><span class="sxs-lookup"><span data-stu-id="0a960-558">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="0a960-559">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="0a960-559">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="0a960-560">3.1.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-560">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-561">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-561">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-562">Rilascio di Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-562">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="0a960-563">Rilascio di Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-563">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-564">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-564">Az.Compute</span></span>
* <span data-ttu-id="0a960-565">Funzionalità Riapplica macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-565">VM Reapply feature</span></span>
    - <span data-ttu-id="0a960-566">Aggiunta del parametro Reapply al cmdlet Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a960-566">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="0a960-567">Funzionalità di riparazione automatica del set di scalabilità di macchine virtuali:</span><span class="sxs-lookup"><span data-stu-id="0a960-567">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="0a960-568">Aggiunta dei parametri EnableAutomaticRepair, AutomaticRepairGracePeriod e AutomaticRepairMaxInstanceRepairsPercent ai cmdlet seguenti:   New-AzVmssConfig   Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-568">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="0a960-569">Supporto delle immagini della raccolta tra tenant per New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a960-569">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="0a960-570">Aggiunta di 'Spot ' al completer di argomenti del parametro Priority nei cmdlet New-AzVM, New-AzVMConfig e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-570">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a960-571">Aggiunta dei parametri DiskIOPSReadWrite e DiskMBpsReadWrite al cmdlet Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a960-571">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="0a960-572">Modifica del parametro SourceImageId del cmdlet New-AzGalleryImageVersion in facoltativo</span><span class="sxs-lookup"><span data-stu-id="0a960-572">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="0a960-573">Aggiunta dei parametri OSDiskImage e DataDiskImage al cmdlet New-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0a960-573">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="0a960-574">Aggiunta del parametro HyperVGeneration al cmdlet New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="0a960-574">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="0a960-575">Aggiunta dei parametri SkipExtensionsOnOverprovisionedVMs ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-575">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="0a960-576">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="0a960-576">Az.DataBoxEdge</span></span>
* <span data-ttu-id="0a960-577">Aggiunta del cmdlet `Get-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0a960-577">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a960-578">Recupera l'ordine</span><span class="sxs-lookup"><span data-stu-id="0a960-578">Get the Order</span></span>
* <span data-ttu-id="0a960-579">Aggiunta del cmdlet `New-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0a960-579">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a960-580">Crea un nuovo ordine</span><span class="sxs-lookup"><span data-stu-id="0a960-580">Create new Order</span></span>
* <span data-ttu-id="0a960-581">Aggiunta del cmdlet `Remove-AzDataBoxEdgeOrder`</span><span class="sxs-lookup"><span data-stu-id="0a960-581">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="0a960-582">Rimuove l'ordine</span><span class="sxs-lookup"><span data-stu-id="0a960-582">Remove the Order</span></span>
* <span data-ttu-id="0a960-583">Modifica nel cmdlet `New-AzDataBoxEdgeShare`</span><span class="sxs-lookup"><span data-stu-id="0a960-583">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="0a960-584">Ora crea una condivisione locale</span><span class="sxs-lookup"><span data-stu-id="0a960-584">Now creates Local Share</span></span>
* <span data-ttu-id="0a960-585">Aggiunta del cmdlet `Set-AzDataBoxEdgeRole`</span><span class="sxs-lookup"><span data-stu-id="0a960-585">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="0a960-586">Ora è possibile mappare IotRole alla condivisione</span><span class="sxs-lookup"><span data-stu-id="0a960-586">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="0a960-587">Aggiunta del cmdlet `Invoke-AzDataBoxEdgeDevice`</span><span class="sxs-lookup"><span data-stu-id="0a960-587">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="0a960-588">Richiama l'aggiornamento dell'analisi, scarica l'aggiornamento, installa gli aggiornamenti nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="0a960-588">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="0a960-589">Aggiunta del cmdlet `Get-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0a960-589">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a960-590">Recupera le informazioni sui trigger</span><span class="sxs-lookup"><span data-stu-id="0a960-590">Gets the information about Triggers</span></span>
* <span data-ttu-id="0a960-591">Aggiunta del cmdlet `New-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0a960-591">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a960-592">Crea nuovi trigger</span><span class="sxs-lookup"><span data-stu-id="0a960-592">Create new Triggers</span></span>
* <span data-ttu-id="0a960-593">Aggiunta del cmdlet `Remove-AzDataBoxEdgeTrigger`</span><span class="sxs-lookup"><span data-stu-id="0a960-593">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="0a960-594">Rimuove i trigger</span><span class="sxs-lookup"><span data-stu-id="0a960-594">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-595">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-595">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-596">Aggiornamento di ADF .NET SDK alla versione 4.4.0</span><span class="sxs-lookup"><span data-stu-id="0a960-596">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="0a960-597">Aggiunta del parametro 'ExpressCustomSetup' per il comando 'set-AzureRmDataFactoryV2IntegrationRuntime' per abilitare configurazioni di installazione e componenti di terze parti senza script di installazione personalizzato.</span><span class="sxs-lookup"><span data-stu-id="0a960-597">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-598">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-598">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-599">Aggiornamento della documentazione di Get-AzDataLakeStoreDeletedItem e Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="0a960-599">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-600">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-600">Az.EventHub</span></span>
* <span data-ttu-id="0a960-601">Correzione del problema 10301: correzione del formato data del token di firma di accesso condiviso</span><span class="sxs-lookup"><span data-stu-id="0a960-601">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-602">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-602">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-603">Aggiunta del parametro MinimumTlsVersion a Enable-AzFrontDoorCustomDomainHttps e New-AzFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="0a960-603">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="0a960-604">Aggiunta dei parametri HealthProbeMethod ed EnabledState a New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0a960-604">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="0a960-605">Aggiunta di un nuovo cmdlet per la creazione dell'oggetto BackendPoolsSettings da passare alla creazione/aggiornamento della frontdoor</span><span class="sxs-lookup"><span data-stu-id="0a960-605">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="0a960-606">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="0a960-606">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-607">Az.Network</span></span>
* <span data-ttu-id="0a960-608">Modifica degli esempi delle opzioni FilterData 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' e 'Start-AzVirtualnetworkGatewayPacketCapture.md'.</span><span class="sxs-lookup"><span data-stu-id="0a960-608">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="0a960-609">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="0a960-609">Az.PrivateDns</span></span>
* <span data-ttu-id="0a960-610">Aggiornamento di PrivateDns .NET SDK alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-610">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-611">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-611">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-612">Supporto di Azure Site Recovery per la selezione del tipo di disco durante l'abilitazione della protezione.</span><span class="sxs-lookup"><span data-stu-id="0a960-612">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="0a960-613">Correzione del bug di Azure Site Recovery relativo alla modifica dell'azione del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0a960-613">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="0a960-614">Supporto per l'accettazione dei database FileStream in Ripristino SQL di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-614">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a960-615">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a960-615">Az.RedisCache</span></span>
* <span data-ttu-id="0a960-616">Aggiunta del parametro 'MinimumTlsVersion' nei cmdlet 'New-AzRedisCache' e 'Set-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0a960-616">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="0a960-617">È stato anche aggiunto il parametro 'MinimumTlsVersion' nell'output del cmdlet 'Get-AzRedisCache'.</span><span class="sxs-lookup"><span data-stu-id="0a960-617">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="0a960-618">Aggiunta della convalida nel parametro '-Size' per i cmdlet 'Set-AzRedisCache' e 'New-AzRedisCache'</span><span class="sxs-lookup"><span data-stu-id="0a960-618">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-619">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-619">Az.Resources</span></span>
- <span data-ttu-id="0a960-620">Aggiornamento dei cmdlet per i criteri affinché usino la nuova versione API 2019-06-01 con la nuova proprietà EnforcementMode nell'assegnazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0a960-620">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="0a960-621">Aggiornamento dell'esempio della guida per la definizione dei criteri di creazione</span><span class="sxs-lookup"><span data-stu-id="0a960-621">Updated create policy definition help example</span></span>
- <span data-ttu-id="0a960-622">Correzione del bug relativo a Remove-AZADServicePrincipal-ServicePrincipalName, che genera un riferimento Null quando il nome dell'entità servizio non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0a960-622">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="0a960-623">Correzione del bug relativo a New-AZADServicePrincipal, che genera un riferimento Null quando il tenant non contiene sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0a960-623">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="0a960-624">Modifica di New-AzAdServicePrincipal per aggiungere le credenziali solo all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="0a960-624">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-625">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-625">Az.Sql</span></span>
* <span data-ttu-id="0a960-626">Aggiunta del supporto per ReadReplicaCount per il database.</span><span class="sxs-lookup"><span data-stu-id="0a960-626">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="0a960-627">Correzione di Set-AzSqlDatabase quando la ridondanza della zona non è impostata</span><span class="sxs-lookup"><span data-stu-id="0a960-627">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="0a960-628">3.0.0 - Novembre 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-628">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a960-629">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-629">General</span></span>
* <span data-ttu-id="0a960-630">Rilasciato AZ. PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-630">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-631">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-631">Az.Accounts</span></span>
* <span data-ttu-id="0a960-632">Aggiunta di un messaggio di deprecazione per l'alias 'Resolve-error'.</span><span class="sxs-lookup"><span data-stu-id="0a960-632">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a960-633">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a960-633">Az.Advisor</span></span>
* <span data-ttu-id="0a960-634">Aggiunta della nuova categoria 'Operational Excellence' al cmdlet Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="0a960-634">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a960-635">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-635">Az.Batch</span></span>
* <span data-ttu-id="0a960-636">Ridenominazione di `CoreQuota` in `DedicatedCoreQuota` per `BatchAccountContext`.</span><span class="sxs-lookup"><span data-stu-id="0a960-636">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="0a960-637">È disponibile anche un nuovo metodo `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="0a960-637">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="0a960-638">Questa modifica influisce su **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="0a960-638">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="0a960-639">Il parametro `-ResourceFile` di **New-AzBatchTask** ora accetta una raccolta di oggetti `PSResourceFile`, che può essere creata con il nuovo cmdlet **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="0a960-639">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="0a960-640">Nuovo cmdlet **New-AzBatchResourceFile** per semplificare la creazione di oggetti `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a960-640">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="0a960-641">Possono essere specificati in **New-AzBatchTask** nel parametro `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a960-641">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="0a960-642">Sono quindi supportati due nuovi tipi di file di risorse in aggiunta all'attuale `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="0a960-642">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="0a960-643">I file di risorse basati su `AutoStorageContainerName` scaricano un intero contenitore di archiviazione automatica nel nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="0a960-643">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="0a960-644">I file di risorse basati su `StorageContainerUrl` scaricano il contenitore specificato nell'URL del nodo Batch.</span><span class="sxs-lookup"><span data-stu-id="0a960-644">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="0a960-645">Rimozione della proprietà `ApplicationPackages` di `PSApplication` restituita da **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0a960-645">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a960-646">È ora possibile recuperare i pacchetti specifici all'interno di un'applicazione usando **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="0a960-646">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="0a960-647">Ad esempio: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="0a960-647">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="0a960-648">Ridenominazione di `ApplicationId` in `ApplicationName` per **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** e **set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="0a960-648">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="0a960-649">`ApplicationId` è ora un alias di `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="0a960-649">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="0a960-650">Aggiunta della nuova proprietà `PSWindowsUserConfiguration` a `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="0a960-650">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="0a960-651">Ridenominazione di `Version` in `Name` per `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="0a960-651">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="0a960-652">Ridenominazione di `BlobSource` in `HttpUrl` per `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="0a960-652">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="0a960-653">Rimozione della proprietà `OSDisk` da `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a960-653">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="0a960-654">Rimozione di **set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="0a960-654">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="0a960-655">Questa operazione non è più supportata.</span><span class="sxs-lookup"><span data-stu-id="0a960-655">This operation is no longer supported.</span></span>
* <span data-ttu-id="0a960-656">Rimozione di `TargetOSVersion` da `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a960-656">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a960-657">Ridenominazione di `CurrentOSVersion` in `OSVersion` per `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="0a960-657">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="0a960-658">Rimozione di `DataEgressGiB` e `DataIngressGiB` da `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="0a960-658">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="0a960-659">Rimozione di **Get-AzBatchNodeAgentSku** e sostituzione con **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="0a960-659">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="0a960-660">**Get-AzBatchSupportedImage** restituisce gli stessi dati di **Get-AzBatchNodeAgentSku** ma in un formato più intuitivo.</span><span class="sxs-lookup"><span data-stu-id="0a960-660">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="0a960-661">Vengono inoltre restituite nuove immagini non verificate.</span><span class="sxs-lookup"><span data-stu-id="0a960-661">New non-verified images are also now returned.</span></span> <span data-ttu-id="0a960-662">Sono incluse anche informazioni aggiuntive su `Capabilities` e `BatchSupportEndOfLife` per ogni immagine.</span><span class="sxs-lookup"><span data-stu-id="0a960-662">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="0a960-663">Aggiunta della possibilità di montare file system remoti in ogni nodo di un pool tramite il nuovo parametro `MountConfiguration` di **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="0a960-663">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="0a960-664">Sono ora supportate regole di sicurezza di rete che bloccano l'accesso di rete a un pool in base alla porta di origine del traffico.</span><span class="sxs-lookup"><span data-stu-id="0a960-664">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="0a960-665">Questa operazione viene eseguita tramite la proprietà `SourcePortRanges` in `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="0a960-665">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="0a960-666">Quando si esegue un contenitore, Batch supporta ora l'esecuzione dell'attività nella directory di lavoro del contenitore o in quella dell'attività Batch.</span><span class="sxs-lookup"><span data-stu-id="0a960-666">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="0a960-667">Questa operazione è controllata dalla proprietà `WorkingDirectory` in `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="0a960-667">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="0a960-668">Aggiunta della possibilità di specificare una raccolta di indirizzi IP pubblici in `PSNetworkConfiguration` tramite la nuova proprietà `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="0a960-668">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="0a960-669">Ciò garantisce che i nodi del pool avranno un indirizzo IP incluso nell'elenco di quelli specificati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0a960-669">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="0a960-670">Se non specificato, il valore predefinito di `WaitForSuccess` in `PSSTartTask` è ora `$True` (in precedenza era `$False`).</span><span class="sxs-lookup"><span data-stu-id="0a960-670">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="0a960-671">Se non specificato, il valore predefinito di `Scope` in `PSAutoUserSpecification` è ora `Pool` (in precedenza era `Task` in Windows e `Pool` in Linux).</span><span class="sxs-lookup"><span data-stu-id="0a960-671">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-672">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-672">Az.Cdn</span></span>
* <span data-ttu-id="0a960-673">Introduzione di UrlRewriteAction e CacheKeyQueryStringAction in RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="0a960-673">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="0a960-674">Correzione di diversi bug, ad esempio l'input 'Selector' mancante nel cmdlet New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="0a960-674">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-675">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-675">Az.Compute</span></span>
* <span data-ttu-id="0a960-676">Funzionalità Set di crittografia dischi</span><span class="sxs-lookup"><span data-stu-id="0a960-676">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="0a960-677">Nuovi cmdlet:   New-AzDiskEncryptionSetConfig New-AzDiskEncryptionSet Get-AzDiskEncryptionSet Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="0a960-677">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="0a960-678">Aggiunta del parametro DiskEncryptionSetId ai cmdlet seguenti:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a960-678">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="0a960-679">Aggiunta dei parametri DiskEncryptionSetId e EncryptionType ai cmdlet seguenti:   New-AzDiskConfig New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-679">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a960-680">Aggiunta del parametro PublicIPAddressVersion a New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-680">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="0a960-681">Spostamento di FileUris dell'estensione di script personalizzati dall'impostazione pubblica a quella protetta</span><span class="sxs-lookup"><span data-stu-id="0a960-681">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="0a960-682">Aggiunta di ScaleInPolicy ai cmdlet New-AzVmss, New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-682">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a960-683">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0a960-683">Breaking changes</span></span>
    - <span data-ttu-id="0a960-684">Quando CreateOption è Upload, per New-AzDiskConfig viene usato il parametro UploadSizeInBytes al posto di DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="0a960-684">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="0a960-685">PublishingProfile.Source.ManagedImage.Id è stato sostituito con StorageProfile.Source.Id nell'oggetto GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="0a960-685">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-686">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-686">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-687">Aggiornamento di ADF .NET SDK alla versione 4.3.0</span><span class="sxs-lookup"><span data-stu-id="0a960-687">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-688">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-688">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-689">Aggiornamento della versione di ADLS SDK (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), con le correzioni seguenti</span><span class="sxs-lookup"><span data-stu-id="0a960-689">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="0a960-690">Non viene generata un'eccezione se non è possibile deserializzare creationtime della voce trash o directory.</span><span class="sxs-lookup"><span data-stu-id="0a960-690">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="0a960-691">Esposizione dell'impostazione per timeout della richiesta in adlsclient</span><span class="sxs-lookup"><span data-stu-id="0a960-691">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="0a960-692">Correzione del passaggio di syncflag originale per il ripristino di badoffset</span><span class="sxs-lookup"><span data-stu-id="0a960-692">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="0a960-693">Correzione di EnumerateDirectory per il recupero del token di continuazione una volta verificata la risposta</span><span class="sxs-lookup"><span data-stu-id="0a960-693">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="0a960-694">Correzione del bug Concat</span><span class="sxs-lookup"><span data-stu-id="0a960-694">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-695">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-695">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-696">Correzione di vari errori di ortografia nei moduli</span><span class="sxs-lookup"><span data-stu-id="0a960-696">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-697">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-697">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-698">Correzione del bug per cui l'utente riceve un messaggio di errore analogo a 'La stringa non è una stringa Base 64 valida' quando usa Get-AzHDInsightCluster per ottenere il cluster con archiviazione ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="0a960-698">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="0a960-699">Aggiunta di un parametro denominato 'ApplicationId' ai tre cmdlet Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig e New-AzHDInsightCluster in modo che l'utente possa fornire l'ID applicazione dell'entità servizio per accedere ad Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0a960-699">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="0a960-700">Modifica di Microsoft.Azure.Management.HDInsight da 2.1.0 a 5.1.0</span><span class="sxs-lookup"><span data-stu-id="0a960-700">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="0a960-701">Rimozione di cinque cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-701">Removed five cmdlets:</span></span>
    - <span data-ttu-id="0a960-702">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a960-702">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a960-703">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a960-703">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a960-704">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="0a960-704">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="0a960-705">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a960-705">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="0a960-706">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a960-706">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="0a960-707">Aggiunta di tre cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-707">Added three cmdlets:</span></span>
    - <span data-ttu-id="0a960-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a960-708">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a960-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a960-709">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="0a960-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="0a960-710">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="0a960-711">Correzione del cmdlet Get-AzHDInsightProperties per supportare il recupero di informazioni sulle funzionalità da una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="0a960-711">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="0a960-712">Rimozione dei set di parametri ('Spark1', 'Spark2') da Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="0a960-712">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="0a960-713">Aggiunta di esempi nella documentazione per il cmdlet Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="0a960-713">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="0a960-714">Modifica del tipo di output per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a960-714">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="0a960-715">Modifica del tipo di output di Get-AzHDInsightProperties da CapabilitiesResponse a AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="0a960-715">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="0a960-716">Modifica del tipo di output di Remove-AzHDInsightCluster da ClusterGetResponse a bool.</span><span class="sxs-lookup"><span data-stu-id="0a960-716">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="0a960-717">Modifica del tipo di output di Set-AzHDInsightGatewaySettings da HttpConnectivitySettings a GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="0a960-717">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="0a960-718">Aggiunta di alcuni test case dello scenario.</span><span class="sxs-lookup"><span data-stu-id="0a960-718">Added some scenario test cases.</span></span>
* <span data-ttu-id="0a960-719">Rimozione di alcuni alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span><span class="sxs-lookup"><span data-stu-id="0a960-719">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-720">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-720">Az.IotHub</span></span>
* <span data-ttu-id="0a960-721">Modifiche di rilievo:</span><span class="sxs-lookup"><span data-stu-id="0a960-721">Breaking changes:</span></span>
    - <span data-ttu-id="0a960-722">Il cmdlet 'Add-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0a960-722">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a960-723">Il set di parametri '__AllParameterSets' per il cmdlet 'Add-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0a960-723">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a960-724">Il cmdlet 'Get-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0a960-724">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a960-725">Il set di parametri '__AllParameterSets' per il cmdlet 'Get-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0a960-725">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a960-726">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0a960-726">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="0a960-727">La proprietà 'OperationsMonitoringProperties' del tipo 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' è stata rimossa.</span><span class="sxs-lookup"><span data-stu-id="0a960-727">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="0a960-728">Il cmdlet 'New-AzIotHubExportDevice' non supporta più l'alias 'New-AzIotHubExportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0a960-728">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="0a960-729">Il cmdlet 'New-AzIotHubImportDevice' non supporta più l'alias 'New-AzIotHubImportDevices'.</span><span class="sxs-lookup"><span data-stu-id="0a960-729">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="0a960-730">Il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' non supporta più il parametro 'EventHubEndpointName' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0a960-730">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a960-731">Il set di parametri '__AllParameterSets' per il cmdlet 'Remove-AzIotHubEventHubConsumerGroup' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0a960-731">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="0a960-732">Il cmdlet 'Set-AzIotHub' non supporta più il parametro 'OperationsMonitoringProperties' e non è stato trovato alcun alias per il nome del parametro originale.</span><span class="sxs-lookup"><span data-stu-id="0a960-732">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="0a960-733">Il set di parametri 'UpdateOperationsMonitoringProperties' per il cmdlet 'Set-AzIotHub' è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="0a960-733">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-734">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-734">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-735">Supporto di Azure Site Recovery per la configurazione di risorse di rete come gruppi di sicurezza di rete, IP pubblico e servizi di bilanciamento del carico interni per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-735">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-736">Supporto di Azure Site Recovery per la scrittura nel disco gestito per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-736">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="0a960-737">Supporto di Azure Site Recovery per la riduzione delle schede di interfaccia di rete per VMware in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-737">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="0a960-738">Supporto di Azure Site Recovery per l'accelerazione di rete Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-738">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-739">Supporto di Azure Site Recovery per l'aggiornamento automatico dell'agente per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-739">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-740">Supporto di Azure Site Recovery per unità SSD Standard per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-740">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-741">Supporto di Azure Site Recovery per Crittografia dischi di Azure in due passaggi per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-741">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-742">Supporto di Azure Site Recovery per la protezione dei nuovi dischi aggiunti per Azure in Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-742">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-743">Aggiunta della funzionalità SoftDelete per VM e aggiunta di test per softdelete</span><span class="sxs-lookup"><span data-stu-id="0a960-743">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-744">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-744">Az.Resources</span></span>
* <span data-ttu-id="0a960-745">Aggiornamento dell'assembly di dipendenza Microsoft.Extensions.Caching.Memory da 1.1.1 a 2.2</span><span class="sxs-lookup"><span data-stu-id="0a960-745">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-746">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-746">Az.Network</span></span>
* <span data-ttu-id="0a960-747">Modifica di tutti i cmdlet per PrivateEndpointConnection per supportare il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="0a960-747">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="0a960-748">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0a960-748">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a960-749">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-749">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-750">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-750">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-751">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-751">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-752">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-752">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-753">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-753">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a960-754">Aggiunta di un nuovo cmdlet per PrivateLinkResource che supporta il provider di servizi generico.</span><span class="sxs-lookup"><span data-stu-id="0a960-754">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="0a960-755">Nuovo cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-755">New cmdlet:</span></span>
        - <span data-ttu-id="0a960-756">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="0a960-756">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="0a960-757">Aggiunta di nuovi campi e parametro per la funzionalità Proxy Protocol v2.</span><span class="sxs-lookup"><span data-stu-id="0a960-757">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="0a960-758">Aggiunta della proprietà EnableProxyProtocol in PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-758">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="0a960-759">Aggiunta della proprietà LinkIdentifier in PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-759">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="0a960-760">Aggiornamento di New-AzPrivateLinkService per aggiungere un nuovo parametro facoltativo EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="0a960-760">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="0a960-761">Correzione della descrizione del parametro non corretta nella documentazione di riferimento di 'New-AzApplicationGatewaySku'</span><span class="sxs-lookup"><span data-stu-id="0a960-761">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="0a960-762">Nuovi cmdlet per il supporto dei criteri firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-762">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="0a960-763">Aggiunta del supporto per la risorsa figlio RouteTables di VirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a960-763">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="0a960-764">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-764">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-765">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="0a960-765">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="0a960-766">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-766">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a960-767">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-767">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a960-768">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-768">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="0a960-769">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="0a960-769">Set-AzVirtualHub</span></span>
* <span data-ttu-id="0a960-770">Aggiunta del supporto per le nuove proprietà Sku di VirtualHub e VirtualWANType di VirtualWan</span><span class="sxs-lookup"><span data-stu-id="0a960-770">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="0a960-771">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0a960-771">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a960-772">New-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="0a960-772">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a960-773">Update-AzVirtualHub: aggiunta del parametro Sku</span><span class="sxs-lookup"><span data-stu-id="0a960-773">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="0a960-774">New-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0a960-774">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="0a960-775">Update-AzVirtualWan: aggiunta del parametro VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="0a960-775">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="0a960-776">Aggiunta del supporto per la proprietà EnableInternetSecurity per HubVnetConnection, VpnConnection e ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-776">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="0a960-777">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-777">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-778">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-778">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="0a960-779">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0a960-779">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a960-780">New-AzureRmVirtualHubVnetConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a960-780">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a960-781">New-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a960-781">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a960-782">Update-AzureRmVpnConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a960-782">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a960-783">New-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a960-783">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="0a960-784">Set-AzureRmExpressRouteConnection: aggiunta del parametro EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="0a960-784">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="0a960-785">Aggiunta del supporto per la configurazione del criterio TopLevel WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="0a960-785">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="0a960-786">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-786">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-787">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="0a960-787">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="0a960-788">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="0a960-788">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="0a960-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="0a960-789">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="0a960-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="0a960-790">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="0a960-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a960-791">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="0a960-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-792">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="0a960-793">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0a960-793">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a960-794">New-AzApplicationGatewayFirewallPolicy: aggiunta del parametro PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="0a960-794">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="0a960-795">Aggiunta del supporto per l'operatore di corrispondenza geografica in CustomRule</span><span class="sxs-lookup"><span data-stu-id="0a960-795">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="0a960-796">Aggiunta di GeoMatch all'operatore in FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="0a960-796">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="0a960-797">Aggiunta del supporto per i criteri firewall perListener e perSite</span><span class="sxs-lookup"><span data-stu-id="0a960-797">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="0a960-798">Aggiornamento di cmdlet con parametri facoltativi:</span><span class="sxs-lookup"><span data-stu-id="0a960-798">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="0a960-799">New-AzApplicationGatewayHttpListener: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a960-799">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="0a960-800">New-AzApplicationGatewayPathRuleConfig: aggiunta del parametro FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="0a960-800">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="0a960-801">Correzione della subnet richiesta con il nome AzureBastionSubnet in 'PSBastion' che può essere senza distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="0a960-801">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="0a960-802">Supporto per FQDN di destinazione nelle regole di rete e per FQDN tradotto nelle regole NAT per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-802">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="0a960-803">Aggiunta del supporto per la risorsa di primo livello RouteTables di IpGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-803">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="0a960-804">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-804">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-805">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-805">New-AzIpGroup</span></span>
        - <span data-ttu-id="0a960-806">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-806">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="0a960-807">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-807">Get-AzIpGroup</span></span>
        - <span data-ttu-id="0a960-808">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-808">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-809">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-809">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-810">Rimozione del cmdlet Add-AzServiceFabricApplicationCertificate perché questo scenario è gestito da Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="0a960-810">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-811">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-811">Az.Sql</span></span>
* <span data-ttu-id="0a960-812">Aggiunta del supporto per il ripristino dei database eliminati nelle istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0a960-812">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="0a960-813">Deprecazione dei vecchi cmdlet di controllo dal codice.</span><span class="sxs-lookup"><span data-stu-id="0a960-813">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="0a960-814">Rimozione di alias deprecati:</span><span class="sxs-lookup"><span data-stu-id="0a960-814">Removed deprecated aliases:</span></span>
* <span data-ttu-id="0a960-815">Get-AzSqlDatabaseIndexRecommendations (usare invece Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="0a960-815">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="0a960-816">Get-AzSqlDatabaseRestorePoints (usare invece Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="0a960-816">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="0a960-817">Rimozione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-817">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a960-818">Rimozione degli alias per i cmdlet delle impostazioni di Valutazione della vulnerabilità deprecati</span><span class="sxs-lookup"><span data-stu-id="0a960-818">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="0a960-819">Deprecazione dei cmdlet delle impostazioni di Rilevamento minacce avanzato</span><span class="sxs-lookup"><span data-stu-id="0a960-819">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="0a960-820">Aggiunta di cmdlet per disabilitare e abilitare le raccomandazioni sulla riservatezza per le colonne dei database.</span><span class="sxs-lookup"><span data-stu-id="0a960-820">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-821">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-821">Az.Storage</span></span>
* <span data-ttu-id="0a960-822">Supporto per la condivisione di file di grandi dimensioni quando si crea o si aggiorna un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-822">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="0a960-823">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-823">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a960-824">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-824">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a960-825">Quando si usa l'handle di file Close/Get, il controllo del percorso di input per verificare se è directory di file o file viene ignorato per evitare errori con l'oggetto nello stato DeletePending</span><span class="sxs-lookup"><span data-stu-id="0a960-825">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="0a960-826">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a960-826">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="0a960-827">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a960-827">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="0a960-828">2.8.0 - ottobre 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-828">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="0a960-829">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-829">General</span></span>
* <span data-ttu-id="0a960-830">Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-830">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-831">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-831">Az.Accounts</span></span>
* <span data-ttu-id="0a960-832">Aggiornamento dei dati di telemetria e riscrittura degli URL per i moduli generati, correzione degli unit test di Windows.</span><span class="sxs-lookup"><span data-stu-id="0a960-832">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-833">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-833">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-834">**Set-AzApiManagementApi**: aggiunta del supporto per l'aggiornamento API in ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="0a960-834">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="0a960-835">correzione del problema https://github.com/Azure/azure-powershell/issues/10068</span><span class="sxs-lookup"><span data-stu-id="0a960-835">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-836">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-836">Az.Automation</span></span>
* <span data-ttu-id="0a960-837">Correzione del cmdlet New-AzureAutomationSoftwareUpdateConfiguration per il parametro dell'impostazione di riavvio di Linux.</span><span class="sxs-lookup"><span data-stu-id="0a960-837">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a960-838">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-838">Az.Batch</span></span>
* <span data-ttu-id="0a960-839">**Get-AzBatchNodeAgentSku** è deprecato e sarà sostituito da **Get-AzBatchSupportImage** nella versione 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a960-839">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-840">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-840">Az.Compute</span></span>
* <span data-ttu-id="0a960-841">Aggiunta dei parametri Priority, EvictionPolicy e MaxPrice ai cmdlet New-AzVM e New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-841">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="0a960-842">Correzione di un messaggio di avviso e di un documento della Guida per i cmdlet Add-AzVMAdditionalUnattendContent e Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="0a960-842">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="0a960-843">Correzione dell'eccezione -skipVmBackup per le VM Linux con dischi gestiti per set-AzVMDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="0a960-843">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="0a960-844">Correzione di un bug nell'aggiornamento delle impostazioni di crittografia in Set-AzVMDiskEncryptionExtension, scenario di crittografia in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="0a960-844">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-845">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-845">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-846">Aggiunta di comandi CRUD per il flusso di dati Azure Data Factory V2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow e Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="0a960-846">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="0a960-847">Aggiunta di comandi di azione per la sessione di debug del flusso di dati Azure Data Factory V2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand e Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="0a960-847">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="0a960-848">Aggiornamento di ADF .NET SDK alla versione 4.2.0</span><span class="sxs-lookup"><span data-stu-id="0a960-848">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-849">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-849">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-850">Correzione della convalida degli account in modo che gli account che contengono "-" possano essere passati senza dominio</span><span class="sxs-lookup"><span data-stu-id="0a960-850">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="0a960-851">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="0a960-851">Az.HealthcareApis</span></span>
* <span data-ttu-id="0a960-852">Aggiornamento di PowerShell alla versione 1.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-852">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="0a960-853">Aggiornamento dell'SDK alla versione 1.0.2</span><span class="sxs-lookup"><span data-stu-id="0a960-853">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="0a960-854">Aggiornamento nei test per fare riferimento alla nuova versione dell'SDK</span><span class="sxs-lookup"><span data-stu-id="0a960-854">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="0a960-855">Aggiornamento della struttura dell'output da annidata ad appiattita.</span><span class="sxs-lookup"><span data-stu-id="0a960-855">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-856">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-856">Az.IotHub</span></span>
* <span data-ttu-id="0a960-857">Aggiunta di una nuova origine di routing: DigitalTwinChangeEvents</span><span class="sxs-lookup"><span data-stu-id="0a960-857">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="0a960-858">Correzione di bug di minore entità: Get-AzIothub non restituisce subscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a960-858">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-859">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-859">Az.Monitor</span></span>
* <span data-ttu-id="0a960-860">Nuovi ricevitori di gruppi di azioni aggiunti per il gruppo di azioni   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="0a960-860">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="0a960-861">Uso dello schema di avviso comune abilitato per i ricevitori.</span><span class="sxs-lookup"><span data-stu-id="0a960-861">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="0a960-862">Non applicabile per ricevitori di servizi vocali, SMS, push di Azure App e Gestione dei servizi IT</span><span class="sxs-lookup"><span data-stu-id="0a960-862">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="0a960-863">I webhook supportano ora l'autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0a960-863">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-864">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-864">Az.Network</span></span>
* <span data-ttu-id="0a960-865">Aggiunta del nuovo cmdlet Get-AzAvailableServiceAlias che può essere chiamato per ottenere gli alias che possono essere usati per i criteri dell'endpoint di servizio.</span><span class="sxs-lookup"><span data-stu-id="0a960-865">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="0a960-866">Aggiunta del supporto per l'aggiunta di selettori del traffico a connessioni del gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-866">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="0a960-867">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-867">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-868">New-AzureRmTrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-868">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="0a960-869">Cmdlet aggiornati con parametro facoltativo -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-869">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a960-870">Aggiunta del supporto per i protocolli ESP e AH nelle configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="0a960-870">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="0a960-871">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-871">Updated cmdlets:</span></span>
        - <span data-ttu-id="0a960-872">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-872">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a960-873">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-873">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a960-874">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-874">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a960-875">Miglioramento della gestione delle eccezioni nei cmdlet Cortex</span><span class="sxs-lookup"><span data-stu-id="0a960-875">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="0a960-876">Nuove generazioni e SKU per VirtualNetworkGateways</span><span class="sxs-lookup"><span data-stu-id="0a960-876">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="0a960-877">Introduzione di nuove generazioni per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0a960-877">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="0a960-878">Introduzione di nuovi SKU a velocità effettiva elevata per VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="0a960-878">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a960-879">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a960-879">Az.RedisCache</span></span>
* <span data-ttu-id="0a960-880">Aggiornamento della documentazione di riferimento di "Set-AzRedisCache" per includere i valori mancanti per il parametro "-Size"</span><span class="sxs-lookup"><span data-stu-id="0a960-880">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-881">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-881">Az.Sql</span></span>
* <span data-ttu-id="0a960-882">Aggiunta del supporto per l'impostazione dell'amministratore di Active Directory in Istanza gestita</span><span class="sxs-lookup"><span data-stu-id="0a960-882">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-883">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-883">Az.Storage</span></span>
* <span data-ttu-id="0a960-884">Aggiornamento della libreria client di Archiviazione di Azure alla versione 11.1.0</span><span class="sxs-lookup"><span data-stu-id="0a960-884">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="0a960-885">Elenco dei contenitori con l'API del piano di gestione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0a960-885">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a960-886">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0a960-886">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="0a960-887">Elenco degli account di archiviazione dalla sottoscrizione, elencati con NextPageLink</span><span class="sxs-lookup"><span data-stu-id="0a960-887">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="0a960-888">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-888">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a960-889">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a960-889">Az.StorageSync</span></span>
* <span data-ttu-id="0a960-890">Correzione del problema 9810 in Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="0a960-890">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-891">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-891">Az.Websites</span></span>
* <span data-ttu-id="0a960-892">Set-AzWebApp: aggiornamento del piano di servizio app di un'app non riuscito</span><span class="sxs-lookup"><span data-stu-id="0a960-892">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="0a960-893">2.7.0 - Settembre 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-893">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a960-894">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-894">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-895">Aggiornamento della descrizione del parametro '-Format' nella documentazione di riferimento su 'Set-AzApiManagementPolicy'</span><span class="sxs-lookup"><span data-stu-id="0a960-895">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="0a960-896">Rimozione dei riferimenti del cmdlet deprecato ' Update-AzApiManagementDeployment ' dalla documentazione di riferimento.</span><span class="sxs-lookup"><span data-stu-id="0a960-896">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="0a960-897">Usare invece 'set-AzApiManagement'.</span><span class="sxs-lookup"><span data-stu-id="0a960-897">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-898">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-898">Az.Automation</span></span>
* <span data-ttu-id="0a960-899">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Register-AzAutomationDscNode'</span><span class="sxs-lookup"><span data-stu-id="0a960-899">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="0a960-900">Aggiunta di chiarimenti sulla restrizione del sistema operativo a Register-AzAutomationDSCNode</span><span class="sxs-lookup"><span data-stu-id="0a960-900">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="0a960-901">Correzione dell'eccezione di riferimento Null nel cmdlet Start-AzAutomationRunbook per l'opzione -Wait.</span><span class="sxs-lookup"><span data-stu-id="0a960-901">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-902">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-902">Az.Compute</span></span>
* <span data-ttu-id="0a960-903">Aggiunta del parametro UploadSizeInBytes a New-AzDiskConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-903">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="0a960-904">Aggiunta del parametro Incremental a New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-904">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a960-905">Aggiunta di una funzionalità di macchina virtuale a priorità bassa:</span><span class="sxs-lookup"><span data-stu-id="0a960-905">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="0a960-906">Aggiunta dei parametri MaxPrice, EvictionPolicy e Priority a New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="0a960-906">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="0a960-907">Aggiunta del parametro MaxPrice ai cmdlet New-AzVmssConfig, Update-AzVM e Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a960-907">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="0a960-908">Correzione del problema del riferimento alle VM per il cmdlet Get-AzAvailabilitySet quando elenca tutti i set di disponibilità presenti nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a960-908">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="0a960-909">Correzione dell'eccezione Null per Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="0a960-909">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="0a960-910">Correzione del metodo Seek dei dischi rigidi virtuali per la posizione relativa alla fine.</span><span class="sxs-lookup"><span data-stu-id="0a960-910">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="0a960-911">Correzione del problema relativo a UltraSSD per New-AzVM e Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="0a960-911">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-912">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-912">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-913">Aggiunta di 3 nuovi comandi per ADF V2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription e Get-AzDataFactoryV2TriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="0a960-913">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="0a960-914">Aggiornamento di ADF .NET SDK alla versione 4.1.3</span><span class="sxs-lookup"><span data-stu-id="0a960-914">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-915">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-915">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-916">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0a960-916">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-917">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-917">Az.IotHub</span></span>
* <span data-ttu-id="0a960-918">Aggiunta del supporto per richiamare il failover per un hub IoT nell'area di ripristino di emergenza geograficamente abbinata.</span><span class="sxs-lookup"><span data-stu-id="0a960-918">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="0a960-919">Aggiunta del supporto per gestire l'arricchimento di messaggi per un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="0a960-919">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="0a960-920">I nuovi cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="0a960-920">New cmdlets are:</span></span>
    - <span data-ttu-id="0a960-921">Add-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a960-921">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a960-922">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a960-922">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a960-923">Remove-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a960-923">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="0a960-924">Set-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="0a960-924">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-925">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-925">Az.Monitor</span></span>
* <span data-ttu-id="0a960-926">Puntamento alla versione più recente di Monitor SKD, ossia 0.24.1 (anteprima)</span><span class="sxs-lookup"><span data-stu-id="0a960-926">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="0a960-927">Aggiunta di modifiche non di rilievo ai cmdlet Metrics, ossia supporto di numerosi nuovi valori nell'enumerazione Unit.</span><span class="sxs-lookup"><span data-stu-id="0a960-927">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="0a960-928">Questi cmdlet sono di sola lettura, quindi il relativo input non cambia.</span><span class="sxs-lookup"><span data-stu-id="0a960-928">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="0a960-929">La versione API delle richieste **ActionGroups** è ora **2019-06-01**, prima era **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="0a960-929">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="0a960-930">I test dello scenario sono stati aggiornati per riflettere questa modifica.</span><span class="sxs-lookup"><span data-stu-id="0a960-930">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="0a960-931">Nei costruttori per le classi **EmailReceiver** e **WebhookReceiver** è stato aggiunto un nuovo argomento obbligatorio, ossia un valore booleano denominato **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="0a960-931">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="0a960-932">Attualmente il valore è fisso su **false** per nascondere questa modifica di rilievo ai cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a960-932">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="0a960-933">**NOTA**: questa è una modifica temporanea che deve essere convalidata dal team degli avvisi.</span><span class="sxs-lookup"><span data-stu-id="0a960-933">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="0a960-934">L'ordine degli argomenti per il costruttore della classe **Source** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="0a960-934">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a960-935">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="0a960-935">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="0a960-936">L'ordine degli argomenti per il costruttore della classe **AlertingAction** (correlata alla classe **ScheduledQueryRuleSource**) è cambiato rispetto all'SDK precedente.</span><span class="sxs-lookup"><span data-stu-id="0a960-936">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="0a960-937">Questa modifica ha richiesto la correzione di due unit test: venivano compilati, ma non superavano i test.</span><span class="sxs-lookup"><span data-stu-id="0a960-937">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="0a960-938">Supporto dei criteri di soglia dinamica per l'avviso della metrica V2</span><span class="sxs-lookup"><span data-stu-id="0a960-938">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="0a960-939">New-AzMetricAlertRuleV2Criteria: ora crea anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="0a960-939">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="0a960-940">Add-AzMetricAlertRuleV2: ora accetta anche criteri di soglia dinamica</span><span class="sxs-lookup"><span data-stu-id="0a960-940">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="0a960-941">Miglioramenti dei cmdlet Scheduled Query Rule (SQR)</span><span class="sxs-lookup"><span data-stu-id="0a960-941">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="0a960-942">I cmdlet accettano il parametro 'Location' in entrambi i formati, ossia la posizione (ad esempio eastus) o il nome visualizzato della posizione (ad esempio Stati Uniti orientali)</span><span class="sxs-lookup"><span data-stu-id="0a960-942">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="0a960-943">Descrizione corretta del parametro 'Enabled' nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-943">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="0a960-944">Aggiunta di esempi per il parametro facoltativo 'ActionGroup'</span><span class="sxs-lookup"><span data-stu-id="0a960-944">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="0a960-945">Miglioramento generale dei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-945">Overall improved help files</span></span>
* <span data-ttu-id="0a960-946">Correzione di un bug quando si determina il tipo di ambito per 'Set-AzActionRule'</span><span class="sxs-lookup"><span data-stu-id="0a960-946">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-947">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-947">Az.Network</span></span>
* <span data-ttu-id="0a960-948">Correzione di un esempio errato nella documentazione di riferimento di 'New-AzApplicationGateway'</span><span class="sxs-lookup"><span data-stu-id="0a960-948">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="0a960-949">Aggiunta di una nota nella documentazione di riferimento di 'Get-AzNetworkWatcherPacketCapture' sul recupero di tutte le proprietà per l'acquisizione di un pacchetto</span><span class="sxs-lookup"><span data-stu-id="0a960-949">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="0a960-950">Correzione di un esempio nella documentazione di riferimento di 'Test-AzNetworkWatcherIPFlow' per l'enumerazione corretta delle schede di interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="0a960-950">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="0a960-951">Miglioramento dell'analisi delle eccezioni cloud per visualizzare dettagli aggiuntivi, se presenti</span><span class="sxs-lookup"><span data-stu-id="0a960-951">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="0a960-952">Miglioramento dell'analisi delle eccezioni cloud per gestire un tipo aggiuntivo di eccezione SDK</span><span class="sxs-lookup"><span data-stu-id="0a960-952">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="0a960-953">Correzione del mapping errato di modelli di regole di sicurezza</span><span class="sxs-lookup"><span data-stu-id="0a960-953">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="0a960-954">Aggiunta di proprietà all'interfaccia di rete per la funzionalità di IP privato</span><span class="sxs-lookup"><span data-stu-id="0a960-954">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="0a960-955">Aggiunta della proprietà 'PrivateEndpoint' come tipo di PSResourceId a PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="0a960-955">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="0a960-956">Aggiunta della proprietà 'PrivateLinkConnectionProperties' come tipo di PSIpConfigurationConnectivityInformation a PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-956">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="0a960-957">Aggiunta della nuova classe modello PSIpConfigurationConnectivityInformation</span><span class="sxs-lookup"><span data-stu-id="0a960-957">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="0a960-958">Aggiunta della nuova risorsa ApplicationRuleProtocolType 'mssql' per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-958">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="0a960-959">Supporto di MultiLink nella rete WAN virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-959">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="0a960-960">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-960">New cmdlets</span></span>
        - <span data-ttu-id="0a960-961">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="0a960-961">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="0a960-962">New-AzVpnSiteLinkConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-962">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="0a960-963">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0a960-963">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a960-964">New-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0a960-964">New-VpnSite</span></span>
        - <span data-ttu-id="0a960-965">Update-VpnSite</span><span class="sxs-lookup"><span data-stu-id="0a960-965">Update-VpnSite</span></span>
        - <span data-ttu-id="0a960-966">New-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-966">New-VpnConnection</span></span>
        - <span data-ttu-id="0a960-967">Update-VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-967">Update-VpnConnection</span></span>
* <span data-ttu-id="0a960-968">Correzione dei documenti relativi ad alcuni esempi di PowerShell per l'uso dei cmdlet Az invece dei cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="0a960-968">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-969">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-969">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-970">Aggiornamento dell'oggetto AzureVMpolicy con l'attributo ProtectedItemsCount</span><span class="sxs-lookup"><span data-stu-id="0a960-970">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="0a960-971">Aggiunta di test per i criteri delle VM e il ripristino dell'account di archiviazione originale</span><span class="sxs-lookup"><span data-stu-id="0a960-971">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-972">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-972">Az.Resources</span></span>
* <span data-ttu-id="0a960-973">Correzione del bug per cui non è possibile chiamare New-AzRoleAssignment senza il parametro Scope.</span><span class="sxs-lookup"><span data-stu-id="0a960-973">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-974">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-974">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-975">Correzione di un errore ortografico in un esempio della documentazione di riferimento di 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0a960-975">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="0a960-976">Aggiunta di nuovi cmdlet per la gestione di applicazioni e servizi:</span><span class="sxs-lookup"><span data-stu-id="0a960-976">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="0a960-977">New-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a960-977">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a960-978">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a960-978">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a960-979">New-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a960-979">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a960-980">New-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0a960-980">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a960-981">Update-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a960-981">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a960-982">Get-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a960-982">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a960-983">Get-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a960-983">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a960-984">Get-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a960-984">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a960-985">Get-AzServiceFabricService</span><span class="sxs-lookup"><span data-stu-id="0a960-985">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="0a960-986">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="0a960-986">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="0a960-987">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0a960-987">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="0a960-988">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0a960-988">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="0a960-989">Remove-AzServiceFabricServic</span><span class="sxs-lookup"><span data-stu-id="0a960-989">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="0a960-990">Aggiornamento di Service Fabric SDK alla versione 1.2.0 che usa la versione API 2019-03-01 del provider di risorse di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0a960-990">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a960-991">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a960-991">Az.SignalR</span></span>
* <span data-ttu-id="0a960-992">Aggiunta dei cmdlet Update, Restart, CheckNameAvailability, GetUsage</span><span class="sxs-lookup"><span data-stu-id="0a960-992">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-993">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-993">Az.Sql</span></span>
* <span data-ttu-id="0a960-994">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzSqlElasticPool'</span><span class="sxs-lookup"><span data-stu-id="0a960-994">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="0a960-995">Aggiunta di un esempio di vCore per la creazione di pool elastici (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="0a960-995">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="0a960-996">Rimozione della convalida di EmailAddresses e della verifica che EmailAdmins non sia False nel caso in cui EmailAddresses sia vuoto in Set-AzSqlServerAdvancedThreatProtectionPolicy e Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-996">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="0a960-997">Abilitazione della rimozione di impostazioni di controllo di server/database quando esistono più impostazioni di diagnostica che abilitano la categoria di controllo.</span><span class="sxs-lookup"><span data-stu-id="0a960-997">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="0a960-998">Correzione della convalida di indirizzi di posta elettronica in più cmdlet Sql Vulnerability Assessment (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting e Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="0a960-998">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-999">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-999">Az.Storage</span></span>
* <span data-ttu-id="0a960-1000">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzStorageAccountKey'</span><span class="sxs-lookup"><span data-stu-id="0a960-1000">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="0a960-1001">Nel caricamento/dowload di file di Azure, il supporto mantiene le proprietà SMB dei file (attributi, data/ora di creazione e data/ora dell'ultima scrittura dei file) nel file di destinazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1001">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="0a960-1002">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1002">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="0a960-1003">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1003">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="0a960-1004">Correzione del caricamento di BLOB in blocchi con errore di proprietà/metadati nell'oggetto ImmutabilityPolicy abilitato per contenitori.</span><span class="sxs-lookup"><span data-stu-id="0a960-1004">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="0a960-1005">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1005">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="0a960-1006">Supporto della gestione di condivisioni di file di Azure con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="0a960-1006">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="0a960-1007">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-1007">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a960-1008">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-1008">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a960-1009">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-1009">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="0a960-1010">Remove-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="0a960-1010">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1011">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1011">Az.Websites</span></span>
* <span data-ttu-id="0a960-1012">Correzione del problema per cui i tag delle app Web vengono eliminati durante la migrazione dell'app a un nuovo ASP</span><span class="sxs-lookup"><span data-stu-id="0a960-1012">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="0a960-1013">Correzione di Publish-AzureWebapp per renderlo compatibile tra Linux e Windows</span><span class="sxs-lookup"><span data-stu-id="0a960-1013">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="0a960-1014">Aggiornamento di un esempio nella documentazione di riferimento di 'Get-AzWebAppPublishingProfile'</span><span class="sxs-lookup"><span data-stu-id="0a960-1014">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="0a960-1015">2.6.0 - Agosto 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1015">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="0a960-1016">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-1016">General</span></span>
* <span data-ttu-id="0a960-1017">Correzione di vari errori di ortografia in numerosi moduli</span><span class="sxs-lookup"><span data-stu-id="0a960-1017">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-1018">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1018">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1019">Supporto dell'identità del servizio gestito assegnata dall'utente in Autenticazione di Funzioni di Azure (#9479)</span><span class="sxs-lookup"><span data-stu-id="0a960-1019">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a960-1020">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a960-1020">Az.Aks</span></span>
* <span data-ttu-id="0a960-1021">Correzione del problema relativo all'output di 'Get-AzAks'</span><span class="sxs-lookup"><span data-stu-id="0a960-1021">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="0a960-1022">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9847</span><span class="sxs-lookup"><span data-stu-id="0a960-1022">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-1023">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1023">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-1024">correzione del problema https://github.com/Azure/azure-powershell/issues/9351</span><span class="sxs-lookup"><span data-stu-id="0a960-1024">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="0a960-1025">Aggiornamento della versione NuGet .NET, che non impone restrizioni su productId, apiId, groupId e userId</span><span class="sxs-lookup"><span data-stu-id="0a960-1025">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="0a960-1026">**Get-AzApiManagementProduct**: aggiunta del supporto per l'esecuzione di query su prodotti con l'API.</span><span class="sxs-lookup"><span data-stu-id="0a960-1026">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="0a960-1027">**New-AzApiManagementApiRevision**: correzione per il problema che impediva l'impostazione di ApiRevisionDescription durante la creazione della nuova revisione dell'API https://github.com/Azure/azure-powershell/issues/9752</span><span class="sxs-lookup"><span data-stu-id="0a960-1027">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="0a960-1028">Correzione dell'errore di ortografia nel nome del modello 'PsApiManagementOAuth2AuthrozationServer' corretto in 'PsApiManagementOAuth2AuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0a960-1028">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a960-1029">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1029">Az.Batch</span></span>
* <span data-ttu-id="0a960-1030">Correzione dell'errore di ortografia nel messaggio della Guida e nella documentazione in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="0a960-1030">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-1031">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-1031">Az.Cdn</span></span>
* <span data-ttu-id="0a960-1032">Correzione di un errore di ortografia nell'helper di conversione del modulo della rete CDN</span><span class="sxs-lookup"><span data-stu-id="0a960-1032">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1033">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1033">Az.Compute</span></span>
* <span data-ttu-id="0a960-1034">Aggiunta di VmssId al cmdlet New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1034">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="0a960-1035">Aggiunta dei parametri TerminateScheduledEvents e TerminateScheduledEventNotBeforeTimeoutInMinutes a New-AzVmssConfig e Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-1035">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="0a960-1036">Aggiunta della proprietà HyperVGeneration all'oggetto immagine di macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-1036">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="0a960-1037">Aggiunta delle funzionalità Host e HostGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1037">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="0a960-1038">Nuovi cmdlet:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="0a960-1038">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="0a960-1039">Aggiunta del parametro HostId a New-AzVMConfig e New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a960-1039">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="0a960-1040">Aggiornamento dell'esempio nella documentazione di 'Invoke-AzVMRunCommand' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="0a960-1040">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="0a960-1041">Aggiornamento della descrizione di '-VolumeType' nella documentazione di riferimento di 'Set-AzVMDiskEncryptionExtension' e 'Set-AzVmssDiskEncryptionExtension'</span><span class="sxs-lookup"><span data-stu-id="0a960-1041">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1042">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1042">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1043">Correzione dell'errore di ortografia nella documentazione di 'New-AzDataFactoryEncryptValue', in cui Windows era scritto con iniziale minuscola</span><span class="sxs-lookup"><span data-stu-id="0a960-1043">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="0a960-1044">Aggiornamento di ADF .NET SDK alla versione 4.1.2</span><span class="sxs-lookup"><span data-stu-id="0a960-1044">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="0a960-1045">Aggiunta dei parametri 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' e 'DataProxyStagingPath' per il cmdlet 'Set-AzureRmDataFactoryV2IntegrationRuntime' per consentire la configurazione del runtime di integrazione self-hosted come proxy per SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="0a960-1045">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="0a960-1046">Aggiornamento di PSTriggerRun per mostrare le pipeline, il messaggio e le proprietà attivati e di PSActivityRun per mostrare il tipo di attività</span><span class="sxs-lookup"><span data-stu-id="0a960-1046">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1047">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1047">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1048">Correzione della sospensione di Get-DataLakeStoreDeletedItem in caso di eventuali errori o eccezioni remote.</span><span class="sxs-lookup"><span data-stu-id="0a960-1048">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-1049">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1049">Az.EventHub</span></span>
* <span data-ttu-id="0a960-1050">Correzione del problema 9658: errore di ortografia nel parametro VirtualNteworkRule in Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-1050">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="0a960-1051">Correzione del problema 9558: uso di PATCH invece di PUT in Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0a960-1051">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="0a960-1052">Aggiunta del parametro EnableKafka al cmdlet Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="0a960-1052">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="0a960-1053">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="0a960-1053">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="0a960-1054">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a960-1054">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a960-1055">Correzione dell'errore di ortografia nella documentazione in cui 'Azure' era scritto in minuscolo</span><span class="sxs-lookup"><span data-stu-id="0a960-1055">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-1056">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-1056">Az.Monitor</span></span>
* <span data-ttu-id="0a960-1057">Correzione del nome di parametro errato nella documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-1057">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1058">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1058">Az.Network</span></span>
* <span data-ttu-id="0a960-1059">Aggiornamento di New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1059">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="0a960-1060">Deprecazione del parametro 'PublicIpAddress' perché non viene mai usato sul lato server.</span><span class="sxs-lookup"><span data-stu-id="0a960-1060">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="0a960-1061">Aggiunta di un parametro facoltativo 'Primary' che indica se la configurazione IP corrente è o meno primaria.</span><span class="sxs-lookup"><span data-stu-id="0a960-1061">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="0a960-1062">Gestione migliorata dell'eccezione di errore della richiesta da SDK: consente di risolvere il problema per cui le eccezioni SDK precedenti non vengono gestite correttamente e di conseguenza non i dettagli degli errori di chiave non vengono visualizzati</span><span class="sxs-lookup"><span data-stu-id="0a960-1062">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="0a960-1063">Modifica della logica di convalida per il prefisso IP IPv6 per verificare la correttezza della lunghezza del prefisso IPv6.</span><span class="sxs-lookup"><span data-stu-id="0a960-1063">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="0a960-1064">Aggiornamento di Get-AzVirtualNetworkSubnetConfig: aggiunta del set di parametri per ottenere l'ID risorsa per subnet.</span><span class="sxs-lookup"><span data-stu-id="0a960-1064">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="0a960-1065">Aggiornamento della descrizione del parametro Location per AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0a960-1065">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1066">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1066">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1067">Aggiornamento della documentazione per 'New-AzOperationalInsightsLinuxSyslogDataSource'</span><span class="sxs-lookup"><span data-stu-id="0a960-1067">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="0a960-1068">Aggiunta dell'esempio</span><span class="sxs-lookup"><span data-stu-id="0a960-1068">Added example</span></span>
    - <span data-ttu-id="0a960-1069">Aggiornamento della descrizione per il parametro '-Name'</span><span class="sxs-lookup"><span data-stu-id="0a960-1069">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="0a960-1070">Aggiunta di un esempio per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0a960-1070">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="0a960-1071">Modifica della descrizione del parametro -Name per New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="0a960-1071">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1072">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1072">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1073">Aggiornamento di 'Get-AzRecoveryServicesBackupJobDetail.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1073">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1074">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1074">Az.Resources</span></span>
* <span data-ttu-id="0a960-1075">Aggiunta del supporto per la nuova versione API 2019-05-10 per Microsoft.Resource</span><span class="sxs-lookup"><span data-stu-id="0a960-1075">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="0a960-1076">Aggiunta del supporto per 'copy.count = 0' per variabili, risorse e proprietà</span><span class="sxs-lookup"><span data-stu-id="0a960-1076">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="0a960-1077">Le risorse con 'condition = false' o 'copy.count = 0' verranno eliminate in modalità completa</span><span class="sxs-lookup"><span data-stu-id="0a960-1077">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="0a960-1078">Aggiunta di un esempio di assegnazione dei criteri a livello di sottoscrizione alla documentazione della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-1078">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-1079">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-1079">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-1080">Correzione del problema 9658: Errore di ortografia nel parametro VirtualNetworkRule in Set-AzServiceBusNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-1080">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="0a960-1081">Correzione del problema 9786: non è possibile creare una regola con diritti di solo ascolto</span><span class="sxs-lookup"><span data-stu-id="0a960-1081">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="0a960-1082">Aggiunta del nuovo comando 'Test-AzServiceBusNameAvailability' per verificare la disponibilità del nome per la coda e l'argomento</span><span class="sxs-lookup"><span data-stu-id="0a960-1082">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-1083">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1083">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-1084">Correzione dei bug del cmdlet di aggiunta del tipo di nodo:</span><span class="sxs-lookup"><span data-stu-id="0a960-1084">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="0a960-1085">bug NullReferenceException quando nel gruppo di risorse erano presenti altri set di scalabilità di macchine virtuali non correlati al cluster di Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="0a960-1085">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="0a960-1086">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8681</span><span class="sxs-lookup"><span data-stu-id="0a960-1086">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="0a960-1087">Correzione del bug per cui si verificava un errore nel cmdlet se virtualNetwork si trovava in un gruppo di risorse diverso da quello del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a960-1087">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="0a960-1088">Correzione del problema: https://github.com/Azure/azure-powershell/issues/8407</span><span class="sxs-lookup"><span data-stu-id="0a960-1088">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="0a960-1089">Deprecazione del cmdlet Add-AzServiceFabricApplicationCertificate</span><span class="sxs-lookup"><span data-stu-id="0a960-1089">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1090">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1090">Az.Sql</span></span>
* <span data-ttu-id="0a960-1091">Aggiornamento della documentazione dei vecchi cmdlet Auditing.</span><span class="sxs-lookup"><span data-stu-id="0a960-1091">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1092">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1092">Az.Storage</span></span>
* <span data-ttu-id="0a960-1093">Aggiornamento della Guida per Get/Close-AzStorageFileHandle: aggiunta di altri scenari agli esempi di cmdlet e alle descrizioni dei parametri di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="0a960-1093">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="0a960-1094">Supporto di StandardBlobTier nelle operazioni di caricamento e copia BLOB</span><span class="sxs-lookup"><span data-stu-id="0a960-1094">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="0a960-1095">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1095">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="0a960-1096">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-1096">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="0a960-1097">Supporto di Priorità di riattivazione nell'operazione di copia BLOB</span><span class="sxs-lookup"><span data-stu-id="0a960-1097">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="0a960-1098">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-1098">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1099">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1099">Az.Websites</span></span>
* <span data-ttu-id="0a960-1100">Aggiunta di un chiarimento relativo al parametro -AppSettings in Set-AzWebApp e Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a960-1100">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="0a960-1101">2.5.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1101">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1102">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1102">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1103">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0a960-1103">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="0a960-1104">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1104">Az.ApplicationInsights</span></span>
* <span data-ttu-id="0a960-1105">Correzione dell'errore di ortografia nell'esempio della documentazione di 'Remove-AzApplicationInsightsApiKey'</span><span class="sxs-lookup"><span data-stu-id="0a960-1105">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1106">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1106">Az.Automation</span></span>
* <span data-ttu-id="0a960-1107">Correzione dell'errore di ortografia nella stringa di risorsa</span><span class="sxs-lookup"><span data-stu-id="0a960-1107">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-1108">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1108">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-1109">Aggiunta del supporto per NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="0a960-1109">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1110">Az.Compute</span></span>
* <span data-ttu-id="0a960-1111">Aggiunta delle proprietà mancanti (ComputerName, OsName, OsVersion e HyperVGeneration) dell'oggetto visualizzazione istanza di macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-1111">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a960-1112">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a960-1112">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a960-1113">Correzione dell'errore di ortografia in Remove-AzContainerRegistryReplication per il parametro Replication</span><span class="sxs-lookup"><span data-stu-id="0a960-1113">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="0a960-1114">Per altre informazioni, vedere https://github.com/Azure/azure-powershell/issues/9633</span><span class="sxs-lookup"><span data-stu-id="0a960-1114">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1115">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1115">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1116">Aggiornamento di ADF .NET SDK alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0a960-1116">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="0a960-1117">Correzione dell'errore di ortografia nella documentazione relativa a 'Get-AzDataFactoryV2PipelineRun'</span><span class="sxs-lookup"><span data-stu-id="0a960-1117">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-1118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1118">Az.EventHub</span></span>
* <span data-ttu-id="0a960-1119">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzEventHubAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0a960-1119">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a960-1120">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="0a960-1120">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-1121">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1121">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-1122">Aggiunta del supporto per la specifica del valore di KeySize per i criteri dei certificati</span><span class="sxs-lookup"><span data-stu-id="0a960-1122">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a960-1123">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1123">Az.LogicApp</span></span>
* <span data-ttu-id="0a960-1124">Correzione di Get-AzIntegrationAccountMap per la visualizzazione dell'elenco di tutti i tipi di mapping</span><span class="sxs-lookup"><span data-stu-id="0a960-1124">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="0a960-1125">Aggiunta del nuovo parametro MapType per il filtro</span><span class="sxs-lookup"><span data-stu-id="0a960-1125">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="0a960-1126">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1126">Az.ManagedServices</span></span>
* <span data-ttu-id="0a960-1127">Aggiunta del supporto per l'API versione 2019-06-01 (disponibilità generale)</span><span class="sxs-lookup"><span data-stu-id="0a960-1127">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1128">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1128">Az.Network</span></span>
* <span data-ttu-id="0a960-1129">Aggiunta del supporto per l'endpoint privato e il servizio di collegamento privato</span><span class="sxs-lookup"><span data-stu-id="0a960-1129">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="0a960-1130">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1130">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1131">Set-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-1131">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a960-1132">Set-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1132">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a960-1133">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1133">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-1134">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1134">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-1135">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1135">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-1136">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1136">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="0a960-1137">Test-AzPrivateLinkServiceVisibility</span><span class="sxs-lookup"><span data-stu-id="0a960-1137">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="0a960-1138">Get-AzAutoApprovedPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1138">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="0a960-1139">Aggiornamento dei comandi seguenti per la funzionalità: Flag PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies su Subnet in Virtualnetwork</span><span class="sxs-lookup"><span data-stu-id="0a960-1139">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="0a960-1140">Aggiornamento di New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1140">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="0a960-1141">Aggiunta del parametro facoltativo -PrivateEndpointNetworkPoliciesFlag che configura se applicare o meno criteri di rete sull'endpoint privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="0a960-1141">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="0a960-1142">Aggiunta del parametro facoltativo -PrivateLinkServiceNetworkPoliciesFlag che configura se applicare o meno criteri di rete sul servizio Collegamento privato in questa subnet.</span><span class="sxs-lookup"><span data-stu-id="0a960-1142">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="0a960-1143">Il parametro di cmdlet 'ServiceName' di AzPrivateLinkService è stato rinominato in 'Name' con un alias 'ServiceName' per garantire la compatibilità con le versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="0a960-1143">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="0a960-1144">Abilitazione del protocollo ICMP per le configurazioni delle regole di sicurezza di rete</span><span class="sxs-lookup"><span data-stu-id="0a960-1144">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="0a960-1145">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1145">Updated cmdlets</span></span>
        - <span data-ttu-id="0a960-1146">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1146">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a960-1147">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1147">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="0a960-1148">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1148">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="0a960-1149">Aggiunta di ConnectionProtocolType (Ikev1/Ikev2) come parametro configurabile per New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1149">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="0a960-1150">Aggiunta di PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1150">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="0a960-1151">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0a960-1151">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a960-1152">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1152">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a960-1153">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1153">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="0a960-1154">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1154">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="0a960-1155">Aggiornamento del comando New-AzApplicationGatewayProbeConfig del gateway applicazione per il supporto della porta personalizzata in Probe</span><span class="sxs-lookup"><span data-stu-id="0a960-1155">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="0a960-1156">Aggiornamento di New-AzApplicationGatewayProbeConfig: Aggiunta del parametro facoltativo Port usato per il sondaggio del server back-end.</span><span class="sxs-lookup"><span data-stu-id="0a960-1156">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="0a960-1157">Questo parametro è applicabile per gli SKU Standard_V2 e WAF_V2 SKU.</span><span class="sxs-lookup"><span data-stu-id="0a960-1157">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1158">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1158">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1159">Aggiornamento della versione predefinita per le versioni salvate su 1.</span><span class="sxs-lookup"><span data-stu-id="0a960-1159">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="0a960-1160">Correzione della gestione delle espressioni regolari Null di log personalizzati</span><span class="sxs-lookup"><span data-stu-id="0a960-1160">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1162">Aggiornamento di 'Get-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1162">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a960-1163">Aggiornamento di 'Get-AzRecoveryServicesBackupContainer.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1163">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="0a960-1164">Aggiornamento di 'Get-AzRecoveryServicesVault.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1164">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="0a960-1165">Aggiornamento di 'Wait-AzRecoveryServicesBackupJob.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1165">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="0a960-1166">Aggiornamento di 'Set-AzRecoveryServicesVaultContext.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1166">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="0a960-1167">Aggiornamento di 'Get-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1167">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a960-1168">Aggiornamento di 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1168">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="0a960-1169">Aggiornamento di 'Restore-AzRecoveryServicesBackupItem.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1169">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="0a960-1170">Aggiornamento della chiamata al servizio per l'annullamento della registrazione del contenitore per Condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1170">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="0a960-1171">Aggiornamento di 'Set-AzRecoveryServicesAsrAlertSetting.md'</span><span class="sxs-lookup"><span data-stu-id="0a960-1171">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1172">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1172">Az.Resources</span></span>
- <span data-ttu-id="0a960-1173">Rimozione del cmdlet mancante a cui viene fatto riferimento nella documentazione di 'New-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0a960-1173">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="0a960-1174">Aggiornamento dei cmdlet dei criteri per consentire l'uso della nuova versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0a960-1174">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-1175">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-1175">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-1176">Aggiunta del nuovo cmdlet per la generazione del token di firma di accesso condiviso: New-AzServiceBusAuthorizationRuleSASToken</span><span class="sxs-lookup"><span data-stu-id="0a960-1176">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="0a960-1177">Aggiunta del messaggio di errore e verifica per i diritti delle regole di autorizzazione se viene assegnato solo 'Manage'</span><span class="sxs-lookup"><span data-stu-id="0a960-1177">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1178">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1178">Az.Sql</span></span>
* <span data-ttu-id="0a960-1179">Correzione degli esempi mancanti per il cmdlet Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0a960-1179">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="0a960-1180">Correzione delle analisi ricorrenti impostate per Valutazione della vulnerabilità senza specificare alcun indirizzo di posta elettronica</span><span class="sxs-lookup"><span data-stu-id="0a960-1180">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="0a960-1181">Correzione di un errore di ortografia in un messaggio di avviso.</span><span class="sxs-lookup"><span data-stu-id="0a960-1181">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1182">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1182">Az.Storage</span></span>
* <span data-ttu-id="0a960-1183">Aggiornamento dell'esempio nella documentazione di riferimento per 'Get-AzStorageAccount' per consentire l'uso del nome di parametro corretto</span><span class="sxs-lookup"><span data-stu-id="0a960-1183">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a960-1184">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a960-1184">Az.StorageSync</span></span>
* <span data-ttu-id="0a960-1185">Aggiunta del cmdlet Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="0a960-1185">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="0a960-1186">Correzione del problema 9551 per rispettare il valore di TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="0a960-1186">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1187">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1187">Az.Websites</span></span>
* <span data-ttu-id="0a960-1188">Correzione di un bug che impediva la restituzione di alcune proprietà di SiteConfig da parte di Get-AzWebApp e Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1188">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="0a960-1189">Aggiunta di un nuovo parametro Location a Get-AzDeletedWebApp e Restore-AzDeletedWebApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1189">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="0a960-1190">Correzione di un bug relativo alla clonazione di slot delle app Web con New-AzWebApp -IncludeSourceWebAppSlots</span><span class="sxs-lookup"><span data-stu-id="0a960-1190">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="0a960-1191">2.4.0 - Luglio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1191">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1192">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1192">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1193">Aggiunta del supporto per i cmdlet del profilo</span><span class="sxs-lookup"><span data-stu-id="0a960-1193">Add support for profile cmdlets</span></span>
* <span data-ttu-id="0a960-1194">Aggiunta del supporto per ambienti e piani dati nei cmdlet generati</span><span class="sxs-lookup"><span data-stu-id="0a960-1194">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="0a960-1195">Correzione di un bug per cui in alcuni casi viene usato l'endpoint non corretto per i cmdlet del piano dati in Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="0a960-1195">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="0a960-1196">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a960-1196">Az.Advisor</span></span>
* <span data-ttu-id="0a960-1197">Versione in disponibilità generale di Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="0a960-1197">GA release of Az.Advisor</span></span>
* <span data-ttu-id="0a960-1198">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="0a960-1198">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="0a960-1199">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1199">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-1200">correzione del problema https://github.com/Azure/azure-powershell/issues/8671</span><span class="sxs-lookup"><span data-stu-id="0a960-1200">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="0a960-1201">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0a960-1201">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="0a960-1202">Aggiunta del supporto per l'esecuzione di query sulle sottoscrizioni in base a utente e prodotto</span><span class="sxs-lookup"><span data-stu-id="0a960-1202">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="0a960-1203">Aggiunta del supporto per l'esecuzione di query con l'ambito '/', '/apis', '/apis/echo-api'</span><span class="sxs-lookup"><span data-stu-id="0a960-1203">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="0a960-1204">Correzione dei problemi https://github.com/Azure/azure-powershell/issues/9307 e https://github.com/Azure/azure-powershell/issues/8432</span><span class="sxs-lookup"><span data-stu-id="0a960-1204">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="0a960-1205">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a960-1205">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="0a960-1206">Aggiunta del supporto per la specifica di 'ApiVersion' e 'ApiVersionSetId' durante l'importazione di API</span><span class="sxs-lookup"><span data-stu-id="0a960-1206">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1207">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1207">Az.Automation</span></span>
* <span data-ttu-id="0a960-1208">Correzione del bug del cmdlet Set-AzAutomationConnectionFieldValue per la gestione del valore di stringa.</span><span class="sxs-lookup"><span data-stu-id="0a960-1208">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1209">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1209">Az.Compute</span></span>
* <span data-ttu-id="0a960-1210">Aggiunta del parametro HyperVGeneration a New-AzImageConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1210">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1211">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1211">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1212">Aggiornamento dell'output dei cmdlet ADF get activity runs, get pipeline runs e get trigger runs per supportare la pipe Select-Object.</span><span class="sxs-lookup"><span data-stu-id="0a960-1212">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a960-1213">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a960-1213">Az.EventGrid</span></span>
* <span data-ttu-id="0a960-1214">Correzione dell'errore di ortografia nella documentazione di 'New-AzEventGridSubscription'</span><span class="sxs-lookup"><span data-stu-id="0a960-1214">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1215">Az.IotHub</span></span>
* <span data-ttu-id="0a960-1216">Aggiunta del supporto per la rigenerazione delle chiavi dei criteri di autorizzazione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1216">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1217">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1217">Az.Network</span></span>
* <span data-ttu-id="0a960-1218">Aggiunta di 'RoutingPreference' ai tag degli IP pubblici</span><span class="sxs-lookup"><span data-stu-id="0a960-1218">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="0a960-1219">Miglioramento degli esempi nella documentazione di riferimento di 'Get-AzNetworkServiceTag'</span><span class="sxs-lookup"><span data-stu-id="0a960-1219">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-1220">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1220">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-1221">Correzione del problema relativo al riferimento Null in Get-AzPolicyState</span><span class="sxs-lookup"><span data-stu-id="0a960-1221">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="0a960-1222">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/9446</span><span class="sxs-lookup"><span data-stu-id="0a960-1222">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1223">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1223">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1224">Correzione del modello di origine dati CustomLog restituito in Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0a960-1224">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1225">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1225">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1226">Correzione del comando get-policy per le VM IaaS</span><span class="sxs-lookup"><span data-stu-id="0a960-1226">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1227">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1227">Az.Resources</span></span>
    - <span data-ttu-id="0a960-1228">Correzione del testo della Guida per il parametro Get-AzPolicyState -Top</span><span class="sxs-lookup"><span data-stu-id="0a960-1228">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="0a960-1229">Aggiunta del supporto per il paging lato client per Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="0a960-1229">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="0a960-1230">Aggiunta di nuovi parametri per Set-AzPolicyAssignment, -PolicyParameters e -PolicyParametersObject</span><span class="sxs-lookup"><span data-stu-id="0a960-1230">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="0a960-1231">Aggiornamento di documentazione ed esempi per i cmdlet Policy</span><span class="sxs-lookup"><span data-stu-id="0a960-1231">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-1232">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-1232">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-1233">Correzione del problema #4938 - New-AzureRmServiceBusQueue restituisce BadRequest quando si imposta MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="0a960-1233">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1234">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1234">Az.Sql</span></span>
* <span data-ttu-id="0a960-1235">Aggiunta dei cmdlet del gruppo di failover dell'istanza dalla versione di anteprima a quella pubblica</span><span class="sxs-lookup"><span data-stu-id="0a960-1235">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="0a960-1236">Aggiunta di nuovi cmdlet per supportare il controllo di server SQL\database di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1236">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="0a960-1237">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1237">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a960-1238">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1238">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a960-1239">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1239">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="0a960-1240">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1240">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a960-1241">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1241">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="0a960-1242">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="0a960-1242">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="0a960-1243">Rimozione dei vincoli di posta elettronica dalle impostazioni di valutazione della vulnerabilità</span><span class="sxs-lookup"><span data-stu-id="0a960-1243">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1244">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1244">Az.Storage</span></span>
* <span data-ttu-id="0a960-1245">Conversione dei due parametri '-IndexDocument' e '-ErrorDocument404Path' da obbligatori a facoltativi nel cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1245">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="0a960-1246">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a960-1246">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="0a960-1247">Aggiornamento della Guida di Get-AzStorageBlobContent con l'aggiunta di un esempio</span><span class="sxs-lookup"><span data-stu-id="0a960-1247">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="0a960-1248">Visualizzazione di altre informazioni sull'errore del cmdlet con StorageException</span><span class="sxs-lookup"><span data-stu-id="0a960-1248">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="0a960-1249">Supporto della creazione o dell'aggiornamento dell'account di archiviazione con l'autenticazione di AAD DS di File di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1249">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="0a960-1250">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1250">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="0a960-1251">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1251">Set-AzStorageAccount</span></span>
* <span data-ttu-id="0a960-1252">Supporto per ottenere o chiudere gli handle di file di una condivisione file, una directory di file o un file</span><span class="sxs-lookup"><span data-stu-id="0a960-1252">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="0a960-1253">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a960-1253">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="0a960-1254">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0a960-1254">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="0a960-1255">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="0a960-1255">Az.StorageSync</span></span>
* <span data-ttu-id="0a960-1256">Questo modulo è ora incluso come parte del modulo `Az` di rollup</span><span class="sxs-lookup"><span data-stu-id="0a960-1256">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="0a960-1257">2.3.2 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1257">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1258">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1258">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1259">Correzione del bug per cui in alcuni casi viene usato un URL errato nelle chiamate alle funzioni</span><span class="sxs-lookup"><span data-stu-id="0a960-1259">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="0a960-1260">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8983</span><span class="sxs-lookup"><span data-stu-id="0a960-1260">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="0a960-1261">Correzione del problema relativo agli alias dai cmdlet di AzureRM a quelli di Az</span><span class="sxs-lookup"><span data-stu-id="0a960-1261">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="0a960-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="0a960-1262">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="0a960-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span><span class="sxs-lookup"><span data-stu-id="0a960-1263">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1264">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1264">Az.Compute</span></span>
* <span data-ttu-id="0a960-1265">I set di parametri semplici New-AzVm e New-AzVmss ora accettano il parametro 'ProximityPlacementGroup'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1265">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="0a960-1266">Correzione di un errore di battitura nella documentazione di riferimento di 'New-AzVM'</span><span class="sxs-lookup"><span data-stu-id="0a960-1266">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a960-1267">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a960-1267">Az.Dns</span></span>
* <span data-ttu-id="0a960-1268">Correzione di un errore di battitura negli esempi della Guida di 'Set-AzDnsZone'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1268">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a960-1269">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a960-1269">Az.EventGrid</span></span>
* <span data-ttu-id="0a960-1270">Aggiornamento per l'uso della versione dell'API 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="0a960-1270">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="0a960-1271">Nuovi cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1271">New cmdlets:</span></span>
    - <span data-ttu-id="0a960-1272">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a960-1272">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a960-1273">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1273">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a960-1274">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a960-1274">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a960-1275">Ottiene i dettagli di un dominio di Griglia di eventi oppure un elenco di tutti i domini di Griglia di eventi nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1275">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="0a960-1276">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="0a960-1276">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="0a960-1277">Rimuove un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1277">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a960-1278">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a960-1278">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a960-1279">Rigenera la chiave di accesso condiviso per un dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1279">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="0a960-1280">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="0a960-1280">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="0a960-1281">Ottiene le chiavi di accesso condiviso usate per pubblicare eventi in un dominio di Griglia di eventi.</span><span class="sxs-lookup"><span data-stu-id="0a960-1281">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="0a960-1282">New-AzureRmEventGridDomainTopic:</span><span class="sxs-lookup"><span data-stu-id="0a960-1282">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a960-1283">Crea un nuovo dominio di Griglia di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1283">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="0a960-1284">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a960-1284">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="0a960-1285">Ottiene i dettagli di un argomento di dominio di Griglia di eventi oppure un elenco di tutti gli argomenti di dominio di Griglia di eventi nel dominio di Griglia di eventi specifico nella sottoscrizione corrente di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1285">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="0a960-1286">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="0a960-1286">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="0a960-1287">Rimuove un argomento di dominio di Griglia di eventi di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="0a960-1287">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="0a960-1288">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1288">Updated cmdlets:</span></span>
    - <span data-ttu-id="0a960-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a960-1289">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="0a960-1290">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il nuovo dominio di Griglia di eventi e il nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0a960-1290">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a960-1291">Aggiunta di nuovi parametri obbligatori per specificare il nome del nuovo dominio di Griglia di eventi e/o del nuovo argomento di dominio di Griglia di eventi, consentendo di creare una nuova sottoscrizione di eventi in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0a960-1291">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="0a960-1292">Aggiunta di nuovi set di parametri per domini e argomenti di dominio per consentire il riutilizzo di parametri esistenti, ad esempio EndPointType, SubjectBeginsWith e così via.</span><span class="sxs-lookup"><span data-stu-id="0a960-1292">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="0a960-1293">aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0a960-1293">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="0a960-1294">Data di scadenza della sottoscrizione di eventi</span><span class="sxs-lookup"><span data-stu-id="0a960-1294">Event subscription expiration date,</span></span>
            - <span data-ttu-id="0a960-1295">Parametri di filtro avanzati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1295">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="0a960-1296">Aggiunta della nuova enumerazione per usare servicebusqueue come destinazione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1296">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="0a960-1297">Utilizzo di 'All' non consentito nell'opzione -IncludedEventType e relativa sostituzione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1297">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="0a960-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a960-1298">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="0a960-1299">Aggiunta di nuovi parametri facoltativi (Top, ODataQuery e NextLink) per supportare la paginazione e il filtro dei risultati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1299">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="0a960-1300">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="0a960-1300">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="0a960-1301">Aggiunta di nuovi parametri obbligatori per supportare l'invio tramite pipe per il dominio di Griglia di eventi e l'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0a960-1301">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="0a960-1302">Aggiunta di nuovi parametri obbligatori per specificare il nome del dominio di Griglia di eventi e/o dell'argomento di dominio di Griglia di eventi, consentendo di rimuovere una sottoscrizione di eventi esistente in queste risorse.</span><span class="sxs-lookup"><span data-stu-id="0a960-1302">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-1303">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-1303">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-1304">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="0a960-1304">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="0a960-1305">Aggiunta del supporto per le trasformazioni e del nuovo valore per il completamento automatico degli operatori (RegEx)</span><span class="sxs-lookup"><span data-stu-id="0a960-1305">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="0a960-1306">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="0a960-1306">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="0a960-1307">Aggiunta di nuovi valori per il completamento automatico</span><span class="sxs-lookup"><span data-stu-id="0a960-1307">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1308">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1308">Az.Network</span></span>
* <span data-ttu-id="0a960-1309">Aggiunta del supporto per la risorsa gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-1309">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="0a960-1310">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1310">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="0a960-1311">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="0a960-1312">Aggiunta di AvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0a960-1312">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="0a960-1313">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1313">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1314">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="0a960-1314">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="0a960-1315">Aggiunta di PrivatePrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1315">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="0a960-1316">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1316">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1317">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1317">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a960-1318">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1318">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a960-1319">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="0a960-1319">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="0a960-1320">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1320">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="0a960-1321">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1321">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="0a960-1322">Aggiunta di PrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-1322">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="0a960-1323">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1323">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1324">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-1324">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a960-1325">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-1325">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a960-1326">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="0a960-1326">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="0a960-1327">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1327">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="0a960-1328">Aggiornamento dei comandi seguenti per la funzionalità: Flag UseLocalAzureIpAddress in VpnConnection</span><span class="sxs-lookup"><span data-stu-id="0a960-1328">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="0a960-1329">Aggiornamento di New-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="0a960-1329">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="0a960-1330">Aggiornamento di Set-AzVpnConnection: Aggiunta del parametro facoltativo -UseLocalAzureIpAddress per indicare che come indirizzo di origine all'avvio della connessione deve essere usato l'indirizzo IP di Azure locale.</span><span class="sxs-lookup"><span data-stu-id="0a960-1330">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="0a960-1331">Aggiunta del campo di sola lettura PeeredConnections nel peering di ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a960-1331">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="0a960-1332">Aggiunta del campo di sola lettura GlobalReachEnabled in ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0a960-1332">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="0a960-1333">Aggiunta dell'attributo di modifica di rilievo per dare risalto alla deprecazione del campo AllowGlobalReach nel modello ExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="0a960-1333">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="0a960-1334">Correzione del problema 8756 relativo all'errore visualizzato durante l'uso di TargetListenerID con cmdlet AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1334">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="0a960-1335">Correzione del bug in New-AzApplicationGatewayPathRuleConfig che impediva l'impostazione del set di regole di riscrittura.</span><span class="sxs-lookup"><span data-stu-id="0a960-1335">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="0a960-1336">Correzione dell'errore di visualizzazione di VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1336">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="0a960-1337">Correzione dei cmdlet Get di Cortex per la parte list all</span><span class="sxs-lookup"><span data-stu-id="0a960-1337">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="0a960-1338">Correzione dell'errore di creazione dei riferimenti VirtualHub per ExpressRouteGateways, VpnGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1338">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="0a960-1339">Aggiunta del supporto per le zone di disponibilità in AzureFirewall e NatGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1339">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="0a960-1340">Aggiunta del cmdlet Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="0a960-1340">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="0a960-1341">Aggiunta del supporto per più indirizzi IP pubblici per Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1341">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="0a960-1342">Aggiornamento del cmdlet New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="0a960-1342">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="0a960-1343">Aggiunta del parametro -PublicIpAddress che accetta uno o più oggetti indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0a960-1343">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="0a960-1344">Aggiunta del parametro -VirtualNetwork che accetta un oggetto rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-1344">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="0a960-1345">Aggiunta dei metodi AddPublicIpAddress e RemovePublicIpAddress nell'oggetto firewall. Tali metodi accettano come input un oggetto indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="0a960-1345">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="0a960-1346">Parametri deprecati: -PublicIpName e -VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="0a960-1346">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="0a960-1347">Aggiornamento dei comandi seguenti per la funzionalità: Impostazione delle opzioni di autenticazione AAD di VpnClient per la risorsa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a960-1347">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="0a960-1348">Aggiornamento di New-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1348">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a960-1349">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta dei parametri facoltativi AadTenantUri, AadAudienceId, AadIssuerUri per impostare le opzioni di autenticazione AAD di VpnClient nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1349">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="0a960-1350">Aggiornamento di Set-AzVirtualNetworkGateway: Aggiunta del parametro facoltativo RemoveAadAuthentication per rimuovere le opzioni di autenticazione AAD di VpnClient dal gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1350">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1351">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1351">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1352">Abilitazione del piano tariffario **pergb2018** nel comando 'New-AzureRmOperationalInsightsWorkspace'</span><span class="sxs-lookup"><span data-stu-id="0a960-1352">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1353">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1353">Az.Resources</span></span>
* <span data-ttu-id="0a960-1354">Supporto per opzioni aggiuntive di esportazione modelli</span><span class="sxs-lookup"><span data-stu-id="0a960-1354">Support for additional Template Export options</span></span>
    - <span data-ttu-id="0a960-1355">Aggiunta del parametro '-SkipResourceNameParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1355">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a960-1356">Aggiunta del parametro '-SkipAllParameterization' a Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1356">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="0a960-1357">Aggiunta del parametro '-Resource' a Export-AzResourceGroup per il filtro delle risorse esportate</span><span class="sxs-lookup"><span data-stu-id="0a960-1357">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-1358">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1358">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-1359">Correzione del problema per cui aggiungendo il certificato ByExistingKeyVault in alcuni casi si otteneva l'identificazione personale errata</span><span class="sxs-lookup"><span data-stu-id="0a960-1359">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1360">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1360">Az.Sql</span></span>
* <span data-ttu-id="0a960-1361">Correzione del suffisso dell'endpoint di archiviazione di Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0a960-1361">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="0a960-1362">Correzione del problema per cui l'abilitazione di Sicurezza dei dati avanzata veniva eseguito l'override dei criteri Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0a960-1362">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="0a960-1363">Nuovi cmdlet per Management.Sql per consentire ai clienti di aggiungere chiavi TDE e impostare la protezione TDE per le istanze gestite</span><span class="sxs-lookup"><span data-stu-id="0a960-1363">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="0a960-1364">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a960-1364">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a960-1365">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a960-1365">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a960-1366">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a960-1366">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="0a960-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a960-1367">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="0a960-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0a960-1368">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1369">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1369">Az.Storage</span></span>
* <span data-ttu-id="0a960-1370">Supporto del tipo FileStorage e SkuName Premium_ZRS durante la creazione dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1370">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="0a960-1371">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1371">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a960-1372">Descrizione del cmdlet di immutabilità BLOB più chiara</span><span class="sxs-lookup"><span data-stu-id="0a960-1372">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="0a960-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1373">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1374">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1374">Az.Websites</span></span>
* <span data-ttu-id="0a960-1375">Ottimizza Get-AzWebAppCertificate per filtrare in base al gruppo di risorse nel server invece che nel client</span><span class="sxs-lookup"><span data-stu-id="0a960-1375">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="0a960-1376">Aggiunge il parametro -UseDisasterRecovery a Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="0a960-1376">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="0a960-1377">2.2.0 - giugno 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1377">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="0a960-1378">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-1378">Az.Cdn</span></span>
* <span data-ttu-id="0a960-1379">I cmdlet sono stati aggiornati in modo da supportare la funzionalità rulesEngine basata sulla versione dell'API del 15/04/2019.</span><span class="sxs-lookup"><span data-stu-id="0a960-1379">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1380">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1380">Az.Compute</span></span>
* <span data-ttu-id="0a960-1381">È stato aggiunto il parametro `NoWait` che avvia l'operazione e viene restituito immediatamente prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1381">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="0a960-1382">Aggiornamento dei cmdlet:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a960-1382">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-1383">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1383">Az.EventHub</span></span>
* <span data-ttu-id="0a960-1384">Correzione per l'errore 9231 - Get-AzEventHubNamespace non restituisce tag</span><span class="sxs-lookup"><span data-stu-id="0a960-1384">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="0a960-1385">Correzione per l'errore 9230 - Get-AzEventHubNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a960-1385">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1386">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1386">Az.Network</span></span>
* <span data-ttu-id="0a960-1387">Aggiornamento di ResourceId e InputObject per il gateway NAT</span><span class="sxs-lookup"><span data-stu-id="0a960-1387">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="0a960-1388">Aggiunta dell'alias per ResourceId e InputObject</span><span class="sxs-lookup"><span data-stu-id="0a960-1388">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-1389">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1389">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-1390">Correzione del problema relativo al riferimento Null in Get-AzPolicyEvent</span><span class="sxs-lookup"><span data-stu-id="0a960-1390">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1391">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1391">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1392">Periodo minimo di conservazione in giorni modificato da 7 a 1 nei criteri di IaaSVM</span><span class="sxs-lookup"><span data-stu-id="0a960-1392">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-1393">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-1393">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-1394">Correzione per l'errore 9182 - Get-AzServiceBusNamespace restituisce ResourceGroup invece di ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a960-1394">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-1395">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1395">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-1396">Correzione dell'errore di ortografia nel messaggio di errore relativo a 'Update-AzServiceFabricReliability'</span><span class="sxs-lookup"><span data-stu-id="0a960-1396">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="0a960-1397">Correzione del carattere mancante nelle righe di comando di Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1397">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1398">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1398">Az.Sql</span></span>
* <span data-ttu-id="0a960-1399">Aggiunta del parametro DnsZonePartner per il cmdlet New-AzureSqlInstance per supportare AutoDr per Istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="0a960-1399">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="0a960-1400">Deprecazione del cmdlet Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1400">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="0a960-1401">Ridenominazione dei cmdlet Threat Detection in Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="0a960-1401">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="0a960-1402">I parametri -StorageSizeInGB e -LicenseType di New-AzSqlInstance sono ora facoltativi.</span><span class="sxs-lookup"><span data-stu-id="0a960-1402">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1403">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1403">Az.Websites</span></span>
* <span data-ttu-id="0a960-1404">Correzione del problema riscontrato quando durante l'uso di Set-AzWebApp e Set-AzWebAppSlot con la proprietà -WebApp i tag venivano rimossi</span><span class="sxs-lookup"><span data-stu-id="0a960-1404">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="0a960-1405">2.1.0 - maggio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1405">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="0a960-1406">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1406">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-1407">Creazione di nuovi cmdlet per la gestione della diagnostica nell'ambito globale e API</span><span class="sxs-lookup"><span data-stu-id="0a960-1407">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="0a960-1408">**Get-AzApiManagementDiagnostic**: ottiene diagnostiche configurate come ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1408">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="0a960-1409">**New-AzApiManagementDiagnostic**: crea nuove diagnostiche a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1409">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="0a960-1410">**New-AzApiManagementHttpMessageDiagnostic**: crea l'impostazione di diagnostica per le intestazioni da registrare e le dimensioni dei byte del corpo</span><span class="sxs-lookup"><span data-stu-id="0a960-1410">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="0a960-1411">**New-AzApiManagementPipelineDiagnosticSetting**: crea le impostazioni di diagnostica per i messaggi HTTP in ingresso/uscita verso il gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1411">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="0a960-1412">**New-AzApiManagementSamplingSetting**: crea l'impostazione di campionamento per le richieste/risposte di una diagnostica</span><span class="sxs-lookup"><span data-stu-id="0a960-1412">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="0a960-1413">**Remove-AzApiManagementDiagnostic**: rimuove un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1413">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="0a960-1414">**Set-AzApiManagementDiagnostic**: aggiorna un'entità diagnostica a livello di ambito globale o dell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1414">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="0a960-1415">Creazione di nuovi cmdlet per la gestione della cache nel servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1415">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="0a960-1416">**Get-AzApiManagementCache**: ottiene i dettagli della cache specificata dall'identificatore o di tutte le cache</span><span class="sxs-lookup"><span data-stu-id="0a960-1416">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="0a960-1417">**New-AzApiManagementCache**: crea una nuova cache predefinita o una cache in una particolare area di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1417">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="0a960-1418">**Remove-AzApiManagementCache**: rimuove una cache</span><span class="sxs-lookup"><span data-stu-id="0a960-1418">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="0a960-1419">**Update-AzApiManagementCache**: aggiorna una cache</span><span class="sxs-lookup"><span data-stu-id="0a960-1419">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="0a960-1420">Creazione di nuovi cmdlet per la gestione dello schema dell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1420">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="0a960-1421">**New-AzApiManagementSchema**: crea un nuovo schema per un'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1421">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="0a960-1422">**Get-AzApiManagementSchema**: ottiene gli schemi configurati nell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1422">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="0a960-1423">**Remove-AzApiManagementSchema**: rimuove lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1423">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="0a960-1424">**Set-AzApiManagementSchema**: aggiorna lo schema configurato nell'API</span><span class="sxs-lookup"><span data-stu-id="0a960-1424">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="0a960-1425">Creazione di un nuovo cmdlet per la generazione di un token utente.</span><span class="sxs-lookup"><span data-stu-id="0a960-1425">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="0a960-1426">**New-AzApiManagementUserToken**: genera un nuovo token utente valido otto ore per impostazione predefinita. È possibile usare questo cmdlet anche per generare il token per l'utente 'GIT'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1426">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="0a960-1427">Creazione di un nuovo cmdlet per il recupero dello stato della rete</span><span class="sxs-lookup"><span data-stu-id="0a960-1427">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="0a960-1428">**Get-AzApiManagementNetworkStatus**: ottiene informazioni sulla connettività di rete delle risorse da cui dipende il servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a960-1428">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="0a960-1429">È utile quando si distribuisce il servizio ApiManagement in una rete virtuale e si intende verificare eventuali interruzioni delle dipendenze.</span><span class="sxs-lookup"><span data-stu-id="0a960-1429">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="0a960-1430">Aggiornamento del cmdlet **New-AzApiManagement** per la gestione del servizio ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1430">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="0a960-1431">Aggiunta del supporto per il nuovo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="0a960-1431">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a960-1432">Aggiunta del supporto per attivare il flag 'EnableClientCertificate' per lo SKU 'Consumption'</span><span class="sxs-lookup"><span data-stu-id="0a960-1432">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="0a960-1433">Il nuovo cmdlet **New-AzApiManagementSslSetting** consente di configurare l'impostazione 'TLS/SSL' su 'Backend' e 'Frontend'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1433">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="0a960-1434">Può essere usato anche per configurare 'Ciphers' come '3DES' e 'ServerProtocols' come 'Http2' sull'oggetto 'Frontend' di un servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a960-1434">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="0a960-1435">Aggiunta del supporto per la configurazione del nome host 'DeveloperPortal' nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0a960-1435">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="0a960-1436">Aggiornamento dei cmdlet **Get-AzApiManagementSsoToken** in modo che accettino come input l'oggetto 'PsApiManagement'</span><span class="sxs-lookup"><span data-stu-id="0a960-1436">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="0a960-1437">Aggiornamento del cmdlet per visualizzare i messaggi di errore inline</span><span class="sxs-lookup"><span data-stu-id="0a960-1437">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="0a960-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Codice errore: ValidationError Messaggio di errore: Uno o più campi contengono valori non corretti: Dettagli errore:    [Code=ValidationError, Message=C'è un errore nell'elemento 'log-to-eventhub' riga 3, colonna 10: Il logger non è stato trovato, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="0a960-1438">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="0a960-1439">Aggiornamento del cmdlet **Export-AzApiManagementApi** per l'esportazione di API in formato 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0a960-1439">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="0a960-1440">Aggiornamento del cmdlet **Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a960-1440">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a960-1441">Per importare l'API dalla specifica del documento 'OpenApi 3.0'</span><span class="sxs-lookup"><span data-stu-id="0a960-1441">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="0a960-1442">Per eseguire l'override della proprietà 'PsApiManagementSchema' specificata in qualsiasi documento ('Swagger', 'Wadl', 'Wsdl', 'OpenApi').</span><span class="sxs-lookup"><span data-stu-id="0a960-1442">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="0a960-1443">Per eseguire l'override della proprietà 'ServiceUrl' specificata in qualsiasi documento.</span><span class="sxs-lookup"><span data-stu-id="0a960-1443">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="0a960-1444">Aggiornamento del cmdlet **Get-AzApiManagementPolicy** in modo che restituisca i criteri in formato escape non XML con 'rawxml'</span><span class="sxs-lookup"><span data-stu-id="0a960-1444">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="0a960-1445">Aggiornamento del cmdlet **Set-AzApiManagementPolicy** in modo che accetti criteri in formato escape non XML con 'rawxml' e escape XML con 'xml'</span><span class="sxs-lookup"><span data-stu-id="0a960-1445">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="0a960-1446">Aggiornamento del cmdlet **New-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a960-1446">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a960-1447">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1447">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a960-1448">Per creare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0a960-1448">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0a960-1449">Per clonare un'API con 'SourceApiId' e 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1449">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="0a960-1450">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="0a960-1450">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0a960-1451">Aggiornamento del cmdlet **Set-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="0a960-1451">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="0a960-1452">Per configurare l'API con il server di autorizzazione 'OpenId'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1452">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="0a960-1453">Per aggiornare un'API in un'interfaccia 'ApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0a960-1453">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="0a960-1454">Possibilità di configurare 'SubscriptionRequired' a livello di API.</span><span class="sxs-lookup"><span data-stu-id="0a960-1454">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="0a960-1455">Aggiornamento del cmdlet **New-AzApiManagementRevision**</span><span class="sxs-lookup"><span data-stu-id="0a960-1455">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="0a960-1456">Per clonare (copiare tag, prodotti, operazioni e criteri) una revisione esistente con 'SourceApiRevision'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1456">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="0a960-1457">La nuova revisione presuppone l'oggetto 'ApiId' dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="0a960-1457">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="0a960-1458">Per fornire un oggetto 'ApiRevisionDescription'</span><span class="sxs-lookup"><span data-stu-id="0a960-1458">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="0a960-1459">Per eseguire l'override della proprietà 'ServiceUrl' durante la clonazione di un'API.</span><span class="sxs-lookup"><span data-stu-id="0a960-1459">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="0a960-1460">Aggiornamento del cmdlet **New-AzApiManagementIdentityProvider**</span><span class="sxs-lookup"><span data-stu-id="0a960-1460">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="0a960-1461">Per configurare 'AAD' o 'AADB2C' con un oggetto 'Authority'</span><span class="sxs-lookup"><span data-stu-id="0a960-1461">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="0a960-1462">Per configurare 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' e 'PasswordResetPolicy'</span><span class="sxs-lookup"><span data-stu-id="0a960-1462">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="0a960-1463">Aggiornamento del cmdlet **New-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0a960-1463">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a960-1464">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0a960-1464">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a960-1465">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0a960-1465">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a960-1466">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1466">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a960-1467">Aggiornamento del cmdlet **Set-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="0a960-1467">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="0a960-1468">Per tenere in considerazione il nuovo modello di sottoscrizione con 'Scope' e 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0a960-1468">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="0a960-1469">Per tenere in considerazione il vecchio modello di sottoscrizione con 'ProductId' and 'UserId'</span><span class="sxs-lookup"><span data-stu-id="0a960-1469">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="0a960-1470">Aggiunta del supporto per abilitare 'AllowTracing' a livello di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1470">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="0a960-1471">Aggiornamento dei cmdlet seguenti in modo che accettino come input 'ResourceId'</span><span class="sxs-lookup"><span data-stu-id="0a960-1471">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="0a960-1472">'New-AzApiManagementContext'</span><span class="sxs-lookup"><span data-stu-id="0a960-1472">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="0a960-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="0a960-1473">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="0a960-1474">'Get-AzApiManagementApiRelease'</span><span class="sxs-lookup"><span data-stu-id="0a960-1474">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="0a960-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="0a960-1475">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="0a960-1476">'Get-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0a960-1476">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="0a960-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="0a960-1477">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="0a960-1478">'Get-AzApiManagementAuthorizationServer'</span><span class="sxs-lookup"><span data-stu-id="0a960-1478">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="0a960-1479">'Get-AzApiManagementBackend'</span><span class="sxs-lookup"><span data-stu-id="0a960-1479">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="0a960-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1480">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="0a960-1481">'Get-AzApiManagementCertificate'</span><span class="sxs-lookup"><span data-stu-id="0a960-1481">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="0a960-1482">'Remove-AzApiManagementApiVersionSet'</span><span class="sxs-lookup"><span data-stu-id="0a960-1482">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="0a960-1483">'Remove-AzApiManagementSubscription'</span><span class="sxs-lookup"><span data-stu-id="0a960-1483">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1484">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1484">Az.Automation</span></span>
* <span data-ttu-id="0a960-1485">Aggiornamento di Get-AzAutomationJobOutputRecord per la gestione dei valori di record di testo e JSON.</span><span class="sxs-lookup"><span data-stu-id="0a960-1485">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="0a960-1486">correzione del problema https://github.com/Azure/azure-powershell/issues/7977</span><span class="sxs-lookup"><span data-stu-id="0a960-1486">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="0a960-1487">correzione del problema https://github.com/Azure/azure-powershell/issues/8600</span><span class="sxs-lookup"><span data-stu-id="0a960-1487">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="0a960-1488">Modifica del comportamento di Start-AzAutomationDscCompilationJob in modo che avvii solo il processo invece di attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="0a960-1488">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="0a960-1489">correzione del problema https://github.com/Azure/azure-powershell/issues/8347</span><span class="sxs-lookup"><span data-stu-id="0a960-1489">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="0a960-1490">Correzione del problema per il quale Get-AzAutomationDscNode restituiva tutti i nodi quando si usava -Name.</span><span class="sxs-lookup"><span data-stu-id="0a960-1490">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="0a960-1491">Ora viene restituito solo il nodo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="0a960-1491">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1492">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1492">Az.Compute</span></span>
* <span data-ttu-id="0a960-1493">Aggiunta dei parametri ProtectFromScaleIn e ProtectFromScaleSetAction al cmdlet Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="0a960-1493">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="0a960-1494">Il set di parametri New-AzVM ora usa una località disponibile per impostazione predefinita se 'Stati Uniti orientali' non è supportata</span><span class="sxs-lookup"><span data-stu-id="0a960-1494">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1495">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1495">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1496">Aggiorna l'SDK ADLS in modo da usare il client HTTP e integrare il test del piano dati con il framework di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1496">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-1497">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-1497">Az.Monitor</span></span>
* <span data-ttu-id="0a960-1498">Correzione dei nomi di parametri errati negli esempi della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-1498">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1499">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1499">Az.Network</span></span>
* <span data-ttu-id="0a960-1500">Aggiunta del flag DisableBgpRoutePropagation all'output della tabella di route effettiva</span><span class="sxs-lookup"><span data-stu-id="0a960-1500">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="0a960-1501">Cmdlet aggiornato:</span><span class="sxs-lookup"><span data-stu-id="0a960-1501">Updated cmdlet:</span></span>
        - <span data-ttu-id="0a960-1502">Get-AzEffectiveRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-1502">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="0a960-1503">Correzione del trattino doppio nella documentazione di New-AzApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="0a960-1503">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1504">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1504">Az.Resources</span></span>
* <span data-ttu-id="0a960-1505">Aggiunta del nuovo cmdlet Get-AzureRmDenyAssignment per il recupero delle assegnazioni di rifiuto</span><span class="sxs-lookup"><span data-stu-id="0a960-1505">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1506">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1506">Az.Sql</span></span>
* <span data-ttu-id="0a960-1507">Ridenominazione dei cmdlet di Advanced Threat Protection in Sicurezza dei dati avanzata e abilitazione di Valutazione della vulnerabilità per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="0a960-1507">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="0a960-1508">2.0.0 - Maggio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1508">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1509">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1509">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1510">Aggiornamento di Authentication Library per risolvere i problemi di ADFS con l'autenticazione di nome utente/password</span><span class="sxs-lookup"><span data-stu-id="0a960-1510">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-1511">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1511">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-1512">Viene visualizzata solo la dichiarazione di non responsabilità di Bing per i servizi di ricerca Bing.</span><span class="sxs-lookup"><span data-stu-id="0a960-1512">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="0a960-1513">Miglioramento dell'errore quando la creazione dell'account non riesce.</span><span class="sxs-lookup"><span data-stu-id="0a960-1513">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1514">Az.Compute</span></span>
* <span data-ttu-id="0a960-1515">Funzionalità Gruppo di selezione host di prossimità.</span><span class="sxs-lookup"><span data-stu-id="0a960-1515">Proximity placement group feature.</span></span>
    - <span data-ttu-id="0a960-1516">Sono stati aggiunti i nuovi cmdlet seguenti:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1516">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="0a960-1517">Il nuovo parametro ProximityPlacementGroupId è stato aggiunto ai cmdlet seguenti:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1517">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="0a960-1518">Il parametro StorageAccountType è stato aggiunto a New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="0a960-1518">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="0a960-1519">TargetRegion di New-AzGalleryImageVersion può contenere StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="0a960-1519">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="0a960-1520">Il parametro opzionale SkipShutdown è stato aggiunto a Stop-AzVM e Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-1520">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="0a960-1521">Modifiche di rilievo</span><span class="sxs-lookup"><span data-stu-id="0a960-1521">Breaking changes</span></span>
    - <span data-ttu-id="0a960-1522">Set-AzVMBootDiagnostics è stato modificato in Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="0a960-1522">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="0a960-1523">Export-AzLogAnalyticThrottledRequests è stato modificato in Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="0a960-1523">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="0a960-1524">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="0a960-1524">Az.DeploymentManager</span></span>
* <span data-ttu-id="0a960-1525">Prima versione disponibile a livello generale dei cmdlet di Azure Deployment Manager</span><span class="sxs-lookup"><span data-stu-id="0a960-1525">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="0a960-1526">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="0a960-1526">Az.Dns</span></span>
* <span data-ttu-id="0a960-1527">Delega automatica del server dei nomi DNS</span><span class="sxs-lookup"><span data-stu-id="0a960-1527">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="0a960-1528">Il cmdlet di creazione zona DNS accetta il nome di zona padre come parametro facoltativo aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="0a960-1528">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="0a960-1529">Sono stati aggiunti i record NS nella zona padre per la zona figlio appena creata.</span><span class="sxs-lookup"><span data-stu-id="0a960-1529">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="0a960-1530">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-1530">Az.FrontDoor</span></span>
* <span data-ttu-id="0a960-1531">Prima versione disponibile a livello generale dei cmdlet di FrontDoor di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1531">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="0a960-1532">Ridenominazione dei cmdlet WAF in modo da includere 'Waf'</span><span class="sxs-lookup"><span data-stu-id="0a960-1532">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="0a960-1533">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-1533">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-1534">Rimozione di due cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1534">Removed two cmdlets:</span></span>
    - <span data-ttu-id="0a960-1535">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a960-1535">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="0a960-1536">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a960-1536">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a960-1537">Aggiunta del nuovo cmdlet Set-AzHDInsightGatewayCredential per sostituire Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="0a960-1537">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="0a960-1538">Aggiornamento del cmdlet Get-AzHDInsightJobOutput per distinguere il ruolo lettore e il ruolo operatore hdinsight:</span><span class="sxs-lookup"><span data-stu-id="0a960-1538">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="0a960-1539">Gli utenti con ruolo di lettore devono specificare il parametro 'DefaultStorageAccountKey' in modo esplicito; in caso contrario, si verifica un errore.</span><span class="sxs-lookup"><span data-stu-id="0a960-1539">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="0a960-1540">Gli utenti con ruolo di operatore hdinsight non sono interessati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1540">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-1541">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-1541">Az.Monitor</span></span>
* <span data-ttu-id="0a960-1542">Nuovi cmdlet per l'API SQR (regola di query pianificata)</span><span class="sxs-lookup"><span data-stu-id="0a960-1542">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="0a960-1543">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="0a960-1543">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="0a960-1544">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1544">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="0a960-1545">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="0a960-1545">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="0a960-1546">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="0a960-1546">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="0a960-1547">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="0a960-1547">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="0a960-1548">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="0a960-1548">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="0a960-1549">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1549">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a960-1550">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1550">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a960-1551">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1551">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a960-1552">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1552">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a960-1553">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1553">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="0a960-1554">[Altre](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) informazioni sull'API SQR</span><span class="sxs-lookup"><span data-stu-id="0a960-1554">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="0a960-1555">Aggiornamento di Az.Monitor.md per includere i cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="0a960-1555">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1556">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1556">Az.Network</span></span>
* <span data-ttu-id="0a960-1557">Aggiunta del supporto per la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="0a960-1557">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="0a960-1558">Nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-1558">New cmdlets</span></span>
        - <span data-ttu-id="0a960-1559">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1559">New-AzNatGateway</span></span>
        - <span data-ttu-id="0a960-1560">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1560">Get-AzNatGateway</span></span>
        - <span data-ttu-id="0a960-1561">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1561">Set-AzNatGateway</span></span>
        - <span data-ttu-id="0a960-1562">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-1562">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="0a960-1563">Aggiornamento dei cmdlet:</span><span class="sxs-lookup"><span data-stu-id="0a960-1563">Updated cmdlets</span></span>
        - <span data-ttu-id="0a960-1564">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a960-1564">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="0a960-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="0a960-1565">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="0a960-1566">Aggiornamento dei comandi seguenti per la funzionalità: Custom routes set/remove on Brooklyn Gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1566">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="0a960-1567">Aggiornamento di New-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1567">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="0a960-1568">Aggiornamento di Set-AzVirtualNetworkGateway: aggiunta del parametro facoltativo -CustomRoute per impostare i prefissi degli indirizzi come route personalizzate da impostare nel gateway.</span><span class="sxs-lookup"><span data-stu-id="0a960-1568">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-1569">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1569">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-1570">Supporto per eseguire query sui dettagli di valutazione dei criteri.</span><span class="sxs-lookup"><span data-stu-id="0a960-1570">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="0a960-1571">Aggiunta del parametro '-Expand' a Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="0a960-1571">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="0a960-1572">Supporto di '-Expand PolicyEvaluationDetails'.</span><span class="sxs-lookup"><span data-stu-id="0a960-1572">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1573">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1573">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1574">Supporto del ripristino sito da Azure ad Azure tra sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="0a960-1574">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="0a960-1575">Contrassegno delle future modifiche che causano un'interruzione per Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a960-1575">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="0a960-1576">Correzione di piano di azione finale del piano di ripristino di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a960-1576">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="0a960-1577">Correzione del mapping di rete per l'aggiornamento di Azure Site Recovery da Azure ad Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1577">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="0a960-1578">Correzione della direzione di protezione per l'aggiornamento di Azure Site Recovery da Azure ad Azure per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="0a960-1578">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="0a960-1579">Altre correzioni minori.</span><span class="sxs-lookup"><span data-stu-id="0a960-1579">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="0a960-1580">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a960-1580">Az.Relay</span></span>
* <span data-ttu-id="0a960-1581">Correzione di errori ortografici in messaggi per i clienti</span><span class="sxs-lookup"><span data-stu-id="0a960-1581">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-1582">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-1582">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-1583">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0a960-1583">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1584">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1584">Az.Storage</span></span>
* <span data-ttu-id="0a960-1585">Aggiornamento alla Libreria client di archiviazione 10.0.1 (lo spazio dei nomi di tutti gli oggetti di questo SDK viene modificato da 'Microsoft.WindowsAzure.Storage. *' a 'Microsoft.Azure.Storage.* ')</span><span class="sxs-lookup"><span data-stu-id="0a960-1585">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="0a960-1586">Aggiornamento a Microsoft.Azure.Management.Storage 11.0.0 per supportare la nuova versione dell'API 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="0a960-1586">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="0a960-1587">Il tipo di account di archiviazione predefinito nella creazione dell'account di archiviazione è stato modificato da 'Storage' a 'StorageV2'</span><span class="sxs-lookup"><span data-stu-id="0a960-1587">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="0a960-1588">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1588">New-AzStorageAccount</span></span>
* <span data-ttu-id="0a960-1589">L'output del cmdlet dell'account di archiviazione Sku.Name è stato modificato per allinearsi all'input SkuName aggiungendo '-', ad esempio 'StandardLRS' è stato modificato in 'Standard_LRS'</span><span class="sxs-lookup"><span data-stu-id="0a960-1589">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="0a960-1590">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1590">New-AzStorageAccount</span></span>
    - <span data-ttu-id="0a960-1591">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1591">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="0a960-1592">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1592">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1593">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1593">Az.Websites</span></span>
* <span data-ttu-id="0a960-1594">La proprietà 'Kind' verrà ora impostata per gli oggetti PSSite restituiti da Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1594">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="0a960-1595">Get-AzWebApp\*Metrics e Get-AzAppServicePlanMetrics sono stati contrassegnati come deprecati</span><span class="sxs-lookup"><span data-stu-id="0a960-1595">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="0a960-1596">1.8.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1596">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-1597">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-1597">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-1598">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0a960-1598">General availability of `Az` module</span></span>
* <span data-ttu-id="0a960-1599">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a960-1599">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a960-1600">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a960-1600">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a960-1601">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1601">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a960-1602">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0a960-1602">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a960-1603">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1603">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a960-1604">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1604">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-1605">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1605">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1606">Aggiornamento di Uninstall-AzureRm per la corretta eliminazione dei moduli in Mac</span><span class="sxs-lookup"><span data-stu-id="0a960-1606">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="0a960-1607">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1607">Az.Batch</span></span>
* <span data-ttu-id="0a960-1608">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1608">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-1609">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-1609">Az.Cdn</span></span>
* <span data-ttu-id="0a960-1610">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1610">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-1611">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1611">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-1612">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1612">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1613">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1613">Az.Compute</span></span>
* <span data-ttu-id="0a960-1614">Risoluzione del problema con l'installazione di AEM se gli ID risorsa dei dischi contenevano gruppi di risorse in lettere minuscole</span><span class="sxs-lookup"><span data-stu-id="0a960-1614">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="0a960-1615">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1615">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1616">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0a960-1616">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1617">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1617">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1618">Aggiunta di SsisProperties se NodeCount non è null per il runtime di integrazione gestito.</span><span class="sxs-lookup"><span data-stu-id="0a960-1618">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1619">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1619">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1620">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1620">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a960-1621">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a960-1621">Az.EventGrid</span></span>
* <span data-ttu-id="0a960-1622">Aggiornamento del testo della guida dell'endpoint per indicare che è necessario creare risorse prima di usare i cmdlet di sottoscrizione per eventi di creazione/aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="0a960-1622">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-1623">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1623">Az.EventHub</span></span>
* <span data-ttu-id="0a960-1624">Aggiunta di nuovi cmdlet per NetworkRuleSet dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0a960-1624">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="0a960-1625">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="0a960-1625">Az.HDInsight</span></span>
* <span data-ttu-id="0a960-1626">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1626">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-1627">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1627">Az.IotHub</span></span>
* <span data-ttu-id="0a960-1628">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1628">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-1629">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1629">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-1630">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1630">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1631">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0a960-1631">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="0a960-1632">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a960-1632">Az.MachineLearning</span></span>
* <span data-ttu-id="0a960-1633">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1633">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="0a960-1634">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a960-1634">Az.Media</span></span>
* <span data-ttu-id="0a960-1635">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1635">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-1636">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-1636">Az.Monitor</span></span>
  * <span data-ttu-id="0a960-1637">Nuovi cmdlet per la regola di avviso basata su metriche GenV2 (non classica)</span><span class="sxs-lookup"><span data-stu-id="0a960-1637">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="0a960-1638">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="0a960-1638">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="0a960-1639">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="0a960-1639">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="0a960-1640">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a960-1640">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a960-1641">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a960-1641">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="0a960-1642">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="0a960-1642">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="0a960-1643">Aggiornamento di Monitor SDK alla versione 0.22.0-preview</span><span class="sxs-lookup"><span data-stu-id="0a960-1643">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1644">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1644">Az.Network</span></span>
* <span data-ttu-id="0a960-1645">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1645">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1646">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0a960-1646">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="0a960-1647">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="0a960-1647">Az.NotificationHubs</span></span>
* <span data-ttu-id="0a960-1648">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1648">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1649">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1649">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1650">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1650">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="0a960-1651">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="0a960-1651">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="0a960-1652">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1652">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1653">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1653">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1654">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1654">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1655">Aggiornamento del formato tabella per SQL in VM Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1655">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="0a960-1656">Aggiunta del metodo alternativo per recuperare la posizione in AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="0a960-1656">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="0a960-1657">Aggiornamento di ScheduleRunDays nell'oggetto SchedulePolicy in base al fuso orario</span><span class="sxs-lookup"><span data-stu-id="0a960-1657">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a960-1658">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a960-1658">Az.RedisCache</span></span>
* <span data-ttu-id="0a960-1659">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1659">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1660">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1660">Az.Resources</span></span>
* <span data-ttu-id="0a960-1661">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0a960-1661">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1662">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1662">Az.Sql</span></span>
* <span data-ttu-id="0a960-1663">Sostituzione della dipendenza da Monitor SDK con codice comune</span><span class="sxs-lookup"><span data-stu-id="0a960-1663">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="0a960-1664">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1664">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1665">Elaborazione avanzata della classificazione di più colonne.</span><span class="sxs-lookup"><span data-stu-id="0a960-1665">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="0a960-1666">Inclusione di proprietà SKU (nome, famiglia, capacità) nella risposta da Get-AzSqlServerServiceObjective e formattazione come tabella per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0a960-1666">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="0a960-1667">Possibilità di eseguire Get-AzSqlServerServiceObjective in base alla senza la necessità di un server preesistente nell'area.</span><span class="sxs-lookup"><span data-stu-id="0a960-1667">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="0a960-1668">Supporto per il parametro del fuso orario nella creazione di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="0a960-1668">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="0a960-1669">Correzione della documentazione per i caratteri jolly</span><span class="sxs-lookup"><span data-stu-id="0a960-1669">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1670">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1670">Az.Websites</span></span>
* <span data-ttu-id="0a960-1671">Correzione di Set-AzWebApp e Set-AzWebAppSlot affinché non vengano rimossi i tag nell'esecuzione</span><span class="sxs-lookup"><span data-stu-id="0a960-1671">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="0a960-1672">Cmdlet aggiornati da nomi plurali a nomi singolari e nomi plurali deprecati.</span><span class="sxs-lookup"><span data-stu-id="0a960-1672">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="0a960-1673">Aggiornamento di WebSites SDK.</span><span class="sxs-lookup"><span data-stu-id="0a960-1673">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="0a960-1674">Rimozione della proprietà AdminSiteName da PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="0a960-1674">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="0a960-1675">1.7.0 - Aprile 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1675">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-1676">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-1676">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-1677">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0a960-1677">General availability of `Az` module</span></span>
* <span data-ttu-id="0a960-1678">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a960-1678">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a960-1679">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a960-1679">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a960-1680">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1680">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a960-1681">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0a960-1681">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a960-1682">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1682">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a960-1683">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1683">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="0a960-1684">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1684">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1685">Aggiornamento di Add-AzEnvironment e Set-AzEnvironment per accettare il parametro AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="0a960-1685">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a960-1686">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1686">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a960-1687">Uso di ServiceClient nei cmdlet del piano dati e rimozione della logica di autenticazione originale</span><span class="sxs-lookup"><span data-stu-id="0a960-1687">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="0a960-1688">Impostazione di Add-AzureASAccount come wrapper di Connect-AzAccount per evitare una modifica che causa un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0a960-1688">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1689">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1689">Az.Automation</span></span>
* <span data-ttu-id="0a960-1690">Correzione del bug del cmdlet New-AzAutomationSoftwareUpdateConfiguration per le inclusioni.</span><span class="sxs-lookup"><span data-stu-id="0a960-1690">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="0a960-1691">Ora i parametri IncludedKbNumber e IncludedPackageNameMask dovrebbero funzionare.</span><span class="sxs-lookup"><span data-stu-id="0a960-1691">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="0a960-1692">Correzione del bug per il gruppo dinamico di gestione degli aggiornamenti di automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1692">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1693">Az.Compute</span></span>
* <span data-ttu-id="0a960-1694">Aggiunta del parametro HyperVGeneration a New-AzDiskConfig e New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-1694">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="0a960-1695">Creazione di VM consentita con l'immagine della raccolta di altri tenant.</span><span class="sxs-lookup"><span data-stu-id="0a960-1695">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="0a960-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a960-1697">Correzione del problema del parametro -Command di New-AzContainerGroup che ha aggiunto un argomento finale vuoto</span><span class="sxs-lookup"><span data-stu-id="0a960-1697">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1698">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1698">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1699">Aggiornamento di ADF .Net SDK alla versione 3.0.2</span><span class="sxs-lookup"><span data-stu-id="0a960-1699">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="0a960-1700">Aggiornamento del cmdlet Set-AzDataFactoryV2 con parametri aggiuntivi per le impostazioni relative a RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0a960-1700">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1701">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1701">Az.Resources</span></span>
* <span data-ttu-id="0a960-1702">Miglioramento della gestione di provider per 'Get-AzResource' quando si specificano i parametri '-ResourceId' or '-ResourceGroupName', '-Name' e '-ResourceType'</span><span class="sxs-lookup"><span data-stu-id="0a960-1702">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="0a960-1703">Miglioramento della gestione degli errori per 'Test-AzDeployment' e 'Test-AzResourceGroupDeployment'</span><span class="sxs-lookup"><span data-stu-id="0a960-1703">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="0a960-1704">Gestione degli errori generati all'esterno della convalida della distribuzione e inclusione nell'output del comando</span><span class="sxs-lookup"><span data-stu-id="0a960-1704">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="0a960-1705">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0a960-1705">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="0a960-1706">Aggiunta del parametro opzionale '-IgnoreDynamicParameters' per impostare i cmdlet di distribuzione in modo da ignorare il prompt negli scenari di script e processi</span><span class="sxs-lookup"><span data-stu-id="0a960-1706">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="0a960-1707">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/6856</span><span class="sxs-lookup"><span data-stu-id="0a960-1707">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1708">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1708">Az.Sql</span></span>
* <span data-ttu-id="0a960-1709">Supporto della classificazione di dati del database.</span><span class="sxs-lookup"><span data-stu-id="0a960-1709">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1710">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1710">Az.Storage</span></span>
* <span data-ttu-id="0a960-1711">Segnalazione dettagliata degli errori quando si crea il contesto di archiviazione con il parametro -UseConnectedAccount, ma senza account Azure di accesso</span><span class="sxs-lookup"><span data-stu-id="0a960-1711">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="0a960-1712">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a960-1712">New-AzStorageContext</span></span>
* <span data-ttu-id="0a960-1713">Supporto per le proprietà del servizio BLOB gestito di un account di archiviazione specificato con l'API del piano di gestione</span><span class="sxs-lookup"><span data-stu-id="0a960-1713">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="0a960-1714">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a960-1714">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a960-1715">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a960-1715">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="0a960-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1716">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="0a960-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1717">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="0a960-1718">Supporto di -AsJob per i cmdlet di caricamento e download di BLOB e file</span><span class="sxs-lookup"><span data-stu-id="0a960-1718">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="0a960-1719">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1719">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a960-1720">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1720">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="0a960-1721">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1721">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="0a960-1722">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="0a960-1722">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="0a960-1723">1.6.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1723">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="0a960-1724">Novità rispetto all'ultima versione principale</span><span class="sxs-lookup"><span data-stu-id="0a960-1724">Highlights since the last major release</span></span>
* <span data-ttu-id="0a960-1725">Disponibilità generale del modulo `Az`</span><span class="sxs-lookup"><span data-stu-id="0a960-1725">General availability of `Az` module</span></span>
* <span data-ttu-id="0a960-1726">Per altre informazioni sul modulo `Az`, vedere https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="0a960-1726">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="0a960-1727">Aggiunta degli oggetti di completamento Location, ResourceGroup e ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="0a960-1727">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="0a960-1728">Aggiunta del supporto dei caratteri jolly ai cmdlet Get per Az.Compute e Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1728">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="0a960-1729">Aggiunta dell'autenticazione interattiva e nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0a960-1729">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a960-1730">Aggiunta del supporto per i runbook Python 2 in Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1730">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="0a960-1731">Az.LogicApp: nuovi cmdlet per gli account di integrazione e configurazione batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1731">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1732">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1732">Az.Automation</span></span>
* <span data-ttu-id="0a960-1733">Modifica della gestione degli aggiornamenti di Automazione di Azure per supportare le nuove funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a960-1733">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="0a960-1734">Raggruppamento dinamico</span><span class="sxs-lookup"><span data-stu-id="0a960-1734">Dynamic grouping</span></span>
    * <span data-ttu-id="0a960-1735">Script pre-post</span><span class="sxs-lookup"><span data-stu-id="0a960-1735">Pre-Post script</span></span>
    * <span data-ttu-id="0a960-1736">Impostazione di riavvio</span><span class="sxs-lookup"><span data-stu-id="0a960-1736">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1737">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1737">Az.Compute</span></span>
* <span data-ttu-id="0a960-1738">Risoluzione del problema con la risoluzione del percorso in Get-AzVmBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="0a960-1738">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="0a960-1739">Aggiornamento della libreria client di Calcolo a 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="0a960-1739">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-1740">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1740">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-1741">Aggiunta del supporto dei caratteri jolly ai cmdlet KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1741">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1742">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1742">Az.Network</span></span>
* <span data-ttu-id="0a960-1743">Aggiunta del supporto di Intelligence per le minacce a Firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1743">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="0a960-1744">Aggiunta di risorse di livello superiore per i criteri firewall del gateway applicazione e di regole personalizzate</span><span class="sxs-lookup"><span data-stu-id="0a960-1744">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1745">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1745">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1746">Aggiunta di SnapshotRetentionInDays nel criterio di VM di Azure per il supporto di Instant RP</span><span class="sxs-lookup"><span data-stu-id="0a960-1746">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="0a960-1747">Aggiunta del supporto di pipe per annullare la registrazione di contenitori</span><span class="sxs-lookup"><span data-stu-id="0a960-1747">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1748">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1748">Az.Resources</span></span>
* <span data-ttu-id="0a960-1749">Aggiornamento del supporto di caratteri jolly per Get-AzResource e Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-1749">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="0a960-1750">Aggiornamento delle credenziali usate quando si effettuano chiamate generiche ad ARM</span><span class="sxs-lookup"><span data-stu-id="0a960-1750">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1751">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1751">Az.Sql</span></span>
* <span data-ttu-id="0a960-1752">Modifica del parametro (ExcludeDetectionType) dei cmdlet di Rilevamento minacce da DetectionType a string[] per renderlo compatibile con le versioni future quando vengono aggiunti nuovi elementi DetectionType e per supportare anche il completamento automatico.</span><span class="sxs-lookup"><span data-stu-id="0a960-1752">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1753">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1753">Az.Storage</span></span>
* <span data-ttu-id="0a960-1754">Supporto di criteri di gestione Get/Set/Remove in un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1754">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="0a960-1755">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1755">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a960-1756">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1756">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a960-1757">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1757">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="0a960-1758">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="0a960-1758">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="0a960-1759">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="0a960-1759">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="0a960-1760">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="0a960-1760">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1761">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1761">Az.Websites</span></span>
* <span data-ttu-id="0a960-1762">Correzione del bug del modello ARM che interrompe la clonazione di tutti gli slot con "New-AzWebApp -IncludeSourceWebAppSlots"</span><span class="sxs-lookup"><span data-stu-id="0a960-1762">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="0a960-1763">1.5.0 - Marzo 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1763">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1764">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1764">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1765">Aggiunta del comando "Register-AzModule" per supportare i cmdlet generati da AutoRest</span><span class="sxs-lookup"><span data-stu-id="0a960-1765">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="0a960-1766">Aggiornamento degli esempi per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1766">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1767">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1767">Az.Automation</span></span>
* <span data-ttu-id="0a960-1768">Risoluzione del problema relativo al recupero di alcune pianificazioni mensili in diversi cmdlet di Automazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1768">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a960-1769">Risoluzione del problema per il quale Get-AzAutomationDscNode restituiva solo i primi 20 nodi.</span><span class="sxs-lookup"><span data-stu-id="0a960-1769">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="0a960-1770">Ora restituisce tutti i nodi.</span><span class="sxs-lookup"><span data-stu-id="0a960-1770">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-1771">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-1771">Az.Cdn</span></span>
* <span data-ttu-id="0a960-1772">Aggiunta di nuovi cmdlet di PowerShell per l'abilitazione/disabilitazione di HTTPS per domini personalizzati. I cmdlet precedenti sono deprecati</span><span class="sxs-lookup"><span data-stu-id="0a960-1772">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1773">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1773">Az.Compute</span></span>
* <span data-ttu-id="0a960-1774">Aggiunta del supporto dei caratteri jolly ai cmdlet Get</span><span class="sxs-lookup"><span data-stu-id="0a960-1774">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1775">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1775">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1776">Aggiornamento di ADF .Net SDK alla versione 3.0.1</span><span class="sxs-lookup"><span data-stu-id="0a960-1776">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a960-1777">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1777">Az.LogicApp</span></span>
* <span data-ttu-id="0a960-1778">Risoluzione del problema per il quale ListWorkflows recuperava solo la prima pagina dei risultati</span><span class="sxs-lookup"><span data-stu-id="0a960-1778">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1779">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1779">Az.Network</span></span>
* <span data-ttu-id="0a960-1780">Aggiunta del supporto dei caratteri jolly ai cmdlet Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1780">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1781">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1781">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1782">Aggiunta del supporto di SQL Server nelle macchine virtuali di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-1782">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="0a960-1783">Aggiornamento di SDK</span><span class="sxs-lookup"><span data-stu-id="0a960-1783">SDK Update</span></span>
* <span data-ttu-id="0a960-1784">Rimozione del controllo VMappContainer in Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0a960-1784">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="0a960-1785">Aggiunta di Name e ServerName come parametri per Get-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0a960-1785">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1786">Az.Resources</span></span>
* <span data-ttu-id="0a960-1787">Aggiunta del parametro`-TemplateObject`ai cmdlet di distribuzione</span><span class="sxs-lookup"><span data-stu-id="0a960-1787">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="0a960-1788">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2933</span><span class="sxs-lookup"><span data-stu-id="0a960-1788">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="0a960-1789">Risoluzione del problema con il piping del risultato di `Get-AzResource` in `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0a960-1789">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="0a960-1790">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8240</span><span class="sxs-lookup"><span data-stu-id="0a960-1790">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="0a960-1791">Risoluzione del problema con la modifica del tipo di dati JSON durante l'esecuzione di `Set-AzResource`</span><span class="sxs-lookup"><span data-stu-id="0a960-1791">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="0a960-1792">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7930</span><span class="sxs-lookup"><span data-stu-id="0a960-1792">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1793">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1793">Az.Sql</span></span>
* <span data-ttu-id="0a960-1794">Aggiornamento di AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="0a960-1794">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="0a960-1795">Correzione del comportamento di un caso limite durante la creazione di nuove impostazioni di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="0a960-1795">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1796">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1796">Az.Storage</span></span>
* <span data-ttu-id="0a960-1797">Supporto del tipo BlockBlobStorage quando si crea un account di archiviazione - New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-1797">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="0a960-1798">1.4.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1798">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="0a960-1799">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1799">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a960-1800">Cmdlet AddAzureASAccount deprecato</span><span class="sxs-lookup"><span data-stu-id="0a960-1800">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1801">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1801">Az.Automation</span></span>
* <span data-ttu-id="0a960-1802">Aggiornamento della Guida per Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1802">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="0a960-1803">Aggiunta della convalida del nome configurazione nel cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1803">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="0a960-1804">Miglioramento della gestione degli errori per il cmdlet Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1804">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-1805">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1805">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-1806">Aggiunta di CustomSubdomainName come nuovo parametro facoltativo per New-AzCognitiveServicesAccount, usato per specificare un sottodominio della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a960-1806">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1807">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1807">Az.Compute</span></span>
* <span data-ttu-id="0a960-1808">Correzione del problema dei set di parametri ID</span><span class="sxs-lookup"><span data-stu-id="0a960-1808">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="0a960-1809">Aggiornamento di Get-AzVMExtension per elencare tutte le estensioni installate se non viene specificato il parametro Name</span><span class="sxs-lookup"><span data-stu-id="0a960-1809">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="0a960-1810">Aggiunta dei parametri Tag e ResourceId al cmdlet Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0a960-1810">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="0a960-1811">Get-AzVmssVM senza ID istanza e con InstanceView può elencare le VM del set di scalabilità di macchine virtuali con la visualizzazione dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0a960-1811">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1812">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1812">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1813">Aggiunta di cmdlet per l'enumerazione e il ripristino di elementi ADL eliminati</span><span class="sxs-lookup"><span data-stu-id="0a960-1813">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="0a960-1814">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1814">Az.EventHub</span></span>
* <span data-ttu-id="0a960-1815">Aggiunta della nuova proprietà booleana SkipEmptyArchives per ignorare gli archivi vuoti nella classe CaptureDescription di Eventhub</span><span class="sxs-lookup"><span data-stu-id="0a960-1815">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-1816">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1816">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-1817">Correzione dell'assegnazione di tag in Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0a960-1817">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a960-1818">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1818">Az.LogicApp</span></span>
* <span data-ttu-id="0a960-1819">Aggiunta dello SKU Basic per gli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1819">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="0a960-1820">Aggiunta nei tipi XSLT 2.0, XSLT 3.0 e mappa Liquid</span><span class="sxs-lookup"><span data-stu-id="0a960-1820">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="0a960-1821">Nuovi cmdlet per gli assembly di account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1821">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="0a960-1822">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a960-1822">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a960-1823">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a960-1823">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a960-1824">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a960-1824">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="0a960-1825">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="0a960-1825">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="0a960-1826">Nuovi cmdlet per la configurazione batch degli account di integrazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1826">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="0a960-1827">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1827">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a960-1828">New-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1828">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a960-1829">Remove-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1829">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="0a960-1830">Set-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-1830">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="0a960-1831">Aggiornamento dell'SDK dell'app per la logica alla versione 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0a960-1831">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="0a960-1832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-1832">Az.Monitor</span></span>
* <span data-ttu-id="0a960-1833">Aggiornamento della Guida per Get-AzMetric</span><span class="sxs-lookup"><span data-stu-id="0a960-1833">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1834">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1834">Az.Network</span></span>
* <span data-ttu-id="0a960-1835">Aggiornamento dell'esempio della Guida per Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0a960-1835">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-1836">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-1836">Az.OperationalInsights</span></span>
* <span data-ttu-id="0a960-1837">Supporto aggiuntivo per la creazione e il recupero di origini dati di ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="0a960-1837">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="0a960-1838">Aggiunta del nuovo tipo 'ApplicationInsights' per supportare il recupero di tutte o di specifiche origini dati di ApplicationInsights per una specifica area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0a960-1838">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="0a960-1839">Aggiunta del cmdlet New-AzOperationalInsightsApplicationInsightsDataSource per la creazione di un'origine dati in base a specifici parametri della risorsa Application-Insights: ID sottoscrizione, nome del gruppo di risorse e nome.</span><span class="sxs-lookup"><span data-stu-id="0a960-1839">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1840">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1840">Az.Resources</span></span>
* <span data-ttu-id="0a960-1841">correzione del problema https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0a960-1841">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a960-1842">correzione del problema https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0a960-1842">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="0a960-1843">correzione del problema https://github.com/Azure/azure-powershell/issues/6219</span><span class="sxs-lookup"><span data-stu-id="0a960-1843">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="0a960-1844">Correzione del bug che impedisce di ripetere la creazione di KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="0a960-1844">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1845">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1845">Az.Sql</span></span>
* <span data-ttu-id="0a960-1846">Aggiunta del supporto per il livello Hyperscale del database SQL</span><span class="sxs-lookup"><span data-stu-id="0a960-1846">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="0a960-1847">Correzione del bug per cui il ripristino potrebbe non riuscire a causa dell'impostazione di proprietà non necessarie nella richiesta</span><span class="sxs-lookup"><span data-stu-id="0a960-1847">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1848">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1848">Az.Websites</span></span>
* <span data-ttu-id="0a960-1849">Correzione dell'esempio in Get-AzWebAppSlotMetrics</span><span class="sxs-lookup"><span data-stu-id="0a960-1849">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="0a960-1850">1.3.0 - Febbraio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1850">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1851">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1851">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1852">Aggiornamento alla versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0a960-1852">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a960-1853">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1853">Az.AnalysisServices</span></span>
<span data-ttu-id="0a960-1854">Disponibilità generale del modulo Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="0a960-1854">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1855">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1855">Az.Compute</span></span>
* <span data-ttu-id="0a960-1856">Estensione AEM: aggiunta del supporto di UltraSSD e dei dischi P60, P70 e P80</span><span class="sxs-lookup"><span data-stu-id="0a960-1856">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="0a960-1857">Aggiornamento della descrizione della Guida per Set-AzVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="0a960-1857">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="0a960-1858">Aggiornamento della descrizione della Guida e dell'esempio per Update-AzImage</span><span class="sxs-lookup"><span data-stu-id="0a960-1858">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1859">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1859">Az.RecoveryServices</span></span>
<span data-ttu-id="0a960-1860">Disponibilità generale del modulo Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="0a960-1860">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1861">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1861">Az.Resources</span></span>
* <span data-ttu-id="0a960-1862">Correzione dei contrassegni per i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="0a960-1862">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="0a960-1863">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8166</span><span class="sxs-lookup"><span data-stu-id="0a960-1863">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="0a960-1864">Correzione del problema in cui `Get-AzureRmRoleAssignment` non rispetta -ErrorAction</span><span class="sxs-lookup"><span data-stu-id="0a960-1864">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="0a960-1865">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8235</span><span class="sxs-lookup"><span data-stu-id="0a960-1865">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1866">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1866">Az.Sql</span></span>
* <span data-ttu-id="0a960-1867">Aggiunta di Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="0a960-1867">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="0a960-1868">Risoluzione del problema in cui il mancato accesso all'account di Azure comporta un'eccezione nullref durante l'esecuzione di cmdlet SQL</span><span class="sxs-lookup"><span data-stu-id="0a960-1868">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="0a960-1869">Correzione dell'eccezione nullref in Get-AzSqlCapability</span><span class="sxs-lookup"><span data-stu-id="0a960-1869">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="0a960-1870">1.2.1 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1870">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1871">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1871">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1872">Rilascio con la versione corretta dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1872">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="0a960-1873">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1873">Az.AnalysisServices</span></span>
* <span data-ttu-id="0a960-1874">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1874">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-1875">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-1875">Az.RecoveryServices</span></span>
* <span data-ttu-id="0a960-1876">Rilascio con la dipendenza aggiornata dell'autenticazione</span><span class="sxs-lookup"><span data-stu-id="0a960-1876">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="0a960-1877">1.2.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1877">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1878">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1878">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1879">Aggiunta dell'autenticazione interattiva e con nome utente/password solo per Windows PowerShell 5.1</span><span class="sxs-lookup"><span data-stu-id="0a960-1879">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="0a960-1880">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1880">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a960-1881">Aggiunta del messaggio di avviso in PS Core per Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0a960-1881">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="0a960-1882">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="0a960-1882">Az.Aks</span></span>
* <span data-ttu-id="0a960-1883">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1883">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="0a960-1884">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-1884">Az.Automation</span></span>
* <span data-ttu-id="0a960-1885">Aggiunta del supporto dei runbook Python 2</span><span class="sxs-lookup"><span data-stu-id="0a960-1885">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="0a960-1886">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1886">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="0a960-1887">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="0a960-1887">Az.Cdn</span></span>
* <span data-ttu-id="0a960-1888">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1888">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1889">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1889">Az.Compute</span></span>
* <span data-ttu-id="0a960-1890">Aggiunta del cmdlet Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="0a960-1890">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="0a960-1891">Aggiunta del parametro TempDisk a Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="0a960-1891">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="0a960-1892">Correzione del messaggio di avviso di New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a960-1892">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="0a960-1893">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0a960-1893">Az.ContainerRegistry</span></span>
* <span data-ttu-id="0a960-1894">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1894">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="0a960-1895">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="0a960-1895">Az.DataFactory</span></span>
* <span data-ttu-id="0a960-1896">Aggiornamento di ADF .Net SDK alla versione 3.0.0</span><span class="sxs-lookup"><span data-stu-id="0a960-1896">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1897">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1897">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1898">Correzione del problema con l'endpoint ADLS durante l'uso dell'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0a960-1898">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="0a960-1899">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7462</span><span class="sxs-lookup"><span data-stu-id="0a960-1899">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="0a960-1900">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1900">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-1901">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1901">Az.IotHub</span></span>
* <span data-ttu-id="0a960-1902">Aggiunta del formato di codifica al cmdlet Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0a960-1902">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="0a960-1903">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-1903">Az.KeyVault</span></span>
* <span data-ttu-id="0a960-1904">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1904">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-1905">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-1905">Az.Network</span></span>
* <span data-ttu-id="0a960-1906">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1906">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1907">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1907">Az.Resources</span></span>
* <span data-ttu-id="0a960-1908">Correzione di esempi errati nella documentazione di riferimento di "New-AzADAppCredential" e "New-AzADSpCredential"</span><span class="sxs-lookup"><span data-stu-id="0a960-1908">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="0a960-1909">Correzione del problema in cui il parametro "-TemplateFile" non veniva risolto prima di eseguire i cmdlet di distribuzione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0a960-1909">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="0a960-1910">Az.Resources: correzione della documentazione per il valore predefinito New-AzureRmPolicyDefinition -Mode</span><span class="sxs-lookup"><span data-stu-id="0a960-1910">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="0a960-1911">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/7522</span><span class="sxs-lookup"><span data-stu-id="0a960-1911">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="0a960-1912">Az.Resources: correzione del problema https://github.com/Azure/azure-powershell/issues/5747</span><span class="sxs-lookup"><span data-stu-id="0a960-1912">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="0a960-1913">Correzione del problema di formattazione con l'oggetto "PSResourceGroupDeployment"</span><span class="sxs-lookup"><span data-stu-id="0a960-1913">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="0a960-1914">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/2123</span><span class="sxs-lookup"><span data-stu-id="0a960-1914">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-1915">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-1915">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-1916">Rollback quando un certificato viene aggiunto al modello del set di scalabilità di macchine virtuali ma viene generata un'eccezione per correggere il bug: https://github.com/Azure/service-fabric-issues/issues/932</span><span class="sxs-lookup"><span data-stu-id="0a960-1916">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="0a960-1917">Correzione di alcuni messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="0a960-1917">Fix some error messages.</span></span>
* <span data-ttu-id="0a960-1918">Correzione della creazione del cluster con il modello ARM predefinito per New-AzServiceFabriCluster che non funzionava con la migrazione ad Az.</span><span class="sxs-lookup"><span data-stu-id="0a960-1918">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="0a960-1919">Correzione dell'aggiunta del certificato del cluster/dell'applicazione in modo che vengano aggiunti solo i set di scalabilità di macchine virtuali corrispondenti al cluster verificando l'ID cluster nell'estensione.</span><span class="sxs-lookup"><span data-stu-id="0a960-1919">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a960-1920">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a960-1920">Az.SignalR</span></span>
* <span data-ttu-id="0a960-1921">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1921">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1922">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1922">Az.Sql</span></span>
* <span data-ttu-id="0a960-1923">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1923">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a960-1924">Aggiornamento della descrizione del parametro LicenseType con i valori possibili</span><span class="sxs-lookup"><span data-stu-id="0a960-1924">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="0a960-1925">Correzione per l'aggiornamento dell'identità dell'istanza gestita che non funziona quando è l'unica proprietà aggiornata</span><span class="sxs-lookup"><span data-stu-id="0a960-1925">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="0a960-1926">Supporto delle regole di confronto personalizzate nell'istanza gestita</span><span class="sxs-lookup"><span data-stu-id="0a960-1926">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1927">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1927">Az.Storage</span></span>
* <span data-ttu-id="0a960-1928">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1928">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a960-1929">Visualizzazione di un messaggio di errore dettagliato relativo alla ricezione/all'impostazione della registrazione/della metrica classica nell'account di Archiviazione Premium, perché tale account non supporta la registrazione/la metrica classica.</span><span class="sxs-lookup"><span data-stu-id="0a960-1929">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="0a960-1930">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="0a960-1930">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="0a960-1931">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="0a960-1931">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="0a960-1932">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="0a960-1932">Az.TrafficManager</span></span>
* <span data-ttu-id="0a960-1933">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1933">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1934">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1934">Az.Websites</span></span>
* <span data-ttu-id="0a960-1935">Aggiornamento degli URL errati della Guida in linea</span><span class="sxs-lookup"><span data-stu-id="0a960-1935">Update incorrect online help URLs</span></span>
* <span data-ttu-id="0a960-1936">Correzioni a "New-AzWebAppSSLBinding" per caricare il certificato nel gruppo di risorse e nella posizione corretti se l'app è ospitata in un ambiente del servizio app di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-1936">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="0a960-1937">Correzioni a "New-AzWebAppSSLBinding" per evitare che i tag vengano sovrascritti nell'associazione di un certificato SSL a un'app</span><span class="sxs-lookup"><span data-stu-id="0a960-1937">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="0a960-1938">1.1.0 - Gennaio 2019</span><span class="sxs-lookup"><span data-stu-id="0a960-1938">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="0a960-1939">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1939">Az.Accounts</span></span>
* <span data-ttu-id="0a960-1940">Aggiunta dell'ambito 'Local' a Enable-AzureRmAlias</span><span class="sxs-lookup"><span data-stu-id="0a960-1940">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-1941">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-1941">Az.Compute</span></span>
* <span data-ttu-id="0a960-1942">Il nome è ora facoltativo nel parametro ID impostato per Restart/Start/Stop/Remove/Set-AzVM e Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="0a960-1942">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="0a960-1943">Aggiornamento della descrizione dell'ID nei file della Guida</span><span class="sxs-lookup"><span data-stu-id="0a960-1943">Updated the description of ID in help files</span></span>
* <span data-ttu-id="0a960-1944">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1944">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-1945">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-1945">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-1946">Aggiornamento della versione dell'SDK del piano dati alla versione 1.1.14 per le correzioni dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="0a960-1946">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="0a960-1947">Correzione della gestione dei valori negativi di acesstime e modificationtime per getfilestatus e liststatus; correzione del token di annullamento asincrono</span><span class="sxs-lookup"><span data-stu-id="0a960-1947">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="0a960-1948">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="0a960-1948">Az.EventGrid</span></span>
* <span data-ttu-id="0a960-1949">Aggiornamento per l'uso della versione API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="0a960-1949">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="0a960-1950">Aggiornamento dei seguenti cmdlet per supportare un nuovo scenario nella versione API 2019-01-01</span><span class="sxs-lookup"><span data-stu-id="0a960-1950">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="0a960-1951">New-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0a960-1951">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a960-1952">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0a960-1952">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a960-1953">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0a960-1953">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a960-1954">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0a960-1954">Dead letter endpoint.</span></span>
    - <span data-ttu-id="0a960-1955">Update-AzureRmEventGridSubscription: aggiunta di nuovi parametri facoltativi che consentono di specificare:</span><span class="sxs-lookup"><span data-stu-id="0a960-1955">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="0a960-1956">Durata (TTL) dell'evento</span><span class="sxs-lookup"><span data-stu-id="0a960-1956">Event Time-To-Live,</span></span>
        - <span data-ttu-id="0a960-1957">Numero massimo di tentativi di recapito per gli eventi</span><span class="sxs-lookup"><span data-stu-id="0a960-1957">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="0a960-1958">Endpoint di messaggi non recapitabili</span><span class="sxs-lookup"><span data-stu-id="0a960-1958">Dead letter endpoint.</span></span>
* <span data-ttu-id="0a960-1959">Aggiunta di nuovi valori di enumerazione (vale a dire, storageQueue e hybridConnection) per l'opzione EndpointType nei cmdlet New-AzureRmEventGridSubscription e Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="0a960-1959">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="0a960-1960">Visualizzazione del messaggio di avviso se la creazione o l'aggiornamento della sottoscrizione di eventi dovrebbe comportare un'azione manuale da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0a960-1960">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="0a960-1961">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1961">Az.IotHub</span></span>
* <span data-ttu-id="0a960-1962">Aggiornamento alla versione più recente dell'SDK IotHub</span><span class="sxs-lookup"><span data-stu-id="0a960-1962">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="0a960-1963">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="0a960-1963">Az.LogicApp</span></span>
* <span data-ttu-id="0a960-1964">Get-AzLogicApp elenca tutto senza nome specificato</span><span class="sxs-lookup"><span data-stu-id="0a960-1964">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-1965">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-1965">Az.Resources</span></span>
* <span data-ttu-id="0a960-1966">Correzione del problema relativo al set di parametri quando si specificano i parametri '-ODataQuery' e '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0a960-1966">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="0a960-1967">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/7875</span><span class="sxs-lookup"><span data-stu-id="0a960-1967">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="0a960-1968">Correzione della gestione del parametro -Custom in New/Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0a960-1968">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a960-1969">Correzione di un errore di battitura nella documentazione di New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="0a960-1969">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="0a960-1970">Il parametro '-MailNickname' è diventato obbligatorio per 'New-AzADUser'</span><span class="sxs-lookup"><span data-stu-id="0a960-1970">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="0a960-1971">Altre informazioni sono disponibili qui: https://github.com/Azure/azure-powershell/issues/8220</span><span class="sxs-lookup"><span data-stu-id="0a960-1971">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="0a960-1972">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="0a960-1972">Az.SignalR</span></span>
* <span data-ttu-id="0a960-1973">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1973">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-1974">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-1974">Az.Sql</span></span>
* <span data-ttu-id="0a960-1975">Conversione della dipendenza di client di gestione archiviazione nell'implementazione dell'SDK comune.</span><span class="sxs-lookup"><span data-stu-id="0a960-1975">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="0a960-1976">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-1976">Az.Storage</span></span>
* <span data-ttu-id="0a960-1977">Impostazione di StorageAccountName di un contesto di archiviazione come nome reale dell'account di archiviazione al momento della creazione con Sas Token, OAuth o Anonymous</span><span class="sxs-lookup"><span data-stu-id="0a960-1977">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="0a960-1978">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a960-1978">New-AzStorageContext</span></span>
* <span data-ttu-id="0a960-1979">Creazione del token di firma di accesso condiviso dell'oggetto snapshot del BLOB con il parametro '-FullUri'; correzione dell'URI restituito in modo da essere l'URI dello snapshot</span><span class="sxs-lookup"><span data-stu-id="0a960-1979">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="0a960-1980">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="0a960-1980">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-1981">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-1981">Az.Websites</span></span>
* <span data-ttu-id="0a960-1982">Correzione di un bug relativo all'analisi delle date in 'Get-AzDeletedWebApp'</span><span class="sxs-lookup"><span data-stu-id="0a960-1982">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="0a960-1983">Risoluzione del problema relativo alla compatibilità con le versioni precedenti con il modulo Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1983">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="0a960-1984">1.0.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-1984">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="0a960-1985">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-1985">General</span></span>

- <span data-ttu-id="0a960-1986">Disponibilità generale del modulo Az</span><span class="sxs-lookup"><span data-stu-id="0a960-1986">General Availability of Az Module</span></span>
- <span data-ttu-id="0a960-1987">Guida per ogni modulo</span><span class="sxs-lookup"><span data-stu-id="0a960-1987">Online help for each module</span></span>
- <span data-ttu-id="0a960-1988">Per altre informazioni e una roadmap, vedere la [pagina di annuncio di Az](https://aka.ms/azps-announce)</span><span class="sxs-lookup"><span data-stu-id="0a960-1988">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="0a960-1989">Vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide) per informazioni sulla migrazione da AzureRM</span><span class="sxs-lookup"><span data-stu-id="0a960-1989">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="0a960-1990">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-1990">Az.Accounts</span></span>
- <span data-ttu-id="0a960-1991">Modificato da Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a960-1991">Changed from Az.Profile</span></span>
- <span data-ttu-id="0a960-1992">Correzione dei formati di tabella per i tipi di profilo e di contesto</span><span class="sxs-lookup"><span data-stu-id="0a960-1992">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a960-1993">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-1993">Az.ApiManagement</span></span>
- <span data-ttu-id="0a960-1994">Correzioni per #7002</span><span class="sxs-lookup"><span data-stu-id="0a960-1994">Fixes for #7002</span></span>
- <span data-ttu-id="0a960-1995">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-1995">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="0a960-1996">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="0a960-1996">Az.Batch</span></span>
- <span data-ttu-id="0a960-1997">Aggiunta della possibilità di vedere quale versione dell'agente del nodo di Azure Batch è in esecuzione in ciascuna delle macchine virtuali di un pool tramite la nuova proprietà`NodeAgentInformation` in `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="0a960-1997">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="0a960-1998">Il valore predefinito di `Caching` per `PSDataDisk` è ora `ReadWrite` invece di `None`.</span><span class="sxs-lookup"><span data-stu-id="0a960-1998">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="0a960-1999">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-1999">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="0a960-2000">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="0a960-2000">Az.Billing</span></span>
- <span data-ttu-id="0a960-2001">Combina i cmdlet Billing, Consumption e UsageAggregates. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2001">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="0a960-2002">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="0a960-2002">Az.CognitivServices</span></span>
- <span data-ttu-id="0a960-2003">Aggiunta degli strumenti di completamento per SkuName e Typem disponibili nell'operazione New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-2003">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="0a960-2004">Rimozione del set di parametri GetSkusWithAccountParamSetName da Get-AzCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="0a960-2004">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a960-2005">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2005">Az.ContainerInstance</span></span>
- <span data-ttu-id="0a960-2006">Aggiunta del supporto di ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0a960-2006">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="0a960-2007">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="0a960-2007">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="0a960-2008">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2008">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a960-2009">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-2009">Az.DataLakeStore</span></span>
- <span data-ttu-id="0a960-2010">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2010">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="0a960-2011">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="0a960-2011">Az.Monitor</span></span>
- <span data-ttu-id="0a960-2012">Ridenominazione di Az.Insights in Az.Monitor e altre modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2012">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="0a960-2013">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="0a960-2013">Az.KeyVault</span></span>
- <span data-ttu-id="0a960-2014">Rimozione della la proprietà 'PurgeDisabled' deprecata da tipi di output</span><span class="sxs-lookup"><span data-stu-id="0a960-2014">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="0a960-2015">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="0a960-2015">Az.MachineLearning</span></span>
- <span data-ttu-id="0a960-2016">Inclusione dei cmdlet del modulo Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="0a960-2016">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="0a960-2017">Az.Media</span><span class="sxs-lookup"><span data-stu-id="0a960-2017">Az.Media</span></span>
- <span data-ttu-id="0a960-2018">Rimozione dell'alias -Tags deprecato dai New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="0a960-2018">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a960-2019">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-2019">Az.Network</span></span>
<span data-ttu-id="0a960-2020">Aggiunta del supporto per la configurazione di RewriteRuleSets nel gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="0a960-2020">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="0a960-2021">Nuovi cmdlet aggiunti:</span><span class="sxs-lookup"><span data-stu-id="0a960-2021">New cmdlets added:</span></span>
        - <span data-ttu-id="0a960-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2022">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2023">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2024">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2025">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2026">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2027">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="0a960-2027">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="0a960-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2028">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="0a960-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a960-2029">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="0a960-2030">Cmdlet aggiornati con il parametro facoltativo -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="0a960-2030">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="0a960-2031">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0a960-2031">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="0a960-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a960-2032">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a960-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="0a960-2033">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="0a960-2034">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-2034">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="0a960-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-2035">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="0a960-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Aggiunta del supporto di KeyVault al gateway applicazione usando Identity.</span><span class="sxs-lookup"><span data-stu-id="0a960-2036">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="0a960-2037">Cmdlet aggiornati con il parametro facoltativo -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="0a960-2037">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="0a960-2038">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a960-2038">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a960-2039">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a960-2039">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="0a960-2040">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0a960-2040">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="0a960-2041">Cmdlet New-AzApplicationGateway aggiornato con il parametro facoltativo -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0a960-2041">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="0a960-2042">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2042">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="0a960-2043">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-2043">Az.OperationalInsights</span></span>
- <span data-ttu-id="0a960-2044">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2044">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="0a960-2045">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a960-2045">Az.Profile</span></span>
- <span data-ttu-id="0a960-2046">Modifica del nome del modulo in Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="0a960-2046">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-2047">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-2047">Az.RecoveryServices</span></span>
- <span data-ttu-id="0a960-2048">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2048">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="0a960-2049">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2049">Az.Resources</span></span>
- <span data-ttu-id="0a960-2050">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2050">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a960-2051">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-2051">Az.ServiceFabric</span></span>
- <span data-ttu-id="0a960-2052">Supporto della specifica del certificato per nome comune e identificazione personale</span><span class="sxs-lookup"><span data-stu-id="0a960-2052">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="0a960-2053">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2053">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="0a960-2054">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0a960-2054">Az.SIgnalR</span></span>
- <span data-ttu-id="0a960-2055">Disponibilità generale per i cmdlet di PowerShell per SIgnalR</span><span class="sxs-lookup"><span data-stu-id="0a960-2055">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="0a960-2056">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-2056">Az.Sql</span></span>
- <span data-ttu-id="0a960-2057">Aggiunta dei nuovi tipi di rilevamento Data_Exfiltration e Unsafe_Action ai cmdlet di rilevamento delle minacce</span><span class="sxs-lookup"><span data-stu-id="0a960-2057">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="0a960-2058">Aggiornamento degli esempi di documentazione per i cmdlet di controllo Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-2058">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="0a960-2059">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2059">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a960-2060">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-2060">Az.Storage</span></span>
- <span data-ttu-id="0a960-2061">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2061">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a960-2062">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-2062">Az.Websites</span></span>
- <span data-ttu-id="0a960-2063">Modifiche che causano un'interruzione di minore entità. Per informazioni dettagliate, vedere la [Guida alla migrazione](https://aka.ms/azps-migration-guide)</span><span class="sxs-lookup"><span data-stu-id="0a960-2063">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="0a960-2064">0.7.0 - Dicembre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2064">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="0a960-2065">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-2065">General</span></span>

* <span data-ttu-id="0a960-2066">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0a960-2066">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a960-2067">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-2067">Az.Compute</span></span>

* <span data-ttu-id="0a960-2068">Aggiunta del supporto di UltraSSD e delle immagini della raccolta nei set di parametri semplici per i cmdlet `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="0a960-2068">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="0a960-2069">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-2069">Az.DataLakeStore</span></span>

* <span data-ttu-id="0a960-2070">Correzione della barra finale del dominio dell'account adls</span><span class="sxs-lookup"><span data-stu-id="0a960-2070">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="0a960-2071">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="0a960-2071">Az.FrontDoor</span></span>

* <span data-ttu-id="0a960-2072">Correzione di alcuni collegamenti interrotti</span><span class="sxs-lookup"><span data-stu-id="0a960-2072">Fixed some broken links</span></span>
    - <span data-ttu-id="0a960-2073">Negli articoli di New-AzureRmFrontDoor e Set-AzureRmFrontDoor è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="0a960-2073">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="0a960-2074">Nell'articolo di New-AzureRmFrontDoorManagedRuleObject è stato corretto il collegamento all'articolo del cmdlet New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="0a960-2074">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="0a960-2075">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="0a960-2075">Az.RecoveryServices</span></span>

* <span data-ttu-id="0a960-2076">Aggiunta delle convalide lato client per le operazioni di ripristino della condivisione file di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-2076">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="0a960-2077">storageAccountName e storageAccountResourceGroupName sono diventati facoltativi per il ripristino afs.</span><span class="sxs-lookup"><span data-stu-id="0a960-2077">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a960-2078">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2078">Az.Resources</span></span>

* <span data-ttu-id="0a960-2079">Correzione per https://github.com/Azure/azure-powershell/issues/7679</span><span class="sxs-lookup"><span data-stu-id="0a960-2079">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="0a960-2080">Aggiornamento di Get-AzureRmRoleAssignment per usare l'ambito della sottoscrizione se fornito quando vengono richiesti gli amministratori classici.</span><span class="sxs-lookup"><span data-stu-id="0a960-2080">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="0a960-2081">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-2081">Az.Sql</span></span>

* <span data-ttu-id="0a960-2082">Modifiche di lieve entità per l'imminente transizione da AzureRM ad Az</span><span class="sxs-lookup"><span data-stu-id="0a960-2082">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="0a960-2083">Risoluzione del problema relativo all'uso di Get-AzureRmSqlDatabaseVulnerabilityAssessment con DotNet core</span><span class="sxs-lookup"><span data-stu-id="0a960-2083">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="0a960-2084">Modifica della documentazione dei messaggi relativi ai cmdlet di controllo SQL.</span><span class="sxs-lookup"><span data-stu-id="0a960-2084">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="0a960-2085">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-2085">Az.Storage</span></span>

* <span data-ttu-id="0a960-2086">Aggiunta di -EnableHierarchicalNamespace a New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-2086">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="0a960-2087">Risoluzione del problema per cui il cmdlet di copia file non può riusare il contesto di origine nella destinazione quando non viene immesso -DestContext</span><span class="sxs-lookup"><span data-stu-id="0a960-2087">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="0a960-2088">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-2088">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a960-2089">Supporto della configurazione del sito Web statico</span><span class="sxs-lookup"><span data-stu-id="0a960-2089">Support Static Website configuration</span></span>
    - <span data-ttu-id="0a960-2090">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a960-2090">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="0a960-2091">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="0a960-2091">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="0a960-2092">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-2092">Az.Websites</span></span>

* <span data-ttu-id="0a960-2093">Set-AzureRmWebApp e Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="0a960-2093">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="0a960-2094">È stato aggiunto il nuovo parametro (-AzureStoragePath) per specificare i percorsi di Archiviazione di Azure da montare nelle app contenitore di Windows e Linux.</span><span class="sxs-lookup"><span data-stu-id="0a960-2094">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="0a960-2095">Usare l'output del nuovo cmdlet New-AzureRmWebAppAzureStoragePath come parametro per impostare i percorsi di Archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0a960-2095">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="0a960-2096">0.6.1 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2096">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="0a960-2097">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a960-2097">Az.ApiManagement</span></span>
* <span data-ttu-id="0a960-2098">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a960-2098">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="0a960-2099">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="0a960-2099">Az.Automation</span></span>
* <span data-ttu-id="0a960-2100">Cmdlet di Automazione di Azure basati su Swagger</span><span class="sxs-lookup"><span data-stu-id="0a960-2100">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="0a960-2101">Aggiunta di cmdlet di Gestione aggiornamenti</span><span class="sxs-lookup"><span data-stu-id="0a960-2101">Added Update Management cmdlets</span></span>
* <span data-ttu-id="0a960-2102">Aggiunta di cmdlet di controllo del codice sorgente</span><span class="sxs-lookup"><span data-stu-id="0a960-2102">Added Source Control cmdlets</span></span>
* <span data-ttu-id="0a960-2103">Aggiunta del cmdlet Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="0a960-2103">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="0a960-2104">Risoluzione dei problemi del comando Node per il registro DSC</span><span class="sxs-lookup"><span data-stu-id="0a960-2104">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="0a960-2105">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-2105">Az.Compute</span></span>
* <span data-ttu-id="0a960-2106">Risoluzione del problema relativo all'identità per l'identità SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="0a960-2106">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="0a960-2107">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a960-2107">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="0a960-2108">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2108">Az.ContainerInstance</span></span>
* <span data-ttu-id="0a960-2109">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a960-2109">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="0a960-2110">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="0a960-2110">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="0a960-2111">Aggiornamento della descrizione degli esempi per i cmdlet del Marketplace</span><span class="sxs-lookup"><span data-stu-id="0a960-2111">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="0a960-2112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-2112">Az.Network</span></span>
* <span data-ttu-id="0a960-2113">Aggiunta dei cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="0a960-2113">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="0a960-2114">Aggiunta di ICMP nei protocolli di rete di AzureFirewall supportati</span><span class="sxs-lookup"><span data-stu-id="0a960-2114">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="0a960-2115">Aggiornamento del cmdlet Test-AzureRmNetworkWatcherConnectivity e aggiunta della convalida su ID, indirizzo e porta di destinazione.</span><span class="sxs-lookup"><span data-stu-id="0a960-2115">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="0a960-2116">Risoluzione dei problemi relativi all'utilizzo della memoria nel mapping di VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a960-2116">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="0a960-2117">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="0a960-2117">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="0a960-2118">Risoluzione dei problemi relativi alla modifica dei criteri per una condivisione file protetta.</span><span class="sxs-lookup"><span data-stu-id="0a960-2118">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="0a960-2119">Conversione del fuso orario dei criteri in caratteri maiuscoli.</span><span class="sxs-lookup"><span data-stu-id="0a960-2119">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="0a960-2120">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0a960-2120">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="0a960-2121">Correzione dell'esempio in New-AzureRmRecoveryServicesAsrProtectableItem</span><span class="sxs-lookup"><span data-stu-id="0a960-2121">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="0a960-2122">Aggiornamento delle dipendenze per problemi di mapping dei tipi</span><span class="sxs-lookup"><span data-stu-id="0a960-2122">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="0a960-2123">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="0a960-2123">Az.Relay</span></span>
* <span data-ttu-id="0a960-2124">Aggiunta del parametro facoltativo -KeyValue al cmdlet New-AzureRmRelayKey, che consente all'utente di fornire KeyValue.</span><span class="sxs-lookup"><span data-stu-id="0a960-2124">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="0a960-2125">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2125">Az.Resources</span></span>
* <span data-ttu-id="0a960-2126">Aggiornamento della documentazione della Guida per parametri correlati all'identità delle risorse in `New-AzureRmPolicyAssignment` e `Set-AzureRmPolicyAssignment`</span><span class="sxs-lookup"><span data-stu-id="0a960-2126">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="0a960-2127">Aggiunta di un esempio per New-AzureRmPolicyDefinition che usa -Metadata</span><span class="sxs-lookup"><span data-stu-id="0a960-2127">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="0a960-2128">Risoluzione di un problema per consentire la conservazione delle maiuscole/minuscole nelle chiavi dei tag in NetStandard: #7678 #7703</span><span class="sxs-lookup"><span data-stu-id="0a960-2128">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="0a960-2129">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-2129">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-2130">Aggiunta di messaggi di deprecazione per future modifiche che causano un'interruzione</span><span class="sxs-lookup"><span data-stu-id="0a960-2130">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="0a960-2131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-2131">Az.Sql</span></span>
* <span data-ttu-id="0a960-2132">Aggiunta di nuovi cmdlet per operazioni CRUD in Istanza gestita di database SQL di Azure e database SQL di Azure gestito</span><span class="sxs-lookup"><span data-stu-id="0a960-2132">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="0a960-2133">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2133">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a960-2134">New-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2134">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a960-2135">Set-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2135">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a960-2136">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="0a960-2136">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="0a960-2137">Get-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a960-2137">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a960-2138">New-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a960-2138">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a960-2139">Restore-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a960-2139">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="0a960-2140">Remove-AzureRmSqlInstanceDatabase</span><span class="sxs-lookup"><span data-stu-id="0a960-2140">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="0a960-2141">Abilitazione della gestione dei criteri di controllo estesi in un server o un database.</span><span class="sxs-lookup"><span data-stu-id="0a960-2141">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="0a960-2142">Aggiunta di un nuovo parametro (PredicateExpression) per abilitare i filtri per i log di controllo.</span><span class="sxs-lookup"><span data-stu-id="0a960-2142">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="0a960-2143">Modifica dei cmdlet per l'uso dei client SQL invece dei client legacy.</span><span class="sxs-lookup"><span data-stu-id="0a960-2143">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="0a960-2144">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a960-2144">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a960-2145">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a960-2145">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="0a960-2146">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a960-2146">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="0a960-2147">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="0a960-2147">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="0a960-2148">Risoluzione del problema relativo all'uso di Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings con il set di parametri per il nome dell'account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0a960-2148">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="0a960-2149">0.5.0 - Novembre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2149">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="0a960-2150">Generale</span><span class="sxs-lookup"><span data-stu-id="0a960-2150">General</span></span>
* <span data-ttu-id="0a960-2151">Aggiunta di strumenti di completamento di risorse a molti cmdlet di base. Questi strumenti consentono di spostarsi attraverso i nomi di risorse esistenti quando i cmdlet vengono richiamati in modo interattivo</span><span class="sxs-lookup"><span data-stu-id="0a960-2151">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="0a960-2152">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a960-2152">Az.Profile</span></span>
* <span data-ttu-id="0a960-2153">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0a960-2153">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="0a960-2154">Parametro TenantId nel cmdlet Connect-AzAccount rinominato in Tenant e aggiunta di un alias per TenantId</span><span class="sxs-lookup"><span data-stu-id="0a960-2154">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="0a960-2155">Aggiornamento della descrizione di TenantId per Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="0a960-2155">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="0a960-2156">Correzione del messaggio di errore per l'accesso non riuscito quando si specifica il dominio del tenant</span><span class="sxs-lookup"><span data-stu-id="0a960-2156">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="0a960-2157">Risoluzione del conflitto tra nomi di contesto per account senza sottoscrizioni nel tenant</span><span class="sxs-lookup"><span data-stu-id="0a960-2157">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="0a960-2158">Risoluzione del problema con gli endpoint DataLake quando si usa l'identità del servizio gestita</span><span class="sxs-lookup"><span data-stu-id="0a960-2158">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="0a960-2159">Risoluzione del problema per il quale 'Disconnect-AzAccount' generava un errore se non connesso</span><span class="sxs-lookup"><span data-stu-id="0a960-2159">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-2160">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-2160">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-2161">Aggiunta dell'operazione Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="0a960-2161">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-2162">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-2162">Az.Compute</span></span>
* <span data-ttu-id="0a960-2163">Aggiunta dei cmdlet Add-AzVmssVMDataDisk e Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0a960-2163">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="0a960-2164">Get-AzVMImage mostra AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="0a960-2164">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="0a960-2165">Correzione dei valori di opzione di SetAzVMChefExtension -BootstrapOptions e -JsonAttribute non impostati in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="0a960-2165">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-2166">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-2166">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-2167">Aggiornamento del pacchetto DataLake alla versione 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="0a960-2167">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="0a960-2168">Aggiunta della concorrenza predefinita alle operazioni multithreading.</span><span class="sxs-lookup"><span data-stu-id="0a960-2168">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="0a960-2169">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="0a960-2169">Az.Insights</span></span>
* <span data-ttu-id="0a960-2170">Correzione del problema numero 7267 (area Ridimensionamento automatico)</span><span class="sxs-lookup"><span data-stu-id="0a960-2170">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="0a960-2171">Problemi con la creazione di una nuova regola di ridimensionamento automatico che non impostava correttamente i parametri enumerati (i parametri venivano sempre impostati sul valore predefinito).</span><span class="sxs-lookup"><span data-stu-id="0a960-2171">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="0a960-2172">Correzione del problema numero 7513 [Insights] per il quale Set-AzDiagnosticSetting richiedeva l'indicazione esplicita delle categorie durante la creazione dell'impostazione</span><span class="sxs-lookup"><span data-stu-id="0a960-2172">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="0a960-2173">Ora il cmdlet non richiede l'indicazione esplicita delle categorie da abilitare in fase di creazione, ovvero funziona come documentato</span><span class="sxs-lookup"><span data-stu-id="0a960-2173">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-2174">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-2174">Az.Network</span></span>
* <span data-ttu-id="0a960-2175">Modifica di PeeringType in un parametro obbligatorio per i cmdlet seguenti:</span><span class="sxs-lookup"><span data-stu-id="0a960-2175">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="0a960-2176">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-2176">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="0a960-2177">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="0a960-2177">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="0a960-2178">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a960-2178">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="0a960-2179">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="0a960-2179">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="0a960-2180">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="0a960-2180">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="0a960-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="0a960-2181">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="0a960-2182">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="0a960-2182">Az.PolicyInsights</span></span>
* <span data-ttu-id="0a960-2183">Aggiunta di cmdlet di correzione dei criteri</span><span class="sxs-lookup"><span data-stu-id="0a960-2183">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-2184">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2184">Az.Resources</span></span>
* <span data-ttu-id="0a960-2185">Correzione per https://github.com/Azure/azure-powershell/issues/7402</span><span class="sxs-lookup"><span data-stu-id="0a960-2185">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="0a960-2186">È possibile elencare le risorse usando il parametro '-ResourceId' per 'Get-AzResource'</span><span class="sxs-lookup"><span data-stu-id="0a960-2186">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="0a960-2187">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="0a960-2187">Az.ServiceBus</span></span>
* <span data-ttu-id="0a960-2188">Aggiunta della proprietà di sola lettura MigrationState a PSServiceBusMigrationConfigurationAttributes per conoscere lo stato della migrazione.</span><span class="sxs-lookup"><span data-stu-id="0a960-2188">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="0a960-2189">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="0a960-2189">Az.ServiceFabric</span></span>
* <span data-ttu-id="0a960-2190">Correzione dell'aggiunta di un certificato a set di scalabilità di macchine virtuali Linux.</span><span class="sxs-lookup"><span data-stu-id="0a960-2190">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="0a960-2191">Correzione di 'Add-AzServiceFabricClusterCertificate'</span><span class="sxs-lookup"><span data-stu-id="0a960-2191">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="0a960-2192">Uso dell'identificazione personale corretta dal nuovo certificato (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="0a960-2192">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="0a960-2193">Visualizzazione corretta dell'eccezione (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="0a960-2193">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="0a960-2194">Correzione di 'Update-AzServiceFabricDurability' per aggiornare la configurazione del cluster prima di avviare l'operazione CreateOrUpdate del set di scalabilità di macchine virtuali.</span><span class="sxs-lookup"><span data-stu-id="0a960-2194">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="0a960-2195">0.4.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2195">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="0a960-2196">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="0a960-2196">Az.Profile</span></span>
* <span data-ttu-id="0a960-2197">Risoluzione del problema con Get-AzSubscription in CloudShell</span><span class="sxs-lookup"><span data-stu-id="0a960-2197">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="0a960-2198">Aggiornamento del codice comune per l'uso della versione più recente di ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="0a960-2198">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-2199">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-2199">Az.Compute</span></span>
* <span data-ttu-id="0a960-2200">Aggiunta di nuove dimensioni all'elenco delle dimensioni di VM consentite per le quali verrà abilitata la rete accelerata quando si usa il set di parametri semplice per 'New-AzVm'</span><span class="sxs-lookup"><span data-stu-id="0a960-2200">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="0a960-2201">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a960-2201">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="0a960-2202">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="0a960-2202">Az.DataLakeStore</span></span>
* <span data-ttu-id="0a960-2203">Aggiunta del supporto per le regole di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="0a960-2203">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="0a960-2204">Get-AzDataLakeStoreVirtualNetworkRule: Ottiene o elenca la regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a960-2204">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="0a960-2205">Add-AzDataLakeStoreVirtualNetworkRule: Aggiunge una regola di rete virtuale all'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0a960-2205">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a960-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifica la regola di rete virtuale nell'account Data Lake Store specificato.</span><span class="sxs-lookup"><span data-stu-id="0a960-2206">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="0a960-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Elimina una regola di rete virtuale di Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0a960-2207">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-2208">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-2208">Az.Network</span></span>
* <span data-ttu-id="0a960-2209">Aggiornamento del cmdlet Test-AzNetworkWatcherConnectivity per passare il valore del protocollo al back-end.</span><span class="sxs-lookup"><span data-stu-id="0a960-2209">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="0a960-2210">Aggiunta dello strumento di completamento per l'argomento ResourceName a tutti i cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a960-2210">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-2211">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2211">Az.Resources</span></span>
* <span data-ttu-id="0a960-2212">Con l'aggiunta di un'eccezione significativa nello scenario, risolto il problema per il quale Get-AzRoleDefinition generava un'eccezione incomprensibile quando il profilo predefinito non aveva una sottoscrizione e non veniva specificato un ambito.</span><span class="sxs-lookup"><span data-stu-id="0a960-2212">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="0a960-2213">Il set di parametri è stato inoltre impostato su 'RoleDefinitionNameParameterSet'.</span><span class="sxs-lookup"><span data-stu-id="0a960-2213">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="0a960-2214">0.3.0 - Ottobre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2214">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="0a960-2215">Azure.Storage</span><span class="sxs-lookup"><span data-stu-id="0a960-2215">Azure.Storage</span></span>
* <span data-ttu-id="0a960-2216">Correzione della copia di BLOB/file per la mancata copia in caso di problemi nei metadati nella destinazione</span><span class="sxs-lookup"><span data-stu-id="0a960-2216">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="0a960-2217">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-2217">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="0a960-2218">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="0a960-2218">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="0a960-2219">Supporto del recupero dell'utilizzo delle risorse di archiviazione per una località specifica e aggiunta di un messaggio di avviso che informa che il recupero dell'utilizzo delle risorse di archiviazione a livello globale è obsoleto</span><span class="sxs-lookup"><span data-stu-id="0a960-2219">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="0a960-2220">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="0a960-2220">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="0a960-2221">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="0a960-2221">Az.CognitiveServices</span></span>
* <span data-ttu-id="0a960-2222">Supporto di Get-AzCognitiveServicesAccountSkus senza un account esistente.</span><span class="sxs-lookup"><span data-stu-id="0a960-2222">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="0a960-2223">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="0a960-2223">Az.Compute</span></span>
* <span data-ttu-id="0a960-2224">Correzione di Get-AzVM -ResourceGroupName <rg> per la restituzione, se necessario, di oltre 50 risultati</span><span class="sxs-lookup"><span data-stu-id="0a960-2224">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="0a960-2225">Aggiunta di un esempio di 'SimpleParameterSet' alla Guida del cmdlet New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="0a960-2225">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="0a960-2226">Correzione di un errore di digitazione nel messaggio di stato di Crittografia dischi di Azure</span><span class="sxs-lookup"><span data-stu-id="0a960-2226">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="0a960-2227">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0a960-2227">Az.DataFactoryV2</span></span>
* <span data-ttu-id="0a960-2228">Aggiornamento di ADF .Net SDK alla versione 2.3.0</span><span class="sxs-lookup"><span data-stu-id="0a960-2228">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="0a960-2229">Az.Network</span><span class="sxs-lookup"><span data-stu-id="0a960-2229">Az.Network</span></span>
* <span data-ttu-id="0a960-2230">Aggiunta della funzionalità NetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a960-2230">Added NetworkProfile functionality.</span></span> <span data-ttu-id="0a960-2231">e di nuovi cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a960-2231">new cmdlets added</span></span>
    - <span data-ttu-id="0a960-2232">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a960-2232">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a960-2233">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a960-2233">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a960-2234">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a960-2234">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a960-2235">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="0a960-2235">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="0a960-2236">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-2236">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="0a960-2237">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-2237">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="0a960-2238">Aggiunta del collegamento di associazione di servizio nel modello di subnet</span><span class="sxs-lookup"><span data-stu-id="0a960-2238">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="0a960-2239">Aggiunta dei cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="0a960-2239">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="0a960-2240">Aggiunta dei cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="0a960-2240">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="0a960-2241">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="0a960-2241">Az.RedisCache</span></span>
* <span data-ttu-id="0a960-2242">Possibilità di usare in futuro qualsiasi stringa come parametro Size.</span><span class="sxs-lookup"><span data-stu-id="0a960-2242">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="0a960-2243">Aggiunta di P5 nel popup PSArgumentCompleter</span><span class="sxs-lookup"><span data-stu-id="0a960-2243">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="0a960-2244">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="0a960-2244">Az.Resources</span></span>
* <span data-ttu-id="0a960-2245">Aggiunta del parametro -Mode mancante a Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="0a960-2245">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="0a960-2246">Correzione del bug del cmdlet Get-AzProviderOperation per le operazioni in cui Origin contiene User</span><span class="sxs-lookup"><span data-stu-id="0a960-2246">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="0a960-2247">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="0a960-2247">Az.Sql</span></span>
* <span data-ttu-id="0a960-2248">Correzione del problema per cui alcuni cmdlet di backup non riconoscono la sottoscrizione di Azure corrente</span><span class="sxs-lookup"><span data-stu-id="0a960-2248">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="0a960-2249">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="0a960-2249">Az.Websites</span></span>
* <span data-ttu-id="0a960-2250">Nuovo cmdlet Get-AzWebAppContainerContinuousDeploymentUrl per il recupero dell'URL del webhook di distribuzione continua dei contenitori</span><span class="sxs-lookup"><span data-stu-id="0a960-2250">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="0a960-2251">Nuovi cmdlet New-AzWebAppContainerPSSession e Enter-WebAppContainerPSSession per l'avvio di una sessione remota di PowerShell in un'app contenitore Windows</span><span class="sxs-lookup"><span data-stu-id="0a960-2251">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="0a960-2252">0.2.0 - Settembre 2018</span><span class="sxs-lookup"><span data-stu-id="0a960-2252">0.2.0 - September 2018</span></span>
 <span data-ttu-id="0a960-2253">Versione iniziale</span><span class="sxs-lookup"><span data-stu-id="0a960-2253">Initial Release</span></span>
